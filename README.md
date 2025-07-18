# RNA-seq Analysis Workflow in a *De Novo* Transcriptome Assembly

> This walkthrough showcases the key steps used during my M.Sc. research on plant specialized metabolism in *Tacca chantrieri*. It is designed for biology researchers, graduate students, and anyone new to RNA-seq bioinformatics. Oftentimes like in my case genomes are not available in non-model organisms, requiring a thorough transcriptomic profiling without the use of a genome, hence why no emphasis was made on genome alignment here.

---

## 📚 Table of Contents

1. [Key Prerequisites](01_key_prerequisites.md)
   Conda environment, basic UNIX/R, folder setup.

3. **Study Design for RNA Sequencing**  
   Tissue selection, replicates, library prep strategy.

4. **Fetching Raw Data and Reference Databases**  
   SRA, ENA, UniProt, Pfam, KEGG, etc.

5. **Read Quality Control**  
   `fastqc`, `multiqc`, adapter trimming.

6. **Transcriptome Assembly**  
   `Trinity` and considerations for strand-specific reads.

7. **Assembly Quality Assessment**  
   Using `BUSCO`, `TransRate`, and transcript statistics (N50, GC%).

8. **Annotation 1: Transcript Abundance**  
   Quantification with `Salmon`, TPM/FPKM matrices.

9. **Annotation 2: RNA Classification & Translation**  
   `TransDecoder`, coding vs. noncoding transcripts.

10. **Annotation 3: Subcellular Localization & Signal Peptides**  
   `TargetP`, `SignalP`, and `DeepLoc`.

11. **Annotation 4: Homology-Based Function Transfer**  
    `DIAMOND`, `BLASTp`, UniProt/SwissProt search.

12. **Annotation 5: Protein Domains & Features**  
    `HMMER`, `CDD`, and `InterProScan`.

13. **Annotation 6: Functional Networks and Pathways**  
    `eggNOG`, `KEGG`, `GO`, `BRENDA`, `COG`.

14. **Annotation 7: Secondary Structure Prediction**  
    `PSIPRED`, `I-TASSER`, and AlphaFold2.

15. **Annotation 8: AI/ML Tools for Protein Function Prediction**  
    Embedding models like `ESMFold`, `ProtT5`, and `CLEAN`.

16. **Alignments and Phylogenetic Trees**  
    `MAFFT`, `IQ-TREE`, `ggseqlogo` for motif visualization.

17. **Differential Gene Expression Analysis**  
    Using `tximport`, `edgeR`, and `DESeq2`.

18. **GO and KEGG Enrichment Analysis**  
    `ClusterProfiler`, dotplots, GO networks.

19. **Expression Clustering and Coexpression Networks**  
    `WGCNA`, `Mfuzz`, and network module interpretation.

20. **Brief Walkthrough of Using Genomes and Genomic Analysis**

21. **Biosynthetic Gene Cluster Analysis**

22. **Workflow Management with Snakemake**  
    Rule-based reproducible pipelines with DAG visualization.

CASE STUDY: LARGE PLANT DATASET RNA-SEQ ANALYSIS

### 🧠 Advanced Topics & Extras
22. **SPECIAL: Machine Learning and AI Crash Course**
23. **SPECIAL: Cheminformatics and Natural Products**
24. **SPECIAL: Protein Language Models**
25. **SPECIAL: Protein-Small Molecule Docking and Affinity Modeling**
26. **SPECIAL: NVIDIA BioNeMo Toolkit for Protein & Drug Design**

---

> 🔬 Feel free to explore each section for command examples, code snippets, tools used, and interpretation strategies. This guide is intended to bridge the gap between wet lab and computational biology. 
Contact: justin.seyedmoomenkashi@mail.mcgill.ca
