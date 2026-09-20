# Data science, one experiment at a time

Interactive Python notebooks for beginners. Start with pictures and simple questions, then connect them to mathematics and model choices. No previous data science knowledge is required; each notebook explains the Python and notation it introduces.

## Start here

From this project folder, install the environment and open Jupyter Notebook:

```sh
uv sync
uv run jupyter notebook
```

Open a notebook from the list below and select **Run → Run All Cells**, or use **Shift + Enter** to run cells in order. Each notebook runs independently. The plots include sliders or dropdowns; hover for values and double-click a plot to reset its zoom. Read the prediction prompts before moving the controls.

If you use VS Code, select this project's `.venv` Python interpreter as the notebook kernel. Some previews show only text or static output; use a running Jupyter Notebook session to explore all charts.

## Available notebooks

| Order | Notebook | Learning type / supported tasks | What you will learn | Suggested time |
| --- | --- | --- | --- | --- |
| 1 | [From points to lines](notebooks/01_lines_slope_and_noise.ipynb) | Foundations for regression | Coordinates, slope, intercept, and noisy observations. | 30–40 minutes |
| 2 | [Multiple lines, curves, and spirals](notebooks/02_curves_and_data_shapes.ipynb) | Foundations for supervised and unsupervised learning | Geometry and the distinction between regression, classification, and clustering. | 35–45 minutes |
| 3 | [Linear regression](notebooks/03_regression_and_error.ipynb) | Supervised · Regression | Fitting a line, residuals, MAE, MSE, RMSE, and a baseline. | 40–50 minutes |
| 4 | [KNN: neighbors and boundaries](notebooks/04_knn_neighbors_and_boundaries.ipynb) | Supervised · Classification & regression | Classification demo: neighbor votes, K, scaling, and validation accuracy. | 30–40 minutes |
| 5 | [SVM: margins and kernels](notebooks/05_svm_margins_and_kernels.ipynb) | Supervised · Classification & regression | Classification demo: support vectors, C, linear boundaries, and RBF gamma. | 35–45 minutes |
| 6 | [K-means and DBSCAN](notebooks/06_kmeans_and_dbscan.ipynb) | Unsupervised · Clustering | Cluster count, centers, density, noise points, and curved groups. | 35–45 minutes |
| 7 | [Confusion matrix and thresholds](notebooks/07_confusion_matrix_and_thresholds.ipynb) | Evaluation · Classification | TP, TN, FP, FN, precision, recall, F1, and class imbalance. | 30–40 minutes |
| 8 | [Decision trees: splits and depth](notebooks/08_decision_trees_splits_and_depth.ipynb) | Supervised · Classification & regression | Classification demo: synchronized tree and regions, impurity, depth, and overfitting. | 35–45 minutes |
| 9 | [Random forests: combining trees](notebooks/09_random_forests_combining_trees.ipynb) | Supervised · Classification & regression | Classification demo: individual trees, averaged probabilities, and validation. | 35–45 minutes |
| 10 | [Gradient boosting step by step](notebooks/10_gradient_boosting_step_by_step.ipynb) | Supervised · Classification & regression | Regression demo: residual corrections, learning rate, and validation RMSE. | 40–50 minutes |
| 11 | [Time-series forecasting](notebooks/11_time_series_forecasting.ipynb) | Supervised · Regression | Trend, seasonality, smoothing, ordered splits, lag features, and one-step-ahead forecasts. | 40–50 minutes |
| 12 | [Isolation Forest anomaly detection](notebooks/12_isolation_forest_anomaly_detection.ipynb) | Unsupervised · Anomaly detection | Context features, anomaly scores, alert thresholds, precision, recall, and false alarms. | 40–50 minutes |
| 13 | [Distributions and summary statistics](notebooks/13_distributions_and_summary_statistics.ipynb) | Foundations · Descriptive statistics | Mean, median, standard deviation, IQR, skewness, excess kurtosis, and outlier sensitivity. | 40–50 minutes |
| 14 | [Probability, conditional probability, and Bayes](notebooks/14_probability_conditional_probability_and_bayes.ipynb) | Foundations · Probability | Binomial uncertainty, conditional probability, base rates, test errors, and Bayesian updating. | 40–50 minutes |
| 15 | [Sampling, uncertainty, and hypothesis tests](notebooks/15_sampling_uncertainty_hypothesis_tests.ipynb) | Statistical inference | Sampling distributions, standard errors, confidence-interval coverage, hypothesis tests, and p-values. | 45–55 minutes |
| 16 | [Logistic regression and calibration](notebooks/16_logistic_regression_and_calibration.ipynb) | Supervised · Classification | Logistic probabilities, reliability diagrams, Brier score, discrimination, calibration, and thresholds. | 45–55 minutes |
| 17 | [Calculus and optimization](notebooks/17_calculus_and_optimization.ipynb) | Foundations · Calculus | Derivatives, tangent lines, gradients, learning rates, optimization, integration, density, and probability. | 45–55 minutes |
| 18 | [Vectors, matrices, and PCA](notebooks/18_vectors_matrices_and_pca.ipynb) | Unsupervised · Dimensionality reduction | Vector projections, matrix transformations, principal directions, variance, noise, and scaling. | 45–55 minutes |
| 19 | [Neural networks and model selection](notebooks/19_neural_networks_overfitting_and_selection.ipynb) | Supervised · Classification & regression | Classification demo: hidden units, capacity, noisy labels, overfitting, validation, and regularization. | 45–55 minutes |
| 20 | [Clustering geometry and stability](notebooks/20_clustering_scaling_density_and_stability.ipynb) | Unsupervised · Clustering | Feature scaling, variable density, DBSCAN radius, initialization sensitivity, silhouette score, and ARI. | 45–55 minutes |
| 21 | [PCA, LDA, and t-SNE](notebooks/21_pca_lda_and_tsne.ipynb) | Unsupervised & supervised · Dimensionality reduction | Variance, labeled separation, local-neighbor visualization, perplexity, and projection caveats. | 45–55 minutes |
| 22 | [Deep learning, transfer learning, and fine-tuning](notebooks/22_deep_learning_transfer_and_finetuning.ipynb) | Supervised · Classification | Frozen features, fine-tuning, training from scratch, target label budgets, and negative transfer. | 50–60 minutes |

All examples use synthetic data and existing project dependencies. Chart controls operate on prepared values, so exploring them does not rerun model training. To change the underlying Python example, edit the relevant cell and rerun it and any dependent cells below it.

The existing [lines.ipynb](lines.ipynb) is a broader presentation companion with advanced material. The numbered notebooks provide a gentler starting point.

The teaching instructions and topic roadmap live in [skills.md](skills.md).
