# DNA-methylation-Epigenica-vs-Illumina-EPIC-Array

This GitHub page has the R and bash code for the analysis done to compare the DNA methylation technologies, EPigenica EpiFinder GenomePro, and Illumina MethylationEPIC array. 

The data used is from 4 healthy blood donors. 

The pre-processing of the data was done using the MIUNTE pipeline and Deeptools (via conda) for the EpiFinder data. BigWig files were used for downstream analysis.

The array data used was from the study Epigenetic rewiring of pathways related to odour perception in immune cells exposed to SARS-CoV-2 in vivo and in vitro, published in 2022. The array data starts with the IDAT files.

The code contains the following:
- CpG site analysis
  - M value analysis with no normalization and filtering
  - - Overlaying histogram 
  - - Spearman ranked corelation
  - M value analysis with Quantile normalization
    - - Overlaying histogram
      - Spearman ranked corelation
      - Bland-Altman plot
  - Beta value calculation
  - Active TB analysis
  - - Delta beta calculation
    - PCA plot
    - Correlation matrix
    - Box plots for top 7 DMCs
- CpG island analysis
- - Extraction of CpG islands
  - Filtering of CpG islands
  - Normalization of Illumina beta values using Noob
  - Normalization of Epigenica beta values using cyclic loess
  - Histogram of read count vs number of CpG islands - Epigenica data only
  - Beta values analysis
  - - Overlaying histogram for both MBDs - read counts vs beta values
    - 
 
