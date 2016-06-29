# My First Batch Job

## Learning Objectives
- know how to use sbatch to submit a job
- know how to run jobs where all the scripts, data, and results are in the same directory
- know how to run jobs where the scripts, data, and results are all in separate directory
- know that storing scripts, data, and results in separate directories is better for data management and reproducible data science
- understand how you can use variables to name output files 


## Getting the Scripts and Data

1. Copy Rayna's "myfirstbatchscript" directory to your $SCRATCH directory
2. Move into your "myfirstbatchscript" directory

~~~ {.bash}
$ cds
$ cp -r /work/02189/rmharris/myfirstbatchscript/ .
$ cd myfirstbatchscript
$ ls
~~~

~~~ {.output}
launcher	wc_reads	wc_reads_better
~~~

***Note:** These same files and scripts can also be [here found on Github](https://github.com/raynamharris/DataForTACCCourse)


## Getting the Scripts and Data - Alternative, if above doesn't work

If that doesn't work because of some permissions, try the following. The steps are listed first, command line commands come later.
1. Log off stampede with the command `exit`
2. Download, unzip, and save to your desktop this "DataForTACCCourse-master" directory from this website: https://github.com/raynamharris/DataForTACCCourse.git
3. Use `scp -r` to copy this directory to your work
4. Log back into tacc
5. cd into this new directory

~~~ {.bash}
$ exit
$ cd Desktop/DataForTACCCourse-master
$ scp -r DataForTACCCourse-master <username>@stampede.tacc.utexas.edu:<pathto$WORK> 
$ ssh <username>@stampede.tacc.utexas.edu
$ cd <pathto$WORK>/DataForTACCCourse-master
~~~

## launcher
This is pretty much verbatum the example launcher script given by tacc. I've changed it to add the allocation that will be used for the course. Otherwise, its stright out of the box.

### Submit a job to count reads in every file

~~~ {.bash}
$ cd launcher
$ sbatch launcher.slurm
~~~

## wc_reads

This subdirectory contains some tiny .fastq files and three scripts. 

- wc_reads.cmds is the list of commands to be executed on TACC that will count the number of reads in each file.
- wc_reads.slurm is the batch script that will execute the commands on stampede
- .wc_reads.sh is a shell script that I hid from easy access because I think the for loop I used is a little above the scope and I don't want to intruce it write off the bat, but will save that till later in the course.

### Submit a job to count reads in every file

~~~ {.bash}
$ cd ../wc_reads
$ sbatch wc_reads.slurm
~~~

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


## Feedback Welcome

I'm always looking for better ways of doing things, especially when it comes to data management, so feel free to make suggestions for imporvement.