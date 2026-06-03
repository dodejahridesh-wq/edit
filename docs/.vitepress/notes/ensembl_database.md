---
name: ensembl-database
description: Query the Ensembl database to resolve gene, transcript, and protein IDs, fetch genomic or protein sequences, retrieve gene structures, and get variant consequence and effect predictions.
---
# Ensembl Database Specialist

This skill provides instructions for querying the Ensembl database to resolve gene/transcript/protein IDs, fetching genomic sequences, and predicting variant consequences (VEP).

## Core Capabilities

### 1. Resolve Gene ID
Resolve a symbol, alias, or RefSeq ID to Ensembl ENSG ID:
```bash
uv run scripts/ensembl_api.py resolve-gene TP53 --species human
```

### 2. Map ID to External Database
Cross-reference an Ensembl ID to UniProt, HGNC, RefSeq, etc.:
```bash
uv run scripts/ensembl_api.py map-id ENSG00000141510 --external-db UniProt
```

### 3. Get Genomic Sequence
Fetch raw DNA for a coordinate window (assembly defaults to GRCh38):
```bash
uv run scripts/ensembl_api.py get-sequence 17:7661779-7687550 --species human
```

### 4. Variant Consequence (VEP)
Predict molecular consequences for a genomic variant:
```bash
uv run scripts/ensembl_api.py vep 9:21971147:T:C --species human
```
