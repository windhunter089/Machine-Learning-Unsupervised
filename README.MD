# Project 3 - Unsupervised Learning and Dimensionality Reduction

## Introduction

This project explores the application of clustering and dimensionality reduction algorithms on two datasets: Diabetes and White Wine Quality. By employing these algorithms, we aim to uncover hidden patterns, reduce data complexity, and evaluate their impact on clustering performance and neural network efficiency.

## Project Structure

- **1-Diabetes**: Task 1 (Clustering) on the Diabetes dataset.
- **1-Wine**: Task 1 (Clustering) on the Wine dataset.
- **2-3-Diabetes**: Task 2 and 3 (Dimensionality Reduction + Combination with Clustering) on the Diabetes dataset.
- **2-3-Wine**: Task 2 and 3 (Dimensionality Reduction + Combination with Clustering) on the Wine dataset.
- **4-5-Wine**: Task 4 and 5 (Neural Network on Dim. Red. dataset and Clustering dataset) transformation using the Wine dataset.

## Requirements

The project is done in Python 3.8 with the following libraries:
- `pandas`
- `numpy`
- `seaborn`
- `sklearn`
- `scipy`
- `matplotlib`
- `warnings`
- `time`
- `torch`
- `optuna`
- `random`

## Methodology and Experiments

### Task 1: Clustering

#### Diabetes Dataset
- **Algorithms**: K-Means and Expectation Maximization (EM)
- **Evaluation**: Silhouette score, visual inspection, comparison with true labels, training time

#### Wine Dataset
- **Algorithms**: K-Means and Expectation Maximization (EM)
- **Evaluation**: Silhouette score, visual inspection, comparison with true labels, training time

### Task 2: Dimensionality Reduction

#### Techniques
- **Principal Component Analysis (PCA)**
- **Independent Component Analysis (ICA)**
- **Randomized Projection (RP)**

### Task 3: Clustering on Dimensionally Reduced Data

- **Algorithms**: K-Means and EM on PCA, ICA, and RP transformed data
- **Evaluation**: Silhouette score, visual inspection, comparison with true labels, training time

### Task 4: Neural Network on Dimensionally Reduced Data

#### Wine Dataset
- **Evaluation**: Accuracy, F1 score, training time, learning curves, loss curves

### Task 5: Neural Network with Clustering as Additional Features

#### Wine Dataset
- **Evaluation**: Accuracy, F1 score, training time, learning curves, loss curves

## Results and Analysis

### Clustering Algorithms

#### K-Means Clustering
- Optimal clusters: 4 for Diabetes, 6 for Wine
- Better separation and computational efficiency compared to EM
- Higher Silhouette scores and better visual clustering

#### Expectation Maximization (EM)
- Optimal clusters: 6 for Diabetes, 4 for Wine
- Higher computational cost and lower performance compared to K-Means
- Lower Silhouette scores and less clear clustering

### Dimensionality Reduction

#### Principal Component Analysis (PCA)
- 6 Principal Components for Diabetes, 8 for Wine
- Improved clustering performance with K-Means
- Best dimensionality reduction technique in this study

![PCA-wine](image/fig12%20PCA%20wine.png)

#### Independent Component Analysis (ICA)
- 5 Independent Components for Diabetes, 7 for Wine
- Acceptable clustering performance with K-Means on Wine dataset, but not on Diabetes
- EM performed poorly on ICA-transformed data

![ICA-wine](image/fig16%20ICA%20wine.png)

#### Randomized Projection (RP)
- 4 components for both datasets
- Surprisingly good clustering performance with K-Means
- Potential for further research due to promising results

![RP-wine](image/fig18%20RP%20Diabetes.png)

### Neural Network on Dimensionality Reduced Data
- Faster convergence and fewer epochs required
- PCA and RP performed best, with RP being the least effective overall
- Dimensionality reduction improved training efficiency but not accuracy or F1 score

### Neural Network with Clustering as Additional Features
- No significant improvement in accuracy or F1 score
- Early stopping and efficient training due to intrinsic information captured by new features
- Adding clusters as features may introduce noise or redundancy

## Conclusion

- K-Means outperformed EM in clustering performance and training time.
- PCA provided the best improvement in clustering performance, especially with K-Means.
- Dimensionality reduction techniques improved neural network efficiency but not accuracy or F1 score.
- Adding clustering features did not significantly enhance neural network performance.

## Limitations and Future Work

- Results may vary with different datasets.
- Further exploration of K-Means clustering on RP-transformed data is recommended.
- Dimensionality reduction techniques and clustering should be evaluated on more diverse datasets.

## Author

Feedback and questions please send to Ted Pham at trungpham89@gmail.com
