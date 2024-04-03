# Repo for metagenomic read recruitment lesson for BSCG course 

Read recruitment or mapping is one of the most commonly used process in genome analysis. It can be used for various purposes but in single cell genomics , it is often applied to access the relative abundance of SAGs in metagenomic datasets (when metagenomes are used) or to estimate the expression level of the genes within individual SAGs (when metatranscriptomes are used).

In a nutshell short reads are aligned to a genomic reference sequence (many thanks to Meren for creating this animation)
![recruitment](https://github.com/Bigelow-SCG-Course/Day3AM_read_recruitment/blob/main/intro_images/01-metagenomic-read-recruitment-simple.gif)



## CoverM
For this tutorial we will use [CoverM](https://github.com/wwood/CoverM), a pipeline that "aims to be a configurable, easy to use and fast DNA read coverage and relative abundance calculator focused on metagenomics applications". CoverM can calculate coverage of individual contigs or of genomes with `coverm genome` (the mode we will be using; detailed manual [here](https://wwood.github.io/CoverM/coverm-genome.html)). Calculating coverage by read mapping, its input can either be [BAM (Binary Alignemnt Mapping)](https://support.illumina.com/help/BS_App_RNASeq_Alignment_OLH_1000000006112/Content/Source/Informatics/BAM-Format.htm#) files sorted by reference, or raw reads and reference genomes in various formats.

CoverM offers the possibility to use two different aligners, [bwa-mem](https://github.com/lh3/bwa) or [minimap2](https://github.com/lh3/minimap2). The two aligners have comparible accurancies (with bwa-mem performing a bit better) but minimap2 runs 3-4 times as fast ([Li, 2018](https://academic.oup.com/bioinformatics/article/34/18/3094/4994778)). We will be using minimap2, which is the default aligner in CoverM.


## Let's get started
- First let's clone this repository into your own working directory. To do so, open up a terminal window and type the following commands:
```
$ cd ~/storage/userlab/{your_username_here}/
$ git clone (ADD gitrepo linit)
$ cd (ADD the name of the folder)
```
- [1_Metagenome_Recruitment_Setup.ipynb](add repo link): We will next go over how we downloaded the reads we will use for the course. Julia's work (see supplementary material of Pachiadaki et al. 2017) showed that -  regarding the estimation of relative abundance of genomes - mapping million reads provides comparible results with mapping larger metagenomes. For this reason, we are going to subsamples the genomes as we download them.
- [2_CoverM.ipynb](include repo link): We will then run CoverM.
- [3_Metagenome_recruitment_plotting.ipynb](add repo link): Finally, we will explore and visualize the results.

