# Attack vectors

Every greenhouse has pests — some nibble discreetly, others dig tunnels and chew through your best tomatoes. These 
attack vectors are the techniques adversaries use to sneak past the hedgerows of anonymisation and figure out what 
you’re really growing.

## Classification analysis

This one’s a bit of a nosey neighbour. It stares through the hedge and says, “Ooh, looks like you’ve got strawberries. 
You must be Mrs Davies from No. 12!”

Classification analysis is about pattern spotting. Using bits of known information, it links data together and 
guesses hidden traits. Link-based classification? That’s when your plant tags (or social network friends) give you 
away. Group-based classifiers? That’s when your web history gets rummaged through, and suddenly you’re “inferred” 
to be part of the mums-who-bake-and-vote club.

## Matching features

Ah, the classic “you look familiar” move. Matching features is about comparing your anonymous daisy patch to another 
known one and saying, “This petal looks just like yours.”

Cluster analysis and similarity matching are favourites of marketing teams and identity thieves alike. Whether it’s 
what you bought last week or where your Wi-Fi pinged on a Tuesday, if someone’s got enough snippets, they can build a 
you-shaped profile. Think Amazon’s “People who bought A also like B” — except it’s “People who tweeted this also 
live near you and probably own a dog.”

## Graph matching

This one’s for the adversaries with whiteboards and string — proper conspiracy chart stuff. Graph matching doesn’t 
care about your name; it cares about how you’re connected.

It builds maps of social relationships — who talks to whom, how often, and when. Even if all the names are 
scrubbed off, the shape of the network is often enough to spot someone. Got a very specific set of friends or 
habits? Congratulations, you’re now a node signature.

They can match graphs one-to-one, seed a network with fake accounts to track patterns, or even stitch together 
data from multiple leaks over time. Basically, once the structure’s out, the game’s up.

## Trail Re-identification

Ever tried to hide your footprints in a greenhouse? Doesn’t work too well.

Trail re-identification tracks your digital movements — browser history, genetic data trails, even Tor traffic patterns. 
It’s like putting flour on the floor and then acting surprised when someone follows your steps back to the watering can.

Whether it’s matching fingerprints left on websites or correlating public DNA records to anonymous ones, it’s all 
about chasing those faint trails back to you.

## Sparsity-based attacks

Some data is dense and juicy. Other bits are sparse — a few crumbs here and there. And somehow, those crumbs are 
even more dangerous.

Sparsity-based techniques look at rare behaviours or combinations that make you stand out. If you're the only person 
who likes yak cheese, votes Green, and lives in a postcode with six other humans, congrats — you’re now de-anonymisable.

These attacks thrive on uniqueness. The more unusual your data, the easier it is to spot you — especially when 
someone’s already got a handful of matching facts from somewhere else.

## Resources

* [To Join or Not to Join: The Illusion of Privacy in Social Networks with Mixed Public and Private User Profiles](https://users.soe.ucsc.edu/~getoor/Papers/zheleva-www09.pdf), Elena Zheleva and Lise Getoor, 2009
* [A Practical Attack to De-Anonymize Social Network Users](https://sites.cs.ucsb.edu/~chris/research/doc/oakland10_sonda.pdf), Gilbert Wondracek, Thorsten Holz, Engin Kirda, Christopher Kruegel, 2010
* [De-anonymizing Users Across Heterogeneous Social Computing Platforms](http://vision.soic.indiana.edu/papers/deanonymize2013icwsm.pdf), Mohammed Korayem, David Crandall, 2013
* [Trail Re-Identification:Learning Who You Are From Where You Have Been](https://dataprivacylab.org/dataprivacy/projects/trails/paper3.pdf), Bradley Malin et al., 2013
* [Trawling for Tor Hidden Services: Detection, Measurement, Deanonymization](https://www.ieee-security.org/TC/SP2013/papers/4977a080.pdf), Alex Biryukov, Ivan Pustogarov, Ralf-Philipp Weinmann, 2013
* [De-anonymizing Social Networks with Random Forest Classifier](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8051053), Jiangtao Ma, Yaqiong Qiao, Guangwu Hu, Yongzhong Huang, 2017

