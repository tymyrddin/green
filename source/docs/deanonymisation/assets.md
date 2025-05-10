# Assets

## Data releases

Assuming three main contexts of data release, in which each presents a different relationship, therefore a different level of trust between the data provider and data recipient, and a different level of control and risk.

Internal secondary research is about data re-use. For example, clinical trial sponsors store and maintain vast amounts of data collected during clinical studies. The cumulative information may be invaluable for identifying patterns which are not the focus of the original trials. Sponsors are required to obtain consent for such use of patients' data, which they may claim is not possible or entirely impractical (due to the enormous amounts of “data subjects”). The alternative is to anonymise the data such that it is no longer considered personal information. In this scenario access to data is controlled by mechanisms much like those used in primary analysis. While the requirement to de-identify the data needs to be observed, the risk of re-identification attempts is considered minimal.

External secondary research is about sharing data with external researchers, under strict contracts, through secure means will supposedly ensure that the process is safe and the risks involved very low. The anonymisation process will have already considered the probability of de-anonymisation attempts – rogue employee, data breach, etc. - and taken it into account in finding and applying adequate level of anonymisation. Introducing contractual controls and limitations on how the data is accessed, used and disposed of, is thought to significantly limit the motivation of the data recipient to attempt de-anonymisation and illicit use of data.

When data is released to the public domain, there is no control over how it will be used and an adversary wanting to access the data can do so with little effort. The data industry is confronted with finding it hard to assess motivations of adversaries and the level of knowledge and tools they may possess and use and that may land its data guardians in protective states of mind that may lead to significant loss of data usability. The industry therefore finds it crucial to identify plausible adversaries relevant to a context and contents of the data release which they think may result in less de-anonymisation and greater data utility retention. 

## Auxiliary information

Auxiliary information is the information gained as background knowledge by the adversary. It is any data that might be combined with other data(sets) to give meaningful information. It is usually gathered from real world information (but not always, this too has expanded):

* with the usual information gathering techniques for example from work environments, such as personal information of/from colleagues, from dumpster diving, and from any public information, such as a voter list, petition sites, forum comments, or reviews in websites, to name but a few.
* from neighbourhood data collected in open data sets.
* from another dataset that was either bought at a black market or gained from a merger or buying up a small data company.
* and in some cases even from the target dataset.

## Target dataset

The target dataset is a set of anonymous data (also known as de-identified data).

The most common methods for de-identification (anonymisation) are by removing personal identifiable information (PII) such as ID and phone numbers, and using sophisticated anonymisation schemes such as k-anonymity, l-diversity, and t-closeness. The new kid on the block is differential privacy.

Personal data, also known as personal information, personally identifying information (PII), or sensitive personal information (SPI), is any information relating to an identifiable person. Personally identifying information is a legal concept, not a technical concept, and is not used in the same way in all jurisdictions. Plus that with current re-identification attacks, the absence of PII data does not mean that the remaining data does not identify individuals.

### k-anonymity

A dataset provides k-anonymity protection if the information for each individual in the dataset cannot be distinguished from at least k − 1 individuals whose information also appears in the dataset.

k-anonymity and its variants can protect the privacy of structural data to some extent, but are susceptible to structure-based de-anonymisation attacks due to the limitations of the schemes (they are syntactic properties based) and the rich amount of auxiliary information available to adversaries.

### Differential privacy

With static anonymisation, an analyst must decide ahead of time which fields contain sensitive data, and then either remove or alter these fields before running the analysis, which reduces the quality of the data set. Plus, the analyst must also consider any auxiliary information a potential hacker might have that could lead to re-identification of the sensitive fields. With dynamic anonymisation, also called interactive anonymisation, data is anonymised on a query-by-query basis, without destroying the quality of the data set.

In differential privacy a query should not reveal whether any one person is present in a dataset or what their data are. Imagine two otherwise identical datasets, one with an individual's information in it, and one without it. The probability that a query will produce a given result is nearly the same whether conducted on the first or second dataset. If an individual's data does not affect the outcome of a query, then it might be okay to give this information because it is unlikely that the information would be tied back to the individual. And, if an analysis on a dataset finds a correlation between two characteristics, then interpretation of and assigning significance to the correlation, might have an effect on an individual with that characteristic, regardless of whether the individual's dataset was included in the study.

In short, differential privacy supposedly offers the benefits of data research without sacrificing privacy and supports “Legitimate Interest” processing by overcoming shortcomings of “static” data protection techniques that do not adequately protect data subjects against unauthorised re-identification when data is combined from multiple sources or used for various purposes.

Jane Bambauer, Krishnamurty Muralidhar, and Rathindra Sarathy have shown that by itself differential privacy will usually produce either wrong research results or useless privacy protections. Differential privacy was developed to protect the privacy of interactive data release. It cannot defend against structural data de-anonymisation attacks which can breach the privacy of non-interactive data releases.
