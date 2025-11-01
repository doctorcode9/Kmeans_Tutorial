# K-Means Clustering

## 📌 Definition
K-Means is an **unsupervised machine learning algorithm** used to cluster data into **K groups** based on similarity.  
It partitions data so that each point belongs to the cluster with the **closest mean (centroid)**.

---

## ⚙️ Principle of the Algorithm

Steps of K-Means:

1. Choose a value for **K** (number of clusters)
2. Initialize **K centroids**
3. Assign each data point to the **nearest centroid**
4. Recompute centroids as the **mean** of assigned points
5. Repeat assignment + centroid update until convergence

> The algorithm minimizes the **distance between points and their centroids**.

---

## 🧠 Example (No Code)

We have customers described by **Age** and **Income**:

| Person | Age | Income |
|--------|-----|--------|
| A      | 22  | 15k    |
| B      | 25  | 18k    |
| C      | 35  | 60k    |
| D      | 40  | 65k    |
| E      | 50  | 80k    |

If **K = 2**, clustering might look like:

- **Cluster 1** (young, low income): A, B  
- **Cluster 2** (older, higher income): C, D, E

The model groups individuals with similar characteristics.

---

## 🎯 When to Use K-Means

Use K-Means when:

- You need to **find natural groups** in data
- Your data contains **numerical features**
- Clusters are roughly **spherical and similar in size**
- You need a **fast, scalable** algorithm

Common applications:

- Customer segmentation
- Image grouping
- Document/topic clustering
- Anomaly detection (as a preprocessing step)

---

## 🚫 When *Not* to Use K-Means

Avoid K-Means when:

| Problem | Why |
|--------|------|
Non-spherical clusters | K-Means assumes round clusters |
Many outliers | Outliers distort centroid positions |
Unknown K | You must specify number of clusters |
Categorical data | K-Means requires numerical inputs |
Clusters differ in size/density | Performs poorly in such cases |

Alternatives: **DBSCAN, Hierarchical Clustering, Gaussian Mixture Models**

---

## 📂 Data Requirements & Format

To use K-Means effectively:

- **Numeric data only**
- Scale features (e.g., age vs income → different magnitudes)
- Remove or handle **missing values**
- Normalize/standardize data for better performance

**Example input format:**

| Feature 1 | Feature 2 | Feature 3 |
|-----------|-----------|-----------|
| 0.45      | 0.82      | 0.12      |
| 0.12      | 0.78      | 0.50      |
| ...       | ...       | ...       |

---

## ✅ Summary

| Item | Description |
|------|------------|
Type | Unsupervised learning (clustering)
Objective | Group similar data points
Key idea | Minimize distance to centroid
Best for | Clean numeric data, well-separated clusters
Avoid when | Noisy, categorical, or uneven clusters

---
