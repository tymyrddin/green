# Impacts

## ↑ Data

One of the most often mentioned issues with personal information mined from an individual's consumption behaviour for purposes of recommending products and/or services to that individual, is that it can cause pain and embarrassment to individuals, and it can deliver noise.

* What if you are permanently in a wheelchair and out of curiosity or for buying a family member or friend a gift, checked products online that someone in a wheelchair cannot use, and then get offered similar products on your screen for days?
* What if you are a teenage girl visiting a website that sells baby products, and the application of the company sends promotional baby products to your home address?

In short, companies seem to think that if more information is disclosed and used, sales of products will automatically increase. Data gathered in large pools of information, is increasingly a focus of technology competition.

Instead, better approaches on how to interpret data, models, and understanding the limitations of both in order to produce better output are required. Data without sound approaches becomes noise. Better Data != ↑ Data

* Better data does not mean more data, sometimes it means less (data cleansing, outlier removal, stratified sampling).
* Content-based features (or different features in general) might be able to improve accuracy in many cases, but not always.
* High bias situations (a model that is too simple to explain the data) will not benefit from more training examples, but might indeed benefit from more features.
* High variance situations (a model that is too complicated for the amount of data, the training error is much lower than the test error) leads to model over-fitting, and can be addressed by reducing the number of features, and by increasing the number of data points.
* Complex algorithms can limit the ability of scaling up to larger number of features.

## ↑ Bias and discrimination

Human agency and oversight: AI systems are to enable equitable societies by supporting human agency and fundamental rights, and not decrease, limit or misguide human autonomy.

The models used are opaque, using them with real data is officially regulated in Europe (but public authorities and civil society struggle to apply its rules in concrete ways), and the results of the models are mostly incontestable, even when they introduce and reinforce bias and discrimination at every level (selection, confirmation, etc):

