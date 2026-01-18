# Module 1: Knowledge Base, Quick Search & Deep Query

This module aggregates major precision oncology knowledge bases, such as CIViC and OncoKB, to support rapid variant queries and the exploration of association networks among oncogenic terms. It also introduces unique features for deep queries, including cancer family trees, terminology association networks representing direct and indirect relationships, and protein–mutant–drug 3D visualizations.

## Knowledge Base Entities
OncoRisk includes a comprehensive knowledge base of curated oncogenic information.

*   **Assertions**: Curated clinical or functional statements linking variants, diseases, and therapies.
*   **Evidence**: Underlying literature or dataset-level support for assertions and profiles.
*   **Molecular Profiles**: Combinations of variants or biomarkers that define molecular subgroups.
*   **Features**: Individual molecular or clinical features used in profiles or analyses.
*   **Variants**: Catalog of genomic variants with annotations and links to diseases and therapies.
*   **Diseases**: Oncology disease entities, often aligned with common ontologies.
*   **Therapies**: Drugs, regimens, or interventions connected to variants and diseases.
*   **Phenotypes**: Clinical or phenotypic descriptors associated with samples, variants, or diseases.
*   **Sources**: Provenance of data (studies, databases, pipelines) used in the knowledge base.

## Deep Query
The Deep Query tool allows for interactive querying of patients, variants, genes, or other entities across the knowledge base.

## Network Tools Tutorial
Network Tools in OncoRisk is an analysis module for building and visualizing biological and clinical networks derived from the knowledge base to support interpretation and hypothesis generation.

### What Network Tools is for
*   Visualizing relationships between entities such as genes, variants, diseases, therapies, and phenotypes as graphs rather than tables.
*   Exploring connectivity patterns (e.g., which genes link multiple diseases, which therapies target overlapping molecular profiles).
*   Supporting interpretation of analysis results from Pipeline Analysis or Deep Query by placing findings into a network context.

### Accessing Network Tools
In the left navigation under **Analysis Tools**, click **Network Tools**.

### Core Workflow in Network Tools
1.  **Open Network Tools**: Select **Network Tools** from the **Analysis Tools** menu.
2.  **Define the seed set**: Choose a starting entity, such as a variant, disease, or therapy. You can often send results from a Deep Query directly to the Network Tools.
3.  **Configure node and edge types**: Select which entities (nodes) and relationships (edges) to include in the network.
4.  **Generate and layout the network**: Run the tool to build the graph and apply a layout algorithm for clarity.
5.  **Filter and style the network**: Apply filters (e.g., by evidence level) and adjust visual styles (e.g., color by entity type).
6.  **Inspect individual nodes and edges**: Click on nodes or edges to see detailed information and links to the knowledge base.
7.  **Expand or contract the network**: Add or hide nodes to explore connections or simplify the view.
8.  **Export or handoff**: Save the network as an image or data file.

### Practical Use Cases
*   Identifying hub genes or variants that connect multiple tumor types.
*   Mapping therapies to a patient’s variant profile.
*   Discovering potential drug repurposing opportunities.
