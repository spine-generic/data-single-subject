# Spine Generic Public Database (Single Subject)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4299148.svg)](https://doi.org/10.5281/zenodo.4299148)

## About this dataset

This dataset was acquired using the [spine-generic protocol](http://spinalcordmri.org/protocols)
on a 38 y.o. male healthy subject. The list of sites is available in [participants.tsv](./participants.tsv).

This dataset follows the [BIDS](https://bids.neuroimaging.io/) convention.

The contributor has the necessary ethics & permissions to share the data publicly.

The dataset does not include any identifiable personal health information, including names,
zip codes, dates of birth, facial features on structural scans.

The entire dataset is about **1GB**.

## Download

We are using a tool to manage large datasets alled `git-annex`. To download, dataset, you need to have `git` installed, and also [install `git-annex`](https://git-annex.branchable.com/install/) *of version 8*. Then run:

~~~
git clone https://github.com/spine-generic/data-single-subject && \
cd data-single-subject && \
git annex init && \
git annex get
~~~

You may **substitute** `git annex get` with more specific commands if you are only interested in certain subjects. For example:

```
get annex get sub-douglas sub-juntendoPrisma/anat/
```


## Analysis

The instructions to process this dataset are available in the [spine-generic documentation](https://spine-generic.readthedocs.io/en/latest/analysis-pipeline.html).

## Contributing

If you wish to contribute to this dataset please see [the wiki](https://github.com/spine-generic/spine-generic/wiki/git-annex). Thank you for your contribution 🎉 
