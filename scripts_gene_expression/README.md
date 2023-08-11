# Overview

To replicate the analyses and associated figures in the paper associated with gene expression, please run the scripts below in order and in a specific R environment. 

## Running R scripts

Prior to running the scripts, make sure that all of the files in the "data" directory are saved to your current working directory (not to a subfolder called "data"). Note that the files "complete_patchseq_data_sets[1/2].RData" **must be merged** before running Code 3, as follows:
```
load("complete_patchseq_data_sets1.RData")
load("complete_patchseq_data_sets2.RData")
datPatch <- cbind(datPatch1,datPatch2)
save(datPatch,annoPatch,metaPatch,file="complete_patchseq_data_sets.RData")
```

The first two scripts link out a the [patchseq_human_L23 GitHub repo](https://github.com/AllenInstitute/patchseq_human_L23) since the same starting files are used for defining the FACS cells.  The third script contains all of the analyses for this paper.

1. **Code 1. Download and prepare the dissociation data** [(LINK TO SCRIPT)](http://htmlpreview.github.io/?https://github.com/AllenInstitute/patchseq_human_L23/blob/master/scripts/Code1_prepareComparisonDataSets.nb.html)  This script converts RNA-seq data downloaded from the [Allen Institute Cell Types Database](http://celltypes.brain-map.org/rnaseq) into a format compatible for use as comparison data to human and mouse Patch-seq.  
2. **Code 2. Complete preparation for dissociation and Patch-seq data** [(LINK TO SCRIPT)](http://htmlpreview.github.io/?https://github.com/AllenInstitute/patchseq_human_L23/blob/master/scripts/Code2_prepare_data_L23exc.nb.html).  This script prepares the data for comparing mouse VISp and ALM to human MTG using dissociated and Patch-seq in superficial cortical layers, and outputs the results as R objects for remaining R scripts, **and outputs feather files for python scripts**.  
3. **Code 3. GABAergic types in cortex for acute and cultured cells** [(LINK TO SCRIPT)](http://htmlpreview.github.io/?https://github.com/AllenInstitute/human_patchseq_gaba/blob/master/scripts_gene_expression/acute_vs_culture_comparisons_update.nb.html).  This script performs the statistical analyses and makes plots for most of the gene expression components of the paper, and also defines some additioanl cell metadata about immune signatures.  More specifically, it (1) identifies immune signatures for the patch-seq data, (2) finds genes associated with this signature and with acute vs. culture preparations, (3) defines and integrated space for all patch-seq and FACS data to better visualize different GABAergic cell types and show that the immune and acute/culture signatures do not preclude accurate cell type assignments, (4) compares cell type abundances across conditions, (5) performs a series of quality control tests on the data, (6) attempts to find genes specific to double bouquet cells, and (7) compares morphology, electrophysiology, and transcriptomics of L1-3 SST CALB1 cells and attempts to predict morphology of these cells based on other modalities.

## Defining the R environment

All R code was run in Windows in a very specific environment.  **If a different environment is used, you may get different results.**  For example, the layouts of the various UMAP plots shown will likely be different, and in some cases the resolution of cluster steps may need to be adjusted slightly to ensure the same number of clusters are identified.  Finally, different versions of Seurat produce very different sets of differentially expressed genes.  With all of that said, there are no differences in the overall scientific results presented in the manuscript for scripts run in different environments.

This analysis was run with R v4.1.1 on Windows 10 x64, and used the package versions listed in the sessionInfo() at the end of the Code 3 script above.  To recreate this environment, perform the following steps:
1. Download the files in the "rang" folder.  This includes a Docker
2. Install the [R 4.1.1 from the previous releases page](https://cran.r-project.org/bin/windows/base/old/4.1.1/). While I ran the scripts on Windows, you *might* get the same results if you run them on UNIX.
3. Install the all the necessary R libraries by following the "README" in the "rang" folder.  This was generated using the "resolve" and "dockerize" functions in the [rang R library](https://github.com/chainsawriot/rang), which allowed me to reconstuct a of R from snapshot_date = "2021-10-10".