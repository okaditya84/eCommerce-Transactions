# eCommerce Transaction Analysis

A project demonstrating an end-to-end workflow for exploring data, identifying lookalike customers, and segmenting customers using clustering techniques. Three Jupyter notebooks are included for each task.

---

## Table of Contents
1. [Overview](#overview)  
2. [File Structure](#file-structure)  
3. [Task Descriptions](#task-descriptions)  
4. [Dependencies](#dependencies)  
5. [Usage](#usage)  
6. [License](#license)

---

## Overview
This repository analyzes an e-commerce dataset to uncover insights into customer behavior, purchase patterns, and possible marketing strategies.

---

## File Structure
- **Aditya_Jethani_EDA.ipynb** (Task 1): Exploratory Data Analysis  
- **Aditya_Jethani_Lookalike.ipynb** (Task 2): Lookalike customer modeling  
- **Aditya_Jethani_Clustering.ipynb** (Task 3): K-Means clustering for customer segmentation  
- **Customers.csv, Products.csv, Transactions.csv**: Example input data files  
- **README.md**: Project documentation  
- **LICENSE**: MIT License  

---

## Task Descriptions

### Task 1: Exploratory Data Analysis (EDA)
- Merges multiple datasets to create a complete view of customers, products, and transactions.
- Examines sales trends, category-wise revenue, and other key metrics.
- Visualizes daily and monthly revenue, top-selling items, and customer segments.

### Task 2: Lookalike Modeling
- Computes features (e.g., total spend, frequency) for a set of target customers.
- Uses cosine similarity to find the closest matches (lookalikes) based on transactional or demographic profiles.
- Outputs top matches and saves them to a CSV for further use.

### Task 3: Customer Segmentation (K-Means Clustering)
- Scales relevant customer metrics with `StandardScaler`.
- Determines the optimal number of clusters using metrics like Silhouette Score and Davies-Bouldin Index.
- Assigns cluster labels, visualizes the results, and interprets cluster profiles.

---

## Dependencies
Install the following Python libraries:
```bash
pandas
numpy
matplotlib
seaborn
scikit-learn