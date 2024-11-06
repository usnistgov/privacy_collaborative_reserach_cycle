# The NIST Collaborative Research Cycle (CRC) Data and Metrics Archive (A.K.A. Research Acceleration Bundle) v1.2

- [Direct download link for deidentified data and reports (698 MB)](https://github.com/usnistgov/privacy_collaborative_research_cycle/releases/download/v1.2/crc_data_and_metric_bundle_1.2.zip)
- [Direct download link for the metareports (669 MB)](https://github.com/usnistgov/privacy_collaborative_research_cycle/releases/download/v1.2/crc_metareport_bundle_1.2.zip)

## Introduction

Welcome!

This repository contains deidentified data submitted to the CRC and their evaluation results as generated by SDNist v2.3.0. The [CRC homepage](https://pages.nist.gov/privacy_collaborative_research_cycle/) provides more detailed information about the program, its goals, and how to participate.

In short, the CRC seeks to equip the research community with resources to explore, evaluate, and discuss deidentification approaches. The original data for this project are the [NIST Diverse Communities Excerpts](https://github.com/usnistgov/SDNist/tree/main/nist%20diverse%20communities%20data%20excerpts), curated data drawn from the American Community Survey.

There are three ground truth partitions, corresponding to three geographic regions (Boston-area (ma), Dallas-Fort Worth Area (tx), and a national sample (national). Submissions may include any or all of these partitions.

The original data contains 24 features. We also have a list of recommended reduced-size feature sets which can be found in the Excerpts Readme. Deidentified data may include any combination of feature set, though we have encouraged participants to use one of the recommended combinations to facilitate comparison of techniques.

## What do we have here? 

This repository contains all submissions made in 2023. Additional submissions will be added with the next drop (expected in summer 2024). The repository contains the navigable structure for the entire bundle. You can find all of the compressed data in [Releases](https://github.com/usnistgov/privacy_collaborative_research_cycle/releases/tag/v1.2) or you can use the links at the top of this readme.

The `crc-data-and-metrics-bundle` file contains: 

* All of the deidentified data submissions and their evaluation metric results in the current release of our archive,
* An index.csv file that tracks all submission metadata, algorithm properties and definitions,
* A comprehensive set of tutorial jupyter notebooks and utilities that teach users how to programmatically explore the archive using the index file, and
* The ground truth target data ('diverse community excerpts') and data dictionaries as json files.  

The data and metrics bundle enables users to explore the archive programmatically; it supports researchers who'd like to write their own scripts to analyze the data or metric results.

The `crc-metareports-bundle` enables users to explore the archive visually. It contains evaluation metareports that compare results from each deidentification library in the archive, along with additional documentation and guidance on interpretation of results.  The metareports are available in both html and pdf format, and the package also includes detailed evaluation reports on each individual deidentified data sample.  

To learn more about the techniques used to deidentify the data, see the [CRC Techniques page.](https://pages.nist.gov/privacy_collaborative_research_cycle/pages/techniques.html).

## How are the deidentified data samples organized? 

The deidentified data have the following hierarchy: 
```
crc_data_and_metric_bundle_1.2
	index.csv	             			        # directory of metadata
	deid_data
		library_technique_team-name   			# team name is only appended if multiple teams submit on the same technique)
			partition             			# e.g., 'ma', 'tx', 'national'
				technique_variant_data_1	# technique variants are stored together (e.g., DP algorithm with different values of epsilon)
				technique_variant_data_2
				technique_variant_report_1
					report_resources_1
				tehcnique-variant_report 2
					report_resources_2
	notebooks					        # tutorial ipython notebooks to demonstrate navigating the archive.
	diverse_communities_data_excerpts                       # ground truth target data
```
Each deidentified data sample is labeled with its variant information and comes with three files.  The .csv file contains the data itself.  The .json file contains all metadata about the generation of the data.  And the report folder (starting with *'r_'* words) contains metric results from the sdnist evaluation of the data.  

Within the report folder (starting with *'r_'*) you will find subfolders containing .csv results for each metric, and a report.json file with complete metric results for the full report. The report.html file displays the metric results as a user friendly visual report, including metric documentation, definitions and citations.

## How can I use these data? 

These data are available for any investigation a user sees fit. NIST hosts the CRC Explanatory Workshop in December, which will be an ideal venue to present findings. More information can be found on [the project website](https://pages.nist.gov/privacy_collaborative_research_cycle/).  See the license statement contained in the repo for terms and conditions.
## Please cite these resources.

If you use these resources, we ask that you cite the elements of this work. Here are the suggested citations. 

***CRC General Citation****
```
Sen, A., Task, C., Kapur, D., Howarth, G. & Bhagat, K. Diverse Community Data for Benchmarking Data Privacy Algorithms. in Advances in Neural Information Processing Systems vol. 36 51409–51420.

bibtex:
@inproceedings{sen_diverse_2023, title = {Diverse {Community} {Data} for {Benchmarking} {Data} {Privacy} {Algorithms}}, volume = {36}, url = {https://proceedings.neurips.cc/paper_files/paper/2023/file/a15032f8199511ced4d7a8e2bbb487a5-Paper-Datasets_and_Benchmarks.pdf}, booktitle = {Advances in {Neural} {Information} {Processing} {Systems}}, publisher = {Curran Associates, Inc.}, author = {Sen, Aniruddha and Task, Christine and Kapur, Dhruv and Howarth, Gary and Bhagat, Karan}, year = {2023}, pages = {51409--51420}

```


***CRC Research Acceleration Bundle***
```
Task C., Bhagat K., Howarth G.S. (2024), NIST Collaborative Research Cycle Acceleration Bundle, National Institute of Standards and Technology, https://doi.org/10.18434/mds2-3024

bibtex:
@misc{task_nist_2024, title = {{NIST} {Collaborative} {Research} {Cycle} {Data} and {Metrics} {Archive}}, url = {https://data.nist.gov/od/id/mds2-3024}, doi = {10.18434/MDS2-3024}, author = {Task, Christine and Bhagat, Karan and Howarth, Gary}, month = feb, year = {2024}}

```

***NIST Diverse Communities Data Excerpts***
```
Task C., Bhagat K., Streat D., Simpson A., and Howarth G.S. (2023), NIST Diverse Communities Data Excerpts, National Institute of Standards and Technology, https://doi.org/10.18434/mds2-2895

bibtex:
@misc{task_nist_2022, author = {Task, Christine and Bhagat, Karan and Damon, Streat and Howarth, Gary}, doi = {10.18434/MDS2-2895}, month = dec, publisher = {National Institute of Standards and Technology}, title = {{NIST} {Diverse} {Community} {Excerpts} {Data}}, url = {https://data.nist.gov/od/id/mds2-2895}, year = {2023}} 
```

***SDNist***
```
Task C., Bhagat K., and Howarth G.S. (2023), SDNist v2: Deidentified Data Report Tool, National Institute of Standards and Technology, https://doi.org/10.18434/mds2-2943

bibtex: 
 @misc{task_sdnist_2023, author = {Task, Christine and Bhagat, Karan and Howarth, Gary}, doi = {10.18434/MDS2-2943}, month = mar, publisher = {National Institute of Standards and Technology}, shorttitle = {{SDNist} v2}, title = {{SDNist} v2: {Deidentified} {Data} {Report} {Tool}}, url = {https://data.nist.gov/od/id/mds2-2943}, year = {2023}}
```
