# My First Batch Job

## Learning Objectives
- know how to use sbatch to submit a job
- know how to run jobs where all the scripts, data, and results are in the same directory
- know how to run jobs where the scripts, data, and results are all in separate directory
- know that storing scripts, data, and results in separate directories is better for data management and reproducible data science
- understand how you can use variables to name output files 

## wc_reads_better

Basically, really early on I want to introduce students to some data managment tools. 

Here, I've add some organization with sub-directories. 

- The scripts are stored in bin/
- The data are stored in data/
- The results/ will be populated automatically using the lines of code at the .slurm file. I've used variables to name results sub-directories with the job name and job number so that all results are stored with unique identifies for good record keeping. You can see an example output from one time I ran this. 

~~~ {.bash}
$ cd ../wc_reads_better
$ cd bin
$ sbatch wc_reads.slurm
$ ls ../results
~~~

## Getting a new Scripts 


1. Move into your $WORK/myfirstsbatch/wc_reads_better/bin
2. Copy Rayna's "fastqc.slurm" file to your bin

~~~ {.bash}
$ cd $WORK/myfirstsbatch/wc_reads_better/bin
$ cp /work/02189/rmharris/myfirstbatchscript/bin/fastqc.slurm .
$ ls
~~~

~~~ {.output}
fastqc.slurm
~~~

***Note:** These same files and scripts can also be [here found on Github](https://github.com/raynamharris/DataForTACCCourse)


## Run the batch script

~~~ {.bash}
$ sbatch fastqc.slurm
~~~


## Feedback Welcome

I'm always looking for better ways of doing things, especially when it comes to data management, so feel free to make suggestions for imporvement.