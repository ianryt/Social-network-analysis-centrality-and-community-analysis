# Social Network Analysis: Important Nodes and Communities Using Matrix Methods

A Jupyter notebook that analyses a social network (`tiktok_combined.txt.gz`) with matrix methods to find important nodes and detect communities. It was a group project for a university linear algebra course.

## What it does
1. **Loads the network**, keeps the largest connected component and removes self-loops
2. **Adjacency matrix:** checks its properties (symmetric, zero diagonal, density) and plots it as a heatmap
3. **Degree distribution:** linear and log-log histograms
4. **Eigenvalues and eigenvectors:** computes the spectrum with `numpy.linalg.eigh`
5. **Eigenvector centrality:** the leading eigenvector (Perron-Frobenius), cross-checked with a power iteration written from scratch
6. **Laplacian and spectral bisection:** algebraic connectivity and the Fiedler vector
7. **Community detection:** the modularity matrix, with more than two communities found by k-means (also written from scratch) and the best k chosen by modularity
8. **Per-community summary:** the most central node in each community

## Tech stack
- Python 3
- NumPy
- NetworkX (used for loading the graph and drawing it)
- Matplotlib
- Jupyter Notebook

## Getting started

1. Clone the repo:
   ```bash
   git clone https://github.com/ianryt/Social network analysis centrality and community analysis.git
   cd Social network analysis centrality and community analysis
   ```
2. Install the dependencies:
   ```bash
   pip install numpy networkx matplotlib notebook
   ```
3. Make sure `tiktok_combined.txt.gz` is in the same folder as the notebook.
4. Open the notebook and run the cells in order:
   ```bash
   jupyter notebook buri_social_network_proj.ipynb
   ```

The eigen-decompositions use dense matrices, so this works for networks of up to a few thousand nodes.

## Project structure
```
social-network/
├── buri_social_network_proj.ipynb
├── tiktok_combined.txt.gz
├── README.md
└── .gitignore
```

## Authors: Muyanja Ian
