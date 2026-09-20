---
name: data-science-training-guide
description: Plan and develop interactive Python notebooks for this project's visual data science training, connecting mathematical intuition to practical method selection.
---

# Data Science Training Guide

## Purpose

Build an interactive notebook-based learning guide covering statistics, probability, linear algebra, calculus, machine learning, and deep learning. Help learners understand **what a concept means, why it matters, when to use it, and when it can mislead them**.

Start with visible geometry: lines, multiple lines, nonlinear curves, and spiral data. Connect these examples to mathematical ideas, algorithms, and practical decisions. Prefer experiments learners can manipulate over explanations they can only read.

## Planning and brainstorming

When given a topic or rough description:

1. Identify the central question and its prerequisites.
2. Suggest relevant subtopics and connections. Separate essential material from optional extensions; keep the scope focused on the requested topic.
3. Propose interactive experiments and explain what learners should discover.
4. Ask focused questions when audience, depth, or intended use would materially change the lesson. Otherwise state reasonable assumptions and proceed within the requested scope.

The audience is beginners. Assume no prior data science or advanced mathematics. Explain the small amount of Python needed to run and modify each example; do not require learners to understand plotting code before exploring a concept. Introduce notation gradually, define new terms, and explain symbols before using them.

## Teaching approach

For each substantial concept, use a flexible sequence:

- **Question:** Begin with a practical problem or surprising observation.
- **Intuition:** Show geometry or behavior before formal notation.
- **Mathematics:** Explain the equation and connect its terms to the visual.
- **Experiment:** Let learners change a meaningful parameter and observe the result.
- **Interpretation:** Explain what changed, why it changed, and what stayed fixed.
- **Decision:** Describe when to use the method, its assumptions, and a useful alternative.
- **Practice:** Include a prediction or short exercise with an explanation learners can check afterward.

Use the same dataset across related methods when it makes comparisons clearer. Include a failure case alongside a successful example. Avoid suggesting that one algorithm is universally best or that all real-world data follows a small set of curve families.

## Suggested learning sequence

Treat this as a roadmap, not a requirement to include every topic in one notebook.

Build focused notebooks appropriate to each topic, with a clear learning goal and explicit prerequisites. Start with lines and data geometry, then build toward modeling and the broader roadmap. Each notebook should run independently from a fresh kernel, include beginner instructions, and finish with practice and a clear next step. Split a topic when it introduces too many new ideas for one sitting.

In each algorithm notebook's title, state whether it is supervised or unsupervised and whether it supports classification, regression, both, or another task such as clustering. When an algorithm supports both classification and regression, say so in the title and identify which task the notebook demonstrates immediately below it. Label foundational topics and evaluation tools accurately instead of presenting them as training algorithms.

| Area | Questions to explain | Example interaction |
| --- | --- | --- |
| Lines and data geometry | What do slope and intercept mean? How do multiple lines, nonlinear curves, and spirals differ? How do axis scales affect interpretation? | Change slope, intercept, noise, and scale; compare plots. |
| Descriptive statistics | How do center, spread, skewness, and kurtosis describe data? Why do outliers and tail behavior matter? | Change a distribution or inject outliers; compare histograms, box plots, and summary statistics. |
| Probability and inference | When do we need probability? How do conditional probability and Bayes' theorem update beliefs? What does a p-value tell us? | Change base rates and test accuracy; simulate sampling and hypothesis tests. |
| Linear algebra | How do vectors, projections, matrices, and transformations describe data? | Rotate, scale, and project a point cloud; connect the geometry to regression and PCA. |
| Calculus | When do derivatives and integration help? How do local change, optimization, accumulated quantities, and probability connect? | Move a tangent along a curve, adjust a gradient-descent step, or shade an area under a density. |
| Regression and loss | When is regression appropriate? Why use MAE, MSE, or RMSE? How do noise and outliers affect fitting? | Move an outlier and compare residuals, losses, fitted models, and held-out errors. |
| Classification and evaluation | When is classification appropriate? How do thresholds change the confusion matrix, precision, recall, and F1? | Adjust the threshold on fixed labeled predictions and update counts and metrics together. |
| Clustering | When is clustering useful? How do geometry, scale, density, and algorithm choice affect groups? | Compare blobs, moons, and spirals; vary cluster count or density parameters. |
| Dimensionality reduction | When should we use PCA, LDA, or t-SNE? What information does each preserve or use? | Compare projections of labeled data while varying noise, scaling, or method parameters. |
| Model selection | When are decision trees, SVMs, or neural networks suitable? How do capacity and data size affect generalization? | Fit decision boundaries to the same data and compare training and validation behavior. |
| Deep learning and adaptation | When is deep learning justified? When should we train from scratch, use transfer learning, or fine-tune? | Compare frozen features and fine-tuning on a small example; label conceptual simulations clearly. |

