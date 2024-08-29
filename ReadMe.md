[![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![NumPy](https://img.shields.io/badge/NumPy-1.x-013243?style=flat&logo=numpy&logoColor=white)](https://numpy.org/)
[![pandas](https://img.shields.io/badge/pandas-1.x-150458?style=flat&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-F7931E?style=flat&logo=scikitlearn&logoColor=white)](https://scikit-learn.org/)
[![matplotlib](https://img.shields.io/badge/matplotlib-3.x-11557C?style=flat&logo=matplotlib&logoColor=white)](https://matplotlib.org/)
[![seaborn](https://img.shields.io/badge/seaborn-0.11+-4C9A2A?style=flat&logo=databricks&logoColor=white)](https://seaborn.pydata.org/)


# 🏷️ Project: Retail Customer Segmentation & Recommendation System

## 📂 Overview

Segment retail customers and recommend products using an end-to-end Python workflow: data cleaning, feature engineering, scaling, dimensionality reduction, clustering, cluster evaluation, and recommendation system design.

- **Target:** Group customers for personalized marketing and product recommendations
- **Key signals:** Recency, frequency, monetary value (RFM), product diversity, behavioral and geographic features

## Key Objectives
- **Clean and preprocess** transactional data for robust analysis
- **Engineer customer-centric features** (RFM, diversity, cancellation, seasonality)
- **Cluster customers** using K-means and evaluate with Elbow & Silhouette methods
- **Profile clusters** to build actionable customer segments
- **Recommend products** to each segment based on purchase history

## Data
- Source: Retail transaction dataset (`ecommerce-data.csv`)
- Columns: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country
- **Preprocessing:**
  - Remove service-related and anomalous descriptions
  - Drop zero/negative unit price transactions
  - Handle missing values and duplicates
  - Standardize text and optimize dtypes

**Key Features**

| Feature Name                | Data Type | Description                                      |
|----------------------------|-----------|--------------------------------------------------|
| CustomerID                 | int64     | Unique customer identifier                        |
| DaysSinceLastPurchase      | int64     | Days since last purchase                          |
| TotalTransactions          | int64     | Number of transactions                           |
| TotalProductsPurchased     | int64     | Total quantity purchased                         |
| TotalSpend                 | float64   | Total money spent                                |
| AverageTransactionValue    | float64   | Avg value per transaction                        |
| UniqueProductsPurchased    | int64     | Number of unique products bought                 |
| AverageDaysBetweenPurchases| float64   | Avg days between purchases                       |
| DayOfWeek                  | int64     | Preferred shopping day                           |
| Hour                       | int64     | Preferred shopping hour                          |
| IsUK                       | int64     | UK-based customer (1/0)                          |
| CancellationFrequency      | int64     | Number of cancelled transactions                 |
| CancellationRate           | float64   | Cancelled transactions / total transactions      |
| MonthlySpendingMean        | float64   | Avg monthly spend                                |
| MonthlySpendingStd         | float64   | Std dev of monthly spend                         |

## Methods
- **EDA:** Summary statistics, outlier detection (Isolation Forest), correlation analysis
- **Feature Engineering:** RFM, product diversity, behavioral/geographic/cancellation/seasonality features
- **Scaling & Reduction:** StandardScaler, PCA
- **Clustering:** K-means, Elbow & Silhouette methods for optimal k
- **Evaluation:** Silhouette score, cluster profiling, visualization
- **Recommendation:** Suggest popular products in each cluster to customers who haven't purchased them

## Results & Insights
- **Clusters reveal distinct customer segments** based on purchase frequency, spend, and product diversity
- **RFM features** are most influential for segmentation
- **Cancellation and seasonality** help identify at-risk or high-value customers
- **Recommendation system** increases sales opportunities by targeting cluster-specific product gaps

## Strategic Recommendations
| Segment                  | Key Features                | Strategy                                      |
|--------------------------|-----------------------------|-----------------------------------------------|
| High-value loyalists     | High F/M, low R             | Exclusive offers, loyalty rewards             |
| At-risk customers        | High R, low F/M             | Re-engagement campaigns, personalized outreach|
| Bargain seekers          | High cancellation rate      | Targeted discounts, flexible return policies  |
| Seasonal buyers          | High monthly spend std      | Timed promotions, seasonal bundles            |

## Clone and Run
git clone https://github.com/Awnish005123/customer_churn_analysis_and_prediction.git

MIT License | ⭐ Star if helpful!
















