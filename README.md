# Breast Cancer Classification — Supervised Machine Learning

An end-to-end Exploratory Data Analysis (EDA) and Binary Classification project aimed at predicting whether a breast tumor is **Malignant** or **Benign** based on diagnostic cellular measurements.

## Project Overview
Early and accurate detection is critical in medical diagnostics. Using the classic **Breast Cancer Wisconsin (Diagnostic)** dataset, this project builds and evaluates supervised classification models to distinguish malignant from benign cases, prioritizing high sensitivity (Recall) to minimize false negatives.

### Dataset Features
Loaded via Scikit-Learn's `load_breast_cancer` dataset (569 samples and 30 numeric features computed from digitized images of fine needle aspirate of breast masses):
* **Mean, Standard Error, and Worst (largest) values** for 10 cellular nuclei characteristics:
  * `radius`, `texture`, `perimeter`, `area`, `smoothness`, `compactness`, `concavity`, `concave points`, `symmetry`, and `fractal dimension`
* **Target Variable (`target`)**: Binary class (`0` = Malignant, `1` = Benign)

---

## Workflow & Methodology

1. **Exploratory Data Analysis (EDA)**
   * Checked class balance, summary statistics, and feature distributions using Pandas and Seaborn.
   * Analyzed feature correlations using heatmaps to identify multicollinearity among size-related metrics (`radius`, `perimeter`, `area`).

2. **Data Preprocessing & Pipeline**
   * Split the dataset into stratified training and testing sets (`train_test_split`) to preserve class proportions and prevent data leakage.
   * Applied feature scaling (`StandardScaler`) inside a Scikit-Learn `Pipeline` to normalize feature ranges for distance- and gradient-based classifiers.

3. **Model Training & Evaluation**
   * Trained and compared supervised classification algorithms using **Scikit-Learn** (e.g., Logistic Regression, K-Nearest Neighbors / Support Vector Machines / Decision Trees).
   * Evaluated performance using **Confusion Matrix**, **Accuracy**, **Precision**, **Recall**, and **F1-Score** — focusing on **Recall** for the malignant class, as false negatives carry the highest clinical risk.

---

## Tech Stack
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn
* **Environment:** Jupyter Notebook / VS Code

---

## How to Run Locally

1. Clone the repository:
   ```bash
   git clone [https://github.com/RanieriFilho/breast_cancer-classification.git](https://github.com/RanieriFilho/breast_cancer-classification.git)
   cd breast_cancer-classification
