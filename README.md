# Spine Generic Public Database (Single Subject)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4299148.svg)](https://doi.org/10.5281/zenodo.4299148)
[![BIDS Validator](https://github.com/spine-generic/data-single-subject/workflows/BIDS%20Validator/badge.svg)](https://github.com/spine-generic/data-single-subject/actions?query=workflow%3A%22BIDS+Validator%22)

## About this dataset

This dataset was acquired using the [spine-generic protocol](http://spinalcordmri.org/protocols)
on a 38 y.o. male healthy subject. The list of sites is available in [participants.tsv](./participants.tsv).

This dataset follows the [BIDS](https://bids.neuroimaging.io/) convention.

The contributor has the necessary ethics & permissions to share the data publicly.

The dataset does not include any identifiable personal health information, including names,
zip codes, dates of birth, facial features on structural scans.

The entire dataset is about **1GB**.

## Download

We are using a tool to manage large datasets called `git-annex`. To download, dataset, you need to have `git` installed, and also [install `git-annex`](https://git-annex.branchable.com/install/) *of version 8*. Then run:

~~~
git clone https://github.com/spine-generic/data-single-subject && \
cd data-single-subject && \
git annex init && \
git annex get
~~~

You may **substitute** `git annex get` with more specific commands if you are only interested in certain subjects. For example:

```
git annex get sub-douglas sub-juntendoPrisma/anat/
```

## Working from a forked repository

> ⚠️ For advanced users only. Normally the instructions under [Download](#Download) should be enough.
If you have forked this repository on Github (so that you have a copy `your-user-name/data-single-subject` of `spine-generic/data-single-subject`), you will need to take a few extra synchronization steps to get the latest data with `git annex get`. Otherwise, you may get an error message like:
```
get some-file-name.nii.gz (not available)
  No other repository is known to contain the file.
  (Note that these git remotes have annex-ignore set: origin)
failed
```

1. In your local clone of `your-user-name/data-single-subject`, make sure that `spine-generic/data-single-subject` is also configured as a remote:
   ```
   git remote -v
   # the answer should show both your-user-name/data-single-subject.git (probably named "origin")
   # and spine-generic/data-single-subject (probably named "upstream")
   ```

   If `spine-generic/data-single-subject` is missing, you can add it with:
   ```
   git remote add upstream https://github.com/spine-generic/data-single-subject.git
   git config remote.upstream.annex-readonly true
   ```

2. Then, to update your local clone, make sure to fetch the `git-annex` branch from `spine-generic/data-single-subject` before running `git annex get`:
   ```
   git fetch upstream +refs/heads/git-annex:refs/remotes/upstream/git-annex
   git pull && git annex get .
   ```

## Analysis

The instructions to process this dataset are available in the [spine-generic documentation](https://spine-generic.readthedocs.io/en/latest/analysis-pipeline.html).

## Contributing

If you wish to contribute to this dataset please see [the wiki](https://github.com/spine-generic/spine-generic/wiki/git-annex). Thank you for your contribution 🎉 
