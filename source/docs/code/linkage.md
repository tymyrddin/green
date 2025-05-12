# Linkage attack

A simulated linkage attack demonstration in Python, designed for educational purposes to show how disparate datasets 
can be combined to deanonymise users. This code illustrates the core mechanics without using real personal data.

```python
import pandas as pd
from faker import Faker  # For generating synthetic data
import hashlib

# Initialize Faker for realistic fake data
fake = Faker()

# --- Generate Synthetic Datasets ---
def generate_dataset(num_entries=100):
    """Create two datasets with overlapping attributes for linkage demonstration."""
    # Dataset 1: "Anonymous" forum posts with metadata
    forum_data = []
    for _ in range(num_entries):
        user_id = hashlib.sha256(fake.uuid4().encode()).hexdigest()[:8]  # Pseudonymized ID
        forum_data.append({
            "user_hash": user_id,
            "post_time": fake.date_time_this_month(),
            "topic": fake.random_element(elements=("politics", "gardening", "tech")),
            "location": fake.city(),
            "age_range": fake.random_element(elements=("20-30", "30-40", "40-50"))
        })

    # Dataset 2: "Public records" with similar attributes
    public_data = []
    for _ in range(num_entries):
        public_data.append({
            "full_name": fake.name(),
            "residence": fake.city(),
            "age_range": fake.random_element(elements=("20-30", "30-40", "40-50")),
            "voter_id": fake.uuid4()[:6],
            "occupation": fake.job()
        })

    return pd.DataFrame(forum_data), pd.DataFrame(public_data)

# --- Linkage Attack Simulation ---
def linkage_attack(forum_df, public_df):
    """Demonstrate how overlapping attributes can reveal identities."""
    # Step 1: Find common cities and age ranges
    common_locations = set(forum_df["location"]).intersection(set(public_df["residence"]))
    potential_matches = []

    # Step 2: Cross-reference attributes
    for loc in common_locations:
        forum_users = forum_df[forum_df["location"] == loc]
        public_records = public_df[public_df["residence"] == loc]

        for _, forum_row in forum_users.iterrows():
            matches = public_records[
                (public_records["age_range"] == forum_row["age_range"])
            ]
            if not matches.empty:
                potential_matches.append({
                    "forum_hash": forum_row["user_hash"],
                    "public_name": matches.iloc[0]["full_name"],
                    "location": loc,
                    "age_range": forum_row["age_range"],
                    "confidence": "High" if len(matches) == 1 else "Medium"
                })

    return pd.DataFrame(potential_matches)

# --- Run Simulation ---
if __name__ == "__main__":
    # Generate and link datasets
    forum_df, public_df = generate_dataset()
    matches = linkage_attack(forum_df, public_df)

    print("\n--- Linkage Attack Results ---")
    print(f"Matched {len(matches)} pseudonymous users to public records:")
    print(matches.head(3))

    # Export for analysis (optional)
    forum_df.to_csv("forum_data.csv", index=False)
    public_df.to_csv("public_data.csv", index=False)
    matches.to_csv("linkage_results.csv", index=False)
```

## Key components explained:

Synthetic Data Generation:

* Uses Faker to create realistic but fake datasets:
  * Forum posts with pseudonymized IDs, timestamps, and metadata
  * Public records with names, locations, and demographics

Linkage Logic:

* Joins datasets on overlapping attributes (location + age_range)
* Assigns confidence scores based on uniqueness of matches

Privacy Implications:

* Shows how even "anonymized" data can be re-identified
* Highlights risks of publishing datasets with overlapping attributes

## Ethical note

This code is for educational use only. Always obtain proper consent and anonymise data properly in real-world scenarios.

## Enhancements that can be added

* Temporal analysis: Link users based on posting times vs. work schedules
* Behavioural patterns: Correlate writing style or topic preferences
* Differential privacy: Add noise to see how it disrupts linkage