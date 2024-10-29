
# **Spatial Transcriptomics of Human Colorectal Cancer**

This repository contains a spatial transcriptomics analysis of human colorectal cancer, using data obtained from the [10X Genomics Dataset](https://www.10xgenomics.com/datasets/human-colorectal-cancer-whole-transcriptome-analysis-1-standard-1-2-0).

## **Files in This Repository**
* Parent_Visium_Human_ColorectalCancer_filtered_feature_bc_matrix.h5: Filtered gene expression data matrix for the sample, storing the expression levels for each gene across different spatial barcodes.
* Parent_Visium_Human_ColorectalCancer_spatial.tar.gz: Contains spatial metadata and images, including the high-resolution tissue image and positional information for spatial barcodes.
* Spatial_Transcriptomics_Colorectal_cancer.ipynb: Jupyter notebook containing the analysis workflow, including data loading, clustering, pathway enrichment, and spatial visualization.
* tissue.png: A reference tissue image used for overlaying spatial gene expression clusters.


## **Analysis Overview**

The analysis is divided into the following key steps:

* Data Loading: Load gene expression data and spatial metadata from the 10X Genomics Visium files.
* Clustering and Dimensionality Reduction: Identify distinct clusters of cells based on gene expression profiles using UMAP and K-means clustering.
* Pathway Enrichment Analysis: Analyze the biological pathways enriched in each cluster to infer the functional roles of different cell populations within the tumor.
* Spatial Visualization: Map clusters back onto the high-resolution tissue image to visualize the spatial distribution of different cell types or functional states.


## **Conclusion**

This analysis of spatial transcriptomics data identifies distinct clusters of cells based on gene expression and explores their biological significance through pathway enrichment, and finally maps it into the original image using spacial distribution, from a sample of human Colorectal cancer.



### **Applications of this Analysis:**

In the context of drug discovery and precision medicine, this spatial transcriptomics analysis of a human colorectal cancer sample provides key insights that could guide therapeutic development and personalized treatment strategies:

#### 1. **Identification of Functional Zones in the Tumour:**
  By clustering cells based on gene expression and mapping them spatially, we identified distinct regions within the tumour with unique biological functions. For instance, clusters enriched in **protein synthesis** and **ribosomal activity** likely represent **proliferative zones**, where rapid cell division is fueling tumour growth. 
  
  **Suggestions:** Targeting these proliferative zones with **protein synthesis inhibitors** or **anti-proliferative drugs** could disrupt the tumour’s expansion.
<br><br> 

#### 2. **Metabolic Vulnerabilities:**
  Clusters with **high mitochondrial activity** and **oxidative phosphorylation** point to cells with **increased energy demands**, often characteristic of cancer cells adapting to a nutrient-limited microenvironment. 
  
  **Suggestions:** These findings suggest potential metabolic vulnerabilities that could be targeted by **metabolic inhibitors** to reduce the energy supply essential for tumour survival, especially in well-vascularized or highly proliferative regions.
<br><br>

#### 3. **Immune Cell Localization and Immune Microenvironment:**
  The spatial distribution of **immune cell-related genes**, especially in Cluster 3, highlights areas where immune cells are present within or around the tumour. This cluster includes pathways related to **immunoglobulins**, suggesting the presence of **antibody-producing B cells** or other immune cells actively responding to the tumour. 
  

  **Suggestions:** **Immunotherapies** could be effective if they amplify these immune responses or improve immune cell infiltration into the tumour, potentially increasing the tumour’s vulnerability to immune attack.
<br><br>

#### 4. **Pathway-Specific Insights for Targeted Therapies:**
The pathway enrichment analysis revealed overactive pathways associated with **protein synthesis**, **mitochondrial function**, and **immune signalling**. These pathways could serve as therapeutic targets, where pathway-specific inhibitors or combination therapies may be explored.


**Suggestions:** **Protein synthesis inhibitors** could target clusters with **high ribosomal activity**.
**Mitochondrial inhibitors** may affect clusters relying on **oxidative phosphorylation**.
**Immune checkpoint inhibitors** or **CAR-T cell therapies** could be enhanced by **targeting immune-enriched regions** of the tumour.
<br><br>

#### 5. **Implications for Precision Medicine:**
Mapping the functional and spatial heterogeneity of the tumour offers a roadmap for personalized treatment by identifying which pathways and cell types are active in specific tumour regions. 

**Suggestions:** By tailoring therapies to the specific characteristics of each cluster, we could potentially improve treatment outcomes. For example, targeting proliferative clusters aggressively while supporting immune activation could offer a dual approach to shrink the tumour and bolster the body's own defenses.


## **Dataset Information**
Sample: Fresh frozen invasive adenocarcinoma of the large intestine.
Source: Provided by BioIVT Asterand and processed with the 10X Genomics Visium platform.
Data Link: [10X Genomics Dataset](https://www.10xgenomics.com/datasets/human-colorectal-cancer-whole-transcriptome-analysis-1-standard-1-2-0)

## **Dependancies:**

The notebook uses the following Python packages:

* scanpy
* h5py
* matplotlib
* seaborn
* umap-learn
* scipy
* pandas
* gprofiler-official
