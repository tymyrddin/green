# Attacks

## Inference attacks

The majority of attacks are inference attacks. The simplest inference attacks are derived from early code breaking, where codes were created by swapping around individual letters, or by substituting glyphs for the alphabetic characters. Once the relative frequency of the various letters in a character substitution language is found, messages using the code can be easily cracked.

In a similar fashion, a pseudonymised database may have the City field disguised. Cities have varying populations, and if the population in the database conforms to a known population, those cities can be identified, and this tentative identification can be firmed up by looking at the distribution of addresses within the city, or by other auxiliary information (also called background information) on individual cities. A seemingly somewhat harmless example. But not when combined with other information.

The easiest way of revealing individual data is to combine two or more databases. Once the individual is identified, an inference attack can then use the GPS location and movement data of a user, possibly with some auxiliary information, to deduce other personal data such as their home and place of work, interests and social network, and even home in on religion, health condition or business confidential data coming from the user's employer.

Data about people and their activities is passed around for research purposes. Advances in medicine can be made by finding patterns in existing patient and biomedical data. When such data is pseudonymised and made public or shared, it can unintentionally reveal sensitive data about an individual, such as their medical condition, or how much they were charged for treatment.

Every inference attack is slightly different because it depends on the data and relies on drilling down to a unique combination of characteristics. Available information such as friendships or group relationships in social media datasets can be used to infer sensitive properties that reveal hidden values or behaviours. Some techniques use algorithms to infer values or behaviours from customers' transactions using auxiliary information with temporal changes of recommender systems. Bayesian inference can be used to gain knowledge about communication patterns and profile information of users.

Naive suppression such as pseudonymising datasets does not prevent privacy breaches. The more useful a record is for scientific or marketing research, the more vulnerable it is to inference attack.

## Linkage attacks

Linkage attacks are another common form of de-anonymisation attacks. In this attack, adversaries collect and combine auxiliary information about a certain individual from multiple data sources with their anonymised records in a dataset to form a whole picture about their target, which is often an individual’s personally identifiable information.

For example, the adversary downloads a sanitised production network dataset that was released in the past. The dataset contains captured traces in which all MAC addresses have been sanitised and are thus unknown to the adversary. The adversary observes a sequence of AP association records of a target victim for a short period of time, to infer the MAC address from the released dataset that is associated with the victim. The attacker obtains broader knowledge of the victim’s mobility history from the released dataset, which leads to an infringement on the privacy of the user.

The possibilities are endless:

* A health care provider shares anonymised data with for example researchers from a pharmaceutical or health assurance company about medical conditions. The export contains "Gender," "Postal code," "Date of birth," and "Medical condition description." An adversary can easily use an open data (public made) voter list that contains "Name," "Gender," "Postal code," and "Date of birth" to cross-reference the patients.
* Netflix published data about movie rankings for 500,000 customers, and researchers showed they could de-anonymise the data using a few additional inputs from IMDb.
* AOL published search data for 650,000 users, thinking it was enough to anonymise their name using a unique ID. Unfortunately, most users often query their own name.
* Someone with access to an anonymous dataset of telephone records, might partially de-anonymise it by correlating it with a telephone order database of a catalogue merchant.
* Amazon online book reviews can be key to partially de-anonymising a database of credit card purchases, or a larger database of anonymous book reviews.
* Search engine databases with logs of internet searches, could easily be used de-anonymise a database of internet purchases, or zoom in on searches of medical terms to de-anonymise a public health database.
* And vice versa, detailed customer and purchase information datasets can be used to partially de-anonymise any released large anonymised search engine data set.
* A data broker holding databases of several companies might be able to de-anonymise most of the records in those databases.

The most common approach to mitigate linkage or correlation attacks is to anonymise data before exporting by removing personally identifiable information (PII). This does not suffice. At all. A better approach to protect against correlation attacks is to simply not share.

