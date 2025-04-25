# Cancer Type Classification Using Gene Expression Data

This project presents a complete machine learning pipeline for predicting cancer types using RNA-seq gene expression profiles. It includes data preprocessing, exploratory data analysis (EDA), feature selection, model training, validation, and test evaluation — all implemented in Python using scikit-learn and XGBoost.

---

## Overview

- **Dataset**: RNA-seq gene expression data, with cancer types grouped into biologically relevant categories.
- **Task**: Multiclass classification to predict cancer group from gene expression profiles.
- **ML Models**: Logistic Regression, SVM, Decision Tree, Random Forest, XGBoost, Gradient Boosting.

---
## Dataset
Source: Kaggle - Cancer RNA-Seq Data

Description: The dataset contains RNA-seq gene expression profiles of various cancer types, grouped into biologically meaningful categories.

Please download and extract the dataset (archive_kaggle_cancer.zip) into the working directory before running the notebook.

## Features

### Feature Selection
- Top 75 genes selected from each of 3 methods:
  - ANOVA F-score
  - Mutual Information
  - Random Forest importance
- Final features = **intersection** of top 75 from all three methods

### Model Training & Evaluation
- Data split into **train (60%) / validation (20%) / test (20%)**
- Six classifiers trained and evaluated using:
  - Precision, Recall, F1-score
  - Macro-averaged ROC-AUC
- Best model selected by **validation F1-score**
- Final performance reported on the **independent test set**

### Visual Outputs
- PCA plots
- Heatmaps (correlation & sample-gene)
- ROC curves (macro-average)
- Confusion matrices

---

## How to Run

1. Clone this repo
2. Open `CancerPred.ipynb` in Jupyter Notebook or Google Colab
3. Install dependencies:
   ```bash
   pip install pandas scikit-learn xgboost matplotlib seaborn numpy
   ```
   or
   ```bash
   pip install -r requirements.txt
   ```
5. Run all cells step-by-step

---

## Files

```
├── CancerPred.ipynb       # Main notebook
├── README.md              # You're reading this
└── requirements.txt       
└── data.zip               # Dataset used for the work 

```

---

## License

This project is licensed under the MIT License.

---

## Acknowledgements

- Kaggle and The Cancer Genome Atlas (TCGA)
- scikit-learn developers
- XGBoost community

---

> This notebook is Colab-ready and designed to be easily extended for clinical genomics applications.