* A chatbot that became racist. Tay made it to the [MIT Technology Review’s list of 2016’s biggest technology failures](https://www.technologyreview.com/2016/12/27/106828/the-biggest-technology-failures-of-2016-3/).
* HR resume/candidate screening applications that discriminate based on some characteristic (age, gender, religion, etc).  If a marginalised person does not get a job because an employer receives a report that contains by the employer unwanted characteristics, he/she will not get the opportunity to gain respectability and independence. Instead, the vicious spiral continues.
* If a poor student cannot get a loan because a lending model deems him or her too risky (by virtue of where he/she lives), he/she is then cut off from the kind of education that could pull him/her out of poverty, and another vicious spiral continues.
* If DNA analysis companies start selling anonymised data to insurance companies they will be able to include it into their risk analysis. There will be a lot of biases, a lot of mistakes. On average nothing will change but there will be biased shifts in premiums in subgroups.

In short, if your data belongs to a subgroup even if you do not share every characteristic of that subgroup you might be negatively impacted. Models favour the lucky and punish the underdogs. The dark side of Big Data. Yet recommending that humans should be involved in the decision-making processes also has to take into account that it is people that have the most bias. They create algorithms that are biased.

Avoiding bias is hard. Techniques and checks to identify it is not so hard to make and critical thinking to rectify it is not that hard to learn either. But as with security in the past decades, it seems not a main concern of digital business-as-usual because it doesn't make money.

## ↓ Competition

Datasets seem to be incredibly valuable to companies:

* Microsoft purchased LinkedIn for $26.2 billion last year. LinkedIn has about 467 million members (and their profiles and connections).
* IBM has acquired Truven Health (data on the cost and treatment of more than 200 million patients) for $2.6 billion and $2 billion for the digital assets of the Weather Company.
* Google offers businesses a new software service to improve job finding and recruiting. Its data includes more than 17 million online job postings and the public profiles and résumés of more than 200 million people.

Increasingly, data collection, analysis and distribution creates and shapes markets. If the big internet companies attract more users and advertisers, and gather more and more data, a powerful "network effect" may prevent users and advertisers from moving away from a dominant digital platform, like Google in search or Facebook in consumer social networks. As a result, people might be afforded less privacy than they would choose in a more competitive market.

## ↑ Surveillance and tracking 

Every citizen on this planet is subject to some sort of tracking/surveillance. This includes information that does not, by itself, identify individuals, but sits in various databases (datasets) until data scientists use it for some purpose. The proximate reasons for the culture of surveillance are clear:

* Storage is cheap enough that we can keep everything.
* Computers are fast enough to examine this information, both in real time and retrospectively.
* Our daily activities are mediated with software that can easily be configured to record and report everything it sees upstream.
* But to fix surveillance, we have to address the underlying reasons that it exists. These are no mystery either.
  * State surveillance is driven by fear.
  * And corporate surveillance is driven by financial gain (which is also driven by fear).

Data can be explicit or implicit. Explicit data consists of data users provide explicitly such as ratings and comments on products. Users have a choice whether to provide it or not. Implicit data does not need any extra action from the user. Examples of implicit data are order history/return history, cart events, page views, click through, and search logs. This data set is created for every user visiting an e-commerce/online business. Behavioural data is easy to collect because it can be extracted from a log of user activities and/or bought from data brokers.

Tracking is categorised into first-party and third-party tracking. The user is the second-party. In first-party tracking, the tracking is performed by the site or application with which the user is directly interacting. In third-party tracking, the tracking is performed by a third party that tracks the user's activity over time and across different devices and (digital or analogue) locations.

* Facebook tracks across sites via its Like button; each time a user visits a site that contains a Facebook Like button, Facebook collects this information, even if the user does not click on the button.
* In the first-party context, behavioural tracking and profiling is used to recommend products that are likely to be of interest to users. Amazon recommends products to online users based on individuals’ past behaviours (personalised recommendation), on past behaviours of similar users (social recommendation) and on searched items (item recommendation).
* With the rise of mobile phones, mobile applications track users' locations and movement. Location information enables many useful services such as receiving driving directions and knowing where your kids are. And this information is also collected by marketers to improve profiling. This poses a threat to location privacy, as illustrated by iPhone and Android controversies.
* Increasingly, consumer devices are capable of being connected online. Smart entertainment systems can monitor what users watch, smart meters can hand over information that can be used to discover what you watch, when you do your laundry and how much, what time you leave and come home, and more such behaviours.
* Somatic surveillance is the increasingly invasive technological monitoring of and intervention into body functions. Within this type of tracking regime, bodies are recast as nodes on vast information networks, enabling corporeal control through remote network commands, automated responses, or self-management practices. Insurance companies are very, very interested.

## ↑ Regulation

The GDPR only addresses privacy concerns related to data processing by the private sector and not by individual EU member states. With the internet being a global network (driven by established interests), laws regarding for example, digital fingerprinting by law enforcement and intelligence agencies, may develop completely differently from one country to another regardless of raised concerns at the EU level as to the compatibility of such activities with human rights standards.

Social media shift the boundaries of what counts as private and public space, creating anxieties about the very visible and seemingly permanent nature of social media activity. Given the long history of disproportionate surveillance among marginalised people and activists by law enforcement through practices such as profiling, infiltration and other covert policing tactics, the question is what is new and different about social media that may risk aggravating these inequalities. With not enough understandable information about how monitoring tools are used by the police, we cannot effectively assess the risks of discriminatory practices and targeting of minorities.

Social media can produce evidence in some cases, but data mining fails to capture the complexity of human relationships, and can sometimes distort the interpretations. It is important to make sure that social media data is not misused or misinterpreted in the pursuit of justice.

Both Evanna Hu ([Responsible Data Concerns with Open Source Intelligence, Evanna Hu, November 2016](https://responsibledata.io/2016/11/14/responsible-data-open-source-intelligence/)) and Millie Graham Wood ([Social media intelligence, the wayward child of open source intelligence, Millie Graham Wood, December 2016](https://responsibledata.io/2016/12/12/social-media-intelligence-the-wayward-child-of-open-source-intelligence/)) made a case by stating that social media do not easily fit into either the category of public or private and argue that it is instead a pseudo-private space, where there is an expectation of privacy from the state. Millie Graham Wood, Legal Officer at Privacy International, proposes making a distinction between Open Source Intelligence (OSINT) and Social Media Intelligence (SOCMINT).

***OSINT*** is intelligence collected from publicly available sources, including the internet, newspapers, radio, television, government reports and professional and academic literature. ***SOCMINT*** can be defined as "the analytical exploitation of information available on social media networks".

Data is increasingly a focus of technology competition ([Big data: Bringing competition policy to the digital era, OECD, November 2016](https://www.oecd.org/daf/competition/big-data-bringing-competition-policy-to-the-digital-era.htm)). And academics and some policy-makers, especially in Europe, are considering whether big internet companies like Google and Facebook might use their data resources as a barrier to new entrants and innovation. Who controls what data could be the next worldwide regulatory focus because monopolies could threaten privacy.

The [EU’s ePrivacy regulation](https://iapp.org/resources/topics/eu-eprivacy-regulation/) extends the GDPR, focusing specifically on cookies and other tracking technologies. It’s set to go into effect as early as 2023 and promises to be even more stringent than the GDPR regarding protecting internet user privacy.
