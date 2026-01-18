# Module 2: Somatic VCF Analysis

Based on the single-query function, OncoRisk implements a semi-automated workflow for patient-specific somatic mutation analysis. This module is designed for analyzing whole somatic VCF files.

## Pipeline Analysis
The main feature of this module is the Pipeline Analysis tool, which allows you to upload and process genomic result files (e.g., VCF) and generate diagnostic, prognostic, and therapeutic reports. The interface allows for manual adjustment and exportation of organized outputs, accelerating the process from identifying actionable variants to delivering information back to patients.

---

## Detailed Tutorial: Pipeline Analysis

### Overview

**Pipeline Analysis** is a comprehensive genomic analysis tool within OncoRisk that enables users to upload and analyze genomic sequencing data (VCF, DNA, RNA files), generating detailed clinical reports with variant interpretation, tier classification, therapeutic recommendations, and clinical trial information.

### Main Interface Components

#### 1. **Upload File Button** (Top-Left)
Located in the toolbar next to "Analysis Jobs" heading.

**Function:** Opens the file upload dialog to initiate a new genomic analysis.

**Steps to Use:**
1. Click the "Upload File" button (with upload icon).
2. Dialog titled "Upload Genomic Files" appears.
3. Choose file types for upload (see File Upload Section below).

### File Upload Dialog - Three Upload Sections

#### **Section 1: VCF File / JSON**
**Icon:** Document/file icon

**Description:** "Upload Variant Call Format or JSON .gz files containing genomic variations"

**Button:** "Choose File"

**Supported Formats:**
- `.vcf.gz` (Variant Call Format, gzipped)
- `.json.gz` (JSON format, gzipped)

**Use Case:** Primary mutation data input; variants will be parsed and analyzed.

**Technical Note:** VCF files contain genomic coordinates, reference/alternate alleles, quality scores, and genotype information.

#### **Section 2: DNA Sequence**
**Icon:** DNA helix icon

**Description:** "Upload DNA sequence files (TSV format) for genomic analysis"

**Button:** "Choose File (Optional)"

**Supported Format:**
- `.tsv` (Tab-Separated Values)

**Use Case:** Complementary genomic data; provides context for variant annotation.

**Technical Note:** TSV files typically contain sequence identifiers, genomic positions, and nucleotide information.

#### **Section 3: RNA Sequence (Optional)**
**Icon:** DNA helix icon (similar to Section 2)

**Description:** "Upload RNA sequence files for expression analysis"

**Button:** "Choose File (Optional)"

**Format:** Typically `.tsv` or similar structured format

**Use Case:** Optional but powerful for functional analysis; links variants to gene expression changes.

**Clinical Relevance:** Expression data can support or contradict predicted variant pathogenicity.

### Data Privacy & Security Section

**Four Information Items Displayed:**

1.  ✓ **"All uploads are anonymized using unique identifiers (UUID)"**
    *   Each analysis assigned unique identifier
    *   Patient identifiers removed/replaced

2.  ✓ **"Data is encrypted in transit and at rest using industry-standard protocols"**
    *   HTTPS for transport
    *   AES-256 or similar for storage

3.  ✓ **"Uploaded files are automatically deleted after 30 days"**
    *   Automatic cleanup policy
    *   30-day retention window

4.  ✓ **"Your data is never sold, shared, or used for purposes other than your own analysis session"**
    *   Privacy guarantee
    *   Single-use, single-user data model

### Form Control Buttons

#### **Clear All Button**
**Location:** Bottom-right of upload dialog

**Function:** Removes all selected files and resets the form.

**Use When:**
*   Need to start over with file selection
*   Want to change all files at once

#### **Submit Analysis Button**
**Location:** Bottom-right of upload dialog (primary action button, blue)

**Status:**
*   **Disabled** (grayed out) until at least VCF/JSON file is selected
*   **Enabled** once primary file is chosen

**Function:** Submits the selected files to the analysis pipeline.

