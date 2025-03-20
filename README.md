# Ribosome profiling on mouse organoid

This repository contains the code and associated files for a ribosome profiling study analysis on mouse organoid ([https://pmc.ncbi.nlm.nih.gov/articles/PMC10795831/](#)).

## Repository Organization

The repository is structured into folders with self-descriptive names to facilitate navigation and understanding of the project workflow:

- `code`: Contains the code used for data processing, analysis, and figure generation.
- `data_frames`: Holds various data files created or used during the analysis.
- `seqdata`: Raw and processed sequencing data organized by analysis type (e.g.,Riboseq). Due to large files, the seqdata folder is omitted in this repo. Please download the original file from pubmed and follow the name order of the files as provided in the codes for seqdata_processing.
- `alignment`: Omitted from this repo, but please create your own folder according to the folder names provided during the seqdata_processing and alignment. 
- `figures`: Includes figures generated from the analysis.

## Hardware and Software Information

**Hardware:**
- **CPUs**: 2 Intel Xeon CPU E5-2660 v4 @ 2.00GHz, each with 14 cores and 2 threads per core, totaling 56 threads.
- **RAM**: 264 GB
- **Operating System**: Ubuntu 18.04.6 LTS

**Software Versions:**
| Software      | Version   |
|---------------|-----------|
| cutadapt      | 3.5       |
| python        | 3.6.9     |
| hisat2        | 2.2.1     |
| kallisto      | 0.48.0    |
| samtools      | 1.16.1    |
| UMI-tools     | 1.1.2     |
| fastp         | 0.23.2    |
| R             | 4.2.3     |

### Additional Information:

When knitted to an HTML, each R Markdown (**`Rmd`**) document will display the versions of the packages used at the bottom, ensuring reproducibility. Many steps in the analysis can utilize multiple threads to speed up processing, although this is optional. If needed, you can adjust the thread usage; the only impact will be increased runtime.

**Phases of the Analysis:**
1. Sequencing Data Processing: Processes the raw sequencing data to prepare it for alignment and quantification.

2. Analysis: Executes various analyses based on the processed sequencing data.

3. Interpretation: Creates visualizations of the data generated during the analysis phase.

### Notes on Directory Structure and Files:
- `codes`: This folder contains scripts specifically related to the processing of the raw data (adaptor removal, quality control, trimming, UMI_extraction, rtRNA removal, different types of alignment- genome, transcriptome, CDS, or UTR specific, and finally analysis and generation of figures.
- `dataframe`: Contains data files that are used for the respective figures, matching the data used in the analysis scripts.
- `figures`: Stores all the generated figures.

  
