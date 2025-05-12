# Machine learning deanonymisation

Author identification through writing style

```python
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.svm import SVC
import pandas as pd

def train_author_model(texts, authors):
    vectorizer = TfidfVectorizer(
        ngram_range=(1, 3),
        stop_words='english',
        max_features=1000
    )
    X = vectorizer.fit_transform(texts)
    model = SVC(kernel='linear')
    model.fit(X, authors)
    return vectorizer, model

# Example usage:
texts = ["sample text 1...", "sample text 2..."]  # Actual text samples
authors = ["author1", "author2"]                  # Corresponding authors
vectorizer, model = train_author_model(texts, authors)
```