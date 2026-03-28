# AI-powered behavioural profiling

The content of what someone posts is only one layer. The patterns beneath it are legible to a machine learning model trained to read them: the times of posting, the topics that recur, the emotional register sustained across a period of time, the vocabulary, the rhythm. A behavioural profiling system reads posts as data rather than as text. It does not try to understand what someone means. It measures what they produce, statistically, and assigns them a category.

## How it works

The process has two stages. The first assigns a sentiment value to each post: a numerical score reflecting how positive or negative the content is. The second converts the words into vectors and groups similar vectors into clusters, each cluster representing a behavioural pattern.

```
# Stage 1: Sentiment scoring
for each post in user_history:
    sentiment_score = analyse(post.text)
    # result is a float: -1.0 (negative) to +1.0 (positive)
    store(user_id, post_timestamp, sentiment_score)

# Stage 2: Topic and behaviour clustering
for each post:
    feature_vector = TF_IDF_transform(post.text)
    # converts text to a numerical representation of topic/word patterns

run K_means_clustering on all feature_vectors
assign each post to a cluster

# Build user profile:
dominant_cluster = most frequent cluster for this user
average_sentiment = mean of sentiment scores over time
topic_map = most prominent terms across this user's feature_vectors
```

A user who posts frequently about work frustration, weekend socialising, and outdoor activities will generate a profile with a characteristic shape: negative sentiment spikes mid-week, positive spikes on weekends, topics clustering around professional stress and leisure. Mapped across millions of users, these profiles sort people into categories.

## What this reveals

The profile is not a psychological assessment in the clinical sense. It is a statistical approximation that is useful for commercial and political targeting at scale. An advertiser with a profile labelled "high stress, physically active, 30-40 age range" can target that person specifically. A political operation with a profile labelled "politically disengaged, economic anxiety, suburban" can target them with tailored messaging.

The person did not consent to being categorised. In many cases the posts were public. In others the data was purchased from data brokers, obtained through leaked datasets, or collected through embedded tracking on sites the person visited. The Cambridge Analytica affair demonstrated this pattern at scale: Facebook likes served as the input, personality profiles as the output, and targeted political advertising as the use. Accuracy was imperfect. Accuracy did not need to be perfect.

## Defences

Behavioural profiling at this level operates on aggregate patterns over time. Reducing the volume and consistency of publicly available data limits profile quality. Using separate accounts for different contexts prevents the aggregation of behaviour from multiple areas of life into a single profile. Being aware that public posts are training data for systems the poster never sees is a useful frame for deciding what to share and where.
