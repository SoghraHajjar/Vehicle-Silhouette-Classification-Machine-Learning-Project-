# 🚗 Vehicle Silhouette Classification – Machine Learning Project  
### Supervised & Unsupervised Learning on Geometric Silhouette Features

This repository contains a complete machine learning workflow for classifying vehicles based on geometric features extracted from their silhouettes.  
The project explores the problem from two analytical perspectives:

- **Supervised Learning** — using labeled data  
- **Unsupervised Learning** — discovering structure without labels  

Both approaches use the same dataset and complement each other in understanding the underlying patterns of the silhouette features.

---

## 📌 Project Overview

Prospect Auto, a car repair chain, wants to automatically identify vehicle types based on their silhouettes.  
The dataset includes numerical shape descriptors extracted from images of three vehicle categories:

- **bus** (double‑decker bus)  
- **van** (Chevrolet van)  
- **car** (Saab 9000 or Opel Manta)

The goal is to determine whether machine learning models can distinguish these vehicle types based solely on silhouette geometry.

---

## 📂 Dataset Description

The dataset contains **18 numerical features**, all derived from geometric properties of vehicle silhouettes.  
These include:

- compactness  
- circularity  
- distance_circularity  
- radius_ratio  
- pr.axis_aspect_ratio  
- max.length_aspect_ratio  
- scatter_ratio  
- elongatedness  
- pr.axis_rectangularity  
- max.length_rectangularity  
- scaled_variance (and variants)  
- scaled_radius_of_gyration (and variants)  
- skewness_about (and variants)  
- hollows_ratio  

### Target Variable
- `class` — bus, van, or car  
  *(Used only in the supervised model and for evaluating clustering results.)*

---

# 🧠 Part 1 — Supervised Learning  
### Building a Classification Model Using Labeled Data

This part focuses on predicting the vehicle class using the silhouette features.

### 🔧 Workflow

#### 1. Data Loading & Exploration
- Inspect dataset structure  
- Analyze distributions and correlations  
- Review class balance  

#### 2. Preprocessing
- Standardize numerical features  
- Split into training and test sets  

#### 3. Model Training
Possible algorithms include:
- Logistic Regression  
- Support Vector Machine  
- Random Forest  
- k‑Nearest Neighbors  

#### 4. Model Evaluation
- Accuracy  
- Precision, Recall, F1  
- Confusion matrix  

---

# 🧠 Part 2 — Unsupervised Learning  
### Discovering Structure Without Using Labels

This part investigates whether natural clusters emerge from the silhouette features.

### 🔧 Workflow

#### 1. Preprocessing
- Standardize all numerical features  
- Split into training and test sets  

#### 2. Dimensionality Reduction (PCA)
- Evaluate explained variance  
- Reduce dimensionality if appropriate  
- Visualize PCA components  

#### 3. Clustering
Methods may include:
- **K‑Means**  
- **Agglomerative Clustering**  
- **DBSCAN** (optional)

#### 4. Cluster Evaluation
Using true labels only for assessment:
- Adjusted Rand Index (ARI)  
- Normalized Mutual Information (NMI)  
- Silhouette Score  

---

# 🔄 Combined Insight

Both approaches provide different perspectives on the same problem:

- **Supervised learning** offers accurate classification when labels are available.  
- **Unsupervised learning** reveals natural groupings and helps understand the structure of the silhouette features.  
- PCA can highlight dominant geometric patterns and may improve clustering performance.  

Together, the two methods give a more complete understanding of how vehicle silhouettes differ and how well these differences can be captured by machine learning models.

---

# 📁 Repository Structure
