# Mermaid example: scRNA-seq pipeline (code → diagram)

```mermaid
flowchart TD
  A[Raw FASTQ] --> B[QC: FastQC / MultiQC]
  B --> C[Adapter & Quality Trimming]
  C --> D[Alignment or Mapping<br/>(STAR / Cell Ranger / Salmon-Alevin)]
  D --> E[UMI Processing & Counting]
  E --> F[Gene x Cell Count Matrix]
  F --> G[Cell QC Filters<br/>(low genes, high mito, doublets)]
  G --> H[Normalization & Scaling]
  H --> I[Batch Correction / Integration<br/>(Harmony / Seurat / Scanpy)]
  I --> J[Dimensionality Reduction<br/>(PCA → UMAP/t-SNE)]
  J --> K[Clustering]
  K --> L[Marker Genes & Cell Type Annotation]
  L --> M[Downstream Analyses<br/>(DE, trajectories, cell-cell comms)]
  M --> N[Figures + Reproducible Report]