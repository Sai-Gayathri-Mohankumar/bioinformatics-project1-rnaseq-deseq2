# Project 1: RNA-seq Differential Expression Analysis using DESeq2

## Overview
This project performs RNA-seq differential gene expression analysis on human cornea tissue infected with SARS-CoV-2 using the DESeq2 package in R.

The goal of this analysis is to identify genes that are significantly upregulated or downregulated in infected tissue compared to control samples.

Dataset source:
GEO: GSE164073 from NCBI

---

# Dataset

The dataset contains RNA-seq count data from human eye tissues.

For this project, only "cornea samples" were analysed.

Samples used:

Control samples:
- MW1_cornea_mock_1
- MW2_cornea_mock_2
- MW3_cornea_mock_3

Infected samples:
- MW4_cornea_CoV2_1
- MW5_cornea_CoV2_2
- MW6_cornea_CoV2_3

Total genes analysed: 27,946

---

# Methods

The analysis pipeline included the following steps:

1. Load RNA-seq count matrix
2. Subset cornea samples
3. Perform normalisation using DESeq2
4. Differential expression analysis
5. Visualisation of results

Tools used:

- R
- DESeq2
- ggplot2
- EnhancedVolcano
- pheatmap
- dplyr

---

# Results

## PCA Plot

Principal Component Analysis shows clear separation between control and infected samples.

PC1 explains **69% of the variance**, indicating strong transcriptional differences caused by infection.

![PCA Plot](results/PCA_plot_project1.png)

Interpretation:

Control samples cluster together while infected samples form a separate cluster, indicating consistent biological differences between conditions.

---

## Volcano Plot

The volcano plot shows genes that are significantly upregulated or downregulated in infected samples.

![Volcano Plot](results/volcano_plot_project1.png)

Key observations:

Significant upregulated genes include:

-SOD2
-C3
-CFB
-CA12

These genes are associated with immune response and inflammation pathways.

---

## Heatmap of Top Differentially Expressed Genes

The heatmap shows expression patterns of the top significant genes.

![Heatmap](results/heatmap_project1.png)

Interpretation:

Control samples show lower expression of immune-related genes, while infected samples display strong upregulation of genes involved in immune signaling and inflammation.

Examples include:

- SOD2
- CXCL6
- IL11
- TNFAIP genes
- Complement pathway genes (C3, CFB)

---

# Biological Interpretation

The analysis suggests that SARS-CoV-2 infection induces strong immune and inflammatory responses in cornea tissue.

Upregulated genes are associated with:

- oxidative stress response
- complement activation
- cytokine signalling
- innate immune response

These findings are consistent with known host responses to viral infection.

---

# Files in this Repository
scripts/
project1_deseq2_analysis.R

results/
volcano_plot_project1.png
PCA_plot_project1.png
heatmap_project1.png
DEG_results.csv

Data/GSE164073_Eye_count_matrix.csv

---
# Author
Sai Gayathri Mohankumar
