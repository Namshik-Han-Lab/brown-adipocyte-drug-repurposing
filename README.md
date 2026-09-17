# Drug repurposing for brown adipocyte recruitment

Code repository for:

**An amyloid-β/APP regulatory layer in human brown adipocyte recruitment nominates repurposable drugs for thermogenic fat expansion**

Hannah Mia Lyubov Bazin\*, Sonia Rodríguez-Fdez\*, Fatima Baldo\*, Iman D. Mali, Nazuk Gupta, Milidili Maimiti, Taylor Simonian, Mark Campbell, Namshik Han\*\*, Antonio Vidal-Puig\*\*

\*These authors contributed equally | \*\*Co-last authors

---

## Overview

This repository contains all computational scripts used in the above manuscript. The study integrates single-nucleus RNA sequencing (snRNA-seq) analysis of human perivascular adipose tissue (PVAT) with network-based drug prioritisation and knowledge graph analysis to identify repurposable compounds that modulate brown adipocyte differentiation.

---

## Repository structure

```
scripts/
├── snRNAseq/
│   └── 01_snRNAseq_PVAT_analysis.Rmd
├── network_analysis/
│   ├── 01_network_reformatting_PPI.Rmd
│   ├── 02_network_reformatting_DPI.Rmd
│   ├── 03_generate_PPI_DPI_gene_lists.ipynb
│   ├── 04_identify_key_genes.ipynb
│   ├── 05_drug_proximity_analysis_full_gene_lists.py
│   ├── 06_drug_proximity_analysis_key_genes.ipynb
│   ├── 07_extract_significant_drugs.ipynb
│   ├── 08_extract_significant_drug_targets.ipynb
│   └── 09_classify_and_visualise_significant_drugs.ipynb
├── knowledge_graph/
│   └── 01_knowledge_graph_neo4j_queries.md
└── in_vitro/
    ├── 01_extract_in_vitro_validation_drug_targets.R
    └── 02_bulk_RNAseq_drug_treatment.Rmd
```

---

## Data availability

Human PVAT snRNA-seq data are publicly available from NCBI GEO:
[GSE164528](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE164528) (samples GSM5068996, GSM5068997, GSM5068998)

Bulk RNA-seq data generated in this study are deposited in GEO: [GSE342095](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE342095)

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

snRNA-seq analysis builds on code originally developed by Holly A. R. Giles. We thank Nicholas M. Katritsis for helpful discussions and for critically reviewing and revising the manuscript.