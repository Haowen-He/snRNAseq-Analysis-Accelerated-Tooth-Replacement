# snRNA-Accelerated-Tooth
## Single cell RNA-seq analysis of cichlid dental apparatus to model embryonic cell fate specification and map cellular and molecular events governing the lifelong tooth replacement in cichlids

## contents
- ./analysis/
  Analysis scripts.
  - **00_QC.R** computes basic quality control values for the scRNA-seq dataset.
  - **01_ClusterAllCells.R** performs normalization and high-level clustering of the cells, according to general standards the Seurat pipeline.
  - **02_SubclusterNeurons.R** selects neuronal clusters and subclusters GABAergic and glutamatergic cell types.
  - **03_BulkSequencingAnalysis.R** performs the DeSEQ2 pipeline for our bulk sequencing dataset, so that we identify DEGs for different pallial regions.
  - **04_BulkCorrelationAnalysis.R** correlates the pallial regions and the neuronal cell types to establish potential regions of origion for the single cell types.
  - **05_GeneFamilyAnalysis.R** calculates the expression of genes belonging to different gene families within our identified cell types.
  - **06_GeneInformationContent.R** performs a Random Forest analysis with which we assess how informative different gene families are to retrieve the cell type structure of the dataset.
  - **07_NeuromodulatoryNetworks.R** computes expression thresholds for GPCRs, calculates graph structures of distinct neuromodulatory networks, and performs dimensionality reduction on the neuromodulation-associated gene expression dataset.
  - **08_SAMapConservedGenes.R** takes the output of the SAMap pipeline to extract conserved GPCRs and transcription factors.
  - **09_MuSiC.R** uses the [MuSiC](https://xuranw.github.io/MuSiC/articles/MuSiC.html) package to deconvolve contributions of single cell types to the four pallial regions from which we have obtained bulk sequencing data.
  - **py_01_SAMap_Visualization_pv_dr.ipynb** is an ipython notebook that visualizes the output of the SAMap script (cell type homologies). 
- ./data/
  Additional files necessary for analysis.

## data availability
  Data can be downloaded as indicated in the manuscript and from the SRA depository linked with the BioProject .
  For easier access, processed .rds files for the entire dataset or the neuronal cell types can be accessed via [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.10210550.svg)](https://doi.org/10.5281/zenodo.10210550)
