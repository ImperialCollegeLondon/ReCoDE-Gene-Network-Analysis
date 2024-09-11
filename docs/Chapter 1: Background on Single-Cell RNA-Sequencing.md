# Chapter 1: Background on Single-Cell RNA-Sequencing

## Introduction

In this notebook, we will cover the foundations of single-cell RNA-sequencing as well as how to acquire and process the data into the desired format for gene network analysis.

## Learning Objectives

- Discuss the steps involved in single-cell RNA-sequencing
- Learn how to find publicly accessible snRNA-seq data
- Use python to process filtered data to an appropriate format for downstream analysis

## Single-Cell RNA-sequencing (scRNA-seq)

Transcriptomics studies to explore gene expression were initially conducted using bulk RNA-sequencing (RNA-seq), which provided the average gene expression profile for the population of cells within the sample. While bulk RNA-seq is useful for comparing gene expression levels between different conditions (such as control vs. disease states), it fails to capture the variability and unique gene expression patterns within individual cells, a phenomenon known as cellular heterogeneity.

Cellular heterogeneity is critical in understanding complex biological processes. For example, within a tissue, not all cells behave identically. Some may be driving disease progression while others remain unaffected. By averaging gene expression in bulk RNA-seq, you lose this detailed, cell-specific information, which is crucial for uncovering mechanisms such as disease-specific gene expression or responses to treatment.

Single-cell RNA-sequencing (scRNA-seq) overcomes this limitation by capturing and analysing gene expression at the individual cell level. Each transcript from each cell is sequenced, allowing researchers to identify and quantify mRNA molecules within thousands to millions of individual cells simultaneously.

Why is Single-Cell Analysis Important?
Single-cell RNA-seq enables:

- Detection of rare cell populations that may play critical roles in disease.
- Identification of cellular states within complex tissues, such as cancer or the brain.
- Discovery of gene expression networks driving specific cellular behaviors.
- Mapping of cell development processes, such as differentiation in stem cells.

For example, in studying cancer, using bulk RNA-seq may reveal overall differences between disease and control samples. However, scRNA-seq allows for identification of disease-relevant cell types, and uncovers how these cells behave differently at the individual level.

Each transcript is sequenced using standard technology platforms such as 10x Genomics.  The sequenced reads are the raw data and need to be pre-processed before any downstream analysis. 

## Basic Workflow of scRNA-seq Data Processing
The steps of single-cell RNA-seq analysis typically include:

1. Cell isolation: Cells are separated from a tissue or sample.
2. Library preparation: Single cells are encapsulated, and their RNA is reverse-transcribed into cDNA.
3. Sequencing: The cDNA libraries are sequenced to capture all RNA transcripts present in each cell.
4. Data generation: The sequenced reads are processed to generate a cell-by-gene count matrix, where each cell is represented by its unique expression profile.
5. Data preprocessing: This includes quality control to filter out poor-quality cells or genes (low-read cells, doublets, and contaminants), normalisation to account for sequencing depth, and scaling to enable comparisons between cells.
6. Downstream analysis: After preprocessing, the data is ready for various downstream analyses, such as clustering, cell-type identification, trajectory inference, and differential gene expression analysis.

## Gene Expression Matrices
The primary output of scRNA-seq is a gene expression matrix, where:

- Rows represent genes
- Columns represent cells

Each entry in the matrix contains the count of reads corresponding to a gene in a specific cell. The goal is to prepare this matrix for downstream analysis by filtering out low-quality cells and genes that may introduce noise into the data.

## Working with Public Single-Cell Datasets
Numerous publicly accessible scRNA-seq datasets are available for download through repositories like:

- Cellxgene (a tool for exploring large scRNA-seq datasets),
- Gene Expression Omnibus (GEO), and
- Human Cell Atlas (HCA)

For this chapter, we will be using a filtered dataset from a public database focussing on B cells from both patients that are control and those with clonal haematopoiesis. 

It is good practice to download the dataset for yourself to see what kind of data format you are working with and whether anything needs altered to fit the desired format for your project.

## Dataset Preparation in Python
Once you have acquired the data, the next step is to load it into Python for inspection and processing. The dataset is typically in an HDF5-based format, such as .h5ad (used in AnnData), which stores the expression matrix along with metadata for cells and genes.

Before analysis, it's essential to:

- Review and reformat metadata: Metadata often contains important information about cell types, sample conditions, and batch effects. Ensuring this metadata is clean and well-structured is crucial for accurate downstream analysis.
- Quality control: Check for missing or mislabeled data, and reformat columns as necessary.

By the end of this chapter, you will have a clean, filtered single-cell RNA-seq object to use for gene network analysis.

## Resources

For more information on single-cell RNA sequencing please see: <https://hbctraining.github.io/scRNA-seq/>
<https://www.nature.com/articles/s12276-018-0071-8>
