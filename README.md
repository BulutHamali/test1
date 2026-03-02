# Mermaid example: scRNA-seq pipeline (code → diagram)

```mermaid
flowchart TD
  A[Raw FASTQ] --> B[QC FastQC MultiQC]
  B --> C[Trim adapters and low quality]
  C --> D[Mapping STAR CellRanger Alevin]
  D --> E[UMI processing and counting]
  E --> F[Gene by cell count matrix]
  F --> G[Cell QC filters mito percent genes doublets]
  G --> H[Normalize and scale]
  H --> I[Batch correction integration]
  I --> J[Dimensionality reduction PCA UMAP]
  J --> K[Clustering]
  K --> L[Marker genes and annotation]
  L --> M[Downstream DE trajectory cell cell]
  M --> N[Figures and reproducible report]