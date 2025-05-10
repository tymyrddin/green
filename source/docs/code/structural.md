# Structural attack

A Python demonstration of a structural attack, where an attacker exploits the inherent structure of a system 
(like social networks or organizational hierarchies) to infer sensitive information. This example focuses on 
deanonymizing users in a corporate communication network by analyzing email metadata patterns:

```python
import networkx as nx
import pandas as pd
import numpy as np
from faker import Faker
from collections import defaultdict

# --- Generate Synthetic Corporate Email Data ---
def generate_org_communications(num_employees=50, num_emails=500):
    """Create synthetic email metadata with organizational structure."""
    fake = Faker()
    
    # Generate org hierarchy (CEO -> VPs -> Managers -> Staff)
    roles = ['CEO'] + ['VP']*3 + ['Manager']*10 + ['Staff']*(num_employees-14)
    np.random.shuffle(roles)  # Not perfectly hierarchical for realism
    
    employees = []
    for i in range(num_employees):
        employees.append({
            'employee_id': f"emp_{i:03d}",
            'name': fake.name(),
            'department': fake.random_element(elements=('Finance', 'Engineering', 'HR', 'Legal')),
            'role': roles[i],
            'email': fake.email()
        })
    
    # Generate email traffic patterns (more within departments/hierarchy levels)
    emails = []
    for _ in range(num_emails):
        sender = np.random.choice(employees)
        if np.random.rand() > 0.7:  # 70% intra-department
            receiver = np.random.choice([e for e in employees if e['department'] == sender['department']])
        else:
            receiver = np.random.choice(employees)
        
        # VPs/CEO communicate more with each other
        if sender['role'] in ('VP', 'CEO') and np.random.rand() > 0.8:
            receiver = np.random.choice([e for e in employees if e['role'] in ('VP', 'CEO')])
        
        emails.append({
            'from': sender['email'],
            'to': receiver['email'],
            'time': fake.date_time_this_month(),
            'subject': fake.sentence()
        })
    
    return pd.DataFrame(employees), pd.DataFrame(emails)

# --- Structural Attack Simulation ---
def structural_attack(employees_df, emails_df, known_targets):
    """
    Reconstruct org hierarchy using only email metadata.
    known_targets: Dictionary of {email: known attributes} for a few users
    """
    # Build communication graph
    G = nx.DiGraph()
    for _, email in emails_df.iterrows():
        G.add_edge(email['from'], email['to'], time=email['time'])
    
    # Step 1: Identify central nodes (likely leadership)
    betweenness = nx.betweenness_centrality(G)
    top_senders = sorted(G.out_degree(), key=lambda x: x[1], reverse=True)[:5]
    
    # Step 2: Cluster by communication patterns
    communities = nx.algorithms.community.greedy_modularity_communities(G.to_undirected())
    
    # Step 3: Infer roles based on structure and known targets
    role_predictions = {}
    for email in G.nodes():
        # Use known targets as reference points
        if email in known_targets:
            role_predictions[email] = known_targets[email]
            continue
            
        # Predict based on graph metrics
        if email in dict(top_senders):
            role_predictions[email] = 'VP/CEO'
        elif G.in_degree(email) > np.median([d for n,d in G.in_degree()]):
            role_predictions[email] = 'Manager'
        else:
            role_predictions[email] = 'Staff'
    
    # Step 4: Map communities to departments
    dept_predictions = {}
    community_depts = defaultdict(list)
    for i, comm in enumerate(communities):
        for email in comm:
            if email in known_targets:
                community_depts[i].append(known_targets[email]['department'])
    
    for i, comm in enumerate(communities):
        most_common_dept = max(set(community_depts[i]), key=community_depts[i].count) if community_depts[i] else 'Unknown'
        for email in comm:
            dept_predictions[email] = most_common_dept
    
    return role_predictions, dept_predictions, G

# --- Demonstration ---
if __name__ == "__main__":
    # Generate synthetic data
    employees, emails = generate_org_communications()
    
    # Simulate partial knowledge (3 known employees)
    known_targets = {
        employees.iloc[0]['email']: {'role': employees.iloc[0]['role'], 'department': employees.iloc[0]['department']},
        employees.iloc[10]['email']: {'role': employees.iloc[10]['role'], 'department': employees.iloc[10]['department']},
        employees.iloc[20]['email']: {'role': employees.iloc[20]['role'], 'department': employees.iloc[20]['department']}
    }
    
    # Run attack
    role_preds, dept_preds, graph = structural_attack(employees, emails, known_targets)
    
    # Evaluate
    print("\n--- Structural Attack Results ---")
    print(f"Reconstructed hierarchy for {len(role_preds)} employees")
    
    # Compare predictions with actual data
    evaluation = []
    for _, emp in employees.iterrows():
        evaluation.append({
            'email': emp['email'],
            'actual_role': emp['role'],
            'predicted_role': role_preds.get(emp['email'], 'Unknown'),
            'actual_dept': emp['department'],
            'predicted_dept': dept_preds.get(emp['email'], 'Unknown')
        })
    
    eval_df = pd.DataFrame(evaluation)
    print("\nAccuracy Samples:")
    print(eval_df.sample(5))
    
    # Visualize the network (optional)
    import matplotlib.pyplot as plt
    plt.figure(figsize=(10,8))
    pos = nx.spring_layout(graph)
    nx.draw(graph, pos, node_size=20, alpha=0.5)
    plt.title("Corporate Email Network Structure")
    plt.show()
```

## Key components explained

Synthetic Data Generation:

* Creates a realistic corporate structure with roles (CEO, VP, Manager, Staff)
* Simulates email patterns where communication follows organizational lines
* Departments naturally cluster in communication patterns

Attack Methodology:

* Graph Analysis: Uses network centrality measures to identify leadership
* Community Detection: Finds departmental clusters via modularity
* Known-Target Bootstrapping: Leverages minimal known information (3 employees) to label others

Real-World Implications:

* Demonstrates how metadata alone can reveal org charts
* Shows why "anonymous" communication datasets often aren't
* Highlights risks in corporate leak investigations

## Ethical considerations

```python
# THIS IS FOR EDUCATIONAL PURPOSES ONLY
# Never conduct such analysis without explicit authorisation
```

## Possible defences

Network obfuscation:

```python
# Add noise to communication patterns
if np.random.rand() > 0.95:  # 5% random emails
    sender, receiver = np.random.choice(employees, size=2, replace=False)
```

Differential privacy for graphs:

```python
from diffprivlib.tools import quantile
# Add random edges with privacy guarantees
num_edges_to_add = int(0.1 * len(emails_df))  # Epsilon=1.0
```
