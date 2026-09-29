
# K-Means Clustering Analysis

A Data Science project using **Scikit-Learn**, **Pandas**, and **Matplotlib** to perform unsupervised K-Means clustering on 2D numerical data.

---

## 📌 Project Overview

This project loads a 2D dataset, standardizes feature values, applies the **Elbow Method** to determine the optimal number of clusters ($K$), and labels data points using the **K-Means Clustering** algorithm.

---

## 🛠️ Tech Stack & Requirements

- **Python** 3.10+
- **Pandas** for data handling
- **Matplotlib** for visualization
- **Scikit-Learn** for feature scaling and clustering

### Installation

Install all required packages:

```bash
pip install pandas matplotlib scikit-learn

```

---

## 📁 Repository Structure

```text
├── dataset.csv            # Input dataset containing 2D numerical features (x,y)
├── kmeans_analysis.ipynb  # Jupyter Notebook containing full implementation
└── README.md              # Project documentation

```

---

## ⚙️ Workflow & Implementation

1. **Data Loading**: Load dataset containing `x` and `y` coordinate features from `dataset.csv`.
2. **Feature Scaling**: Apply `StandardScaler()` to standardize $X$ values (zero mean, unit variance).
3. **Elbow Method**: Iterate $K$ from $1$ to $10$ to compute Within-Cluster Sum of Squares (WCSS/inertia) and locate the optimal cluster count.
4. **Model Fitting**: Train `KMeans(n_clusters=4, init="k-means++", random_state=42)` on the scaled data.
5. **Cluster Assignment**: Assign cluster labels ($0, 1, 2, 3$) back to the main DataFrame (`df['Cluster']`).

---

## 📊 Results Summary

* **Optimal $K$ Value**: `4` (chosen based on elbow point reduction in WCSS)
* **Sample Output Data Structure**:

| x | y | Cluster |
| --- | --- | --- |
| 0.496714 | 4.861736 | 2 |
| 0.647689 | 6.523030 | 2 |
| -3.195765 | 0.887503 | 0 |
| -2.377962 | -0.953711 | 3 |

---

## 🚀 How to Run

1. Place your data file named `dataset.csv` in the root folder.
2. Launch Jupyter Notebook or JupyterLab:
```bash
jupyter notebook

```


3. Open `kmeans_analysis.ipynb` and run all cells.

---

## 🎯 Conclusion

In this analysis, feature scaling via `StandardScaler` proved essential in ensuring uniform distance computations across dimensions. By plotting the Within-Cluster Sum of Squares (WCSS) across multiple values of $K$, the **Elbow Method** clearly identified **$K = 4$** as the optimal cluster count where inertia reduction levels off. Training the final model with $K=4$ successfully categorized the 2D dataset into four distinct clusters, providing a clean data partitioning pipeline suitable for downstream pattern recognition and spatial segmentation tasks.

```

```
