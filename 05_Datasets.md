## Motivating Dataset

## *Cancer borealis* Transcriptomes 

Dave Schulz has provided us with *Cancer borealis* transciptomes to use for our training. Rayna has stored a copy of these in her work directory that you can copy over to your work directory. 

- [ ] Navigate to your work directory then copy this folder from Rayna's "community" directory. 

~~~ {.bash}
$ cdw
$ cp -r /work/02189/rmharris/community/transcriptomes .
$ ls -lht
~~~ 

~~~ {.output}
-rwxrwxrwx 1 rmharris G-813760 168K Jun 21 17:34 SchulzD_Cb_CDS_CHR.fasta
-rwxrwxrwx 1 rmharris G-813760  65M Jun 21 17:34 Cborealis_ref.fa
~~~ 

- The Cborealis_ref.fa file is a full transcriptome. 
- The SchulzD_Cb_CDS_CHR.fasta is a partial transcrpitome, made up of 88 candidate genes