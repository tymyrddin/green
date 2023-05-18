# Attack vectors

## Classification analysis

Classification analysis is a data mining technique that enables recognising patterns (recurring schemes) inside a dataset. It is considered an effective solution to improving marketing strategy performance, deleting superfluous information and creating subclasses.

Real-world datasets, such as scientific publication datasets and social network datasets, contain interlinked entities and exhibit correlations among labels of the interlinked entities (for example, friendships and group memberships). Link-based classification can exploit such correlations in the link structure to identify private attributes.

Group-based classifiers can be combined with auxiliary information to identify users in social networks (or to significantly reduce the set of possible candidates). Meaning that rather than tracking a user’s browser with cookies, it is possible to track a person. To determine the group membership of a user, well-known web browser history stealing attacks have been used: whenever a social network user visits a malicious website, this website can launch the de-anonymisation attack and learn the identity of its visitors.

The similarity classifiers approach uses local features such as activity over time, text, geographic, and social features to form similarity classifiers that predict whether or not two accounts from two different social platforms are belonging to the same individual by deciding on similarities between them.

## Matching features

Cluster analysis enables identifying a given user or user group according to features, that can include age, geographic location, education level, etc. It is a data mining technique that is in use in marketing to segment a dataset and, for example, send a message to the right target for that product or service (young people, mothers, pensioners, etc.). The variable combinations are endless and make cluster analysis more or less selective according to the search requirements.

Similarity is the underlying principle for making product recommendations (identifying people who are alike in terms of the products they have purchased or have liked). Online retailers such as Amazon use similarity to provide recommendations of similar products. When expressions like “People who like A also like B” appear, similarity has been applied. Similarity matching tries to recognise similar individuals based on known information about them.

Similarity matching is also an approach where attacks rely on similar features between a target dataset and auxiliary information to perform the matching. For example, mobility traces (WiFi contacts, Instant Message contacts) can be used to find distance similarities that are then matched with the help of statistical predictors. Similarities can be matched between social data and mobility traces data, and between resume and tweets, and some techniques use node similarity to match graphs in social networks.

Matching statistics maps datasets statistically and relies on the unique features of users' data (intrinsic characteristics, such as interests and political views), to perform matching operations that can lead to users being identified and tracked.

## Graph matching

Graph matching is a network structure vector and the most common approach. It focuses on matching two graphs from the same target domain or two different domains. Privacy can be breached once its network structure is revealed, as a standard technique of re-identification can be developed based on that.

* Find the largest common sub-graph between a pair of ego nets
* Focus on common nodes of two graphs that are at 1-hop from the center
* Use the degree distribution of nodes and observe the 1-hop neighbourhood degree distribution of the common nodes, storing each node's degrees in a list as a signature.
* If matching signatures are found between a pair of nodes from the two graphs, those nodes are considered to be the same.

This simple version does not work with graphs where common nodes are 2-hops away from the centre, but n-hop algorithms have been developed and can de-anonymise more data. Naive anonymisation of social network graphs often uses deleting all identifying information of the users, while maintaining the original graph structure.

Graph matching can start by creating a node (for example a user account) in a social graph and building up links with other nodes. Some call this graph matching expansion process “seed & grow”. When combined with link prediction it can give high accuracy and coverage for an attack.

Active attacks in which the adversary registers a number of fake users (sybils) with the social network, allows for creating unique structural patterns that can be used used to re-identify the sybil nodes and other users after anonymisation. Studies showed that adding a small amount of noise to the published graph sufficed to mitigate such active attacks, but new robust active attacks merely see that as an optimisation problem for which various heuristics can be used.

Graph matching can also start with threading. The threading method can be used for correlating sequential releases that are then matched. This works best in dynamic social networks that grow fast. In later research it was noted this can be used to detect users with multiple accounts (sybils).

## Trail re-identification

The trail re-identification approach was developed for linking genomic data to their identified users whose records are publicly available in various databases.

The concept of trail re-identification includes de-anonymising users by collecting network data and then mapping their anonymised traces with IP addresses, matching IP addresses with Tor hidden services using traffic analysis, and tracking users by detecting their fingerprints in web browsers (visited web pages in the browser’s history).

## Sparsity-based

Sparse data share few relationships, but the activity stream of the target within anonymised sets of streams can be gathered from other users. Activity relationship mining consists of rules that link various aspects of two captured activity types and can help decide if two activities were probably achieved by the same individual or not. Existing sparsity-based techniques have been adapted to exploit mobile sensor data characteristics, indicating significant threats to user anonymity within shared mobile sensor data.

Several studies looked at the advantages of sparsity for de-anonymisation. De-anonymisation could improve due to database sparsity and if the auxiliary information consists of values matching with rare attributes of a target database, then the de-anonymisation achieved is greater. It is not the sparsity, but in what way it is sparse that provides information.

In 2017, the social network de-anonymisation problem was converted into a binary classification problem between node pairs. Using the spectral partition method, large sparse social networks were partitioned into a number of small sub graphs. The features of the network structure were used to train the random forest classifier. As a result, candidate node pairs from anonymous network and auxiliary network can be classified as matched pair by the random forest classifier.

## Resources

* [To Join or Not to Join: The Illusion of Privacy in Social Networks with Mixed Public and Private User Profiles](https://users.soe.ucsc.edu/~getoor/Papers/zheleva-www09.pdf), Elena Zheleva and Lise Getoor, 2009
* [A Practical Attack to De-Anonymize Social Network Users](https://sites.cs.ucsb.edu/~chris/research/doc/oakland10_sonda.pdf), Gilbert Wondracek, Thorsten Holz, Engin Kirda, Christopher Kruegel, 2010
* [De-anonymizing Users Across Heterogeneous Social Computing Platforms](http://vision.soic.indiana.edu/papers/deanonymize2013icwsm.pdf), Mohammed Korayem, David Crandall, 2013
* [Trail Re-Identification:Learning Who You Are From Where You Have Been](https://dataprivacylab.org/dataprivacy/projects/trails/paper3.pdf), Bradley Malin et al., 2013
* [Trawling for Tor Hidden Services: Detection, Measurement, Deanonymization](https://www.ieee-security.org/TC/SP2013/papers/4977a080.pdf), Alex Biryukov, Ivan Pustogarov, Ralf-Philipp Weinmann, 2013
* [De-anonymizing Social Networks with Random Forest Classifier](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8051053), Jiangtao Ma, Yaqiong Qiao, Guangwu Hu, Yongzhong Huang, 2017

