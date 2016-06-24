# Modules

## Learning Objectives
- know how to find and load modules

Modules are programs or sets of programs that have been set up to run on TACC. They make managing your computational environment very easy. All you have to do is load the modules that you need and a lot of the advanced wizardry needed to set up the linux environment has already been done for you. New commands just appear.

## module avail

To see the commands that can be used with the module program itself type:

~~~ {.bash}
tacc:~$ module avail
~~~

## module spider

After running `module avil`, you can see that the sub-module "spider" can be used to list modules matching a string input. Here we will use the example `module spider fastqc` to look to see if the program fastqc is installed.

~~~ {.bash}
tacc:~$ module spider fastqc
~~~

~~~ {.output}
----------------------------------------------------------------------------
  fastqc:
----------------------------------------------------------------------------
    Description:
      fastqc - A Quality Control application for FastQ files

     Versions:
        fastqc/0.10.1
        fastqc/0.11.5

----------------------------------------------------------------------------
  For detailed information about a specific "fastqc" module (including how to load the modules) use the module's full name.
  For example:

     $ module spider fastqc/0.11.5
----------------------------------------------------------------------------
~~~

### Challenge: What is the latest version of the transcriptome assembler *Trinity* is installed?
 
## module load

To load the latest version of a module, type `module load <module name>`. Here, let's load fastqc.

~~~ {.bash}
tacc:~$ module load fastqc
~~~
~~~ {.bash}
tacc:~$ 
~~~

If it load correctly, you are met with an empty prompt and now you're ready to starting using the program.

## Proceed to the Next and Previous lessons
**Next Lesson:** [07 Launch Jobs](07_Launch_Jobs.md)  
**Previous Lesson:** [05 Motivating Datasets](05_Datasets.md)  