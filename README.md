# Drug repurposing for brown adipocyte recruitment

Code repository for:

**An amyloid-β/APP regulatory layer in human brown adipocyte recruitment nominates repurposable drugs for thermogenic fat expansion**

*Authors: to be added upon publication*

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)

---

## Overview

This repository contains all computational scripts used in the above manuscript. The study integrates single-nucleus RNA sequencing (snRNA-seq) analysis of human perivascular adipose tissue (PVAT) with network-based drug prioritisation and knowledge graph analysis to identify repurposable compounds that modulate brown adipocyte differentiation.

---

## Repository structure

scripts/
├── snRNAseq/
│   └── 01_snRNAseq_PVAT_analysis.Rmd
├── network_analysis/
│   ├── 01_network_reformatting_PPI.Rmd
│   ├── 02_network_reformatting_DPI.Rmd
│   ├── 03_generate_PPI_DPI_gene_lists.ipynb
│   ├── 04_drug_proximity_analysis_full_gene_lists.py
│   ├── 05_drug_proximity_analysis_key_genes.ipynb
│   ├── 06_extract_significant_drugs.ipynb
│   └── 07_extract_significant_drug_targets.ipynb
├── knowledge_graph/
│   └── [to be added]
└── in_vitro/
    └── 01_extract_in_vitro_validation_drug_targets.R
    └── [to be added]

---

## Data availability

Raw snRNA-seq data are publicly available from NCBI GEO:
[GSE164528 – Defining the lineage of thermogenic perivascular adipose tissue](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE164528)

External databases used:
- **STRING** v12.0: https://string-db.org
- **BioGRID** v4.4.245: https://thebiogrid.org
- **HINT** (June 2024): http://hint.yulab.org
- **DrugBank** (accessed May 2025): https://go.drugbank.com
- **ChEMBL** v35: https://www.ebi.ac.uk/chembl
- **PrimeKG**: https://zitniklab.hms.harvard.edu/projects/PrimeKG

---

## Software

All analyses were run in **R (v4.4.1)** and **Python (v3.9.12)**. Python dependencies are listed in `requirements.txt`. R package versions are documented in the `sessionInfo()` output at the end of `scripts/snRNAseq/01_snRNAseq_PVAT_analysis.Rmd`.

---

## Acknowledgements

snRNA-seq analysis builds on code originally developed by Holly A. R. Giles.