# 🧬 Code availability

This repository contains my implementation analysis for my bachelor thesis project. 

## 1. PyOrthoANI
Calculate the ANI value based on four reference strains. 

## 2. T3SS1 analysis

T3SS1 has 2 gene clusters—one on each chromosome. Therefore, I worked on each cluster separately:
+ Results for chromosome 1 are in the T3SS1_chr1 folder (T3SS1_chr1_normalized.fasta).
+ Results for chromosome 2 are in the T3SS1_chr2 folder (T3SS1_chr2_normalized.fasta).
Then, I used MAFFT (on UseGalaxy) to align these files. The outputs are:
+ MAFFT_chr1.fasta
+ MAFFT_chr2.fasta
+ Both are in the T3SS1_chr12 folder (does not show in here).

Then, I took the core parts of each alignment and combined them into one file:
+ combined_chr12.fasta (found in the phylogenetic_tree_output folder)

After that, I made a modified Nexus file (with the model I got from running IQ-TREE) and used it to build a phylogenetic tree with IQ-TREE3 using partitioned alignment.

### 3. T6SS2 analysis
T6SS2 only has one cluster (22 genes) on chromosome 2.The process was basically the same as for T3SS1, but this does not have combined step.
