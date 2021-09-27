---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

My research focuses on genome assembly, the process of reconstructing a genome 
from sequencing data. This is a challenging process, where algorithmic accuracy 
as well as efficiency are crucial. By developing new approaches to several 
relevant assembly problems I try to further our understanding of microbial 
genomics. Further details on my contributions to the topics described below 
can be found in my Publications.


### Haplotype reconstruction

The copy-specific sequences of the genome are called haplotypes, and the number 
of haplotypes in a given organism is described by its ploidy. Ploidy can vary 
across species, some species being haploid (one copy per chromosome, e.g. 
bacteria), some being diploid (two copies per chromosome, e.g. many mammals, 
including humans), and others having higher ploidies (many plants have at least 
4 copies per chromosome).

Generic de novo assembly approaches produce a consensus assembly, meaning that 
the different haplotypes that make up the genome are collapsed onto a single 
consensus sequence. In haplotype-aware genome assembly, the goal is rather to 
reconstruct the individual haplotypes in an organism or population. This is 
particularly challenging: beyond distinguishing true genomic variation from 
sequencing artifacts, the true variants need to be assigned to the different 
genome copies.

In my PhD thesis I discuss the topic of haplotype reconstruction and present 
new algorithms for de novo haplotype assembly (see also Software).

 
### Strain-aware metagenomics

Metagenomics studies the genetic material found in environmental samples, for 
example taken from the ocean or the human gut. These samples typically contain 
a large number of different species, as well as different strains from the 
same species; a metagenome captures all genomes in a given microbial community. 
The goal of strain-aware metagenome assembly is to reconstruct each of the 
individual genomes in a metagenome, thus preserving all within-species 
variation. I have developed an approach for strain-aware assembly from mixed 
samples which will be extended to an accurate workflow for strain-aware 
metagenomics.

 
### Viral quasispecies assembly

A highly relevant application of haplotype reconstruction appears in the 
analysis of viral infections. Since viruses (in particular RNA viruses) exhibit 
very high mutation rates, their genomes undergo rapid changes that allow them 
to adapt to their environment and escape drug treatment and immune response. As 
a result, the virus exists as a “quasispecies”: a cloud of closely-related 
mutant strains, each with its own characteristics in terms of virulence and 
resistance. Since knowledge of the infecting strains contributes to improved 
treatment design, I have developed a series of methods that enables highly 
accurate, full-length viral quasispecies assembly.

 
### Bacterial evolutionary genomics

Bacterial genomes can be dramatically rearranged by mobile genetic elements, 
recombination, and horizontal gene transfer. Such rearrangements result in 
structural variation between genomes, including large repetitive sequences 
(repeats). Identifying these repeats and other structural variants is important, 
because these genomic changes can influence phenotypes such as virulence and 
susceptibility to antibiotics. I work on methods for accurately resolving 
structural variation, to further our understanding of bacterial evolution and 
antibiotic resistance.
