# Interpretable-ML
## Project Overview

Traditional machine learning models often act as black boxes, making it difficult to understand the underlying patterns and decisions. In this project, we aim to make clustering more **interpretable** by using **spectral clustering**, which leverages graph theory to reveal meaningful groupings in data.

Key concepts explored:
- Graph representations of data
- Construction of the Degree Matrix, Adjacency Matrix, and Graph Laplacian
- Eigen decomposition for dimensionality reduction
- Clustering in the spectral domain

## Methodology

1. **Graph Construction**  
   The dataset is represented as a graph where each data point is a node, and edges reflect similarity (e.g., using an RBF kernel).

2. **Matrix Computation**  
   - **Adjacency Matrix (A)**: Encodes similarities between data points.
   - **Degree Matrix (D)**: Diagonal matrix with node degrees.
   - **Graph Laplacian (L = D - A)**: Captures the structure of the graph.

3. **Spectral Embedding**  
   We compute the eigenvalues and eigenvectors of the Laplacian to embed the data in a lower-dimensional space.

4. **Clustering**  
   Apply K-Means on the spectral embeddings to identify meaningful clusters.
