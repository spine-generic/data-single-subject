# Spine Generic Public Database (Single Subject)

## About this dataset

This dataset was acquired using the [spine-generic protocol](http://spinalcordmri.org/protocols)
on a 38 y.o. male healthy subject. The list of sites is available in [participants.tsv](./participants.tsv).

This dataset follows the [BIDS](https://bids.neuroimaging.io/) convention.

The contributor has the necessary ethics & permissions to share the data publicly.

The dataset does not include any identifiable personal health information, including names,
zip codes, dates of birth, facial features on structural scans.

## Download

To download the latest version of this dataset, you have two options:

### Download zip package (recommended)

If you are only planning on using the dataset for processing, you can download the latest version as a zip package:

~~~
curl -o spinegeneric.zip -L https://github.com/spine-generic/data-single-subject/archive/master.zip
unzip spinegeneric.zip
~~~

### Clone the repository (slower)

If you are planning on contributing to this repository (e.g. uploading manual segmentations/labels), you need to clone this repository:
~~~
git clone https://github.com/spine-generic/data-single-subject.git
~~~

## Analysis

The instructions to process this dataset are available in the [spine-generic documentation](https://spine-generic.readthedocs.io/en/latest/analysis_pipeline.html).

## Contributing

If you wish to contribute to this dataset by adding new images and/or manual ground truths (e.g., spinal cord segmentations, disc labels, etc.), please fork this repository and submit a pull request. Thank you for your contribution 🎉 
