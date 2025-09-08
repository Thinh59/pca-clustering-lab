# 🌸 PCA and Clustering Lab

This repository contains the notebook and source code for the **PCA and Clustering Lab**.  
The main objective is to implement **Principal Component Analysis (PCA) from scratch (without using sklearn)** and apply it to dimensionality reduction and clustering tasks.

We are Group 9 in Class 23TNT1 at Ho Chi Minh City University of Science.

We are excited to share our work with you and look forward to your feedback.  
Best regards from Group 9!

---

## 📊 Datasets
1. **Iris Dataset** (for PCA implementation & validation)  
   - Source: `sklearn.datasets.load_iris`  
   - Features: Sepal Length, Sepal Width, Petal Length, Petal Width.  
   - Target: Iris species (Setosa, Versicolor, Virginica).  

2. **ABIDE II Modified Dataset** (for clustering task)  
   - Source: Provided by the instructor via Moodle (not included in this repository).  
   - Shape: 1004 samples × 1444 features.  
   - Labels: `"group"` column with values `"Cancer"` or `"Normal"`.  

---

## 🛠 Workflow  

1. **PCA Implementation**  
   - Build custom `MyPCA` class with methods `__init__`, `fit`, and `transform`.  
   - Standardize dataset before applying PCA.  
   - Compute covariance matrix and perform eigen-decomposition.  
   - Calculate **Explained Variance Ratio (EVR)** and **Cumulative EVR (CEVR)**.  
   - Project data onto the top *n* principal components.  
   - Validate results against `sklearn.decomposition.PCA`.  

2. **Dimensionality Reduction on Iris**  
   - Reduce from 4D to 2D using PCA.  
   - Preserve **97.77%** of total variance with 2 principal components.  
   - Visualize reduced data to confirm separability of Iris species.  

3. **Clustering on ABIDE II Dataset**  
   - Apply PCA to reduce dimensions before clustering.  
   - Experiment with different numbers of components and choose the optimal.  
   - Perform **KMeans clustering (k=2)** multiple times with different initializations.  
   - Compare predicted cluster labels against true labels (`group`).  
   - Evaluate using Accuracy, Precision, Recall, and F1-score.  

---

## 📈 Results

### PCA on Iris Dataset
- Reduced to 2 principal components, preserving **97.77% variance**.  
- Visualization shows clear separation between species.  
- Results match sklearn PCA implementation.  

### KMeans Clustering on ABIDE II Dataset
- Best performance with **k=2** after PCA dimensionality reduction.  
- Evaluation metrics:  
  - **Accuracy:** 0.546  
  - **Precision:** 0.510  
  - **Recall:** 0.389  
  - **F1-score:** 0.442  

---

## 🚀 How to Run
```bash
# Install dependencies
pip install -r requirements.txt

# Launch notebook
jupyter notebook notebooks/Source.ipynb
