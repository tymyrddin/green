# Mitigations

Privacy-preserving techniques are the cold frames and cloches of the data garden: necessary, somewhat
effective, and frequently overestimated by the people who deploy them. None of these approaches are
a complete solution. All of them involve trade-offs between utility and protection that someone,
eventually, gets wrong.

## k-Anonymity

The idea is straightforward: ensure that every individual in a dataset is indistinguishable from at
least k-1 others who share the same combination of quasi-identifying attributes. If at least five
people in your dataset share the same postcode, age bracket, and occupation, no single record can be
attributed to one person with certainty.

In practice, k-anonymity has well-documented limits. If those five records each contain a different
medical condition, grouping them achieves nothing: anyone who knows one person's postcode and age can
still infer their condition. Extensions like l-diversity (ensuring the sensitive values within each
group are varied) and t-closeness (ensuring that variation mirrors the overall distribution in the
dataset) address some of this, but the underlying problem remains: quasi-identifiers are everywhere,
not always obvious, and combinatorially explosive.

## Differential privacy

A mathematically grounded approach that adds calibrated noise to query results, making it
statistically implausible to determine whether any individual contributed to a given output. A
well-specified differential privacy guarantee means that the result of a query is almost identical
whether or not a particular person's data was included, up to a defined privacy budget (epsilon).

Used by Apple, Google, and the US Census Bureau, which lends it credibility in large-scale deployments.
The trade-off is utility: too little noise and individuals remain exposed; too much and the data
becomes misleading. Choosing an appropriate epsilon is as much a policy decision as a technical one,
and it is rarely made with full transparency.

## Synthetic data

Generating entirely artificial records that mimic the statistical properties of the original dataset,
without containing any real individuals. Widely used in healthcare and finance where sharing raw data
is impractical or legally constrained.

Synthetic data is not automatically safe. Membership inference attacks can sometimes establish whether
a real individual's data was used to train the generative model. If the synthetic data is too
statistically faithful to the original, it may preserve the same identifying patterns at one remove.
And if the model is trained on a small or unusual population, rare combinations of attributes may
appear in the synthetic output even when they were not deliberately included.

## Federated learning

Rather than centralising data for model training, federated learning keeps data on-device and trains
models locally, sharing only gradient updates with a central aggregator. This reduces the attack
surface for bulk exfiltration.

The risks are not eliminated. Gradient updates can leak information about the training data they were
computed from: reconstruction attacks on gradients are an active research area. The aggregation server
remains a point of potential compromise. And participants in a federated system may still be vulnerable
to membership inference from the final model.

## Access controls and data release modes

The least glamorous mitigation and often the most effective. Controlling who gets access to what,
under what conditions, with what audit trail, directly limits the attack surface before any technical
anonymisation is applied. Internal secondary research has a far smaller exposure than public data
release, regardless of what anonymisation technique is applied to both.

Contractual controls, tiered access, query auditing, and data use agreements are unglamorous but
load-bearing. They do not make the news, which is roughly how you want your security mitigations
to behave.

For operational guidance on minimising data exposure, see the [minimise long-term storage](../../playbooks/minimise.md)
playbook.
