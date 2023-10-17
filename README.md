# human_patchseq_gaba
Code for reproducing the analyses presented in [Signature morpho-electric properties of diverse GABAergic interneurons in the human neocortex]((https://www.science.org/doi/full/10.1126/science.adf6484).  It includes the following files:

* **complete_patchseq_data_sets[1/2].Rdata** - These are R objects that (together) have **all of the gene expression data** and relevant cell metadata used for analysis.  *These files must be merged before use, as described in "scripts_gene_expression".*
* **vgic_genes.csv** - This is a manually curated table of voltage-gated ion channels. 
* **dbc_calb1_ADGRG6.csv** - This is the set of cells in the paper that map to Inh L1-3 SST CALB1 or Inh L3-5 SST ADGRG6 along with a call of whether or not they have double bouquet cell morphology.
* **acute.culture.locked_sstcalb1.ephys.csv** - A set of electrophyisological properties for all patch-seq cells in this study that were mapped to the "Inh L1-3 SST CALB1" cluster.   
* **cell_morphology_predictions_CALB1.csv** - A table of morphologies and predicted morphologies for the same cells mapped to the "Inh L1-3 SST CALB1" cluster.  

## Data

Most of the data for this manuscript are located in the "data" folder above.  In addition you will need to download some larger data files from the [Allen Brain Map](https://portal.brain-map.org/atlases-and-data/rnaseq), as described in the relevant scripts.  Additional project information and links to raw data are included [in the paper](https://www.biorxiv.org/content/10.1101/2022.11.08.515739v1).

## Scripts

Scripts for reproducing most of the analyses presented in this paper are available in the "scripts_**" folders above, which are described in the README for the relevant folders.

## License

The license for this package is available on Github at: https://github.com/AllenInstitute/human_patchseq_gaba/blob/master/LICENSE

## Level of Support

This code will be updated only if figures change during review or if corrections need to be made.  

## Contribution Agreement

If you contribute code to this repository through pull requests or other mechanisms, you are subject to the Allen Institute Contribution Agreement, which is available in full at: https://github.com/AllenInstitute/human_patchseq_gaba/blob/master/CONTRIBUTION
