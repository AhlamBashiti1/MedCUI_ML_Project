# MedCUI: Multi-label Medical Image Classification using CUI Categories

This repository accompanies the paper **"MedCUI: Multi-label Medical Image Classification using CUI Categories"**, which introduces a dual-framework approach for classifying medical images and their captions into clusters of clinical concepts represented by Concept Unique Identifiers (CUIs).

## 🧠 Overview

MedCUI addresses the challenge of sparse and high-dimensional multi-label classification in medical imaging by:
- **Clustering CUI labels** using semantic BioBERT embeddings.
- **Separating processing pipelines** for caption text and grayscale images.
- **Extracting features** via both contextual language models (e.g., ClinicalBERT, BioBERT) and handcrafted visual descriptors (e.g., LBP, HOG, GLCM).
- **Evaluating multiple traditional classifiers** including Logistic Regression, Random Forest, AdaBoost, LinearSVC, and more.

| Model       | Feature Type | F1 (micro) |
| ----------- | ------------ | ---------- |
| LinearSVC   | TF-IDF       | 0.894      |
| LogisticReg | BioBERT      | 0.836      |
| RF + PCA    | Image        | 0.78       |


