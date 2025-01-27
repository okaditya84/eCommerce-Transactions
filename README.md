# **Customer Segmentation Using K-Means Clustering**

![Project Banner](path/to/your/banner/image.png)  
_A project for identifying meaningful customer segments to optimize marketing strategies._

---

## **Table of Contents**

- [Introduction](#introduction)
- [Objectives](#objectives)
- [Data Description](#data-description)
- [Approach](#approach)
  - [1. Data Preprocessing](#1-data-preprocessing)
  - [2. Feature Engineering](#2-feature-engineering)
  - [3. Data Scaling](#3-data-scaling)
  - [4. Clustering](#4-clustering)
  - [5. Visualization](#5-visualization)
- [Results](#results)
  - [Clustering Metrics](#clustering-metrics)
  - [Cluster Profiles](#cluster-profiles)
- [Visualizations](#visualizations)
- [Usage](#usage)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)

---

## **Introduction**
Customer segmentation is a key process in understanding customer behavior and tailoring marketing strategies. This project uses the K-Means clustering algorithm to segment customers based on their transaction data, providing actionable insights for business growth.

---

## **Objectives**
1. Group customers into meaningful segments based on spending behavior and purchasing patterns.
2. Identify high-value customer groups for targeted marketing strategies.
3. Provide actionable insights to improve customer retention and engagement.

---

## **Data Description**
This project uses two datasets:

1. **Customers Dataset**:
   - `CustomerID`: Unique identifier for each customer.
   - `SignupDate`: Date when the customer registered.

2. **Transactions Dataset**:
   - `CustomerID`: Unique identifier for each transaction.
   - `TransactionID`: Unique ID for the transaction.
   - `TransactionDate`: Date of the transaction.
   - `TotalValue`: Amount spent in the transaction.
   - `Quantity`: Number of items purchased.

---

## **Approach**

### **1. Data Preprocessing**
- Converted `SignupDate` and `TransactionDate` into datetime format.
- Handled missing values by filling in zeros for derived metrics where appropriate.

### **2. Feature Engineering**
Created the following metrics for each customer:
- **Days Active**: Number of days since the customer signed up.
- **Transaction Count**: Total number of transactions made.
- **Total Spend**: Sum of all transactions.
- **Average Transaction Value**: `Total Spend / Transaction Count`.
- **Purchase Frequency**: Transactions per month.
- **Purchase Duration**: Active period between the first and last transaction.

### **3. Data Scaling**
Standardized the features using `StandardScaler` to ensure all metrics had comparable scales.

### **4. Clustering**
- Used the K-Means algorithm to cluster customers based on the derived features.
- Determined the optimal number of clusters using:
  - **Davies-Bouldin Index**: Lower values indicate better-defined clusters.
  - **Silhouette Score**: Higher values indicate better separation between clusters.

### **5. Visualization**
- **Scatter Plot**: Visualized clusters in a 2D space based on `Total Spend` and `Purchase Frequency`.
- **Radar Chart**: Showed normalized cluster centers across all features.

---

## **Results**

### **Clustering Metrics**
- **Optimal Number of Clusters**: 8
- **Davies-Bouldin Index**: 0.9116
- **Silhouette Score**: 0.2924

### **Cluster Profiles**

| Cluster | Customers | Avg Total Spend | Avg Transactions | Avg Frequency (trans./month) | Avg Transaction Value |
|---------|-----------|-----------------|------------------|------------------------------|------------------------|
| **0**   | 26        | $5,861.11       | 8.38             | 0.95                         | $706.65               |
| **1**   | 19        | $627.26         | 2.11             | 0.23                         | $295.05               |
| **2**   | 19        | $2,462.81       | 2.53             | 0.41                         | $968.23               |
| **3**   | 1         | $931.83         | 2.00             | 12.00                        | $465.92               |
| **4**   | 19        | $4,767.65       | 4.89             | 0.80                         | $996.64               |
| **5**   | 48        | $2,512.05       | 4.23             | 0.69                         | $610.20               |
| **6**   | 22        | $5,696.99       | 6.77             | 0.79                         | $856.64               |
| **7**   | 46        | $3,075.35       | 5.37             | 0.77                         | $585.12               |

---

## **Visualizations**

### **Scatter Plot**
![Scatter Plot](path/to/scatter_plot.png)  
_Distribution of customers across clusters based on `Total Spend` and `Purchase Frequency`._

### **Radar Chart**
![Radar Chart](path/to/radar_chart.png)  
_Normalized feature comparison across all clusters._

---

## **Usage**

### **Dependencies**
Ensure the following libraries are installed:
```bash
numpy
pandas
matplotlib
seaborn
scikit-learn
```

### **Running the Code**
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/customer-segmentation.git
   ```
2. Navigate to the project directory:
   ```bash
   cd customer-segmentation
   ```
3. Run the Jupyter Notebook or Python script:
   ```bash
   jupyter notebook customer_segmentation.ipynb
   ```
4. Visualizations and results will be generated automatically.

---

## **Future Improvements**
- Incorporate additional features such as demographics or product preferences.
- Experiment with alternative clustering algorithms like DBSCAN or Hierarchical Clustering.
- Enhance cluster visualization with interactive plots using tools like Plotly.

---

## **Contributing**
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`feature/your-feature`).
3. Commit your changes.
4. Push to your branch.
5. Open a Pull Request.

---

## **License**
This project is licensed under the [MIT License](LICENSE). Feel free to use and modify as needed.

---

## **Acknowledgments**
- This project was inspired by the need to better understand customer behavior in retail and e-commerce.
- Thanks to the open-source community for providing valuable libraries and tools.

---
