# LUAD Proteomics Pipeline 
# LUAD Proteomics Pipeline

End-to-end computational proteomics analysis pipeline applied to the CPTAC Lung Adenocarcinoma (LUAD) dataset.

## Overview
This project was inspired by the research framework of the **Pauling Lab** (Computational Integrative Omics in Biomedicine, Universitätsklinikum Carl Gustav Carus Dresden).

## Dataset
- **Source:** CPTAC LUAD (Clinical Proteomic Tumor Analysis Consortium)
- **Samples:** 211 (110 Tumor, 101 Normal)
- **Features:** 10,699 proteins
- **Publication:** [Nature, 2020](https://pubmed.ncbi.nlm.nih.gov/32649874/)

## Pipeline Steps
1. **Data Loading** — CPTAC API, proteomics + clinical metadata
2. **Quality Control** — Missing value analysis, filtering (>30% missing removed)
3. **Normalization** — kNN imputation + median centering
4. **Differential Expression** — t-test, FDR correction (Benjamini-Hochberg)
5. **Dimensionality Reduction** — PCA + UMAP
6. **Network Analysis** — STRING DB + NetworkX connected components

## Key Results
- **6,601 proteins** significantly different between Tumor and Normal (FDR < 0.05)
- **PC1 explains 36.4%** of variance, cleanly separating Tumor from Normal
- **4 connected components** identified in the protein interaction network
- **Hub proteins:** TLN1, CAV1, CDH5 — all downregulated in Tumor

## Tools & Libraries
`Python` `pandas` `numpy` `scipy` `scikit-learn` `umap-learn` `networkx` `matplotlib` `seaborn` `cptac`

## Author
Zeynep Aslan — University of Göttingen