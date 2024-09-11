# Chapter 3: Gene Network Downstream Analysis
## Gene Set Enrichment Analysis and Enrichment Strategies

## Introduction

Once a gene network has been constructed, or a list of differentially expressed genes has been obtained, it is important to extract meaningful biological insights from the data. Gene set enrichment analysis (GSEA) is a powerful technique used to interpret large gene lists by determining if certain biological pathways or processes are overrepresented. By identifying overrepresented gene sets, researchers can link the observed changes in gene expression to specific biological processes, functions, or diseases.

This chapter focuses on enrichment strategies, including Gene Set Enrichment Analysis (GSEA) and Fisher Exact Test, to uncover key biological pathways.

## Learning Outcomes

- Understand the concept and importance of gene set enrichment analysis in biological data interpretation.
- Apply gene set enrichment techniques to identify overrepresented biological pathways in gene lists.
- Perform enrichment analysis using common tools like GSEA and the Fisher Exact Test.

## What is Gene Set Enrichment Analysis?

Gene set enrichment analysis (GSEA) is a computational method that determines whether predefined sets of genes are statistically overrepresented in a list of differentially expressed genes. These predefined gene sets are typically grouped based on shared biological functions, pathways, or cellular processes and are stored in databases like:

- Kyoto Encyclopedia of Genes and Genomes (KEGG)
- Gene Ontology (GO)

GSEA helps uncover the biological processes or pathways that are most likely responsible for the observed changes in gene expression.

## Fisher Exact Test for Enrichment

The Fisher Exact Test is a common method for performing enrichment analysis, especially when working with smaller gene sets. It calculates whether the observed overlap between a set of differentially expressed genes and a predefined gene set is higher than expected by chance.

Steps in Fisher Exact Test:

- Input Gene List: Start with a list of differentially expressed genes or a gene network.
- Gene Set: Select gene sets from databases like KEGG or GO.
- Overlap Calculation: Calculate how many genes from the input list overlap with the predefined gene set.
- P-value Calculation: Use the Fisher Exact Test to determine whether the overlap is statistically significant, providing a p-value that indicates the strength of enrichment.

The test considers a 2x2 contingency table to assess the overlap between the gene list and the gene set, calculating the probability of the observed overlap occurring by chance.

## Multiple Testing Correction

Since multiple gene sets are often tested for enrichment, the chances of false positives increase. To address this, the False Discovery Rate (FDR) correction method is applied to adjust p-values, making the results more reliable.

## Applications of Gene Set Enrichment Analysis

- Disease Mechanisms: GSEA can identify biological pathways that are dysregulated in diseases, such as cancer or neurodegenerative disorders.
- Drug Discovery: By identifying pathways enriched in response to a drug, GSEA can help determine potential targets for therapeutic intervention.
- Functional Annotation: Enrichment analysis is used to assign functional significance to gene clusters or networks, improving our understanding of their biological roles.

## Practical Steps for Gene Set Enrichment

- Data Preparation: Obtain a list of differentially expressed genes or genes from a gene network.
- Select Gene Sets: Choose relevant gene sets from databases like KEGG or GO.
- Perform Enrichment Analysis: Use tools like GSEA, Enrichr, or custom Python scripts to run the enrichment analysis.
- Interpret Results: Identify pathways or processes with significant enrichment based on corrected p-values (FDR).

## Resources
<https://www.gsea-msigdb.org/gsea/index.jsp>
<https://www.genome.jp/kegg/>
<https://geneontology.org/>
<https://www.pathwaycommons.org/guide/primers/data_analysis/gsea/>
<https://www.pathwaycommons.org/guide/primers/statistics/fishers_exact_test/>
<https://www.pathwaycommons.org/guide/primers/statistics/multiple_testing/>
