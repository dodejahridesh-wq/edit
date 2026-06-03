---
name: pubchem-database
description: Query PubChem, search by name/CID/SMILES, retrieve physical/chemical properties, safety/hazard information, and bioactivity targets.
---
# PubChem Database Specialist

This skill provides instructions for querying PubChem to resolve chemical names/CIDs, retrieving molecular properties, safety data, and bioactivity targets.

## Core Capabilities

### 1. Compound Resolution
Convert chemical or trade names to Compound ID (CID) and SMILES:
```bash
uv run scripts/pubchem_api.py resolve --name "aspirin"
```

### 2. Retrieve Properties
Fetch computed physical and chemical properties (Molecular Weight, XLogP, TPSA, etc.):
```bash
uv run scripts/pubchem_api.py properties --cid 2244
```

### 3. Safety and Hazard Info (GHS)
Retrieve hazard statements, handling precautions, and GHS classifications:
```bash
uv run scripts/pubchem_api.py safety --cid 2244
```

### 4. Structure-Based Search
Find similar compounds using a SMILES string:
```bash
uv run scripts/pubchem_api.py similarity --smiles "CC(=O)OC1=CC=CC=C1C(=O)O"
```
