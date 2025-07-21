# Lab 2: K-Means and K-Medoids Clustering on Wine Dataset

## Purpose of the Lab Work

The primary objective of this lab was to explore and compare two unsupervised 
clustering algorithms, **K-Means** and **K-Medoids**, applied to the Wine dataset. 
By implementing and evaluating both algorithms, we aimed to understand how different 
clustering approaches handle real-world data with inherent class structures, while assessing their 
cluster quality using internal and external validation metrics.

## Key Insights from Clustering Results

- **Cluster Quality Metrics:**  
  - *K-Means* achieved a Silhouette Score of **0.2849** and an Adjusted Rand Index (ARI) of **0.8975**, 
    indicating relatively well-defined, compact clusters with strong alignment to the true wine classes.  
  - *K-Medoids* (custom implementation) produced a Silhouette Score of **0.2660** and ARI of **0.7263**, 
  showing slightly less cohesive clusters and weaker correspondence with the ground truth.

- **Cluster Shape and Robustness:**  
  - K-Means centroids, computed as means, allow flexible cluster centers that may not correspond to actual data 
    points, which contributed to more compact clusters under Euclidean distance assumptions.  
  - K-Medoids medoids, restricted to actual data points, yielded more robust cluster representatives less sensitive 
    to outliers but at the expense of cluster compactness and label alignment.

- **Visual Analysis:**  
  - Side-by-side PCA scatter plots highlighted smoother, tighter clusters in K-Means versus slightly more irregular
    cluster boundaries with K-Medoids, reinforcing quantitative findings.

## Challenges Faced and Decisions Made

- **Implementation Choices:**  
  Due to environment constraints and package compatibility issues, a custom implementation of K-Medoids was 
  developed from scratch using NumPy and SciPy. This ensured full control and transparency at the cost 
  of increased coding complexity.

- **Metric Selection:**  
  We chose the Silhouette Score to evaluate cluster cohesion and separation internally, and the Adjusted 
  Rand Index to measure external agreement with known class labels—balancing unsupervised evaluation with 
  supervised validation.

- **Interpretation Nuances:**  
  The ARI difference suggests that while K-Medoids is more robust, it may underperform when cluster shapes 
  are roughly spherical and noise is limited, as in this dataset. This insight informed the discussion on 
  algorithm selection based on data characteristics.

This lab deepened understanding of clustering algorithm trade-offs and reinforced the importance of tailored 
algorithm choice to data geometry and application needs.
