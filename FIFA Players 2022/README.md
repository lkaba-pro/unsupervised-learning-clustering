# ⚽ Clustering FIFA 2022 Players using K-means & DBSCAN algorithms

In this notebook inspired by a tutorial on Youtube, we apply two unsupervised learning algorithms — **K-means** and **DBSCAN** — to the FIFA 2022 players dataset. 


## 🎯 Objective

The goal is to group players with similar potential based on their attributes, which can help in scouting, team formation, and player performance analysis.


## ⚙️ Pipeline Overview

The pipeline consists of the following main steps:

1. **Data Loading** – Import and inspect the dataset.
2. **Preprocessing** – Clean and normalize relevant features.
3. **Dimensionality Reduction** – Apply PCA for visualization.
4. **K-means Clustering** – Cluster players and determine optimal `k`.
5. **Visualization** – Project results on 2D PCA space.
6. **DBSCAN Clustering** – Detect dense regions and outliers.
7. **Visualization** – Project results on 2D PCA space.
8. **Conclusion** – Compare both methods and summarize insights.


## 📂 Loading and Exploring the Data

We begin by importing necessary libraries and loading the FIFA 2022 dataset. Then, we take a quick look at the data structure using `head()` and basic info.


## 🧼 Data Preprocessing

Before applying clustering algorithms, we clean and prepare the data:
- Drop irrelevant columns
- Handle missing values
- Select meaningful features
- Normalize the data for fair clustering


## 📊 Exploratory Data Analysis

We perform descriptive statistics and use **Principal Component Analysis (PCA)** to reduce the dataset to two dimensions for visualization and clustering insight.


## 🎯 K-means Clustering

We apply the K-means algorithm to find clusters of similar players. The **elbow method** is used to determine the optimal number of clusters (`k`).


## 📌 Visualizing K-means Clusters

We project the clustered data onto the first two PCA components for a clear 2D visualization of the clusters found by K-means.


## 🌐 DBSCAN Clustering

Next, we apply **DBSCAN**, a density-based clustering method. Unlike K-means, DBSCAN can discover clusters of arbitrary shape and identify outliers (noise).


## 📌 Visualizing DBSCAN Clusters

DBSCAN results are also visualized in the PCA-reduced space. Note that points labeled `-1` are considered outliers by the algorithm.

## 🧠 Conclusion

- **K-means** is efficient for spherical clusters and requires specifying `k`.
- **DBSCAN** detects noise and non-linear clusters but is sensitive to `eps` and `min_samples`.

Combining both methods offers complementary insights for analyzing FIFA 2022 player data.
