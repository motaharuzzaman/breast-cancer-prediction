# 🧠 Breast Cancer Prediction using Machine Learning

This project demonstrates how machine learning algorithms can be used to accurately predict the presence of breast cancer based on clinical features from a well-known dataset.

## 📌 Overview

Breast cancer is one of the leading causes of death among women worldwide. Early detection through reliable diagnostic tools is crucial. This project uses several machine learning models to classify tumors as **malignant** or **benign** using features derived from digitized images of fine needle aspirates of breast masses.

---

## 🗂️ Dataset

- **Source**: [UCI Machine Learning Repository – Breast Cancer Wisconsin (Diagnostic) Data Set](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic))
- **Samples**: 569
- **Features**: 30 numeric features (mean, standard error, and "worst" of various cell characteristics)
- **Target Variable**: Diagnosis (M = Malignant, B = Benign)

---

## 🔍 Project Workflow

1. **Data Loading & Exploration**
   - Summary statistics and data structure
   - Diagnosis distribution
   - Correlation heatmap

2. **Data Preprocessing**
   - Label encoding (`M` = 1, `B` = 0)
   - Feature scaling using `StandardScaler`
   - Train-test split (80:20)

3. **Model Training & Evaluation**
   - Models used:
     - Decision Tree (CART)
     - Support Vector Machine (SVM)
     - Naive Bayes (Gaussian)
     - K-Nearest Neighbors (KNN)
   - 10-fold Cross Validation
   - Accuracy and run-time comparison
   - Boxplot for model performance

4. **Feature Scaling & Improvement**
   - Improved model performance after standardization
   - Pipeline implementation with `StandardScaler`

5. **Hyperparameter Tuning (SVM)**
   - Grid Search over different values of `C` and kernel types
   - Best Result: `SVM (C=0.1, kernel='linear')`

6. **Final Model Evaluation**
   - Accuracy: **99.12%**
   - Confusion matrix
   - Classification report

---

## 🏆 Best Results

| Model        | Accuracy | Std Dev  | Run Time (s) |
|--------------|----------|----------|--------------|
| **SVM (scaled)** | **0.9669** | 0.0299   | 0.1247       |
| KNN (scaled) | 0.9495   | 0.0278   | 0.1495       |
| NB (scaled)  | 0.9296   | 0.0381   | 0.0780       |
| CART (scaled)| 0.9252   | 0.0344   | 0.1900       |

➡️ Final test accuracy (after tuning): **99.12%**

---

## 📊 Confusion Matrix
[[75 0]
[ 1 38]]

- Only **one misclassification** on the test set.
- Excellent balance between precision and recall.