**After Click:**
*   Files are uploaded and anonymized.
*   Analysis job created with UUID.
*   Queued for processing.
*   Page updates to show job status.

### Analysis Jobs Section

#### **Search Jobs by Name, Patient, UUID... (Textbox)**
**Location:** Top of job list

**Function:** Filter existing analysis jobs.

**Search Parameters:**
*   Job name (filename)
*   Patient identifier
*   UUID (unique job identifier)
*   Analysis ID

**Behavior:** Real-time filtering as you type.

#### **All Statuses Dropdown**
**Location:** To the right of search box

**Available Options:**
*   **All Statuses** (default) - Shows all jobs
*   **Running** - Currently processing jobs
*   **Completed** - Finished analyses with results
*   **Failed** - Jobs that encountered errors
*   **Queued** - Waiting to begin processing

**Use Case:** Filter jobs by completion state.

### Job Status Indicators

Each job entry displays:

1.  **Status Label**: "Completed" (green dot), "Running" (processing icon), "Failed" (red indicator).
2.  **File Name**: Heading shows uploaded filename.
3.  **Patient/ID**: Shows assigned UUID.
4.  **DEMO Tag**: Indicates example/demo analysis.

### Expanded Job Details Panel (After Selecting a Job)

#### **Job Information Section**

*   **Job UUID**: Full unique identifier for job.
*   **Patient ID**: Same as UUID (anonymized).
*   **Status**: Current state of job; last updated timestamp.
*   **Primary File Type**: Identifies input file format (VCF, JSON, etc.).
*   **Initiated Time**: Date and time analysis started.
*   **Completion Time**: Date and time analysis finished; shows processing duration.

### Action Buttons (Below Job Metadata)

#### **Parameters Button**
**Location:** Below job details

**Function:** View and manage analysis pipeline parameters.

**Shows:**
*   Quality control thresholds
*   Variant filter settings
*   Annotation databases used
*   Tier classification criteria

#### **Report Generation Button**
**Location:** Next to Parameters

**Function:** Generate or regenerate analysis report.

**Options:**
*   OncoRisk Report (full comprehensive report)
*   Export formats available

**Output:** PDF report (35+ pages typically).

#### **Export Data Button**
**Location:** Right side of action buttons

**Function:** Download raw analysis results.

**Formats Available:**
*   CSV/TSV tables (filterable results)
*   JSON (machine-readable format)
*   Excel workbooks

### Variant Results Table

#### **Search Bar (Above Results)**
**Text:** "Search by Gene, Consequence, rsID..."

**Function:** Filter variants in results table.

**Search Capabilities:**
*   Gene symbol (KRAS, TP53, etc.)
*   Consequence type (Missense Variant, SNV, etc.)
*   rsID (dbSNP identifier)
*   Genomic coordinates
*   Protein change notation

#### **Filters Button**
**Location:** Right side of search bar

**Function:** Open advanced filtering panel.

**Filter Options Include:**
*   Variant type (SNV, MNV, indel, fusion, etc.)
*   Consequence (missense, synonymous, frameshift, etc.)
*   Tier classification (TIER I, II, III, Unclassified)
*   Allele frequency
*   Clinical significance
*   Gene panels
*   Functional impact scores
*   VAF range (if RNA/DNA provided)

### Variant Classification Display

#### **Variant Counts (Below Search)**
Shows summary statistics:

*   **Showing of filtered**: Display count (default 20 per page); total variants in analysis; indicates filtering applied.
*   **Insights**: Number of variants with clinical insights; actionable findings.
*   **No insights**: Variants without specific insights; lower clinical priority.

#### **Tier Breakdown**
Shows clinical tier distribution:

*   **TIER I**: High clinical significance, FDA-approved therapies.
*   **TIER II**: Established clinical significance, emerging therapies.
*   **TIER III**: Potential clinical significance, needs further validation.
*   **Unclassified**: VUS or insufficient data.

### Individual Variant Cards (Main Results Display)

#### **Card Header with Buttons**

