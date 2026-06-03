---
name: document-compiler
description: >
  Pandoc and Typst document builders and formats compilers.
---

# Document Compiler (Pandoc & Typst)

## Overview
Pandoc is a command-line markup converter that translates between markup formats. Typst is a new, extremely fast, markup-based typesetting system designed for writing scientific and professional documents.

## Common CLI Commands
```bash
# Convert Markdown to PDF using Pandoc & PDF engine
pandoc input.md -o output.pdf --pdf-engine=xelatex

# Convert Markdown to Word Document (.docx)
pandoc input.md -o output.docx

# Compile Typst document to PDF in milliseconds
typst compile document.typ document.pdf

# Watch document for instant hot-reload compilation
typst watch document.typ document.pdf
```
