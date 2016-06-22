# Configuring Your Profile

## Learning objectives
- setup a bioiteam profile
- know how to view hidden files
- know what's in a .profile


## Copy a preconfigured profile

~~~ {.bash}
$ cdh
$ cp /corral-repl/utexas/BioITeam/scripts/rnaseq_profile_user ~/.profile
$ chmod 600 .profile
$ source .profile
~~~

~~~ {.output}
#FIXME
ADD output example
~~~

What did we just do? Let's look at the .profile file

## .profile

In order to view invisible files in a directory, we must use the `-a` flag to view all files. 

~~~ {.bash}
$ ls -a
~~~

Now, let's take a look at our .profile file

~~~ {.bash}
$ nano .profile
~~~ 

~~~ {.output}
#!/bin/bash

# include common settings for the NGS course
. /corral-repl/utexas/BioITeam/bin/profile_ngs_course.bash

PATH=$PATH:/work/01184/daras/bin
PATH=$PATH:/work/01184/daras/bin/cutadapt-1.3/bin
~~~

What this does is provide links to some useful files scripts

Let's look at profile_ngs_course.bash

~~~ {.output}
cd /corral-repl/utexas/BioITeam/bin/
nano profile_ngs_course.bash
~~~

Here, we are going to a storage system on Corral. Then, we use the nano program to open a new file. 



