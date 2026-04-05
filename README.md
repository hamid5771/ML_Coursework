# CS4730 Coursework 2: Machine Learning Applications

## 📑 Problem Statement
The primary challenge of this coursework is to apply machine learning to extract meaningful patterns from data across three different paradigms: unsupervised, dimensionality reduction, and supervised learning. In the unsupervised task, the problem is to correctly partition data using k-means while accounting for scale sensitivity and cluster stability. For dimensionality reduction, the goal is to identify latent variables and sparse structures using Sparse PCA, specifically evaluating how data normalization affects the resulting components. Finally, the supervised learning task addresses the critical medical challenge of stroke prediction, which is complicated by a severe class imbalance where non-stroke cases significantly outweigh stroke cases, requiring robust sampling and evaluation strategies.

---

## 📂 Project Structure

### 1. Unsupervised Learning (Sub-task 1)
* **Goal**: Partition a 2D dataset into three clusters and evaluate the validity of k-means convergence.
* **Implementation**:
    * Scaling data using Min-Max normalization to prevent feature dominance.
    * Visualizing clusters and centroids in a 2D plane.
    * Evaluating the optimal number of clusters using the Elbow Method (SSE) and Silhouette Scores.

### 2. Dimensionality Reduction (Sub-task 2)
* **Goal**: Use Sparse PCA to find latent variables in a raw and scaled dataset.
* **Implementation**:
    * Applying Sparse PCA with a parameter alpha=5 to find sparse components.
    * Comparing results between raw data and data scaled via `StandardScaler`.
    * Interpreting whether results support potential latent variable models discussed in lectures.

### 3. Supervised Learning: Stroke Prediction (Sub-task 3)
* **Goal**: Build a classification model to predict stroke risk using clinical features.
* **Implementation**:
    * **Data Cleaning**: Imputing or removing missing values in the BMI column and dropping features with weak correlations.
    * **Preprocessing**: Categorical encoding (one-hot) and binning ages into groups (young adult, middle-aged, very old).
    * **Handling Imbalance**: Visualizing class distribution and utilizing `RandomUnderSampler` to improve model sensitivity.
    * **Modeling**: Comparing Random Forest, XGBoost, CatBoost, and Logistic Regression using stratified train/test splits.

---

## 🛠️ Requirements
To run the notebooks, ensure you have the following packages installed:
* `pandas`
* `numpy`
* `scikit-learn`
* `matplotlib`
* `seaborn`
* `catboost`
* `xgboost`
* `imblearn`
* `optuna`

---

## 🚀 How to Run
1. Place the datasets (`cluster.csv` and `stroke-data.csv`) in the root directory.
2. Open the respective Jupyter notebooks to view the step-by-step analysis:
    * `SecondCourseWork.ipynb` (Tasks 1 & 2).
    * `Task3.ipynb` (Stroke Prediction).

---
**Coursework Submission for CS4730.**
