# Microbiome data analysis

This repository provides all data and required tools used in chapter 'Computational and statistical methods to analyse microbial amplicon sequencing data'.

#### Data:
We have used MiSeq SOP data used in Kozich JJ, Westcott SL, Baxter NT, Highlander SK, Schloss PD. (2013): Development of a dual-index sequencing strategy and curation pipeline for analyzing amplicon sequence data on the MiSeq Illumina sequencing platform. Applied and Environmental Microbiology. 79(17):5112-20. 
Download the data from http://mothur.org/w/images/d/d6/MiSeqSOPData.zip/

#### Workflows:

The workflows from book chapter have been converted to online documentation. Please use following links:
1. **QIIME1**: https://microdm.github.io/data_analysis/microbiome/qiime1_workflow.html
2. **DADA2**: https://microdm.github.io/data_analysis/microbiome/dada2_workflow.html
3. **Downstream analysis**: https://microdm.github.io/data_analysis/microbiome/downstream_analysis.html

#### Required tools
1. ##### Amplicon data analysis tools
    * [QIIME1](http://qiime.org/install/install.html) (Quantitative Insights Into Microbial Ecology) - This is open-source OTU based approach for microbial data analysis pipeline
    * [Microbiome helper](https://github.com/LangilleLab/microbiome_helper/wiki) - A repository that contains several resources and scripts to automate microbiome analysis workflows.
    * [DADA2](https://benjjneb.github.io/dada2/index.html) - R package for fast and accurate sample inference from amplicon data with single nucleotide resolution. (ASV based)
2. ##### Quality analysis, filtering, trimming & preprocessing
    * [FASTQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/) - A quality control tool for high throughput sequence data.
    * [FASTX-Toolkit](http://hannonlab.cshl.edu/fastx_toolkit/) - FASTX-Toolkit is a collection of command line tools for Short-Reads FASTA/FASTQ files preprocessing.
    * [PEAR](https://github.com/tseemann/PEAR) - Paired-End reAd mergeR
3. ##### Other tools
    * [VSEARCH](https://github.com/torognes/vsearch) - an alternative to the USEARCH tool developed by Robert C. Edgar (2010)
4. ##### R packages
    * [phyloseq](https://joey711.github.io/phyloseq/) - The phyloseq package is a tool to import, store, analyze, and graphically display complex phylogenetic sequencing data
    * [ALDEX2](https://bioconductor.org/packages/release/bioc/html/ALDEx2.html) - Analysis Of Differential Abundance Taking Sample Variation Into Account

In this book chapter, we have covered two main approaches for microviome data analysis viz. OTU and ASV based using QIIME1 and DADA2. The following figure shows some steps required in respective approach. 
OTU based approach works by clustering sequences using percent identity threshold which can ce reference based or denovo. For example, clustering sequences at 97% identity threshold allows 3% of dissimalarity 
within sequences from each cluster. These clusters are known as Operational Taxonomic Units (OTUs) with an assumption that these sequences from same OTUs belongs to same taxa (like same genera). On the other hand,
ASV based approach using DADA2 or Deblur assume that single nucleotide difference within sequences can give more insights to microbial diversity. Hence, these tool tries to correct the sequencing errors prior
to partition unique sequences into different ASVs.
![alt text](https://github.com/nikeetaC/amplicon_data_analysis/blob/master/img/Fig2.jpeg "Microbiome data analysis approaches")
