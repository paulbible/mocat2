# mocat2, edited for PBS version 2.5.5

I modified MOCAT2 to get it running on my older version of PBS.

Mainly I modified the MOCATCore.pm, to remove `-W block=none` and changed MOCATExecuteJobPBS.pl to use `#PBS` for options.

In your MOCAT.cfg file, add the pbs options:

`-l nodes=1:ppn=8,mem=10gb -I -x`



# mocat2
MOCAT2 (metagenomic analysis toolkit) is a package for analyzing metagenomics datasets. Currently MOCAT2 supports Illumina single- and paired-end reads in raw FastQ format. Using MOCAT2 you can generate taxonomic and functional profiles, as well as assemblereads and predict genes in assembled sequences. The official MOCAT2 page is http://mocat.embl.de/

Development of MOCAT2 continues post the publication of the MOCAT2 Bioinformatics paper (http://bit.ly/1VbJnzi). This Github repo contains a cutting-edge MOCAT2 version. However, it is unsupported and comes as-is. Thus, only features available in the last tested and stable MOCAT2 release will recieve extensive support (http://mocat.embl.de/download.html).


<b>What's new in the developmental version that is not avilable in the public, stable version?</b>
- Support for BWA as mapping software (instead of SOAP2 aligner)
- Support for SLURM queuing system
- Bug fixes
