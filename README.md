# CASA Data Processing for Hamilton Thorne IVOS II

This repository contains Python scripts to extract, clean, and convert sperm motility data exported from **Hamilton Thorne IVOS II CASA systems**.

## Input Files

The system generates two main file types:

- `.DBS` — Summary data (averaged parameters per sample)
- `.DBT` — Individual sperm tracking data

These are typically **tab-separated (.tsv)** ASCII files exported from the IVOS software.

## What the scripts do

- Load and clean `.DBS` and `.DBT` files from a folder
- Combine and standardize output into:
  - `CASA_average.csv` / `.xlsx` → summary metrics per sample
  - `CASA_sperm.csv` / `.xlsx` → per-cell tracking data
- Automatically adds sample names based on filenames
- Renames fields for clarity (e.g., `SORT1_COUNT` → `HYP1_COUNT`)

## Requirements

- Python 3.8+
- pandas

Install with:

```bash
pip install pandas
