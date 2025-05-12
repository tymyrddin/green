# Inference attack

A Python demonstration of an inference attack, where an attacker uses seemingly harmless data to deduce sensitive 
information about individuals. This example focuses on inferring political affiliation from public app usage patterns:

```python
import pandas as pd
import numpy as np
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import train_test_split
from faker import Faker

# --- Generate Synthetic Dataset ---
def generate_app_usage_data(num_users=500):
    """Create synthetic dataset showing app usage patterns and political leanings."""
    fake = Faker()
    data = []
    
    for _ in range(num_users):
        # Simulate app installation patterns
        is_conservative = np.random.rand() > 0.5
        apps = {
            'weather_app': True,
            'social_media': True,
            'news_app': True,
            # Conservative-leaning apps
            'hunting_app': is_conservative and (np.random.rand() > 0.7),
            'religious_app': is_conservative and (np.random.rand() > 0.6),
            # Liberal-leaning apps
            'climate_app': not is_conservative and (np.random.rand() > 0.7),
            'lgbtq_app': not is_conservative and (np.random.rand() > 0.6),
            # Neutral apps with slight biases
            'sports_app': np.random.rand() > 0.3,
            'shopping_app': np.random.rand() > 0.2
        }
        
        data.append({
            **apps,
            'political_leaning': 'conservative' if is_conservative else 'liberal',
            'age': np.random.randint(18, 80),
            'location': fake.state()
        })
    
    return pd.DataFrame(data)

# --- Inference Attack Simulation ---
def run_inference_attack(df):
    """Train a classifier to predict political leaning from app usage."""
    # Prepare data
    X = df.drop(columns=['political_leaning'])
    y = df['political_leaning']
    X = pd.get_dummies(X)  # Convert categorical variables
    
    # Split data
    X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3)
    
    # Train model
    model = RandomForestClassifier()
    model.fit(X_train, y_train)
    
    # Evaluate
    accuracy = model.score(X_test, y_test)
    feature_importances = pd.Series(model.feature_importances_, index=X.columns)
    
    return model, accuracy, feature_importances

# --- Demonstration ---
if __name__ == "__main__":
    # Generate and analyse data
    df = generate_app_usage_data()
    model, accuracy, importances = run_inference_attack(df)
    
    print(f"\n--- Inference Attack Results ---")
    print(f"Model Accuracy: {accuracy:.1%}")
    print("\nTop Predictive Features:")
    print(importances.sort_values(ascending=False).head(5))
    
    # Show a sample prediction
    sample_user = df.drop(columns=['political_leaning']).iloc[0:1]
    sample_user = pd.get_dummies(sample_user)
    prediction = model.predict(sample_user)[0]
    print(f"\nSample Prediction: {prediction} (Actual: {df.iloc[0]['political_leaning']})")
```

## Key components explained:

Synthetic Data Generation:

* Creates realistic app usage patterns with political biases
* Conservative users more likely to have hunting/religious apps
* Liberal users more likely to have climate/LGBTQ apps
* Includes neutral attributes (age, location) as distractors

Machine Learning Attack:

* Uses a Random Forest classifier to predict political leaning
* Achieves ~75-85% accuracy in tests (scary but realistic)
* Identifies which apps are most revealing

Privacy Implications:

* Demonstrates how "harmless" app data can reveal sensitive traits
* Mirrors real-world cases like the Cambridge Analytica scandal
* Shows why aggregate data can still be dangerous

## Ethical considerations:

* This is for educational purposes only
* Never implement this on real user data without consent
* Intended to demonstrate why we need privacy-preserving analytics

## Possible defences to add

Differential Privacy:

```python
from diffprivlib.models import RandomForestClassifier as DPForest
dp_model = DPForest(epsilon=1.0)  # Adds noise to protect privacy
```

Data Minimization:

```python
# Only collect essential data
df.drop(columns=['hunting_app', 'lgbtq_app'], inplace=True)
```
