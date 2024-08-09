

# Gene Expression Analysis to Detect Alzheimer's

## Group 11 Members
- **Abhishek Bansal (2022021)**
- **Debjit Banerji (2022146)**
- **Anish (2022075)**
- **Kartikeya (2022241)**
- **Vijval Ekbote (2022569)**
- **Mohd. Masood (2022299)**

## Introduction

Alzheimer’s disease is a progressive neurodegenerative disease that worsens over time, beginning with mild memory loss and eventually leading to the loss of the ability to carry out even simple daily tasks. This project aims to perform gene expression analysis to differentiate between normal and Alzheimer's-affected genes using data from the NCBI GEO2R tool.

## Problem Statement

Our goal is to perform Gene Expression Analysis to identify normal genes and Alzheimer's genes. By using the NCBI GEO2R tool for Differential Gene Expression (DGE) analysis, we identify which genes are diseased and which are not. The analysis includes the use of Volcano plots, clustered plots, and statistical tests. Additionally, we train a machine learning model to predict whether a person has Alzheimer's disease based on their gene expression data.

## Project Workflow

1. **Identify Problem Statement**
2. **Search Appropriate Dataset**
3. **Filter Out the Data**
4. **Identify Biomarker Genes Responsible for Differential Gene Expression (DGE)**
5. **Train Machine Learning Model Based on Biomarker Genes**
6. **Test the Machine Learning Model**
7. **Validate the Model**

## Data Collection

- **Source:** [NCBI GEO2R](https://www.ncbi.nlm.nih.gov/geo/geo2r/?acc=GSE84422&platform=GPL96)
- **Dataset Description:** The dataset consists of RNA samples from 19 brain regions isolated from 125 MSBB specimens, with a total of 1053 postmortem brain samples. Each sample includes expression levels of 14,160 genes.

## Data Processing

1. **Group Creation:** Grouping the samples based on disease state (Normal, Alzheimer’s).
2. **Normalization:** Applying normalization to the data.
3. **Volcano Plot Analysis:** Identifying differentially expressed genes using Volcano plots.
4. **UMAP Cluster Plot:** Visualizing sample clusters to distinguish between Alzheimer's and normal samples.
5. **Data Cleaning and Formatting:** Preparing the data for machine learning by merging metadata and expression levels.

## Gene Set Enrichment Analysis (GSEA)

- We performed GSEA to analyze biological pathways associated with Alzheimer's disease using the "GO_Biological_Process_2023" library. The results were sorted and plotted to identify relevant pathways.

## Identifying Differentially Expressed Genes (DEGs)

- We set a p-value threshold of 0.05 and a fold change threshold of 2 to narrow down the list of genes. The analysis resulted in identifying 121 genes, which were then reduced to 50 principal components using PCA.

## Machine Learning Model Training

- **Data Split:** 70% of the data was used for training, and 30% for testing.
- **Models Used:** Naive Bayes, KNN, Logistic Regression, SVC.
- **Final Model:** The SVC model was selected as the most appropriate model for detecting Alzheimer's based on gene expression data.

## Validation

- The SVC model was validated using performance metrics like Sensitivity, Accuracy, Precision, and F1-Score. Additionally, LIME was used for model explainability to determine which features most influenced the predictions.

## Conclusion

Our project successfully integrates bioinformatics tools and machine learning to identify differentially expressed genes associated with Alzheimer's disease. The model developed can distinguish Alzheimer's from normal gene expression profiles, offering a valuable tool for early detection.

## Acknowledgments

- **GEO2R Analysis and Data Collection and Cleansing::** Masood
- **Statistical Testing (Using Python):** Abhishek & Kartikeya
- **ML Model and GSEA:** Debjit & Vijval
- **Presentation Quality:** Collective effort by the group

---
