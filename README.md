Principal component analysis (PCA)
Three on NCBI Gene Expression Omnibus (GEO) publicly available transcriptomics data sets generated by our group were combined to study the effect of aging and infection on intestinal epithelial cells. The datasets comprised the following samples (isolated intestinal epithelial cells only): (i) Gene expression data from 3- and 21-day old healthy SPF (specific pathogen-free) mice (GSE35596), (ii) Gene expression data from 28-day old mice, comparing germ-free (GF) and specific pathogen-free conditions (GSE35597), and (iii) gene expression data from 5-day old controls, wildtype Salmonella Typhimurium-infected, and Spi1-deficient Salmonella Typhimurium-infected mice (GSE51160). Raw data were downloaded, sample names were annotated, and corresponding data were pre-processed utilizing the limma package version 3.52.2 (Ritchie et al. 2015). For all three datasets, background correction was performed. Thereafter, GSE35596 and GSE35597 were merged and normalized utilizing between- and within-array-normalization methods (Oshlack et al. 2007). For GSE51160, only between array normalization was performed, due to the single-color design (Oshlack et al. 2007). All three datasets were merged and gene values, not present in all three datasets, excluded. GF samples and one outlier sample from the first data set were excluded from further analysis as well. Metadata for each sample were added. For simplification, samples from three and 5 day old mice were named neonate, 21 and 28 day olds were termed “adult” Then, ComBat batch correction was performed (Johnson, Li, and Rabinovic 2007). Principal Component Analysis (PCA), using the built-in R function prcomp() was executed and PC1 was plotted against PC2 utilizing ggplot2 package version 3.4.0 (Wickham 2016). 95% confident ellipses were added to PCA plot. The code will be made available on GitHub (https://github.com/laurarobrahn/AgingPCA).





References:
Johnson, W. Evan, Cheng Li, and Ariel Rabinovic. 2007. “Adjusting Batch Effects in Microarray Expression Data Using Empirical Bayes Methods.” Biostatistics (Oxford, England) 8 (1): 118–27. https://doi.org/10.1093/BIOSTATISTICS/KXJ037.
Oshlack, Alicia, Dianne Emslie, Lynn M. Corcoran, and Gordon K. Smyth. 2007. “Normalization of Boutique Two-Color Microarrays with a High Proportion of Differentially Expressed Probes.” Genome Biology 8 (1): 1–8. https://doi.org/10.1186/GB-2007-8-1-R2/FIGURES/5.
Ritchie, Matthew E., Belinda Phipson, Di Wu, Yifang Hu, Charity W. Law, Wei Shi, and Gordon K. Smyth. 2015. “Limma Powers Differential Expression Analyses for RNA-Sequencing and Microarray Studies.” Nucleic Acids Research 43 (7): e47. https://doi.org/10.1093/nar/gkv007.
Wickham, Hadley. 2016. ggplot2: Elegant Graphics for Data Analysis. Springer-Verlag New York. ISBN 978-3-319-24277-4, https://ggplot2.tidyverse.org. https://doi.org/10.1007/978-3-319-24277-4.