*   **BIOMARKER Tag**: Color-coded by tier (TIER I=red, TIER II=orange, TIER III=yellow); clickable to expand/collapse details.
*   **TIER Button**: Shows assigned clinical tier; links to tier explanation.
*   **"Details" Button**: Expands deep-dive information panel; shows comprehensive clinical data.

#### **Core Variant Information**

*   **Gene Symbol**: Primary gene affected.
*   **Protein Change**: HGVS notation.
*   **rsID**: dbSNP identifier.
*   **Variant Type**: SNV, MNV, Indel, etc.
*   **Consequence**: Predicted functional impact.

#### **Genomic Information Section**

*   **GENOMIC LOCATION**: Full genomic coordinate.
*   **TRANSCRIPT**: Affected gene transcript identifier.
*   **cDNA CHANGE**: cDNA-level notation.
*   **IMPACT SCORE**: Numerical prediction of variant impact.

#### **Clinical Significance Section**
Shows concordance across multiple clinical databases:
*   **OncoKB**: Oncogenic / Unknown / Inconclusive
*   **ClinVar**: Pathogenic / Likely Pathogenic / Benign / Conflicting
*   **CancerVar**: Tier classification and confidence level
*   **AlphaMissense**: likely pathogenic / likely benign / uncertain

#### **Highlights Section**
Quick-view clinical tags:
*   ✓ **Is Rare**
*   ✓ **Has Active Trials**
*   ✓ **Is Strongly Pathogenic**
*   ✓ **Has Prognostic Impact**
*   ✓ **Has Fda Approved Therapy**
*   ✓ **Is Likely Pathogenic**

#### **TIER SUMMARY Section**
**Function:** Brief clinical interpretation.

#### **ONCOKB INSIGHT Section**
**Content:** Curated expert interpretation from OncoKB.

#### **THERAPIES Section**
**Function:** Lists relevant targeted treatments, including therapy name, associated cancer type, and evidence level.

#### **CLINICAL TRIALS Section**
**Function:** Links to active clinical studies, including trial name, phase, status, and Trial ID.

#### **COMPUTATIONAL PREDICTIONS Section**
**Function:** In-silico pathogenicity predictions from tools like SIFT, POLYPHEN, and REVEL SCORE.

### Report Preview Pane (Right Side)

#### **Report Viewer Header**
*   **Title**: "Report Preview"
*   **Download icon** (top-right)

#### **PDF Document Display**
*   Shows UPG-retrieve-report
*   35-page comprehensive clinical report
*   Paginated view with thumbnails

#### **PDF Controls**
*   Page navigation
*   Zoom controls
*   Print/save options
*   Full-page view toggle

### Complete Workflow Summary

**Step 1:** Click "Upload File" button.
**Step 2:** Select files (VCF/JSON required, DNA/RNA optional).
**Step 3:** Click "Submit Analysis" button.
**Step 4:** Job processed (Queued → Running → Completed).
**Step 5:** Click job to view metadata, parameters, and generate report.
**Step 6:** Filter and search variants (search box, "Filters" button).
**Step 7:** Interpret clinical significance (TIER, OncoKB, therapies, trials).
**Step 8:** Export results (raw data, PDF report).

### Key Clinical Sections in Generated Report
1.  **Executive Summary**
2.  **Variant Inventory**
3.  **TIER I Variants**
4.  **TIER II Variants**
5.  **TIER III Variants**
6.  **Therapeutic Recommendations**
7.  **Clinical Trial Matching**
8.  **Computational Predictions**
9.  **Gene/Disease/Therapy Links**
10. **Methodology**

### Tips for Effective Use
*   ✓ **Always validate with VCF file**
*   ✓ **Add RNA data if available**
*   ✓ **Review TIER I variants first**
*   ✓ **Check OncoKB insights**
*   ✓ **Cross-reference clinical trials**
*   ✓ **Use Export Data for downstream analysis**
*   ✓ **Keep job UUID for future reference**