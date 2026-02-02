<<<<<<< HEAD
# Module 1: Tabular Data

Working with larger-than-RAM datasets using `duckdbfs` and DuckDB.

## Overview

This module introduces high-performance workflows for analyzing tabular data that exceeds available RAM. Using the `duckdbfs` package, we leverage DuckDB's streaming capabilities and remote file access to work efficiently with cloud-hosted datasets.

## Case Study: EXIOBASE Global Supply Chains

We analyze [EXIOBASE 3.8.1](https://source.coop/youssef-harby/exiobase-3), a Multi-Regional Input-Output (MRIO) database tracking:
- Economic transactions between 44 countries + 5 rest-of-world regions
- Environmental impacts (emissions, resource use)
- Historical data from 1995–2022
- Cloud-optimized Parquet format, partitioned by year and matrix type

## Learning Objectives

- Connect to remote cloud datasets without downloading
- Filter and aggregate large datasets efficiently
- Use lazy evaluation to minimize memory usage
- Apply `dplyr` verbs that translate to optimized SQL queries

## Prerequisites

### R Packages
```r
install.packages(c("duckdbfs", "dplyr"))
```

### Required Knowledge
- Basic R programming
- Familiarity with `dplyr` syntax
- Understanding of the pipe operator (`|>`)

## Getting Started

1. **Clone this repository**
   ```sh
   git clone <repository-url>
   ```

2. **Open the Quarto document**
   
   Open [tabular-data.qmd](tabular-data.qmd) in RStudio or VS Code with the Quarto extension.

3. **Run the exercises**
   
   Work through the exercises in order, executing code chunks to connect to the remote dataset and perform analyses.

## Key Concepts

### Lazy Evaluation
Data is not loaded into memory until explicitly collected with `collect()`. All filtering, grouping, and summarization happens in DuckDB before bringing results into R.

### Remote Data Access
The dataset is accessed directly from AWS S3 using public credentials. No authentication required for this public dataset.

### Memory-Efficient Workflows
- ✅ Filter and aggregate *before* `collect()`
- ✅ Use `glimpse()` to inspect schema without loading data
- ✅ Use `head()` to preview small samples
- ❌ Avoid `collect()` on unfiltered large datasets

## Exercises

### Exercise 1: Connecting to Remote Data
Learn to connect to cloud-hosted Parquet datasets using `open_dataset()`.

### Exercise 2: Efficient Filtering
Practice filtering and aggregating data remotely before collecting results.

## Additional Resources

- [duckdbfs Documentation](https://github.com/cboettig/duckdbfs)
- [DuckDB Documentation](https://duckdb.org/docs/)
- [EXIOBASE on Source Cooperative](https://source.coop/youssef-harby/exiobase-3)
- [Quarto Documentation](https://quarto.org/)

## Course Information

**Course**: ESPM 288  
**Module**: 1 - Tabular Data  
**Format**: Quarto document (`.qmd`)

## License

This educational material is provided for ESPM 288 coursework.
=======
# tabular-data-template
Module 1
Longyu & Mei's team in ESPM 288 Spring 2026
>>>>>>> 3b2068e (Update README)
