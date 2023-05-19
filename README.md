# The NIST Collaborative Research Cycle (CRC) Research Acceleration Bundle v1

- [Direct download link for deidentified data and reports (480 MB)](https://github.com/usnistgov/privacy_collaborative_research_cycle/releases/download/v1.0/crc_data_and_metric_bundle_1.0.zip)
- [Direct download link for the metareports (454 MB)](https://github.com/usnistgov/privacy_collaborative_research_cycle/releases/download/v1.0/crc_metareport_bundle_1.0.zip)

## Introduction

## What do we have here? 

This repository contains the results of the first round of submissions. Additional submissions will be added with the next drop expected in July 2023. In the Releases section of this repository, you can access the data. The resources are partitioned into two zip files.  

The crc-data-and-metrics-bundle.zip file contains all of the deidentified data samples and evaluation metric results in the first release of our archive.  It also includes meta-data json files that describe the technique used to produce each sample.  And finally, it contains the ground truth target data (‘diverse community excerpts’) which the deidentification approaches were deidentifying. This bundle enables users to explore the archive programmatically; it supports researchers who’d like to write their own scripts to analyze the data or metric results.   

The crc-metareports-bundle.zip enables users to explore the archive visually.   It contains evaluation meta-reports that compare results from each deidentification library in the archive, along with additional documentation and guidance on interpretation of results.  The meta-reports are available in both html and pdf format, and the package also includes detailed evaluation reports on each individual deidentified data sample.  

To learn more about the techniques used to deidentify the data, see the [CRC Techniques page.](https://pages.nist.gov/privacy_collaborative_research_cycle/pages/techniques.html).

## How are the deidentified data samples organized? 

The deidentified data have the following hierarchy: 
```
	root
		library- technique - team_name
			technique variant data 1
			technique variant data 2
			technique variant report 1
			tehcnique variant report 2
```
Each deidentified data sample is labeled with its variant information and comes with three files.  The .csv file contains the data itself.  The .json file contains all meta-data about the generation of the data.  And the report folder contains metric results from the sdnist evaluation of the data.  

Within the report folder you will find subfolders containing .csv results for each metric, and a .json file with complete metric results for the full report.  The .html file displays the metric results as a user friendly visual report, including metric documentation, definitions and citations. 


## How can I use these data? 

See the license statement in this repo about usage, conditions, etc.


## Please cite these resources.

If you use these resources, we ask that you cite the elements of this work. Here are the suggested citations. 

***CRC Research Acceleration Bundle***
```
Task C., Bhagat K., Howarth G.S. (2023), NIST Collaborative Research Cycle Acceleration Bundle, National Institute of Standards and Technology, https://doi.org/10.18434/mds2-3024
(NOTE: DOI is not yet active, but should be live by June 2023)
```


***NIST Diverse Communities Data Excerpts***
```
Task C., Bhagat K., Streat D., Simpson A., and Howarth G.S. (2023), NIST Diverse Communities Data Excerpts, National Institute of Standards and Technology, https://doi.org/10.18434/mds2-2895
(NOTE: DOI is not yet active, but should be live by June 2023)
```

***SDNist***
```
Task C., Bhagat K., and Howarth G.S. (2023), SDNist v2: Deidentified Data Report Tool, National Institute of Standards and Technology, https://doi.org/10.18434/mds2-2943
```
