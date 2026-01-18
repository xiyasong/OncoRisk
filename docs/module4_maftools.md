# Module 4: Server-Maftools

## Overview
Server-Maftools is a web-based Shiny application that integrates the `maftools` R package and `G3viz` visualization package to analyze and visualize MAF (Mutation Annotation Format) files from cancer genomics studies. It enables comprehensive analysis of somatic mutations in TCGA cohorts and user-provided mutation data.

## Main Sections and Features
### 1. Introduction
Entry point providing an overview of the application structure and capabilities. Displays example visualizations showing the complete analysis pipeline.

### 2. Available TCGA Cohorts
Displays a searchable table of all available TCGA cancer studies with:
*   **Study Abbreviation**: Cancer type (ACC, BLCA, BRCA, etc.)
*   **Data Source**: MC3, Firehose, or CCLE
*   **Sample Counts**: Number of samples available for each study

### 3. Load & Analyze
Data ingestion interface with two options:
*   **Load TCGA Cohort Data**: Select from pre-loaded TCGA studies.
*   **Upload My Own MAF File**: Upload custom mutation data files.

### 4. Cohort Visualization
Basic visualization tools for cohort-level mutation analysis:
*   **MAF Summary Plot**: Overall mutation statistics.
*   **Oncoplot**: Visual summary of genes and samples with mutations.
*   **Ti/Tv Analysis**: Transition/Transversion ratio analysis.
*   **TCGA Mutation Load Comparisons**: Compare mutation burdens across studies.
*   **Recurrent Mutation Analysis**: Identify frequently mutated genes.

### 5. Genes/Samples Visualization
Advanced visualization focusing on individual genes and samples:
*   **Lollipop Plots**: Protein-level mutation distribution.
*   **Rainfall Plots**: Identify mutation clusters.
*   **VAF Distribution Plots**: Visualize Variant Allele Frequency.

### 6. Cohort Analysis
Comprehensive analysis modules:
*   **TMB Calculation**: Tumor Mutational Burden quantification.
*   **Somatic Interactions**: Co-mutation patterns between genes.
*   **Cancer Driver Genes**: Identify significantly mutated genes.
*   **Pfam Domains**: Protein domain-level mutation analysis.
*   **Survival Analysis**: Correlate mutations and patient survival.
*   **Mutational Comparison**: Compare mutation patterns across cohorts.
*   **Clinical Enrichment**: Link mutations to clinical phenotypes.
*   **Drug-Gene Interactions**: Connect mutations to therapeutic targets.
*   **Oncogenic Pathways**: Map mutations to signaling pathways.
*   **Tumor Heterogeneity**: Quantify genetic diversity.
*   **Mutation Signatures**: Identify mutational signatures.

## Typical Workflow
1.  Navigate to **Available TCGA Cohorts** to browse studies.
2.  Go to **Load & Analyze** and select a TCGA study or upload your MAF file.
3.  Click **LOAD DATA**.
4.  Use **Cohort Visualization** to explore overall mutation patterns.
5.  Use **Genes/Samples Visualization** for detailed variant inspection.
6.  Access **Cohort Analysis** modules for specialized analyses.

## Data Format Requirements
*   **Input**: MAF files (Mutation Annotation Format) or TCGA study selection.
*   **Output**: Interactive plots, summary statistics, downloadable visualizations.