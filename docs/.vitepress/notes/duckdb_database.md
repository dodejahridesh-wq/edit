---
name: duckdb-database
description: >
  In-process SQL OLAP database engine optimized for analytical queries.
---

# DuckDB Analytical Database

## Overview
DuckDB is an embedded, in-process, relational SQL database management system optimized for analytical query workloads. It is designed to be fast, easy to install, and run inside the same process as the application.

## Common CLI Commands
```bash
# Start an interactive CLI session with a persistent DB
duckdb my_data.db

# Direct query on a CSV file
duckdb -c "SELECT * FROM 'data.csv' LIMIT 10;"

# Direct query on a Parquet file
duckdb -c "SELECT category, SUM(value) FROM 'data.parquet' GROUP BY category;"
```

## Python Integration
```python
import duckdb
conn = duckdb.connect('my_data.db')
print(conn.execute("SELECT 42").fetchall())
```
