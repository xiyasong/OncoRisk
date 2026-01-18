# Network Tools Tutorial

Network Tools in OncoRisk is an analysis module for building and visualizing biological and clinical networks derived from the knowledge base (variants, genes, diseases, therapies, phenotypes) to support interpretation and hypothesis generation.

## What Network Tools is for
*   Visualizing relationships between entities such as genes, variants, diseases, therapies, and phenotypes as graphs rather than tables.
*   Exploring connectivity patterns (e.g., which genes link multiple diseases, which therapies target overlapping molecular profiles).
*   Supporting interpretation of analysis results from Pipeline Analysis or Deep Query by placing findings into a network context.

## Accessing Network Tools
In the left navigation under **Analysis Tools**, click **Network Tools**. Network Tools runs inside the OncoRisk application, so you reach it only after logging into the Phenome Portal and choosing the OncoRisk project.

## Typical Inputs and Entity Types
Network Tools operates on the main OncoRisk entity classes and their relationships.

### Node types typically include:
*   **Variants**: Genomic variants cataloged in the knowledge base.
*   **Molecular profiles**: Combinations of features, such as variant sets.
*   **Genes/features**: From the Features section.
*   **Diseases**: Oncology diagnoses.
*   **Therapies**: Drugs/regimens.
*   **Phenotypes**: Clinical descriptors linked to samples or diseases.

### Edge types represent curated or derived relationships, such as:
*   Variant–gene (a variant is in a gene).
*   Variant/profile–disease (association or assertion).
*   Disease–therapy (therapeutic relevance).
*   Variant/profile–phenotype (associated phenotypic effect).
*   Evidence/assertions that support a link.

### Inputs are normally either:
*   A result or subset from Deep Query (e.g., selected variants, diseases, therapies).
*   A specific entity (e.g., a single disease or profile) with “neighbors” expanded.
*   A saved analysis or cohort from Pipeline Analysis.

## Core Workflow in Network Tools
A detailed network-analysis session typically follows these steps.

1.  **Open Network Tools**
    *   Select **Network Tools** from the **Analysis Tools** menu.
    *   Start from a clean canvas or load a previously saved network.

2.  **Define the seed set**
    *   Choose a starting entity or entity set, for example:
        *   All variants from a pipeline run.
        *   A disease of interest (e.g., a specific cancer subtype).
        *   A therapy or molecular profile.
    *   Many deployments allow you to push a Deep Query result directly into Network Tools (e.g., “Send to Network” / “Visualize in Network Tools”).

3.  **Configure node and edge types**
    *   Select which node classes to include: genes, variants, diseases, therapies, phenotypes, profiles.
    *   Select which relationships (edges) to show, for example:
        *   Only clinically supported assertions.
        *   All evidence-based associations (possibly including lower-confidence links).
    *   Optionally restrict to a subset (e.g., only pathogenic variants, only specific tumor types).

4.  **Generate and layout the network**
    *   Run the network construction to generate the graph from the knowledge base for the chosen seed and relationship set.
    *   Apply a layout algorithm (force-directed, circular, or hierarchical) to position nodes clearly.
    *   Use zoom and pan to focus on regions of interest.

5.  **Filter and style the network**
    *   Apply filters, such as:
        *   Minimum evidence/support level for edges.
        *   Node type visibility (e.g., hide phenotypes, show only diseases and variants).
        *   Frequency or prevalence thresholds (e.g., variants appearing in multiple profiles).
    *   Adjust visual mappings:
        *   Color by node type (gene vs disease vs therapy).
        *   Node size by degree (connectivity) or evidence strength.
        *   Edge thickness by number of supporting evidence items.

6.  **Inspect individual nodes and edges**
    *   Click a node (e.g., a variant or disease) to open a side panel or popup showing:
        *   Basic metadata: ID, name, functional annotation.
        *   Linked molecular profiles, diseases, therapies, phenotypes.
        *   Counts of supporting evidence and assertions, with shortcuts to Knowledge Base pages.
    *   Click edges to see the relationship explanation:
        *   Associated assertion(s) and evidence items.
        *   Links back to source publications or datasets.

7.  **Expand or contract the network**
    *   Use “expand neighbors” functions to add additional related nodes.
    *   Collapse or hide nodes to reduce clutter.
    *   Save a view or snapshot.

8.  **Export or handoff**
    *   Export the network as an image or a graph file.
    *   Move back to Deep Query or Knowledge Base entity pages to investigate specific findings.

## Practical Use Cases
*   Identifying hub genes or variants that connect multiple tumor types or phenotypes.
*   Mapping therapies to a patient’s variant profile via disease and profile nodes.
*   Discovering potential repurposing opportunities where a therapy is linked to related profiles across diseases.
*   Visualizing phenotype clusters associated with particular genomic features.
