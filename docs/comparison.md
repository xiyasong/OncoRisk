# Comparison: Server-Maftools vs Pan-Cancer-Visual

| Feature | Server-Maftools | Pan-Cancer-Visual |
|---|---|---|
| **Primary Use** | Individual cohort mutation analysis | Cross-cohort pan-cancer analysis |
| **Data Input** | TCGA + custom MAF uploads | Pre-loaded GENIE, MSK, TCGA data |
| **Analysis Type**| Deep single-cohort analysis | Variant/gene lookup across cohorts |
| **Key Outputs** | Oncoplot, survival curves, pathways | VAF distributions, frequency comparisons |
| **Best For** | Detailed mutation characterization | Pan-cancer variant prevalence |

## Technical Details

### Server-Maftools
*   Built on Shiny (R web framework)
*   Uses `maftools` R package for MAF parsing and analysis
*   Uses `G3viz` for visualization
*   Integrates TCGA data from MC3, Firehose, CCLE databases
*   Supports both public and user-uploaded data

### Pan-Cancer-Visual
*   Built on Shiny (R web framework)
*   Integrates GENIE, MSK, TCGA, PCAWG cohorts
*   Provides standard VAF/frequency analysis
*   Optimized for cross-cancer queries
*   Real-time lookup capability
