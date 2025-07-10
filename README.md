# MedCUI_ML_Project


# K-Means Clustering of BioBERT CUI Embeddings

This Colab project performs unsupervised clustering of Concept Unique Identifiers (CUIs) using their BioBERT embeddings. The goal is to group similar biomedical concepts based on their vector representations, identify representative CUIs per cluster, and visualize cluster structures.

---

## Project Overview

- **Input Data:**
  - `biobert_embeddings.npy`: NumPy file containing precomputed BioBERT embeddings for each CUI.
  - `cui_with_embeddings.csv`: CSV file containing metadata for each CUI, including the canonical name.

- **Core Tasks:**
  1. **Load embeddings and metadata.**
  2. **Determine optimal number of clusters (k)** using Elbow and Silhouette methods.
  3. **Apply K-Means clustering** to group CUIs based on embeddings.
  4. **Identify cluster representatives** as CUIs closest to cluster centroids.
  5. **Summarize clusters** by size and top canonical names.
  6. **Visualize clusters** using PCA and t-SNE embeddings.
  7. **Export results** for further analysis.

---

## Features

- **Automatic selection of the best cluster number** using silhouette scores.
- **Cluster representative identification** to label clusters by their closest central CUI.
- **Summary tables** including:
  - Cluster ID
  - Representative CUI and canonical name
  - Number of CUIs in each cluster
  - Top 3 most frequent canonical names per cluster
- **Rich visualizations**:
  - Cluster size distribution bar plots
  - PCA and t-SNE scatter plots with cluster coloring and representative labels
- **Interactive visualizations** optimized for use in Google Colab.

---

## How to Use

1. Upload your embedding and metadata files when prompted in the Colab.
2. Run cells sequentially to perform:
   - Data loading
   - Cluster number determination
   - Clustering and representative selection
   - Visualizations and summary generation
3. Download the output CSV files containing clustering results and summaries.
4. Review visualizations inline for cluster insights.

---

## Dependencies

- Python 3.x
- numpy
- pandas
- scikit-learn
- matplotlib
- seaborn
- Google Colab environment (for file upload/download integration)

You can install missing dependencies with:

```bash
!pip install numpy pandas scikit-learn matplotlib seaborn
