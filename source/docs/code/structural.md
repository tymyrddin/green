# Structural attack

Who communicates with whom, and how often, reveals as much about an organisation as the content of the communications themselves. A structural attack maps the pattern of interactions rather than reading any message, using graph analysis to infer roles, hierarchies, and relationships from metadata alone.

The technique treats each person as a node and each communication as a directed edge. The properties of the resulting network, which nodes have the most connections, which serve as bridges between groups, which clusters communicate densely internally and sparsely across boundaries, carry information that was never intended to be disclosed.

## How it works

The input is a log of email metadata: sender, recipient, and timestamp. No message content is needed. The attack proceeds in stages.

```
# Build communication graph from metadata only
for each email in log:
    add directed edge from sender to recipient
    record timestamp on edge

# Compute structural properties for each node
for each node (email address):
    out_degree = count of emails sent
    in_degree  = count of emails received
    betweenness_centrality = how often this node lies on the
                             shortest path between other nodes

# Identify clusters (probable departments or teams)
run community_detection on undirected version of graph
→ groups of nodes with dense internal edges and sparse external edges

# Infer roles from graph position
if node has high betweenness AND high out_degree:
    → likely leadership (VP or above)
if node receives many messages from within one cluster:
    → likely manages that cluster
otherwise:
    → likely individual contributor

# Bootstrapping from partial knowledge
if a small number of identities are known:
    use them to label their clusters
    extend labels to unlabelled nodes by structural proximity
```

The bootstrapping step is particularly powerful. With knowledge of only three or four employees, an analyst can label entire departments. The structure of the communication graph carries the information; the known identities are anchors for reading it.

## What this reveals

The structural attack was demonstrated against the Enron email dataset, which was made public during legal proceedings and has since been used extensively in research. Analysts were able to reconstruct the organisation's hierarchy and identify key players from email metadata alone, before reading any message content.

The same technique applies to leaked corporate datasets, to intelligence collection on organisations of interest, and to internal investigations. A dataset of anonymised email logs, with addresses replaced by hashes, may still carry a legible organisational structure if the graph is sufficiently dense.

This is also the argument against the claim that collecting metadata rather than content is inherently less invasive. The metadata of a communication network is its structure, and its structure is substantially informative about the people within it.

## Defences

Adding noise to communication patterns, occasionally sending messages to randomly selected contacts with no substantive content, disrupts the statistical reliability of graph analysis. End-to-end encrypted messaging protects content but not metadata: the fact of communication, its frequency, and its timing are still observable to the infrastructure carrying it. Metadata-minimising protocols, which limit what timing and addressing information is available to intermediate systems, address this at the infrastructure level. For most individuals and organisations, the practical implication is an awareness that communication frequency and pattern are themselves sensitive data, not merely a neutral record of who talked about what.
