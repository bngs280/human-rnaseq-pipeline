# RNA-seq Analysis Pipeline (STAR + DESeq2)

![STAR](https://img.shields.io/badge/STAR-2.7.10a-blue)
![DESeq2](https://img.shields.io/badge/DESeq2-1.38.3-red)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A comprehensive Nextflow pipeline for human RNA-seq data analysis, from raw FASTQs to pathway visualization.

## Key Features
- **Alignment**: STAR with GENCODE v44 annotations
- **Quantification**: FeatureCounts → DESeq2 normalization
- **Visualization**:
  - Interactive volcano plots (Plotly)
  - Heatmaps with hierarchical clustering
- **Pathway Analysis**:
  - KEGG/GO enrichment (clusterProfiler)
  - GSEA preranked analysis

## Quick Start
```bash
nextflow run rna-seq-star-deseq2/main.nf \
  --input samplesheet.csv \
  --gtf Homo_sapiens.GRCh38.104.gtf \
  --outdir results \
  -profile docker
