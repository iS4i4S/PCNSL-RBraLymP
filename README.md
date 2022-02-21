# PCNSL-RBraLymP

## Graphical abstract
![alt text](https://github.com/iS4i4S/Landscape-AICDA-mutations/blob/main/Data/Pan-cancer%20landscape%20of%20AID%20mutations.jpeg "Hi there!")

## Abstract
Primary central nervous system lymphoma (PCNSL) is a rare and distinct entity within diffuse large B cell lymphoma located in the central nervous system with a less favorable prognosis, variable response to treatment, and outcome despite homogenous pathological presentation. Here, we report a multi-omic analysis of 147 PCNSL from fresh-frozen (FF) tumor tissue from immunocompetent, treatment naïve patients that comprises mutations, copy-number alterations (CNA), fusions, gene expression, TCR/BCR clonotypes, tumor microenvironment (TME), methylation, tumor localization, and clinical data to identify molecular subtypes of PCNSL with clinically distinct behaviors. These results were validated in an independent series of 93 PCNSL formalin-fixed, paraffin-embedded (FFPE) samples. Our results generated an explanatory bridge between the different multi-omic layers and ultimately potential therapeutic targets across subtypes. Here, we present RBraLymP (RNA-based Brain Lymphoma Profiler), a diagnostic algorithm that takes gene expression data from either FFPE or FF tissue for identifying the PCNSL molecular subtypes associated with multi-omic features.

## Citation
If you use any data or code derived from this study, please cite:
Hernandez-Verdin, I. et al. Molecular and clinical diversity in primary central nervous system lymphoma. (DOI and journal pending...)

## Instructions (software requirements)
...

## The RBraLymP (RNA-based Brain Lymphoma Profiler) algorithm
The current code takes an RNA expression matrix (gene names as rows; samples as columns) as input from either FFPE (DegNorm normalization of reads is highly recommended, see [Supplementary Appendix](link) from our article for more information) or FF tissue. The output is a two column matrix with the "Sample ID" and the "Cluster significant [CS] group". Downstream analysis for evaluating clinical impact using univariate-multivariate models is also given.

[Complete tutorial for RBraLymP is avaliable here](Insert_link)

## Data avaliability
Raw WES, RNA-seq, DNA methylation, and clinical data that support the findings of this study have been deposited at the European Genome-phenome Archive (EGA) under accession number [EGAS...pending](insert link). 

## Contact
E-mail any questions to [isaias.hernandez@icm-institute.org].

