# Mitigating Bias in Recidivism Classification Models

Evaluating recidivism prediction models and comparing group-wise performance across two racial groups.
If unable to render code block in GitHub due to size, view code in [Colab Notebook](https://colab.research.google.com/drive/1-b4lKpZiMdq62xKFwO-fQdZoQP8PAjCO?usp=sharing).

## Overview
This notebook:
- Cleans and preprocesses a recidivism dataset (handling missing values, dropping redundant features, encoding + scaling)
- Trains and evaluates multiple models:
  - **Supervised:** Random Forest, K-Nearest Neighbors (with PCA / t-SNE / UMAP embeddings)
  - **Unsupervised baselines:** K-Means, DBSCAN (used primarily for clustering diagnostics/visualization)
- Reports metrics by demographic group (Race 1 vs Race 2), including **F1, precision, recall, and confusion matrices**
- Generates visualizations (correlation heatmap, elbow curves, PCA/t-SNE/UMAP plots)

## Dataset
This project uses the Kaggle dataset:
- **Recidivism** (uocoeeds): https://www.kaggle.com/datasets/uocoeeds/recidivism

## Outputs
When you run the notebook, you should see:
- EDA outputs (value counts, pie charts, correlation heatmap, mutual information table)
- Cross-validation performance summaries
- Confusion matrices per group
- Dimensionality reduction + clustering visualizations
- Group-wise metric comparisons and basic statistical tests

## Notes / limitations
- Fairness here is assessed via **group-wise performance comparisons** (F1/precision/recall + confusion matrices). This is not a full fairness audit (e.g., equalized odds, calibration).
- Clustering methods (DBSCAN/K-Means) are included as **unsupervised baselines** and may not behave like classifiers.
- Results depend on preprocessing choices and dataset characteristics.