It was proposed, that if data is shared — to create layers of abstraction or generalisation by redacting parts of the data. If only microdata that contain spatial information in an aggregated form are released, the choice of applicable techniques for analysis becomes drastically reduced because distance calculations that are based on aggregated data become difficult and imprecise, especially for entities that are spatially close to each other. This then leads to the conclusion that to continue to do research on large datasets with privacy protection for the owners of the data, it is necessary to investigate the extent to which additionally published (approximate) inter-record distances influence the risk of identity disclosure and how a possible non-acceptable increase of this risk can be prevented.

Many organizations are not aware of the linkage risk involving quasi identifiers, and while they may de-identify direct identifiers in a dataset, they often do not think of de-identifying the quasi-identifiers in the dataset. Advanced anonymisation techniques of target datasets are needed.

## Structural attacks

This type of attack typically exploits social network structures by using graph matching on network datasets. Many people have accounts through various social networks such as Facebook, Twitter, etc. With structure-based attacks an individual's network context can be used to identify them even if other identifying information is removed. Even when equipped with advanced anonymisation techniques, the privacy of structural data can suffer from de-anonymisation attacks assuming that adversaries have access to rich auxiliary information from other channels.

Abstractly there is a graph G from which two graphs Gt (for "target") and Ga (for "auxiliary") are derived via some stochastic process. There is thus a natural notion of (partial) correspondence between the nodes of Gt and Ga; the goal of de-anonymization is to recover this correspondence.

The stochastic process involved could be as simple as the deletion of random edges. At the other extreme, if we're considering two entirely different online social networks, say Facebook and LinkedIn, then $ G$ is the underlying social graph of human relationships, and Gt and Ga are generated according to the processes by which users join online social networks, which has no simple algorithmic description.

The privacy-sensitive data closely related to individual behaviour usually contain rich graph structural characteristics. For example, social network data can be modelled as graphs and mobility traces (WiFi contacts, Instant Message contacts) can also be modelled as graph topologies. Even general spatio-temporal data (mobility traces) with the classical (latitude, longitude, timestamp) format can be converted to structural data. The resulting graphs represent entities connected by edges representing relations such as friendship, communication or shared activity, and can be combined for de-anonymisation purposes. Heuristics such as eccentricity, edge directionality, and reverse match receive an entirely new meaning.

Backstrom designed both active and passive attacks to break the privacy of SN users (leveraging the success of a "sybil" attack before actual anonymised data publication, therefor less practical); Narayanan effectively de-anonymised a Twitter dataset by using a Flickr dataset as auxiliary information based on the inherent cross-site correlations; Nilizadeh exploited the community structure of graphs to de-anonymise social networks; Srivatsa proposed to de-anonymise a set of location traces based on a social network (only suitable for small datasets due to the computational infeasibility of finding a proper land-mark mappings for large datasets); and the Grasshopper technique has a higher de-anonymisation effectiveness than other structural attacks.

Recently, in 2017 a novel blind structure-based de-anonymization attack, which does not require the attacker to have prior information (seeds), saw the light. The method experimentally demonstrated to be robust to data perturbations and claims to significantly outperform state-of-the-art de-anonymization techniques by up to 10× improvement. The method uses multi-hop neighbourhood information, and optimises the process of de-anonymization by exploiting enhanced machine learning techniques.

Several papers have claimed to provide k-anonymity, or variants thereof, for graphs. These have only been evaluated against graphs with a small number of nodes and small average degree, and only consider the threat of adversaries with restricted types of auxiliary information, which does not include global information such as another graph that is structurally related to the target graph.

Differential privacy might offer a potential method to bypass the need for anonymisation. A differentially private dataset (primarily, a sanitised item-item covariance matrix) instead of raw user data could be used, but restricts the class of machine learning algorithms that can be applied, and may require a shift from the "release-and-forget" model to an online privacy-preserving computation model.

## Resources

* [Daily Swigger: Inference attacks: How much information can machine learning models leak?](https://portswigger.net/daily-swig/inference-attacks-how-much-information-can-machine-learning-models-leak)
