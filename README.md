# Walkthrough of RNA-seq Analysis Workflow in a *De Novo* Transcriptome Assembly

> This walkthrough showcases the key steps used during my M.Sc. research on plant specialized metabolism in *Tacca chantrieri*. It is designed for biology researchers, graduate students, and anyone new to RNA-seq bioinformatics. Oftentimes like in my case genomes are not available in non-model organisms, requiring a thorough transcriptomic profiling without the use of a genome, hence why no emphasis was made on genome alignment here.

---

## 📚 Table of Contents

1. **Key Prerequisites**  
   Conda environment, basic UNIX/R, folder setup.

2. **Study Design for RNA Sequencing**  
   Tissue selection, replicates, library prep strategy.

3. **Fetching Raw Data and Reference Databases**  
   SRA, ENA, UniProt, Pfam, KEGG, etc.

4. **Read Quality Control**  
   `fastqc`, `multiqc`, adapter trimming.

5. **Transcriptome Assembly**  
   `Trinity` and considerations for strand-specific reads.

6. **Assembly Quality Assessment**  
   Using `BUSCO`, `TransRate`, and transcript statistics (N50, GC%).

7. **Annotation 1: Transcript Abundance**  
   Quantification with `Salmon`, TPM/FPKM matrices.

8. **Annotation 2: RNA Classification & Translation**  
   `TransDecoder`, coding vs. noncoding transcripts.

9. **Annotation 3: Subcellular Localization & Signal Peptides**  
   `TargetP`, `SignalP`, and `DeepLoc`.

10. **Annotation 4: Homology-Based Function Transfer**  
    `DIAMOND`, `BLASTp`, UniProt/SwissProt search.

11. **Annotation 5: Protein Domains & Features**  
    `HMMER`, `CDD`, and `InterProScan`.

12. **Annotation 6: Functional Networks and Pathways**  
    `eggNOG`, `KEGG`, `GO`, `BRENDA`, `COG`.

13. **Annotation 7: Secondary Structure Prediction**  
    `PSIPRED`, `I-TASSER`, and AlphaFold2.

14. **Annotation 8: AI/ML Tools for Protein Function**  
    Embedding models like `ESMFold`, `ProtT5`, and `CLEAN`.

15. **Alignments and Phylogenetic Trees**  
    `MAFFT`, `IQ-TREE`, `ggseqlogo` for motif visualization.

16. **Differential Gene Expression Analysis**  
    Using `tximport`, `edgeR`, and `DESeq2`.

17. **GO and KEGG Enrichment Analysis**  
    `ClusterProfiler`, dotplots, GO networks.

18. **Expression Clustering and Coexpression Networks**  
    `WGCNA`, `Mfuzz`, and network module interpretation.

19. **Workflow Management with Snakemake**  
    Rule-based reproducible pipelines with DAG visualization.

20. **SPECIAL: Brief Walkthrough of Using Genomes and Genomic Analysis**

21. **SPECIAL: Machine Learning and AI Crash Course**
---

> 🔬 Feel free to explore each section for command examples, code snippets, tools used, and interpretation strategies. This guide is intended to bridge the gap between wet lab and computational biology. 
Contact: justin.seyedmoomenkashi@mail.mcgill.ca
