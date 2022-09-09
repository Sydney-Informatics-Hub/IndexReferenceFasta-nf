[IndexReferenceFasta-nf]
===========

  - [Description](#description)
  - [Diagram](#diagram)
  - [User guide](#user-guide)
  - [Benchmarking](#benchmarking)
  - [Workflow summaries](#workflow-summaries)
      - [Metadata](#metadata)
      - [Component tools](#component-tools)
      - [Required (minimum)
        inputs/parameters](#required-minimum-inputsparameters)
  - [Additional notes](#additional-notes)
  - [Help/FAQ/Troubleshooting](#helpfaqtroubleshooting)
  - [3rd party Tutorials](#3rd-party-tutorials)
  - [Licence(s)](#licences)
  - [Acknowledgements/citations/credits](#acknowledgementscitationscredits)

---

# Description

```
This is a flexible pipeline for generating common reference genome index files for WGS data analysis. IndexReferenceFasta-nf is a Nextflow (DSL2) pipeline that runs the following tools using Singularity containers:
* Samtools faidx
* BWA index
* GATK CreateSequenceDictionary 

# Diagram

<p align="center"> 
<img src="https://user-images.githubusercontent.com/73086054/189310509-375fea4f-11fb-41ca-ba52-90760e9a5aa3.png" width="80%">
</p> 

# User guide
## Quick start guide

1. Set up 

Clone this repository by running:
```
git clone https://github.com/Sydney-Informatics-Hub/IndexReferenceFasta-nf.git
cd IndexReferenceFasta-nf
``` 

2. Generate indexes
Users can specify which index files to create by using the `--samtools`, `--bwa`, and/or `--gatk` flags. All are optional. Run the pipeline with:

```
nextflow run main.nf /path/to/ref.fasta --bwa --samtools --gatk 
```

# Benchmarking

Coming soon! 

# Workflow summaries

## Metadata
|metadata field     | workflow_name / workflow_version  |
|-------------------|:---------------------------------:|
|Version            | workflow_version                  |
|Maturity           | under development                 |
|Creators           | Georgie Samaha                    |
|Source             | NA                                |
|License            | GPL-3.0 license                   |
|Workflow manager   | NextFlow                          |
|Container          | None                              |
|Install method     | Manual                            |
|GitHub             | Sydney-Informatics-Hub/IndexReferenceFasta-nf                                |
|bio.tools          | NA                                |
|BioContainers      | NA                                | 
|bioconda           | NA                                |

---

## Component tools

* samtools/1.15.1
* gatk/4.2.6.1 
* bwa/0.7.17

## Required (minimum) inputs/parameters

* A reference genome file in fasta format.

# Additional notes

# Help / FAQ / Troubleshooting

# Acknowledgements/citations/credits
## Authors 
- Georgie Samaha (Sydney Informatics Hub, University of Sydney)   

## Acknowledgements 

- This pipeline was built using the [Nextflow DSL2 template](https://github.com/Sydney-Informatics-Hub/Nextflow_DSL2_template).  
- Documentation was created following the [Australian BioCommons documentation guidelines](https://github.com/AustralianBioCommons/doc_guidelines).  

## Cite us to support us! 
Acknowledgements (and co-authorship, where appropriate) are an important way for us to demonstrate the value we bring to your research. Your research outcomes are vital for ongoing funding of the Sydney Informatics Hub and national compute facilities. We suggest including the following acknowledgement in any publications that follow from this work:  

The authors acknowledge the technical assistance provided by the Sydney Informatics Hub, a Core Research Facility of the University of Sydney and the Australian BioCommons which is enabled by NCRIS via Bioplatforms Australia. 
