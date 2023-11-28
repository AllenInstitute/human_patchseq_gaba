Raw (NWB2) electrophysiology data files are stored at DANDI (https://dandiarchive.org/dandiset/000636).

Additionally, this folder contains all files required for reproducing the analyses in [Signature morpho-electric properties of diverse GABAergic interneurons in the human neocortex][(https://www.biorxiv.org/content/10.1101/2022.11.08.515739v1)](https://www.science.org/doi/epdf/10.1126/science.adf6484).  It includes the following files:

* **complete_patchseq_data_sets[1/2].Rdata** - These are R objects that (together) have **all of the gene expression data** and relevant cell metadata used for analysis.  *These files must be merged before use, as described in "scripts_gene_expression".*
* **vgic_genes.csv** - This is a manually curated table of voltage-gated ion channels. 
* **dbc_calb1_ADGRG6.csv** - This is the set of cells in the paper that map to Inh L1-3 SST CALB1 or Inh L3-5 SST ADGRG6 along with a call of whether or not they have double bouquet cell morphology.
* **acute.culture.locked_sstcalb1.ephys.csv** - A set of electrophyisological properties for all patch-seq cells in this study that were mapped to the "Inh L1-3 SST CALB1" cluster.   
* **cell_morphology_predictions_CALB1.csv** - A table of morphologies and predicted morphologies for the same cells mapped to the "Inh L1-3 SST CALB1" cluster.  
