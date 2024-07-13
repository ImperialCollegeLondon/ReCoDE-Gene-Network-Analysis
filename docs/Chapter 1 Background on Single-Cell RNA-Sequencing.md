# Chapter 1: Background on Single-Cell RNA-Sequencing

## Introduction

In this notebook, we will cover the foundations of single-cell RNA-sequencing, how to acquire and process the data into the desired format for gene network analysis.

## Learning Objectives

- Discuss the steps involved in single-cell RNA-sequencing
- Learn how to find publicly accessible snRNA-seq data
- Use python to process filtered data to an appropriate format for downstream analysis

## Single-Cell RNA-sequencing

Transcriptomics studies were initially conducted using bulk RNA-sequencing but this method only compared the averages of all cells within cell populations, masking cellular heterogeneity. Single-cell RNA-sequencing.

![Single Cells]()

For example, while bulk RNA-seq can facilitate explorations of gene expression between different conditions (e.g. disease and control), this is just calculated as the average expression of the total cell population within each condition. In contrast, when cells have been grouped, this more accurately captures gene expression driving the differences between conditions. Overall, this now shows the correct association between Gene A and Gene B within this example.

Each transcript is sequenced using standard technology platforms such as 10x Genomics or Drop-seq.  The sequenced reads are the raw data and need to be pre-processed before any downstream analysis. The basic steps of the workflow are: generation of the count matrix from the sequenced reads, creating a cell x gene matrix, quality control of raw counts and gene marker identification for cell typing.

![Single Cells]()

The number of reads from the sequenced transcripts within each cell are counted for each gene and input as a value within the matrix. This matrix is usually processed further to remove any poor quality cells, and outputs a filtered version of the matrix.

We will be working with a filtered snRNA-seq dataset acquired from cellxgene. This particular dataset contains microglia from Control and Alzheimer's Disease patients.

It is good practice to download the dataset for yourself to see what kind of data format you are working with and whether anything needs altered to fit the desired format for your project.

In this case, some formatting is needed to correct the metadata into a useable format. Generally, this can be done in R and python. We will be continuing with python to keep the language used consistent.

See the docs/? notebook on how to load the data into python. Have a look at the data and format the metadata. When you open the file, as can be seen ? columns needs to be reformatted so that it displays ? instead.
A correctly formatted h5ad object can be found in the solutions folder.
You now have a filtered snRNA-seq object to work with for the next steps.

## Resources

For more information on single-cell RNA sequencing please see: <https://hbctraining.github.io/scRNA-seq/>
