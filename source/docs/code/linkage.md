# Linkage attack

Anonymisation removes names. It does not remove distinctiveness. A person who appears in two different datasets, one with their name stripped and one without, can often be re-identified by the combination of other attributes that are present in both: the city they live in, their age range, the time of day they tend to post, the topics they discuss. The linkage attack matches these quasi-identifiers across datasets to re-identify individuals who believed themselves protected.

## How it works

The attack requires two datasets with overlapping attributes. Neither dataset need contain an explicit identifier. The quasi-identifiers do the work of matching.

```
dataset_A: anonymised forum posts
    user_hash | post_timestamp | topic | city | age_range

dataset_B: public records (voter rolls, company directories, etc.)
    full_name | city | age_range | occupation | other_attributes

# Attack:
for each user in dataset_A:
    candidate_matches = find records in dataset_B where:
        city matches dataset_A.city
        AND age_range matches dataset_A.age_range

    if exactly one candidate_match:
        confidence = "high"
        inferred_identity = candidate_match.full_name
    if multiple candidates:
        confidence = "medium"
        apply additional attributes to narrow further:
            posting_time vs. work_schedule
            topic_preferences
            writing_style
```

Each additional quasi-identifier reduces the number of candidates. City and age range alone may leave dozens of possibilities. Add posting time patterns and the field narrows. Add topic preferences and it narrows further. The combination of individually unremarkable attributes converges on a specific person.

## What this reveals

Latanya Sweeney's landmark research, published in 2000, demonstrated that 87% of Americans could be uniquely identified from only three attributes: zip code, date of birth, and sex. None of those is a name. All of them appear routinely in "anonymised" health records, research datasets, and government data releases.

The implications are significant for any organisation that releases aggregated or anonymised datasets. Releasing a medical dataset with names removed, ages and postcodes intact, alongside a voter roll that contains ages and postcodes, creates the conditions for re-identification without either dataset being inherently sensitive. The risk is not in the individual datasets but in their combination.

This is also the mechanism behind many data broker profiles: no single source contains a complete picture, but combining purchases, location history, browsing data, and public records creates one that is effectively comprehensive.

## Defences

Differential privacy adds calibrated noise to aggregate statistics in a dataset, making it possible to publish useful results while providing mathematical guarantees against re-identification. Data minimisation, collecting and publishing only the attributes genuinely necessary for the stated purpose, reduces the surface available for linkage. Generalising attributes before release, publishing age ranges rather than ages, city rather than postcode, reduces quasi-identifier precision. The appropriate level of generalisation depends on the size of the population and the number of other available datasets, which makes this a calculation rather than a policy.
