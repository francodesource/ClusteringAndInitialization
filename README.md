# Clustering Algorithms: K-Means and K-Means++

This project implements and compares the K-Means and K-Means++ clustering algorithms. It includes synthetic dataset generation, visualizations, and performance evaluations on various datasets, including real-world data.

## Features

- **K-Means Implementation**: Standard K-Means algorithm with random initialization.
- **K-Means++ Implementation**: Improved initialization for better clustering performance.
- **Synthetic Dataset Generation**: Create custom datasets with specified number of clusters, samples, and features.
- **Visualizations**: Plot clusters, compare algorithms interactively, and analyze inertia distributions.
- **Performance Trials**: Run multiple trials to compare inertia, stability, and variability between K-Means and K-Means++.
- **Extensions**: Experiments with high-dimensional data and overlapping clusters.

## Datasets

The project uses the following datasets:

- **Synthetic Datasets**: Generated with varying parameters (e.g., 25 centers, 100 samples per cluster, 15 features).
- **Real-World Datasets**:
  - Olivetti faces: from OpenML, real world high dimensionality multiclass dataset
- **Extensions**:
  - High-Dimensional: 1000 features.
  - Overlapping Clusters: Smaller hypercube side for overlap.

## Usage

1. Open `main.ipynb` in Jupyter Notebook.
2. Run cells sequentially to:
   - Implement and test K-Means algorithms.
   - Generate synthetic datasets.
   - Visualize clusters.
   - Run trials on different datasets and values of K.
3. Adjust parameters like `N_TRIALS`, `ks`, and dataset settings as needed.
4. View plots and printed results for comparisons.

### Key Functions

- `kmeans(k, points, initial_centroids=None, max_iter=300, seed=42)`: Runs K-Means.
- `kmeanspp(k, points, max_iter=300, seed=42)`: Runs K-Means++.
- `synthetic_dataset(n_centers, n_samples, n_features, sigma=1, hypercube_side=500, seed=42)`: Generates synthetic data.
- `run_trials_and_print_results(n_trials, k, points, dataset_name, save_tex=False)`: Runs trials and displays results.

## Results

The project compares K-Means and K-Means++ across multiple trials, measuring inertia (sum of squared distances) and variability. K-Means++ typically shows lower inertia and better stability, especially in suboptimal initializations.

## Dependencies

- numpy
- matplotlib
- scikit-learn
- pandas
- jupyter (for notebook)