## Important distinctions to teach

- Distinguish a nonlinear relationship in the inputs from a model that is nonlinear in its parameters; polynomial regression is a useful example.
- Explain MSE's squared units, RMSE's target units, and MAE's lower sensitivity to large residuals. Distinguish a training objective from an evaluation metric.
- Define a p-value under a specified null model; it is not the probability that the null hypothesis is true. Pair significance with effect size and uncertainty.
- Use skewness and kurtosis with plots and sample-size context. State whether kurtosis means Pearson kurtosis or excess kurtosis; avoid describing it only as peak height.
- Here, LDA means **Linear Discriminant Analysis**. Contrast its use of labels with unsupervised PCA and t-SNE. Explain that t-SNE is primarily exploratory visualization and apparent cluster spacing can mislead.
- Connect derivatives to gradients and optimization, and integration to accumulated quantities and probabilities. For continuous variables, distinguish density from probability.
- Explain threshold tradeoffs and class imbalance. Define how metrics handle zero denominators and show the confusion-matrix axis convention.
- Explain that fine-tuning is a form of transfer learning, rather than treating them as mutually exclusive approaches.
- Introduce train/validation/test separation, overfitting, and leakage when comparing models. Fit preprocessing on training data and use held-out data for performance claims.
- For time-series work, preserve temporal order, distinguish one-step-ahead from recursive multi-step forecasting, and construct every feature using information available by prediction time.
- For unsupervised anomaly detection, separate the continuous anomaly score from the operational alert threshold. Explain what the reference data represents, how features define “unusual,” and that an anomaly is not automatically a fault or cause.

## Notebook and interaction guidance

Use the existing Python environment and dependencies where practical: NumPy and pandas for data, scikit-learn for models, Plotly for visuals, and ipywidgets for controls. Add dependencies only when the lesson needs them.

- Give controls descriptive labels, sensible ranges, and useful defaults. Prefer a few meaningful controls to a crowded panel.
- Explain what each control represents and what learners should watch. Update related plots, metrics, and annotations consistently.
- Keep random seeds fixed for comparisons unless resampling is part of the experiment. Offer an explicit resampling control when useful.
- Label axes, units, legends, classes, and scales. Use distinguishable colors and avoid relying on color alone.
- Keep experiments responsive; use small synthetic datasets for intuition and realistic examples when they add value. Identify synthetic data clearly.
- Organize notebooks into focused sections with reusable helpers where needed. Keep essential explanations visible without requiring a widget interaction.
- Inspect existing notebooks before editing and preserve relevant work. Extend the existing `lines.ipynb` narrative where appropriate; use focused additional notebooks when the requested topic would overwhelm it.

## Completion checks

For notebook work, run affected examples and verify that controls change the intended outputs. For a new notebook or changes to shared setup, restart the kernel and run all cells in order. Check that numerical examples support the written claims, comparisons are fair, and explanations match displayed results. Report any runtime or rendering limitations that prevented verification.

For a planning-only request, deliver the proposed lesson outline, experiments, and unresolved choices without implementing an entire notebook.
