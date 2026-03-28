# Machine learning deanonymisation

A person's writing style is as distinctive as a fingerprint. The words they favour, the sentence structures they default to, the way they punctuate, the phrases they reach for without thinking: these are consistent across contexts and measurable. An author identification model trained on known writing samples can predict the authorship of anonymous texts with accuracy that is uncomfortable for anyone writing under a pseudonym.

## How it works

The model learns to associate statistical patterns in text with specific authors. The key transformation is from readable text into a numerical representation that captures word choice and phrase patterns while discarding meaning.

```
# Training phase: build a model that recognises each author's style
for each known author:
    collect multiple text samples from that author
    for each sample:
        convert to feature_vector using TF-IDF:
            measure frequency of each word and phrase (n-gram)
            weight rare terms more heavily than common ones
            result: a numerical fingerprint of writing style
    store (author_label, feature_vector)

train classifier to map feature_vectors to author_labels

# Attack phase: identify anonymous text
anonymous_text = load suspicious document or post
feature_vector = TF_IDF_transform(anonymous_text)
predicted_author = classifier.predict(feature_vector)
confidence_scores = classifier.predict_probability(feature_vector)
→ author_A: 68%, author_B: 21%, author_C: 11%
```

The model does not need certainty to be useful. A 68% probability assigned to one of three candidates is a significant lead. Combined with corroborating metadata, posting time, vocabulary domain, apparent technical knowledge, the probability may be sufficient to act on.

## What this reveals

Stylometric analysis identified the author of The Cuckoo's Calling as J.K. Rowling in 2013. The novel had been published under the pseudonym Robert Galbraith; a statistical comparison of the text against Rowling's known work, and against work by other candidate authors, produced a clear match. The analysis was conducted by academics at Nottingham Trent University and published alongside the accusation.

The technique has been applied in criminal investigations to attribute extremist writings and in academic fraud detection to identify ghost-written work. It is available as open-source software. The barrier to applying it is low: access to sufficient writing samples from candidate authors is the main requirement, and for anyone who posts publicly under their real name that requirement is easily met.

## Defences

The defences available are limited. Writing style can be partially obscured by consciously using different vocabulary, shorter sentences, or different punctuation habits. Paraphrasing tools can alter surface features while preserving meaning. Neither approach is reliable against a model trained specifically on that author's style, because the patterns that are most distinctive are often below the level of conscious awareness and difficult to suppress consistently.

The most effective protection is preventing the association between the anonymous account and any known writing sample in the first place. This is harder than it sounds: anyone who has posted under their real name on any public platform has provided training data. Using a completely separate writing register, a different persona with different linguistic habits maintained consistently from the beginning, is more protective than trying to obscure an existing style after the fact.
