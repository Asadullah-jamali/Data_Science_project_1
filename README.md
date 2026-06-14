# Data_Science_project_1

This repository contains the complete three-stage enterprise data pipeline for Project 1, developed using Jupyter Notebooks to document the progression from raw data to a validated, enterprise-ready feature store.

## Pipeline Architecture

### Stage 1: Input Fidelity
- **Imputation Rules:** Statistical median imputation for numeric features.
- **Outlier Neutralization:** Interquartile Range (IQR) boundary capping (Winsorizing) to neutralize anomalies while preserving sample size.

### Stage 2: Vectorized Computation
- **RAM-based Vectorization:** Utilization of Pandas/NumPy vectorized operations to avoid procedural loop overhead.
- **Categorical Translation:** One-Hot Encoding (OHE) to map nominal categories into orthogonal coordinate axes.
- **Collinearity Eradication:** Systematic Pearson correlation analysis and removal of redundant features (> 0.80 threshold).

### Stage 3: Structural Contracts
- **Runtime Validation:** Automated Pandera schema assertions enforcing explicit datatypes and statistical boundary contracts.
- **Data Integrity Vault:** Implementation of "Lazy Validation" to prevent silent data corruption and eliminate training-serving skew.

## How to Run
1. Ensure your environment is set up with: `pip install -r requirements.txt`
2. Open `notebooks/Data_science_project_1.ipynb` in Jupyter.
3. Run cells sequentially to execute the pipeline.
