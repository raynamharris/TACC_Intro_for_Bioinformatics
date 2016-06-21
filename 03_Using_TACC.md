# Using the TACC Clusters

## Learning objectives
- know where to get more detailed information on the clusters
- use ssh to logon to TACC

## User Guides

**The Stampede User Guide**: For complete up-to-date information, see the complete [Stampede User Guide](https://portal.tacc.utexas.edu/user-guides/stampede).

## Use SSH to logon to TACC

~~~ {.bash}
$ ssh <username>@stampede.tacc.utexas.edu
~~~

You will be prompted to enter your password

~~~ {.output}
Password:
~~~

Then you will be asked if you are okay logining in. Say yes. 

Then, you will be greeted with a login screen. 


~~~ {.output}

------------------------------------------------------------------------------
                   Welcome to the Stampede Supercomputer
      Texas Advanced Computing Center, The University of Texas at Austin
------------------------------------------------------------------------------
...

--------------------- Project balances for user rmharris ----------------------
| Name           Avail SUs     Expires | Name           Avail SUs     Expires |
| NeuroEthoEvoDevo      45309  2016-12-31 | AltReproTactics      24715  2017-03-31 | 
| UT-2015-05-18       1173  2016-12-31 |                                      |
------------------------ Disk quotas for user rmharris ------------------------
| Disk         Usage (GB)     Limit    %Used   File Usage       Limit   %Used |
| /home1              0.1       5.0     2.57         3402      150000    2.27 |
| /work             859.3    1024.0    83.92           15     3000000    0.00 |
| /scratch          218.5       0.0     0.00         1058           0    0.00 |
-------------------------------------------------------------------------------

Tip 160   (See "module help tacc_tips" for features or how to disable)

   To see how to control an ssh session type: <enter>~?

tacc:~$
~~~

## 
