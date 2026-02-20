# Mall Customer Segmentation using KMeans and PCA

![Python](https://img.shields.io/badge/Python-3.10-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![status](https://img.shields.io/badge/status-completed-green)
![project](https://img.shields.io/badge/project-unsupervised--learning-blue)
![method](https://img.shields.io/badge/method-KMeans-red)
![dimensionality](https://img.shields.io/badge/PCA-dimensionality--reduction-purple)

## Overview
This project performs customer segmentation using unsupervised machine learning techniques on the Mall Customer dataset.
The workflow includes:
- Exploratory Data Analysis (EDA)
- Data preprocessing and feature scaling
- Customer clustering using KMeans
- Optimal cluster selection using Elbow Method and Silhouette Score
- Dimensionality reduction using PCA
- Clustering comparison between high-dimensional data and PCA-transformed data
- Customer segment profiling and interpretation
This project demonstrates a complete unsupervised learning pipeline using scikit-learn.

## Objective
The goal of this project is to segment customers into distinct groups based on behavioral and demographic features.

This allows businesses to:
- Identify different customer types
- Understand spending behavior
- Improve marketing strategies
- Enable targeted customer engagement

## Dataset Description
Dataset: Mall Customers Dataset (Kaggle)
Each row represents one customer.

### Features
| Feature | Description | Type |
|--------|-------------|------|
| CustomerID | Unique identifier | Numerical |
| Gender | Customer gender | Categorical |
| Age | Customer age | Numerical |
| Annual Income (k$) | Customer annual income | Numerical |
| Spending Score (1-100) | Customer spending score | Numerical |

## Exploratory Data Analysis (EDA)
EDA was performed to understand feature distributions and dataset composition.

Generated visualization:
```
EDA_plots.png
```
EDA findings:
- Most customers are between 20–40 years old
- Income is evenly distributed
- Spending scores vary significantly
- Dataset contains both male and female customers
These patterns suggest meaningful clustering potential.

## Data Preprocessing
The following preprocessing steps were applied:

### Feature Selection

Removed:
- CustomerID → identifier only
Used:
- Age
- Annual Income (k$)
- Spending Score (1-100)
- Gender

### Encoding
Applied One-Hot Encoding to Gender.

### Scaling
Applied StandardScaler to normalize numerical features.
This ensures fair distance computation for clustering.

## Clustering Methodology
Customer segmentation was performed using KMeans clustering.

### Optimal Cluster Selection
Two methods were used:

### 1. Elbow Method

File generated:
```
Elbow_Method.png
Elbow_Method_PCA.png
```
Shows WCSS vs number of clusters.

### 2. Silhouette Score

File generated:
```
Silhouette_Method.png
Silhouette_Method_PCA.png
```

Measures clustering quality and separation.

Optimal clusters selected:
```
K = 5
```

## Dimensionality Reduction using PCA

Principal Component Analysis (PCA) was applied to:
- Reduce dimensionality
- Remove redundancy
- Improve cluster separation

Generated visualization:
```
PCA_Explained_Variance.png
```
PCA retained ≥ 90% of dataset variance.

## Clustering Comparison
Clustering was performed on:
1. Original high-dimensional data
2. PCA-transformed data
Comparison visualization:
```
Clustering_Comparison.png
```
This allows evaluation of PCA impact on clustering quality.

## Customer Segment Profiling
Each cluster represents a distinct customer segment.
Example segments include:
- Young Target Audience
- Luxury Enthusiasts
- Budget-Conscious Customers
- High-Income Careful Spenders
- Average Middle-Class Customers
Cluster profiling was performed using mean feature values.

## Model Evaluation
Clustering performance evaluated using:
- Silhouette Score
Higher score indicates:
- Better separation
- More meaningful segmentation

## Project Structure
```
project/
│
├── analysis.ipynb
├── Mall_Customers.csv
│
├── EDA_plots.png
├── Elbow_Method.png
├── Silhouette_Method.png
├── PCA_Explained_Variance.png
├── Elbow_Method_PCA.png
├── Silhouette_Method_PCA.png
├── Clustering_Comparison.png
│
├── report.md
└── README.md
```

## Technologies Used

Python
Libraries:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
Machine Learning Techniques:
- KMeans Clustering
- PCA
- Silhouette Analysis
- Feature Scaling
- One-Hot Encoding

## How to Run

### Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Run notebook
```bash
jupyter notebook
```
Open:
```
analysis.ipynb
```
Run all cells.


## Machine Learning Concepts Demonstrated
- Exploratory Data Analysis
- Data preprocessing
- Feature scaling
- Unsupervised learning
- KMeans clustering
- Cluster evaluation
- Silhouette analysis
- PCA dimensionality reduction
- Customer segmentation
- Cluster profiling

## Author

Nadine Octavia  
Machine Learning Project — Customer Segmentation using KMeans and PCA