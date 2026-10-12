# Iris Clustering and Dimensionality Reduction

## Project Overview

This project explores unsupervised machine learning techniques using the Iris dataset from `sklearn.datasets`. It applies K-Means clustering, Principal Component Analysis (PCA), Hierarchical Clustering, and DBSCAN to discover patterns and group similar iris flowers based on their measurements.

The project also compares clustering results across different algorithms and examines how dimensionality reduction affects clustering performance.

## Dataset

The Iris dataset contains 150 samples of iris flowers, with four numerical features and three known species.

**Dataset source:** `sklearn.datasets.load_iris`

### Features

| Feature      | Description         |
| ------------ | ------------------- |
| Sepal Length | Length of the sepal |
| Sepal Width  | Width of the sepal  |
| Petal Length | Length of the petal |
| Petal Width  | Width of the petal  |

**Species:** Setosa, Versicolor, and Virginica.

The species labels are used for interpretation and comparison where appropriate. Since the project focuses on unsupervised learning, the clustering algorithms do not use these labels to form clusters.

## Project Objectives

* Apply K-Means clustering and use the Elbow Method to estimate a suitable number of clusters.
* Reduce the dataset to two dimensions using PCA.
* Visualize principal components and analyze explained variance.
* Apply Hierarchical Clustering and visualize relationships using a dendrogram.
* Apply DBSCAN with different `eps` and `min_samples` parameters.
* Compare the clustering behavior of different algorithms.
* Visualize clusters and identify noise points where applicable.

## Methodology

### 1. K-Means Clustering and Elbow Method

K-Means partitions the dataset into a specified number of clusters based on feature similarity.

Tasks:

* Load and inspect the Iris dataset.
* Apply K-Means clustering.
* Calculate inertia for different values of `k`.
* Plot the Elbow Method curve to estimate a suitable number of clusters.
* Visualize the resulting clusters using the first two or three features.

### 2. Principal Component Analysis (PCA)

PCA transforms the original features into a smaller set of components while preserving as much variance as possible.

Tasks:

* Standardize the features before PCA.
* Reduce the four-dimensional dataset to two principal components.
* Visualize the samples in the two-dimensional PCA space.
* Display the explained variance ratio of each component.
* Compare clustering results using the original standardized features and the PCA-reduced features.

### 3. Hierarchical Clustering

Hierarchical Clustering builds a hierarchy of groups based on distances between samples or clusters.

Tasks:

* Apply agglomerative Hierarchical Clustering.
* Generate and visualize a dendrogram.
* Form clusters using an appropriate number of clusters.
* Compare the resulting groups with K-Means clustering.

### 4. DBSCAN Clustering

DBSCAN is a density-based clustering algorithm that identifies dense regions as clusters and can label isolated samples as noise.

Tasks:

* Apply DBSCAN to the Iris dataset.
* Experiment with different `eps` and `min_samples` values.
* Visualize the identified clusters.
* Highlight noise points separately.
* Compare DBSCAN results with K-Means clustering.

## Evaluation and Comparison

The clustering algorithms are compared based on their cluster assignments, visualization patterns, and ability to identify meaningful groups.

Possible evaluation measures include:

* **Silhouette Score:** Measures how well samples fit within their assigned clusters compared with other clusters.
* **Adjusted Rand Index (ARI):** Compares clustering assignments with known species labels for interpretation.
* **Number of Clusters:** Shows how many groups each algorithm identifies.
* **Noise Points:** Measures how many samples DBSCAN classifies as noise.

ARI uses the known species labels only for evaluation, not for training the clustering algorithms. Silhouette scores should be interpreted carefully when an algorithm produces only one cluster or assigns every sample to a separate cluster.

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* SciPy
* Google Colab / Jupyter Notebook

## Project Structure

```text
iris-clustering-dimensionality-reduction/
│
├── Iris_Clustering_PCA.ipynb
└── README.md
```

The notebook contains the Python code, visualizations, parameter experiments, and interpretations.

## How to Run

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Install the required libraries if they are not already available.
3. Run the cells in order.
4. Review the plots and compare the clustering results.

The Iris dataset can be loaded directly from Scikit-learn, so no separate dataset download is required.

## Results and Findings

This section should be completed after running the notebook.

Include:

* The estimated number of clusters from the Elbow Method.
* The explained variance captured by the first two principal components.
* The differences between K-Means clustering on the original and PCA-reduced features.
* The grouping structure shown by the Hierarchical Clustering dendrogram.
* The best-performing DBSCAN parameter combinations and the number of noise points.
* A comparison of the algorithms using appropriate evaluation metrics.

## Conclusion

This project demonstrates how unsupervised machine learning algorithms can identify patterns in a dataset without relying on predefined class labels. It explores the strengths and limitations of partition-based, hierarchical, and density-based clustering methods, while using PCA to visualize high-dimensional data in two dimensions.

## Author

Nadiya Nowshin
