Prostate Cancer TWAS in OncoArray GWAS Meta-analysis
====================================================

The repository contains the main results for the transcriptome-wide association study (TWAS) reported in

*Large-scale transcriptome-wide association study identifies new prostate cancer risk regions*,
Nicholas Mancuso, Simon Gayther, Alexander Gusev, Wei Zheng, Kathryn L. Penney, the PRACTICAL consortium, CRUK, BPC3,
CAPS, PEGASUS, Zsofia Kote-Jarai, Rosalind Eeles, Matthew Freedman, Christopher Haiman, Bogdan Pasaniuc. [bioRxiv 345736; doi: https://doi.org/10.1101/345736](https://www.biorxiv.org/content/early/2018/06/14/345736)

Results
-------
`ONCOARRAY.TWAS.txt` contains the main TWAS association statistics.

| Column | Description |
|--------|-------------|
| `S.NAME` | Short description of the gene expression reference panel |
| `G.ID` | Canonical gene name |
| `ID` | Canonical gene name (for total expression) or exon/exon junction (for splice variant) |
| `CHR` | Chromosome |
| `P0` | Transcription start site |
| `P1` | Transcription end site |
| `HSQ` | SNP-hertiability explained by cis-SNPs in reference panel |
| `BEST.GWAS.ID` | SNP ID of the best GWAS SNP in the prediction model (i.e. smallest p-value) |
| `BEST.GWAS.Z` | Z-score of the best GWAS SNP |
| `EQTL.ID` | SNP ID of the  best cis-eQTL SNP in the reference panel |
| `EQTL.R2` | Variance-explained in measured gene expression by best cis-eQTL SNP |
| `EQTL.Z` | Z-score of the best cis-eQTL SNP |
| `EQTL.GWAS.Z` | GWAS Z-score of the best cis-eQTL SNP |
| `NSNP` | Number of SNPs in the model |
| `NWGT` | Number of SNPs with non-zero weights in the model |
| `MODEL` | Model with the best prediction accuracy |
| `MODELCV.R2` | Adjusted estimate of variance-explained in measured gene expression using 5-fold CV |
| `MODELCV.PV` | P-value of cross-validation R2 estimate |
| `TWAS.Z` | Z-score for TWAS test of association |
| `TWAS.P` | P-value for TWAS test |
| `PERM.PV` | Permutation test P-value for TWAS |
| `PERM.N` | Number of permutations performed |
| `PERM.ANL_PV` | Analytic P-value determined by re-adjusting Z-score by stdev estimate from permutations |


`ONCOARRAY.FINEMAP.txt` contains the secondary gene-based fine-mapping analysis over TWAS associations.

| Column | Description |
|--------|-------------|
| `S.NAME` | Short description of the gene expression reference panel |
| `G.ID` | Canonical gene name |
| `ID` | Canonical gene name (for total expression) or exon/exon junction (for splice variant) |
| `CHR` | Chromosome |
| `P0` | Transcription start site |
| `P1` | Transcription end site |
| `BLOCK` | Identifier for a risk region |
| `TWAS.Z` | Z-score for TWAS test of association |
| `BF` | Bayes-Factor of association |
| `PIP` | Marginal posterior probability for explaining observed association signal at BLOCK |

Software and support
--------------------
For performing TWAS using summary-data, computing expression weights using custom expression panels,
and additional post-TWAS analyses please see [FUSION](http://github.com/gusevlab/fusion_twas).

If you have any questions or comments please contact nmancuso@mednet.ucla.edu
