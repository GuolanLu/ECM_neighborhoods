# ECM Neighborhoods

This repository contains a Jupyter notebook for identifying extracellular matrix (ECM) neighborhoods from single-cell spatial proteomics data.

## File
- `ECM_neighborhood.ipynb` — notebook for clustering ECM features and annotating ECM neighborhood types

## Overview
The notebook performs a simple workflow to define ECM neighborhoods for individual cells based on local ECM composition. It uses normalized ECM marker features, applies clustering, assigns biologically interpretable neighborhood names, and visualizes the resulting cluster structure and neighborhood abundance.

## Input
The notebook currently expects a CSV file:
- `hnscc_ecm_de.csv`

The input table should contain at least:
- `cell_id`
- normalized ECM feature columns:
  - `CollagenI_count_norm`
  - `Fibronectin_count_norm`
  - `TenascinC_count_norm`
  - `Periostin_count_norm`
  - `CollagenIV_count_norm`

## Output
The notebook generates:
- ECM neighborhood assignment for each cell
- named ECM neighborhood categories (`ecm25um_name`)
- cluster centroid heatmap
- neighborhood abundance bar plot

## Requirements
Suggested Python packages:
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`

## Usage
Open the notebook and run all cells:

```bash
jupyter notebook ECM_neighborhood.ipynb
