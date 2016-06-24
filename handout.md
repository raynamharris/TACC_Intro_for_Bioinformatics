## Commands Handout

TACC-Specific Commands | Explanation
:---|:---
`ssh <username>@stampede.tacc.utexas.edu` | **s**ecure **sh**ell to Stampede
`ssh <username>@ls5.tacc.utexas.edu` | **s**ecure **sh**ell to Lonestar5
`cdh`, `cd $HOME`, `cd`, and `cd ~` | **c**hange **d**irectory to **h**ome directory
`cdw` and `cd $WORK`| **c**hange **d**irectory to **w**ork directory
`cds` and `cd $SCRATCH` | **c**hange **d**irectory to **s**scratch directory
`module avil` | lists available modules
`module spider` | lists all modules
`module help` | lists options for the module program
`module help <module name>` | lists options for a specified module
`module spider <module name>` | lists all versions of a particular module
`module load <module name>` | loads the most recent versions of a module
`module unload <module name>` | unloads a module
`module swap <module1> <module2>` | swaps module2 for module1
`sbatch <filename.slurm>` | submit a job script for execution
`scancel <jobid>` | cancel a pending or running job
`squeue` | reports the state of all jobs 
`squeue -u <userid>` | reports state of all user jobs