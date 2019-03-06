# Cloud-scale genomic data science with Bioconductor

# Instructor(s) name(s) and contact information

Vincent J. Carey

# Workshop Description

Bioconductor's approach to the analysis of genome-scale assays is
rooted in commitments to the use of self-describing data objects 
representing genomic assays and annotation.  Analysis tools and workflows
based on these objects have proven effective in a large
number of scientific projects and publications.

The dominant model for utilization of Bioconductor to date 
involves a locally controlled deployment of R and 
Bioconductor/CRAN packages in an essentially closed
storage and execution environment.

New approaches to federated
elastic computing with lab-resident or commercial cloud
environments provide opportunities for inference on questions
of vast scope.  This workshop is devoted to understanding how
to leverage Bioconductor's strengths
in seizing these new opportunities.  Special attention is devoted
to how
programming and reporting
patterns familiar from two decades of Bioconductor development
and use can be retained, or must change, in cloud-scale genomic
data science.

Our approach will be a mix of lecture and hands-on programming
with Rstudio Cloud.  We will learn how the restfulSE and BiocOncoTK
packages work with HDF Scalable Data Service and Google BigQuery
to provide immediate interactive access to a compendium of 181000
human transcriptomics experiments, and to the PanCancer Atlas.
We will also learn how to couple Docker containers with formal
workflows in CWL and WDL to achieve sharable reproducible analyses
with nearly zero configuration.  

## Pre-requisites

List any workshop prerequisites, for example:

* Basic knowledge of R syntax
* Familiarity with the SummarizedExperiment class
* Familiarity with one or more of TCGA, GTEx, BigQuery
* Familiarity with docker containers is not required but a running docker installation will be useful

## Workshop Participation

Students should have a laptop and be prepared to execute
specific commands to load packages and
evaluate functions.  It will be helpful to have a Google identity
that may be necessary to work with BigQuery.

## _R_ / _Bioconductor_ packages used

DelayedArray, restfulSE, rhdf5client, BiocOncoTK, 
htxcomp (github/vjcitn), TxRegInfra

## Time outline

An example for a 45-minute workshop:

| Activity                     | Time |
|------------------------------|------|
| Review of Bioconductor software and data structures | 10m  |
| DelayedArray concepts          | 5m  |
| Exercises with htxcomp and the HDF Scalable Data Service | 10m  |
| Exercises with PanCancer Atlas and Google BigQuery | 10m |
| Docker and CWL/WDL with Dockstore.org | 10m |

# Workshop goals and objectives

Goals:

* Develop an appreciation of strengths and limitations
of Bioconductor's approach
to structure and annotation of genome-scale data as scope
of data grows to cloud scale

* Learn about alternatives to "all-in-memory" models of
computing in R, and how Bioconductor has used such alternatives
in the local computing model
(e.g., external SQLite databases, local HDF5 serialization,
API to remote services)

* Obtain experience using Bioconductor
methods and tools with data and annotation that are cloud-scale

* Develop an appreciation of threats to reliability and predictable
costs that arise when working with commercial cloud computing

Objectives:

* Use rhdf5client to interact with matrix data in HDF Scalable Data Service

* Use BiocOncoTK to interrogate multiomic PanCancer atlas data in Google BigQuery

* Understand the role of Docker containers and formal workflow
expression in establishing reproducible and shareable large
scale analyses 
