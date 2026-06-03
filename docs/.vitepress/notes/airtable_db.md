---
name: airtable-db
description: >
  Relational database API layered on collaborative spreadsheets.
---

# Airtable Database API

## Overview
Airtable combines the simplicity of a spreadsheet with the power of a database. Its API exposes developer-friendly REST endpoints mapped to custom table schemas.

## REST API Integration
Airtable uses personal access tokens (PAT) in the header: `Authorization: Bearer pat...`
- **Retrieve table records**: `GET https://api.airtable.com/v0/{baseId}/{tableName}`
- **Create records**: `POST https://api.airtable.com/v0/{baseId}/{tableName}`
  ```json
  {
    "records": [
      {
        "fields": {
          "Name": "New Task",
          "Status": "Todo"
        }
      }
    ]
  }
  ```
