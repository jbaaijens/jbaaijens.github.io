---
layout: archive
title: "Software"
permalink: /software/
author_profile: true
---

## AmpliDiff

AmpliDiff is a computational tool for designing amplicons for viral metagenome 
analysis. AmpliDiff finds amplicons and corresponding primers 
*simultaneously*, in order to differentiate maximally between different 
lineages, strains, or species, as defined by the user. The method is described in our [BMC Bioinformatics paper](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-024-05735-4).

AmpliDiff is implemented in Python and publicly available on [github](https://github.com/JaspervB-tud/AmpliDiff/).


## VLQ: Viral Lineage Quantification

VLQ enables fast and accurate SARS-CoV-2 variant prediction from wastewater 
sequencing data. The approach is based on computational techniques initially 
used for RNA-Seq quantification (kallisto). All details are described in our [Genome Biology paper](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-022-02805-9). 

VLQ is implemented in python/bash and publicly available on [github](\url{https://github.com/baymlab/wastewater_analysis).
There is also a [NextFlow implementation](https://github.com/rki-mf1/vlq-nf) 
of VLQ.


## HaploConduct

HaploConduct is a package designed for reconstruction of individual haplotypes
from next generation sequencing data. Currently, HaploConduct consists of two
methods: SAVAGE and POLYTE. The complete HaploConduct package is publicly
available on [github](https://github.com/HaploConduct/HaploConduct) under the 
GPLv3 license and can be easily installed using the Conda package manager.

### SAVAGE: Strain Aware VirAl GEnome assembly
SAVAGE is a computational tool for reconstructing individual haplotypes of
intra-host virus strains (a viral quasispecies) without the need for a high
quality reference genome. SAVAGE makes use of either FM-index based data
structures or ad-hoc consensus reference sequence for constructing overlap
graphs from patient sample data. In this overlap graph, nodes represent reads 
and/or contigs, while edges reflect that two reads/contigs, based on sound 
statistical considerations, represent identical haplotypic sequence. Following 
an iterative scheme, a new overlap assembly algorithm that is based on the 
enumeration of statistically well-calibrated groups of reads/contigs then 
efficiently reconstructs the individual haplotypes from this overlap graph.

Further methodological details are described in our
[Genome Research paper](https://genome.cshlp.org/content/early/2017/04/10/gr.215038.116).


### POLYTE: POLYploid genome fitTEr
POLYTE is a method for reconstructing haplotigs for diploid and polyploid
genome, specifically designed for a low-coverage setting where the ploidy of
the organism is known. POLYTE follows an iterative scheme where in each
iteration reads or contigs are joined, based on their interplay in terms of an
underlying haplotype-aware overlap graph. Along the iterations, contigs grow
while preserving their haplotype identity. POLYTE has been shown to produce very
accurate and complete assemblies, reaching high target genome reconstruction
values at extremely low error rates.

Further methodological details are described in our
[Bioinformatics paper](https://academic.oup.com/bioinformatics/article-abstract/35/21/4281/5474903?redirectedFrom=fulltext).


## VG-Flow

VG-Flow is a computational tool for full-length haplotype reconstruction and
abundance estimation from mixed samples. By reformulating the assembly
challenge as a flow problem, this algorithm is much more efficient than its
predecessor, Virus-VG, allowing also bacterial genomes to be processed. The
method is based on the construction of a flow variation graph, capturing all
diversity present in the sample. VG-Flow computes a solution to the contig
abundance estimation problem and employs a greedy algorithm to efficiently build
full-length haplotypes. Finally, VG-Flow calculates accurate frequency estimates
for the reconstructed haplotypes through linear programming techniques. Further
details are described in our [RECOMB paper](https://www.biorxiv.org/content/10.1101/645721v3).

VG-Flow is publicly available under the MIT license at [https://bitbucket.org/jbaaijens/vg-flow](https://bitbucket.org/jbaaijens/vg-flow).


## Virus-VG

Virus-VG aims to reconstruct full-length viral haplotypes together with their
abundances from the contigs obtained through de novo viral quasispecies assembly
(e.g. using SAVAGE). The algorithm makes use of a contig variation graph to
capture relationships between pre-assembled contigs, and the final output is
represented in the form of a genome variation graph. Further details are
described in our [Bioinformatics paper](https://pubmed.ncbi.nlm.nih.gov/31147688/). 

Virus-VG is publicly available under the MIT license at [https://bitbucket.org/jbaaijens/virus-vg](https://bitbucket.org/jbaaijens/virus-vg).
