# Graph-Based Clustering using Minimum Spanning Tree (MST)

## Objective
- Implement graph-based clustering using a Minimum Spanning Tree (MST)
- Form clusters by removing the (k−1) largest edges
- Compare MST-based clustering with K-Means clustering

## Dataset
- Iris Dataset (UCI)
- File used: iris.data
- Features:
  - Sepal Length
  - Sepal Width
  - Petal Length
  - Petal Width
- Class labels were removed for clustering

## Methodology

### MST-Based Clustering
- Constructed a complete weighted graph using pairwise Euclidean distances
- Built the Minimum Spanning Tree using Kruskal’s algorithm (via NetworkX)
- Removed the (k−1) largest edges to form k clusters
- Extracted connected components as cluster labels

### K-Means Clustering
- Applied K-Means with k = 3
- Used centroid-based clustering approach
- Compared results with MST clustering

## Implementation Details
- Language: Python
- Libraries Used:
  - pandas
  - numpy
  - scikit-learn
  - networkx

## Output Files
- mst_clusters.csv
  - Contains cluster labels generated using MST
- kmeans_clusters.csv
  - Contains cluster labels generated using K-Means

## Evaluation Metric
- Silhouette Score was used to evaluate clustering performance

## Results
- MST Silhouette Score: 0.5118
- K-Means Silhouette Score: 0.5526

## Conclusion
- K-Means achieved a higher silhouette score, indicating better-defined clusters
- The Iris dataset contains relatively spherical and well-separated clusters, favoring K-Means
- MST-based clustering is more flexible and can detect non-spherical clusters
- However, MST is sensitive to edge removal and noise, which can affect performance
- MST is more suitable for datasets with irregular cluster shapes

## Key Insight
- MST clustering does not assume cluster shape, making it effective for complex structures
- K-Means performs better when clusters are compact and centroid-based separation is valid
