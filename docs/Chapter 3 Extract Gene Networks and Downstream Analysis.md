# Extract Gene Networks and Downstream Analysis- GSEA
## Introduction:

High-throughput experimental measures such as those obtained from sequencing data can result in a long list of genes that are difficult to interpret in their original form. Gene set enrichment analyses are therefore a means to extract meaningful, potentially biologically interesting pathways from the data. Gene-sets are therefore usually a list of genes with shared attributes, such as membership of the same biological pathway or process. Such gene-sets can be obtained from curated databases, such as Kyto Encyclopaedia of Genes and Genomes (KEGG) and Gene Ontology (GO).

Gene set enrichment analysis is therefore a good way to label the resulting sub-networks to give biological meaning to them.

## Learning Outcomes:

- Understand what gene set enrichment is and how it can be useful.
- Apply the acquired knowledge and carry out pathway based gene set enrichment analysis on resulting sub-networks.

## Pathway Gene Set Enrichment Analysis:
Enrichment scores can be calculated to determine whether specific gene sets are overrepresented in a given gene list compared to what would be expected by chance. A common method for this calculation is the Fisher Exact Test. This is a proportion test that assumes a binomial distribution and independence for probability of any gene belonging to any set. This test calculates the probability of observing the overlap between the input gene list and a particular gene set by chance, given the total number of genes in the dataset and the size of the gene set. It considers the number of genes in the input list that are also present in the gene set, as well as the total number of genes in the input list and the gene set. The resulting p-value indicates significance of the overlap, with lower p-values suggesting stronger evidence of enrichment. 

Once the p-values have been calculated, a multiple testing correction method such as the false discovery rate needs to be implemented to account for the inflation of false positives due to multiple hypothesis testing. The corrected p-values are then used to assess the significance of enrichment, with lower corrected p-values indicating stronger evidence of enrichment.

## Resources:


