# TulipTreePopGen
Population genomic analysis of the Tuliptree (Liriodendron tulipifera)

[TOC]

### Reference Genome 

#### Digital Digest

There is a Tuliptree reference genome that can be used for read mapping. The first step to support genotyping is to perform a digital digest with the possible restriction enyzmes.

Download the *Liriodendron tulipifera* [genome]() from phytozome

Using egads, perform a digital digest. The rare cutters are just the list that are available at UConn's sequencing core.

```
egads=~/methods/egads/egads

# Path to genome
genome=/home/karl.fetter/tuliptree/assembly/Phytozome/PhytozomeV13/LtulipiferaYP108A/v1.1/asse
mbly/LtulipiferaYP108A_766_v1.0.softmasked.fa.gz

rare_cutters="PstI,SbfI,NsiI,SphI"
frequent_cutters="MspI,EcoRI,MluCI,NlaIII,Sau3Ai,BfaI,HinP1I,SbfI"

$egads \
        --genome $genome \
        --rare $rare_cutters \
        --freq $frequenct_cutters \
        --html lirtul_egads_report.html \
        --bed lirtul.bed
```

The report contains the relevant information.