# pathExplore

This repository contains code used to perform analysis for the pathExplore paper.

## Requirements

- Snakemake
- Conda (optionally with mamba installed for faster environment creation)
- Cytoscape (must be running)
  - EnrichmentMap
  - AutoAnnotate

## How to run

In order to perform all analyses, run

```shell
snakemake --cores 1 --use-conda --conda-frontend mamba
```

## Quality and performance assessment

We have obtained `N` datasets containing various gene set enrichment results from previous analyses
we have performed (code not provided). In each dataset, we used 1000 most significant pathways. For
each gene set enrichment analysis, we used either clusterProfiler or the GSEA software. The results
and the datasets can be found in the `data` directory and are shortly described below:

1. `dataset1.RDS`: GSEA analysis of RNAseq data of persons with Alzheimer's disease (comparing AD and Controls).
    Performed using clusterProfiler.
2. `dataset2.RDS`: GSEA analysis of RNAseq data of persons with Alzheimer's disease (comparing AD and Controls).
    Performed using the GSEA software.
