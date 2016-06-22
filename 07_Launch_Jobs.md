# Launching Jobs

## Learning Objectives
- understand the difference between login and compute nodes
- know that you need a job submission script and a commands file to submit jobs
- understand the two ways to prepare the submission script - launcher.slurm and launcher creator.py
- use both ways to launch jobs

## Login and Compute Nodes
Recall the last time you went to the dentist or the doctor. When you arrived, you signed in, filled out a bunch of paper work about you and your insurance, and maybe paid a co-pay. Then you waited around and read a magazine or played on your phone until your name was called. Then you went into the procedure room where the doctor and nurses came and worked their magic. 

Its not a perfect analogy, but I think this helps conceptualize login and compute nodes. The login nodes are where you go to get all your paper work in order and settle the payment, but compute nodes are where the magic of bioinformatics or computing happen. In the same way that a doctor won't operate on you in the waiting room, don't do your hard core computing on the login nodes.  

In order to use the computer nodes of a super computer like TACC, you must go through a  "Queue Manager" program. This program keeps track of what's running, what is in the queue, and how much processing power and time each of those jobs need. The "Queue Manager" program needs two things files from you:

1. a job submission script (.slurm)
2. a commands file (.cmds)

Your commands file will be referenced in the job submission script. 

You tell the Queue Manager what you want done via a .slurm file - your job submission script. That specifies how many nodes you need, what allocation to use, the maximum run time of the job, etc. The Queue Manager doesn't really care what you're running, just how you want it run. It needs to pass info on what you're running off to the compute node - you do that with the line setenv CONTROL_FILE commands.
The Queue Manager sends off the commands in the file commands to the compute nodes; so commands is really the first thing to start with.

## Commands File (.cmds)

In the Unix tutorial, we saw that we could put some commands inside a .sh bash script in order to execute them from the command line. For supercommuting, we put the commands inside a commands file that will be referenced in our job submission script. There are a handful of standard file extensions one can use. The .cmd extension is nice because it helps you see at a glance that this is a commands file.


## Job Submission Script



