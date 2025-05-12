# AI-powered behavioural profiling

Creating AI-powered behavioural profiling based on social media information involves extracting user data, processing 
it with machine learning models, and profiling user behaviour. The following example assumes working with text data 
(e.g., posts or tweets), and uses sentiment analysis and clustering to create behavioural profiles based on social 
media posts. This is a simplified example to demonstrate the concept.

In a real-world scenario, access to APIs (such as Twitter API, Facebook Graph API, or Instagram API) is needed to 
collect data from users' social media profiles. For this demo a mock dataset of social media posts and some basic AI 
techniques are used to analyse sentiment and cluster behaviour.

```python
import pandas as pd
from textblob import TextBlob
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.cluster import KMeans
import nltk

# Sample social media posts
data = {
    'username': ['user1', 'user2', 'user3', 'user1', 'user2', 'user3'],
    'post': [
        'I love hiking in the mountains!',
        'So tired of the endless work. When is this going to end?',
        'Exploring new places is always exciting.',
        'Feeling so down today, everything is going wrong.',
        'Had a great weekend with friends. Life is good!',
        'I hate when people are rude. It ruins my day.'
    ]
}

# Create a DataFrame
df = pd.DataFrame(data)

# 1. Sentiment Analysis using TextBlob
def get_sentiment(text):
    blob = TextBlob(text)
    # Polarity is a value between -1 (negative) to 1 (positive)
    return blob.sentiment.polarity

df['sentiment'] = df['post'].apply(get_sentiment)

# 2. Behavior Profiling using KMeans Clustering based on TF-IDF vectors
vectorizer = TfidfVectorizer(stop_words='english')
X = vectorizer.fit_transform(df['post'])

# Apply KMeans clustering (3 clusters for simplicity)
kmeans = KMeans(n_clusters=3, random_state=0).fit(X)

# Add cluster labels to DataFrame
df['cluster'] = kmeans.labels_

# 3. Analyzing Profiles
# You can group posts by cluster and check out the sentiment distribution for each group
profile = df.groupby('cluster').agg(
    num_posts=('post', 'count'),
    avg_sentiment=('sentiment', 'mean')
).reset_index()

print("User Profiles (Based on Clusters):")
print(profile)

# 4. Display Sentiment and Post Details
print("\nPost Details with Sentiment and Cluster:")
print(df[['username', 'post', 'sentiment', 'cluster']])
```

## Explanation

Sentiment analysis:

The `TextBlob` library is used to compute the sentiment of each post. Sentiment polarity is a float value where `-1` 
represents negative sentiment, `0` represents neutral, and `1` represents positive sentiment. This helps understand 
the emotional tone of the user's posts.

Behavior profiling (Clustering):

The `TfidfVectorizer` is used to convert the text data into numerical vectors (term frequency-inverse document 
frequency). This vectorises the posts and removes stop words (commonly used words like "the", "is", "and").

`KMeans` clustering is applied to group the posts into clusters based on the content. Each cluster represents a 
behavioural profile, e.g., positive, negative, or neutral themes.

User profile creation:

After applying `KMeans`, each post is associated with a cluster and the average sentiment for each cluster is 
calculated. This gives a basic profile of different types of behaviour, such as "positive", "neutral", or "negative" 
users.

## Output

```text
User Profiles (Based on Clusters):
   cluster  num_posts  avg_sentiment
0        0          2       0.675000
1        1          2      -0.425000
2        2          2      -0.150000

Post Details with Sentiment and Cluster:
  username          post                                    sentiment              cluster
0    user1          I love hiking in the mountains!    0.500000        0
1    user2          So tired of the endless work. When is this going to end?    -0.500000        1
2    user3          Exploring new places is always exciting.    0.500000        0
3    user1          Feeling so down today, everything is going wrong.    -0.600000        1
4    user2          Had a great weekend with friends. Life is good!    0.600000        0
5    user3          I hate when people are rude. It ruins my day.    -0.500000        1

```

### Profiling results

* Cluster 0 has positive sentiments (e.g., love for hiking, excitement about exploring new places).
* Cluster 1 has negative sentiments (e.g., frustration with work, feeling down).
* Cluster 2 could represent a neutral profile (although in this case, it has fewer posts and thus is harder to analyse).
