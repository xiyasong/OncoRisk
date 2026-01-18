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

## Knowledge Base Search Function
The OncoRisk Knowledge Base integrates a multi-layered search system that enables researchers to efficiently discover and explore genomic, clinical, and therapeutic information.

### Overview
The Knowledge Base contains over 11,000 evidence items, 4,000+ molecular profiles, 3,890 genomic variants, 578 therapies, 435 diseases, and 169 clinical assertions—all searchable through integrated search interfaces.

### Search Methods
**1. Quick Search (Global Search)**
The Quick Search bar at the top of every page provides rapid cross-entity searching:

*   **Location**: Top navigation bar (labeled "Quick Search...")
*   **Function**: Instantly searches across all Knowledge Base entity types.
*   **Autocomplete**: Returns real-time suggestions as you type, categorized by entity type.
*   **Result Types**: Shows matching therapies, molecular profiles, diseases, variants, and features with color-coded icons.
*   **Example**: Typing "EGFR" returns results such as Anti-EGFR Monoclonal Antibody (Therapy), BRAF V600E AND EGFR L858R AND EGFR T790M (Molecular Profile), and more.

**2. Data Explorer Search (Entity-Specific)**
Each Knowledge Base section features a dedicated Data Explorer with column-based filtering and searching:

*   **Assertions Section**: Search by Name, Molecular Profile, Disease, Therapies, Summary, Type, Direction, Significance, and Evidence.
*   **Variants Section**: Filter by Name, Feature ID, Aliases, Associated Diseases, Therapies, Profiles, and Groups.
*   **Diseases Section**: Search by Name, DOID, Aliases, and view associated Evidence Items and Assertions.
*   **Therapies Section**: Search by Name, NCIT ID, Aliases, and view associated Evidence and Assertions.
*   **Evidence Section**: Filter by Name, Profile, Disease, Therapies, Description, Type, Direction, and Significance.
*   **Molecular Profiles Section**: Search by Name, Aliases, Variants, and view associated Assertions and Diseases.

**3. Column Filtering**
Within each Data Explorer view, individual column headers include search/filter textboxes. Searches are case-insensitive and support partial matching.

**4. Pagination and Load Controls**
Large result sets are paginated, and a "Load 20 more" button allows for efficient browsing.

### Search Workflow Example
**Scenario: Find therapeutic options for EGFR-mutant lung cancer**
1.  **Quick Search**: Type "EGFR L858R".
2.  **Navigate to Variants**: Click the Variants section in the left sidebar.
3.  **Filter by Name**: Search "EGFR L858R" in the Name column.
4.  **Review Results**: See associated diseases (Lung Non-small cell), therapies (Gefitinib, Afatinib), and molecular profiles.
5.  **Deep Dive**: Click on an assertion link to see evidence and tier levels.

### Key Features
*   **Cross-Linked Entities**: Each result links to related variants, diseases, therapies, and evidence.
*   **Evidence Attribution**: All assertions backed by evidence levels.
*   **Standardized IDs**: Uses HGNC, DOID, and NCIT IDs.
*   **Batch Filtering**: Multiple column searches combine with AND logic.

### Integration with Analysis Tools
Search results can be exported to:
*   **Deep Query**: Construct complex queries.
*   **Network Tools**: Visualize relationships among search results.
*   **Pipeline Analysis**: Use variant/disease filters to subset genomic datasets.

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