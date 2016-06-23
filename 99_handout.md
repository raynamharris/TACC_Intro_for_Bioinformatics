## Commands Handout

General HPC Commands | Explanation
:---|:---
`ssh <username>@<remotehost>`

TACC-Specific Commands | Explanation
:---|:---
`ssh <username>@stampede.tacc.utexas.edu` | **s**ecure **sh**ell to Stampede
`ssh <username>@ls5.tacc.utexas.edu` | **s**ecure **sh**ell to Lonestar5
`cdh` | **c**hange **d**irectory to **h**ome directory
`cdw` | **c**hange **d**irectory to **w**ork directory
`cds` | **c**hange **d**irectory to **s**scratch directory
`sbatch <filename.slurm>` | submit a job script for execution
`scancel <jobid>` | cancel a pending or running job
`squeue` | reports the state of all jobs 
`squeue -u <userid>` | reports state of all user jobs
