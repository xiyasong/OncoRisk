# OncoRisk Help Documentation
Welcome to the official documentation for OncoRisk, an integrative precision oncology platform designed to bridge precision oncogenic databases and pan-cancer cohorts for translational research.

## 1. Introduction
OncoRisk unifies curated oncogenic knowledge with large-scale cohort data (TCGA, DepMap) to provide actionable insights for researchers and clinicians.

**Key Vision**: Streamlining tumor profiling and accelerating discovery in translational oncology.

**Theme Settings**: Users can toggle between Light and Dark modes via the settings page.

## 2. Core Modules
### 2.1 Knowledge Navigation & Search
The platform integrates nine categories of oncogenic terms sourced from the CIViC Public API, cached locally for high performance.

**Side Panel Navigation**: A two-step navigation system. Click a category to expand the list, then select an item to view detailed clinical records.

**Integrated Data**: Displays information from CIViC, ClinVar, and OncoKB, including variant alternative names and clinical associations.

**Quick Search**: Use the top search box for genes (e.g., BRAF) or fusions. Use bottom filters to narrow search results by category.

### 2.2 Network Tools
Visualize complex relationships between genes, variants, and therapies.

**Interactive Queries**: Supports single or multi-term queries (e.g., searching Afatinib and EGFR simultaneously).

**Visual Mapping**: Nodes are color-coded by ontological category.

**Customization**: Use the bottom-right panel to hide features or focus on specific interaction nodes.

### 2.3 Deep Query Module
Go beyond existing records by analyzing novel variants through our in-house annotation pipeline.

**Structural Analysis**: Automatically retrieves protein complexes to visualize the spatial proximity of mutants and drug-binding sites.

**Disease Ontology**: Explore disease relationships using a "family tree" view (e.g., Lung Non-Small Cell Carcinoma subtypes).

**Clinical Trials**: Access linked targeted therapies, evidence levels, and direct links to official recruiting clinical trials.

**VEP Annotation**: Full Variant Effect Predictor (VEP) details are provided at the bottom of the result page.

### 2.4 Oncogenic Reporting System
A streamlined pipeline for individual sequencing data analysis.

**Input**: Supports direct upload of somatic VCF files containing thousands of mutations.

**Triage & Tiering**: Mutations are categorized into Tiers 1–4 based on clinical significance.

**Outputs**:
- Live PDF preview of the clinical report.
- Downloadable PDF reports and JSON outputs for downstream integration.

### 2.5 MAF Tools (Cohort Analysis)
For efficient cohort-level mutation visualization and statistical analysis.

**Integrated Resources**: Includes 33 TCGA cancer cohorts and 2,427 DepMap cell line profiles.

**Custom Uploads**: Users can upload their own .maf files.

**Visualization Modules**:
- **Cohort Level**: Oncoplots, mutation load comparisons, and landscape overviews.
- **Gene/Sample Level**: Lollipop plots, rainfall plots, and VAF distributions.

**Statistical Modules**: Includes 11 analytical tools (adapted from the maftools R package) covering:
- TMB Calculation, Somatic Interactions, Cancer Driver Genes, Survival Analysis, Mutational Signatures, and Drug-Gene Interactions.

### 2.6 Pan-Cancer Visual
Explore variant and gene prevalence across seven major pan-cancer cohorts.

**Single Variant Query**: Analyze mutation frequency, mean/median VAF, and distribution across cancer types.

**Gene Analysis**: Identify and visualize the most frequently mutated genes using bar plots and heatmaps.

## 3. Technical References
For advanced users looking for detailed parameter descriptions in the Statistical Analysis module, please refer to:
- [maftools R Package Documentation](https://bioconductor.org/packages/release/bioc/html/maftools.html)
- Our supplementary documentation files.

## 4. Summary
OncoRisk empowers the oncology community by transforming complex genomic data into structured, visual, and actionable knowledge.