# MouseContamEstimator

## Introduction

  **MouseContamEstimator** is a simple python script for end users to estimate mouse contamination level of their WES samples.
  Based on the HAMAlist, it calculates the median of VAFs for all HAMAs in your WES data.<br>
  ###### The only library dependency for this script is NumPy.<br>
  
  [**Download current version**](https://github.com/ShockYoung/MouseContamEstimator/releases/latest)
  
## Usage

  `MouseContamEstimator` takes **_tsv_** formatted output of `GATK CollectAllelicCounts` as input.<br>
  Therefore, in order to perform the estimation, the result file of CollectAllelicCounts should be generated as follows.
  ```
  gatk CollectAllelicCounts \
    -I $AlignedPath$SAMPLE.bam \
    -R $REF \
    -L $INTERVAL \
    -O $AnalysisPath$SAMPLE.allelicCounts.tsv
  ```
  The usage of `MouseContamEstimator` is simple as follows.
  ```
  python MouseContamEstimator $AnalysisPath$SAMPLE.allelicCounts.tsv
  ```
  
## Reference

  *Under revision.*
