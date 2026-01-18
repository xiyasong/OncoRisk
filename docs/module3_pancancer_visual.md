# Module 3: Pan-Cancer Visualizer

## Overview
Pan-Cancer-Visual is a specialized Shiny application for cross-cancer analysis and variant exploration across multiple TCGA and other cancer cohorts. It integrates GENIE (Gene Oncology and External Illumination Engine) data for broad variant frequency analysis.

## Main Sections and Features
### 1. Cohort Comparison
Cross-cohort analysis dashboard showing:
*   **Plot 1: Cohort Metrics Overview**:
    *   Cohort Sample Size
    *   Total Mutations
    *   Number of Cancer Types
    *   Mutation Burden Distribution
*   **Cohorts included**: GENIE, MSK-IMPACT, Pan-Cancer (TCGA), PCAWG, TCGA, and others.

### 2. GENIE VAF Overview
Variant Allele Frequency (VAF) analysis panel with:
*   Overall VAF Distribution
*   VAF by Top 20 Mutated Genes

### 3. Single Variant Query
Query interface for investigating specific mutations by:
*   Gene Symbol
*   Protein Change (HGVSp_Short)
*   Genomic Coordinates (Optional)
*   Reference/Alternate Allele
*   HGVSc (cDNA-level notation)

Results display Mutation Frequency Analysis and Variant Frequency by Cancer Type.

### 4. Gene Analysis
Single-gene or cohort-specific analysis:
*   Select Cohort and Cancer Subtype.
*   Lookup gene frequency for a specific gene symbol.
*   **Outputs**:
    *   Top 10 Mutated Genes by Frequency
    *   All Gene Frequencies table
    *   Gene Mutation Frequency Heatmap

## Data Sources
*   GENIE: Georgetown University Initiative on Evidence-based Precision Oncology
*   MSK-CHORD: Memorial Sloan Kettering Cancer Tumor Open Research Database
*   TCGA: The Cancer Genome Atlas
*   PCAWG: Pan-Cancer Analysis of Whole Genomes

## Typical Workflow
1.  Start with **Cohort Comparison** to understand cohort sizes and mutation burdens.
2.  Use **GENIE VAF Overview** to explore overall variant allele frequency patterns.
3.  Go to **Single Variant Query** to search for specific mutations of interest.
4.  Use **Gene Analysis** to explore gene-level mutation frequencies.
5.  Review generated visualizations (heatmaps, bar charts, frequency tables).