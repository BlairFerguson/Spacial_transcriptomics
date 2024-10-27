
##**Spatial Transcriptomics of Human Colorectal Cancer**

This repository contains a spatial transcriptomics analysis of human colorectal cancer, using data obtained from the 10X Genomics dataset.
https://www.10xgenomics.com/datasets/human-colorectal-cancer-whole-transcriptome-analysis-1-standard-1-2-0

**Files in This Repository**
* Parent_Visium_Human_ColorectalCancer_filtered_feature_bc_matrix.h5: Filtered gene expression data matrix for the sample, storing the expression levels for each gene across different spatial barcodes.
* Parent_Visium_Human_ColorectalCancer_spatial.tar.gz: Contains spatial metadata and images, including the high-resolution tissue image and positional information for spatial barcodes.
* Spatial_Transcriptomics_Colorectal_cancer.ipynb: Jupyter notebook containing the analysis workflow, including data loading, clustering, pathway enrichment, and spatial visualization.
* tissue.png: A reference tissue image used for overlaying spatial gene expression clusters.


**Analysis Overview**

The analysis is divided into the following key steps:

* Data Loading: Load gene expression data and spatial metadata from the 10X Genomics Visium files.
* Clustering and Dimensionality Reduction: Identify distinct clusters of cells based on gene expression profiles using UMAP and K-means clustering.
* Pathway Enrichment Analysis: Analyze the biological pathways enriched in each cluster to infer the functional roles of different cell populations within the tumor.
* Spatial Visualization: Map clusters back onto the high-resolution tissue image to visualize the spatial distribution of different cell types or functional states.


**Dataset Information**
Sample: Fresh frozen invasive adenocarcinoma of the large intestine.
Source: Provided by BioIVT Asterand and processed with the 10X Genomics Visium platform.
Data Link: [10X Genomics Dataset](https://www.10xgenomics.com/datasets/human-colorectal-cancer-whole-transcriptome-analysis-1-standard-1-2-0)

**Dependancies:**

The notebook uses the following Python packages:

* scanpy
* h5py
* matplotlib
* seaborn
* umap-learn
* scipy
* pandas
* gprofiler-official
