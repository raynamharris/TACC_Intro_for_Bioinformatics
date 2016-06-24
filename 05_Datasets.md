## Motivating Dataset

## Learning objectives
- know how to copy files from someone else's file system
- know what data is available for use in this part of the module
- be familiar with different ways to organize project directories

## *Cancer borealis* references transcriptomes and data
Dave Schulz and the greater STG community have worked diligently to create *Cancer borealis* transciptomes that can be used as reference transcriptomes for RNA-seq projects or for asking biologically meaningful questions about differences across tissue types. Additionally, the Schultz, Marder, and Hofmann labs worked together to sequences some single STG neurons that we will be using in thins module.  

### Coping the files
The first thing you are going to do is copy them from Rayna's $WORK directory to your own. Let's go ahead and 
1. move to our $WORK directory
2. copy the project folder
3. move into the project folder
4. list the contents

~~~ {.bash}
$ cdw
$ cp -r /work/02189/rmharris/IntMolModule/ .
$ cd IntMolModule
$ ls
~~~
~~~ {.output}
data references
~~~

### The reference transcriptomes
We have two references transcriptomes. 
1. The Cborealis_ref.fa file is a full transcriptome. 
2. The SchulzD_Cb_CDS_CHR.fasta is a partial transcrpitome, made up of 88 candidate genes

~~~ {.bash}
$ ls -lht references
~~~ 

~~~ {.output}
-rwxrwxrwx 1 rmharris G-813760 168K Jun 21 17:34 SchulzD_Cb_CDS_CHR.fasta
-rwxrwxrwx 1 rmharris G-813760  65M Jun 21 17:34 Cborealis_ref.fa
~~~ 

### The datasets
The data directory is broken down in subdirectories for the STG and the mouse module. Within the STG subdirectory, have a directory that is named according to the date it was downloaded (2016-05-24) and the job submission number (JA16268). This two numbers help keep track of information about when these samples were sequenced. Let's look at the files.

~~~ {.bash}
$ ls -lht data/STG/2016-05-24-JA16268/
~~~ 

~~~ 
-r--rw-r-- 1 rmharris G-813760 984M Jun 24 00:02 PD_11_S_S28_L003_R2_001.fastq.gz
-r--rw-r-- 1 rmharris G-813760 865M Jun 24 00:01 PD_11_S_S28_L003_R1_001.fastq.gz
-r--rw-r-- 1 rmharris G-813760 721M Jun 24 00:01 PD_10_S_S27_L003_R2_001.fastq.gz
-r--rw-r-- 1 rmharris G-813760 636M Jun 24 00:01 PD_10_S_S27_L003_R1_001.fastq.gz
-r--rw-r-- 1 rmharris G-813760 795M Jun 24 00:01 GM_26_S_S32_L003_R2_001.fastq.gz
-r--rw-r-- 1 rmharris G-813760 696M Jun 24 00:01 GM_26_S_S32_L003_R1_001.fastq.gz
-r--rw-r-- 1 rmharris G-813760 680M Jun 24 00:00 GM_25_S_S31_L003_R2_001.fastq.gz
-r--rw-r-- 1 rmharris G-813760 606M Jun 24 00:00 GM_25_S_S31_L003_R1_001.fastq.gz

Let's break down the file name by looking at the first two sequences: 

PD_11_S_S28_L003_R2_001.fastq.gz
PD_11_S_S28_L003_R1_001.fastq.gz

PD_11_: Cell type and cell ID
S_S28: RNA from a *s*ingle neuron, now called RNA sample 28
LOO3: Sequencing lane 3
R1 or R2: Read 1 and Read 2
001: an arbitrary addition?
.fastq.gz : the file extension for a compressed sequence file


















~~~ 