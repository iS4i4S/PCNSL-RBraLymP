# Molecular and clinical diversity in primary central nervous system lymphoma

## Graphical abstract
![alt text](https://github.com/iS4i4S/PCNSL-RBraLymP/blob/main/Images/Graphical_abstract.jpeg "Hi there!")

## Abstract
Primary central nervous system lymphoma (PCNSL) is a rare and distinct entity within diffuse large B cell lymphoma located in the central nervous system with a less favorable prognosis, variable response to treatment, and outcome despite homogenous pathological presentation. Here, we report a multi-omic analysis of 147 PCNSL from fresh-frozen (FF) tumor tissue from immunocompetent, treatment naïve patients that comprises mutations, copy-number alterations (CNA), fusions, gene expression, TCR/BCR clonotypes, tumor microenvironment (TME), methylation, tumor localization, and clinical data to identify molecular subtypes of PCNSL with clinically distinct behaviors. These results were validated in an independent series of 93 PCNSL formalin-fixed, paraffin-embedded (FFPE) samples. Our results generated an explanatory bridge between the different multi-omic layers and ultimately potential therapeutic targets across subtypes. Here, we present RBraLymP (RNA-based Brain Lymphoma Profiler), a diagnostic algorithm that takes gene expression data from either FFPE or FF tissue for identifying the PCNSL molecular subtypes associated with multi-omic features.

## Citation
If you use any data or code derived from this study, please cite:

Hernandez-Verdin, I. et al. Molecular and clinical diversity in primary central nervous system lymphoma. (DOI and journal pending...)

## Instructions (software requirements)
It is essential that you have R 4.0.1 or above already installed on your computer or server. The main tools needed for RBraLymP are implemented in the R package [MOVICS](https://github.com/xlucpu/MOVICS). For all of the steps of the pipeline to work, make sure that you have upgraded Bioconductor to newest version (BiocManager v3.11). After you have R and Bioconductor installed properly, you can start to install MOVICS and other needed packages by the following code into your R session:

```r
## check for missing required packages, install them
required.packages <- c('data.table','ggplot2','cowplot','RColorBrewer','ggsignif','binom','scales','forestplot','ggpubr','survminer','reshape2','ggrepel','Hmisc','Rcpp','pheatmap','ComplexHeatmap','stats','ggforestplot','rmarkdown','survival')
new.packages <- required.packages[!(required.packages %in% installed.packages()[,"Package"])]
if(length(new.packages)>0) install.packages(new.packages)

## install packages from Bioconductor if not installed
if(!c('DESeq2',"DegNorm" %in% installed.packages()) {
    if (!requireNamespace("BiocManager", quietly = TRUE)) install.packages("BiocManager")
    BiocManager::install(c("DESeq2","DegNorm"))

## install some dependencies for MOVICS from source

#### heatmap.plus
install.packages("heatmap.plus_1.3.tar.gz", repos = NULL, type = "source")

#### SNFtool
devtools::install_github("maxconway/SNFtool")

## install MOVICS
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
if (!require("devtools")) 
    install.packages("devtools")
devtools::install_github("xlucpu/MOVICS")
    
}
 ```

heatmap.plus needs to be downloaded from [source here](https://cran.r-project.org/src/contrib/Archive/heatmap.plus/)

The complete guide for installing MOVICS (may you find troubles) can be found [here](https://xlucpu.github.io/MOVICS/MOVICS-VIGNETTE.html#Section.2)

## The RBraLymP (RNA-based Brain Lymphoma Profiler) algorithm
The current code takes an RNA expression matrix (gene names as rows; samples as columns) as input from either FFPE (DegNorm paraffin degradation correction of reads is highly recommended, see [Supplementary Appendix](link) from our article for more information) or FF tissue. The output is a two column matrix with the "Sample ID" and the "Cluster significant [CS] group". Downstream analysis for evaluating clinical impact using univariate-multivariate models is also given.

[Complete tutorial for RBraLymP is avaliable here](http://htmlpreview.github.io/?https://github.com/iS4i4S/PCNSL-RBraLymP/blob/main/Docs/RBraLymP.html)

## Data avaliability
Raw WES, RNA-seq, DNA methylation, and clinical data that support the findings of this study have been deposited at the European Genome-phenome Archive (EGA) under accession number [EGAS...pending](insert link). 

## Contact
E-mail any questions to [isaias.hernandez@icm-institute.org].

