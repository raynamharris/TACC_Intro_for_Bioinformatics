# Configuring Your Profile

## Learning objectives
- know the resources provided by the BioITeam
- setup a bioiteam profile
- know how to view hidden files
- know what's in a .profile


## Helpful Resources from the BioITeam

The mission of the [BioIteam](https://wikis.utexas.edu/display/bioiteam/Home) is to provide "one-stop" unified support for bioinformatics software tools, educational resources, implementation, and support. The BioITeam was initially focused on tools for next-generation sequencing (NGS) analysis but has expanded its expertise in recent years. The BioITeam is a group of users interested in pooling our efforts with others to reduce the time we spend implementing new software and databases and on training ourselves and others we work with.

The general model is that TACC serve as the reference implementation for stable software releases so most of the "power computing" can be done at TACC, but in addition acknowledge that most of us use resources in addition to TACC, and often need tools, databases, or other resources not globally supported at TACC.

## Copy a preconfigured profile

~~~ {.bash}
$ cd
$ cp /work/01063/abattenh/seq/code/script/tacc/bashrc.corengs .bashrc
$ chmod 600 .bashrc
$ source .bashrc
~~~

~~~ {.output}
stamp:~$
~~~

Did you notice that our prompt changed from `login2.stampede(4)$` to `stamp:~$`? That is just one of the changes we made. If you use `cat .bashrc` you can see the whole script. You will notice that there are some aliases that have been added and use links to useful programs that are not install on TACC but have been kindly provided by a colleage Anna Battenhouse.

## add some programs in a folder called local/bin

~~~ {.bash}
cd
mkdir -p local/bin
cd local/bin
ln -s -f /corral-repl/utexas/BioITeam/bin/launcher_creator.py
ln -s -f /work/01063/abattenh/local/bin/cutadapt
ln -s -f /work/01063/abattenh/local/bin/samstat
ls -l
~~~

~~~ {.output}
lrwxrwxrwx 1 train317 G-815002 39 Jun 29 10:23 cutadapt -> /work/01063/abattenh/local/bin/cutadapt
lrwxrwxrwx 1 train317 G-815002 52 Jun 29 10:23 launcher_creator.py -> /corral-repl/utexas/BioITeam/bin/launcher_creator.py
lrwxrwxrwx 1 train317 G-815002 38 Jun 29 10:23 samstat -> /work/01063/abattenh/local/bin/samstat
~~~


What did we just do?
- With `mkdir -p local/bin` we created a hierarchy of directories (using the `-p` flag) to store some useful bioinforamtic programs.
- The `ln -s` command creates a symbolic link, a shortcut the the linked file or directory. Here the link targets are programs we want to use later, allowing us to use them with out changing to the directory where they are located.
 

## Proceed to the Next and Previous lessons
**Next Lesson:** [05 Motivating Datasets](05_Datasets.md)  
**Previous Lesson:** [03 Using TACC](03_Using_TACC.md)  
