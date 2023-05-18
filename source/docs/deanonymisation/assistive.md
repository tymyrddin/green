# Assistive technologies

Data science skills that make adversaries highly effective at de-anonymisation are matching features, prediction and inference, which all require computational, statistical and probabilistic skills.

## Behavioural analysis

The intention of behavioural targeting is to track users over time and build profiles of their interests, characteristics, such as age and gender, and shopping activities. Online advertisements use behavioural targeting to display advertisements that reflect users' interests.

Developing an understanding of behaviour is not a new idea, and it already has uses in a variety of related contexts. For example, behavioural monitoring is a long-standing technique in the context of Intrusion Detection Systems (IDS), law enforcement agents use profiling all the time (and when based on racial profiling interferes with the system of criminal justice), and so-called profilers, specially trained agents, look at a crime scene, autopsy data, victims, and likely pre-crime and post-crime behaviours of a serial killer to make psychological assessments (that are considered by some to be 'worse than useless').

Based on mining data, including inference and linkage attacks in which data is associated from one source with data and online behaviour from other sources, the profiling practice is being used in surveillance systems, to tailor our digital experiences for us, by for example marketers to try to get us to consume more, and by politicians to influence elections.

Behavioural analytics requires and includes:

* Available data sets, possibly bought from data brokers or on a black market.
* Real-time capture of vast volumes of raw event data across all relevant digital devices and applications used during on-line sessions.
* Automatic aggregation of raw event data into relevant data sets for rapid access, filtering and analysis.
* Ability to query data in a number of ways, enabling users of the analytics system to ask questions.
* A library of built-in analysis functions such as cohort, path and funnel analysis.
* A visualization component.

Cohort analysis breaks all users into related groups (sharing common characteristics or experiences within a defined time-span) for analysis in order to understand if a group is doing what it’s supposed to be doing (or what a company/organisation/agency/government wants those individuals to do) on a regular basis.

For example, in an IoT application, are a group of machines – say for example edge devices such as smart thermostats – streaming the necessary data? In an e-commerce site like Amazon, are customers in a certain demographic completing a purchase?

What are the desired actions or results? And what are the paths that can get the actor (user) to take those? These questions belong to the domain of path analysis.

An individual may take any number of steps before reaching a desired state. A path analysis analyses all the points and actions that individuals take at each point. Streamlined paths to a desired state can be identified and points in a path where a barrier exists that keeps individuals from moving forward. Path analysis gives insight into why people are doing what they are doing, and at what point they are doing it.

Funnel analytics are used to identify users’ progress through defined steps towards a specific goal. It shows the narrowing of participants as they move along a sequence to an end state. For example, Amazon offers a portfolio of products, then a specific product page, online reviews about the product, a shopping cart button, fields for shipping options and credit-card entry, and finally a purchase button.

With funnel analysis the rate at which individuals follow the steps of a sequence to produce an end state can be analysed. In other words, how many people dropped out of the funnel versus those that actually bought the product? Who were they?

Funnel analysis can be combined with cohort analysis: Did a specific group of people or machines drop out at one stage of the sequence?

## Content analysis

Content analysis is a method for analysing a user’s content (in online social networks) for providing information about its structure or some attributes.

_Content analysis is a research tool used to determine the presence of certain words or concepts within texts or sets of texts. Researchers quantify and analyze the presence, meanings and relationships of such words and concepts, then make inferences about the messages within the texts, the writer(s), the audience, and even the culture and time of which these are a part. Texts can be defined broadly as books, book chapters, essays, interviews, discussions, newspaper headlines and articles, historical documents, speeches, conversations, advertising, theater, informal conversation, or really any occurrence of communicative language._ 

Because it can be applied to examine any piece of writing or occurrence of recorded communication, content analysis is used in many fields, from marketing and media studies, to literature and rhetoric, ethnography and cultural studies, gender and age issues, sociology and political science, psychology and cognitive science, and many other fields of inquiry.

## Link prediction

Link prediction is a method that an adversary can use to bridge between auxiliary information and a target dataset if they are from different sources and have little in common for matching.

## Predictive analysis

Predictive analytics is the practice of extracting information from existing current and historical data sets in order to determine patterns and predict future outcomes and trends by statistical techniques from modelling, machine learning, and data mining. Predictive analytics does not tell you what will happen in the future.

### Clustering

Cluster analysis can be used when there are a lot of content nodes that are to be divided into different content clusters, and no idea how to create them. Rather than defining groups before looking at the data, clustering allows for finding and analysing groups that have formed “organically” (based on similarity). Applications for cluster analysis include gene sequence analysis, market research, and object recognition.

When choosing a clustering algorithm, consider whether the algorithm scales to the dataset. Not all clustering algorithms scale efficiently. Many clustering algorithms work by computing the similarity between all pairs of examples. This means runtime increases as the square of the number of examples.

