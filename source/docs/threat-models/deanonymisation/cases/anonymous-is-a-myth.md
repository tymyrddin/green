# Anonymous is a myth

The claim that a dataset is "anonymised" because the names were removed has been falsified repeatedly, for nearly three
decades, on exactly the terms that count: given a little outside information, the records name people again.

## The classic demonstrations

The pattern was clear as early as 1997, when Latanya Sweeney re-identified the Massachusetts governor's medical record
in a supposedly anonymous release of state-employee hospital data, by matching it against the public voter roll on three
fields: date of birth, sex and ZIP code. She went on to show that those three fields alone uniquely identify roughly 87%
of the US population.

The demonstrations kept coming as datasets grew. In 2006 AOL published twenty million "anonymised" search queries tagged
by a random user number; reporters identified individual searchers from the content of their own searches within days.
In 2008 Arvind Narayanan and Vitaly Shmatikov re-identified subscribers in the anonymised Netflix Prize dataset by
matching viewing histories against public IMDb ratings. In 2014 a released New York City taxi dataset, its medallion
numbers hashed with a reversible scheme, was turned back into named drivers and traceable trips.

## The general result

These were not lucky one-offs. In 2013 Yves-Alexandre de Montjoye and colleagues showed
that [four spatio-temporal points identify 95% of individuals](https://www.nature.com/articles/srep01376) in a mobility
dataset of 1.5 million people. In 2019 Luc Rocher, Julien Hendrickx and de Montjoye generalised it: using a statistical
model of uniqueness, they estimated
that [99.98% of Americans could be correctly re-identified](https://www.nature.com/articles/s41467-019-10933-3)
in any dataset using just fifteen demographic attributes, including age, sex and marital status.

## Why it counts

Re-identification is the technique the whole model rests on, and it is not exotic. It follows from a plain fact about
people: the combination of a few ordinary attributes is unique. That is the same logic
the [infrastructure-aggregation model](../../infrastructure-aggregation/index.rst) applies to buildings and cables, the
combination is the finding, turned on people. It is why the [mitigations](../mitigations.md) that rely on stripping
identifiers, k-anonymity chief among them, degrade as soon as an adversary brings auxiliary data, and why the commercial
datasets the [surveillance model](../../surveillance/cases/databroker-files.md) describes are dangerous even when they
are sold as anonymous.
