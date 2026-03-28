# Inference attack

The most sensitive information a person holds is often not directly available to an adversary. But it can be inferred from information that is. An inference attack trains a machine learning model on a labelled dataset and uses it to predict private attributes from observable ones. The target person provides no sensitive information directly. The model infers it from the trail they leave without thinking.

## How it works

The clearest example is political affiliation inferred from smartphone app installations. The list of apps installed on a device is visible to the operating system and, through analytics SDKs embedded in those apps, to many third-party services. Certain apps correlate statistically with certain political leanings. A model trained on a dataset that contains both app lists and known political affiliations can then make predictions about people whose affiliation is unknown.

```
# Training phase
training_data = [
    {apps: ["weather", "hunting_app", "bible_study", "news_aggregator"],
     label: "conservative"},
    {apps: ["weather", "climate_tracker", "lgbtq_support_app", "news_aggregator"],
     label: "liberal"},
    # ... hundreds or thousands of labelled examples
]

model = RandomForest.train(features=app_lists, labels=political_leanings)

# Inference phase (attack):
target = {apps: ["weather", "hunting_app", "sports_scores", "news_aggregator"]}
predicted_label = model.predict(target.apps)
prediction_confidence = model.confidence(target.apps)
→ "conservative", 78% confidence

# Additional output: which features mattered most
feature_importance = model.explain()
→ hunting_app: 0.31, bible_study: 0.24, climate_tracker: -0.19, ...
```

The feature importance output tells an analyst which apps are most predictive, and in which direction. This is itself actionable: it reveals which data to collect in future.

## What this reveals

The model does not need to be perfectly accurate to be commercially or politically significant. At 75-80% accuracy across a population of millions, the inferences produce actionable targeting data. A person in that population installed the apps they found useful. They did not provide their political views.

The same pattern generalises to other sensitive attributes: health conditions inferred from pharmacy purchases, pregnancy inferred from buying patterns, sexual orientation inferred from app usage, creditworthiness inferred from behavioural signals. In each case the sensitive attribute is not directly observable; the proxy data is.

The Cambridge Analytica affair made the mechanism public: Facebook likes served as the input, psychographic profiles as the output, and targeted political advertising as the application. The likes were not inherently sensitive. Their combination was.

## Defences

Limiting which apps have access to the device's app list restricts what can be reported to analytics services. On both iOS and Android, analytics SDK permissions can be constrained by the operating system, though enforcement is inconsistent. More fundamentally, being selective about app installations reduces the surface available for inference. An app installed for occasional convenience may contribute significantly to an inferred profile that its user never intended to create.
