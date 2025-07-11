# Walkthrough of bioinformatic workflow used in my masters thesis 
>This walkthrough provides the command line calls of bioinformatic tools, python scripts, bash scripts and SLURM scripts used on HPC to replicate the results obtained in my masters thesis. The thesis looked at investigating the transcriptome of the plant Tacca chantrieri in both its leaf and rhizome tissues. The motivation for this was because this unique plant produces taccalonolides, a family of specialized metabolites exclusively specific to the Tacca species and are found in the rhizomes of the plant while absent in its leaves. We believe the biosynthetic pathway behind the production of taccalonolides consists predominantly of CYP450s, the largest superfamily of enzymes in plants and even across all kingdoms. The strategy was to perform a differential gene expression analysis across leaves and rhizomes to identify CYP450 genes upregulated in rhizome tissues. During my masters, I sourced three biological replicates of T.chantrieri pots of plants and extracted the RNA from its leaves and rhizomes for sequencing. Afterwards, transcriptome assembly was conducted followed by a differential gene expression analysis across the two tissues. This brief guide walks through the main steps of this workflow, along with its integration in a workflow manager with Docker containerization. 

```

fastqc 

```
