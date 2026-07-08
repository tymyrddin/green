# Assistive technologies

In the garden of digital security, sometimes it is not the threats that need worrying about, but
the helpers: the tools and platforms that are meant to make things easier and, in the wrong hands,
make deanonymisation faster, cheaper, and more scalable. These technologies are not inherently
adversarial. They are simply very good at finding patterns, and finding patterns is most of the work.

These are drawn from research literature and documented real-world cases.

## Graph analysis

Social network structure is one of the most powerful re-identification surfaces available. Graph
analysis tools turn a set of relationships into something an analyst can query, visualise, and match
against other graphs.

* Neo4j is a graph database widely used in both legitimate network analysis and adversarial
  social graph deanonymisation research. It supports complex traversal queries across millions
  of nodes and edges, which makes it well suited to identifying structural signatures.
* NetworkX is the Python library of choice for graph manipulation in research contexts.
  Much of the academic work on graph re-identification, from the landmark Narayanan and
  Shmatikov 2008 paper on the Netflix Prize dataset onwards, is built on this style of analysis.
* Gephi provides visualisation for graph structures, making it straightforward to spot
  distinctive sub-graphs or bridge nodes that might identify individuals.

## Machine learning libraries

Re-identification via supervised and unsupervised learning is now routine. The libraries involved
are the same ones used for entirely benign purposes.

* scikit-learn provides clustering (k-means, DBSCAN), classification, and dimensionality
  reduction. Cluster analysis on quasi-identifiers is a standard re-identification technique.
* PyTorch and TensorFlow underpin the deep learning models used for biometric
  re-identification: facial recognition, gait analysis, and voice print matching.
* XGBoost and gradient boosting methods are frequently used in inference attacks where the
  goal is to predict a sensitive attribute from a combination of non-sensitive ones.

## Biometric recognition

* DeepFace and InsightFace are open-source facial recognition frameworks capable of
  matching faces across large image datasets. Both have been used in academic re-identification
  research and are deployable on consumer hardware.
* OpenCV provides the image processing foundation for many biometric pipelines, including
  face detection, feature extraction, and cross-dataset matching.
* Voice print tools built on speaker verification models (often derived from open-source
  implementations of x-vectors or d-vectors) can re-identify individuals across audio recordings
  even when names are absent.

## OSINT tools

Open source intelligence tools automate the collection of publicly available information at a
scale no human investigator could match manually.

* Maltego maps relationships between people, domains, email addresses, social media accounts,
  phone numbers, and organisations. It is used by investigators, journalists, and adversaries
  with equal facility.
* Shodan indexes internet-connected devices and their exposed services. Relevant when device
  identifiers or service configurations form part of a re-identification target.
* SpiderFoot and Recon-ng automate OSINT collection across dozens of data sources,
  cross-referencing usernames, emails, and identifiers to build profiles from fragments.
* theHarvester is a simpler tool focused on aggregating email addresses, hostnames, and
  names from public sources: a useful starting point before heavier correlation tools are applied.

## Stylometry and text fingerprinting

Writing style is a biometric. Stylometric analysis can attribute anonymous or pseudonymous text
to a known author with high confidence given sufficient sample size.

* JGAAP (Java Graphical Authorship Attribution Program) is an academic tool implementing
  a wide range of authorship attribution algorithms. It has been used in court cases and in
  research deanonymising forum posts and published papers.
* Burrows' Delta and related distance metrics are the statistical workhorses of authorship
  attribution, measuring the divergence between writing samples at the character and word level.

Stylometry is particularly relevant to deanonymisation of whistleblowers, anonymous reviewers,
and forum users who post substantial amounts of text under a pseudonym. The classical tools above have
largely been overtaken: transformer and embedding-based models now attribute authorship without a
candidate shortlist, and large language models infer an author's traits and identity from ordinary text
directly, as the [LLM-inference case](cases/llm-inference.md) shows.

## Notable reference cases and datasets

The research literature on re-identification relies on a set of landmark cases that demonstrate
what is possible with these tools.

* Netflix Prize dataset (Narayanan and Shmatikov, 2008): supposedly anonymous film rating
  data re-identified by cross-referencing with public IMDb reviews. Demonstrated that sparse,
  apparently innocuous behavioural data is highly identifying.
* AOL search logs (2006): 20 million search queries released as "anonymous" data. Journalists
  re-identified individuals within days from the content of their queries alone.
* NYC Taxi dataset (2014): taxi trip records with "anonymised" medallion and licence-number
  hashes cracked via brute force by Vijay Pandurangan, with Anthony Tockar then re-identifying
  individual passengers and their trips.
* de Montjoye mobility study (2013): showed that four approximate spatio-temporal data points
  are sufficient to uniquely identify 95% of individuals in a mobile location dataset of 1.5
  million people.

These cases are not historical curiosities. They are the proof of concept that shapes current
adversary practice, worked up in full in the [cases](cases/index.rst).

Last reviewed: 2026-07-08.
