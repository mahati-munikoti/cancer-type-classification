# 🧬 Cancer Type Classification Using Gene Expression Data

This project builds a robust machine learning pipeline for predicting cancer types using RNA-seq gene expression profiles. The notebook includes exploratory data analysis, feature selection, model training, and evaluation on an independent test set.

---

## 📚 Project Overview

### 🔍 Objective
To classify cancer types based on gene expression data using various supervised machine learning algorithms.

### 🧪 Dataset
- RNA-Seq gene expression values per sample
- Each row = 1 patient sample
- Each column = expression of a gene
- Target variable: `Cancer_Group` (multiclass)

---

## 🧠 Features

- 📊 **Exploratory Data Analysis (EDA)**:
  - PCA plots, top gene variance, and correlation heatmaps

- 🧬 **Feature Selection**:
  - Top genes selected by:
    - ANOVA F-score
    - Mutual Information
    - Random Forest Importance
  - Final features = intersection of top 75 from each method

- 🤖 **Model Training**:
  - Classifiers: 
    - Logistic Regression
    - SVM
    - Decision Tree
    - Random Forest
    - XGBoost
    - Gradient Boosting
  - Evaluated using:
    - Precision, Recall, F1-Score
    - ROC-AUC (Macro-average)

- 🧪 **Validation + Testing**:
  - 60/20/20 split: training, validation, test
  - Best model chosen based on validation F1-score
  - Final evaluation done on independent test set

---

## 📊 Results

The notebook outputs:
- 📈 Macro-average ROC curves
- 🧾 Classification reports
- 🧮 Confusion matrices
- 📋 Tabular summary of model metrics

---

## 📦Installation

Install dependencies using:

```bash
pip install -r requirements.txt
```
or 
```Manually
pip install pandas scikit-learn xgboost matplotlib seaborn numpy
```
