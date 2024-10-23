# Customer-Segmentation-Analysis-for-E-Commerce

## Problem statement
This project aims to perform customer segmentation analysis for an e-commerce company. By analyzing customer behavior and purchase patterns, the goal is to group customers into distinct segments. This segmentation will help inform targeted marketing strategies, improve customer satisfaction, and enhance overall business operations.

## Overview
This project is focused on identifying distinct customer segments based on their behavior, specifically:
- Analyzing purchase data (e.g., total spending on various products)
- Understanding customer demographics (e.g., income)
- Applying clustering algorithms to segment customers
- Visualizing and interpreting the results to inform business strategies

## Project Workflow
**1. Data Cleaning**
- Handling Missing Data: The dataset was checked for missing values and duplicates. Any duplicates were removed.
- Feature Removal: Two features, Z_CostContact and Z_Revenue, were dropped as they contained constant values.
- Outliers: Outliers in the MntTotal (total amount spent) feature were identified and removed using IQR (Interquartile Range) to ensure the quality of the analysis.

**2. Exploratory Data Analysis (EDA)**
- Income Distribution: Visualized using a histogram, which showed a normal distribution of income.
- Age Distribution: Analyzed to check for normality, skewness, and kurtosis. The distribution was found to be almost symmetrical.
- Product Spending: Box plots were created for various product categories (e.g., wines, fruits, meat, etc.) to understand spending patterns across different products.
- Marital Status: A custom function was created to categorize marital status, and its relationship with total spending was analyzed.

**3. Standardization**
To ensure features were on the same scale before applying clustering, the following features were standardized:
- Income
- MntTotal (total spending)
- In Relationship: A binary variable created to indicate if a customer is in a relationship (married/together).
- The StandardScaler from Scikit-learn was used to scale these numerical features.

**4. Clustering (K-Means)**
- K-Means Clustering: Applied to group customers into distinct clusters based on their behavior. A silhouette analysis was used to determine the optimal number of clusters.
- Visualization: The clusters were visualized using scatter plots, showing the relationship between Income and MntTotal across different customer segments.

**5. Cluster Analysis**
- Spending Patterns: Cluster analysis showed that different clusters have unique spending behaviors across product categories.
- Customer Segmentation Insights:
   - High-income, high-spending customers were identified as one segment.
   - Low-income, low-spending customers were grouped separately.
   - Customers in relationships were analyzed to see their spending differences across clusters.
- Cluster Sizes: Analyzed the distribution of customers across clusters to understand the size and marketing potential of each segment.