* Centroid-based clustering organises the data into non-hierarchical clusters. K-means is the most widely-used centroid-based clustering algorithm. Centroid-based algorithms are efficient but sensitive to initial conditions and outliers.
* Connectivity-based (alias hierarchical) algorithms create a tree of clusters. An advantage is that any number of clusters can be chosen by cutting the tree at the right level.
* Density-based algorithms connect areas of high example density into clusters, allowing for arbitrary-shaped distributions. These algorithms have difficulty with data of varying densities and high dimensions. And by design, these algorithms do not assign outliers to clusters. With the OPTICS algorithm one can view intrinsic clustering structure that could otherwise be identified only in a process of repeated clustering with different parameter settings.
* Probabilistic (alias distribution-based) algorithms assume data is composed of distributions. As distance from the distribution's centre increases, the probability that a point belongs to the distribution decreases. Do not use if distribution is not known.
* Dimensionality reduction reduces the number of features under consideration, where each feature is a dimension that partly represents the objects. With too many features, the data matrices become sparse and analysis suffers from the curse of dimensionality (loss of statistical significance). Plus that it is easier to process smaller data sets. This is achieved by feature selection or feature extraction (combining existing features). The main technique used for feature extraction is Principle Component Analysis (PCA)
* Neural networks/Deep learning are a set of algorithms, modelled loosely after the human brain, that are designed to recognise patterns. They interpret sensory data through a kind of machine perception, labelling or clustering raw input. The patterns are numerical, contained in vectors, as translations of images, sound, text or time series.

Clustering algorithms can be used in social graph analysis.

### Classification

Classification models classify input data into categories. Typical applications include medical imaging, speech recognition, and credit scoring.

Classification is the process of finding a model (or function) that describes and distinguishes data classes or concepts, for the purpose of being able to use the model to predict the class of objects whose class label is unknown. The derived model is based on the analysis of a set of training data (data objects whose class label is known). The derived model can take the form of classification (IF-THEN) rules, decision trees, mathematical formulae, or neural networks.

* A decision tree is a flow-chart-like tree structure, where each node denotes a test on an attribute value, each branch represents an outcome of the test, and tree leaves represent classes or class distributions. Decision trees can easily be converted to classification rules.
* A neural network, when used for classification, is a collection of neuron-like processing units with weighted connections between the units.
* There are many other methods for constructing classification models, such as support vector machines, Naïve Bayesian Classification, and Nearest Neighbour Classification.

Classification algorithms can be for customer retention or developing a recommendation engine.

### Regression analysis

Regression analysis is a form of predictive modelling technique which investigates the relationship between a dependent (target) and independent variable(s) (predictor). This technique is used for forecasting, time series modelling and finding the causal effect relationship between the variables. Typical applications include electricity load forecasting and algorithmic trading.

Regression analysis:

* Indicates the significant relationships between dependent variable and independent variable.
* Indicates the strength of impact of multiple independent variables on a dependent variable.
* Can be used to compare the effects of variables measured on different scales.

Regression algorithms can be used for predicting the next outcome of time-driven events, for example in network monitoring.

## Spammer elimination

Accounts made for spamming tend to make random links with other users. These developing edges may lower the effectiveness of de-anonymisation attacks. Discovering and removing these spamming nodes may improve effectiveness of de-anonymisation efforts. Classification analysis can be used to identify spam.

## Data storage

The type of storage (NoSQL database, standard SQL database, or some kind of object storage), depends on the type of data (user input or behavioural) and on factors such as ease of implementation, the amount of data that the storage can manage, integration with the rest of the environment, and portability.

Online frameworks such as Apache Hadoop (a software framework for distributed storage and processing of big data using the MapReduce programming model) and Apache Spark (a unified analytics engine for big data processing, with built-in modules for streaming, SQL, machine learning and graph processing) allow for storing data in multiple devices to reduce dependability on one machine. Hadoop uses HDFS to split files into large blocks for distribution across nodes in a cluster. The dataset can be processed faster and more efficiently than it would be in an architecture that relies on a parallel file system.

_Spark has been found to run 100 times faster in-memory, and 10 times faster on disk. It’s also been used to sort 100 TB of data 3 times faster than Hadoop MapReduce on one-tenth of the machines. Spark has particularly been found to be faster on machine learning applications, such as Naive Bayes and k-means._

## Timeliness

* Real-time systems process data as it is created and involves tools that can process and analyse streams of events. These are useful for example, for in-the-moment recommendations.
* Batch analysis requires the processing of data periodically and implies that enough data needs to be available in order to make the analysis relevant. These can be used for analysis at a later date.
* Near-real-time analysis gathers data quickly and allows for refreshing analytics every few minutes or seconds. These are useful for in the same browsing session.

Using the MapReduce programming model to process big data sets, it is possible to run algorithms in a distributed file system at the same time and choose the most similar cluster.

## Resources

* [Content Analysis](https://writing.colostate.edu/guides/guide.cfm?guideid=61), Writing@CSU | The Writing Studio
* [Understanding the qualitative and quantitative methods in the context of content analysis](http://www.isast.org/proceedingsQQML2009/PAPERS_PDF/Devi-Understanding_the_Qualitative_and_Quantatitive_Methods_PAPER-QQML2009.pdf), Naorem Binita Devi, 2009
* [Link Prediction by De-anonymization: How We Won the Kaggle Social Network Challenge](https://arxiv.org/abs/1102.4374), Arvind Narayanan, Elaine Shi, Benjamin Rubinstein, 2011
* [Detecting spammers on social networks](https://www.sciencedirect.com/science/article/pii/S0925231215002106), Xianghan Zheng, Zhipeng Zeng, Zheyi Chen, Yuanlong Yua, Chunming Rong, 2015


