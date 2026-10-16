# Customer Segmentation in E-commerce using RFM and K-Means Clustering

## Project Overview

Customer segmentation is a data science technique used to group customers based on their purchasing behavior. This project analyzes e-commerce transaction data to identify customer groups with different spending patterns, purchase frequency, product preferences, and recency.

The objective is to generate actionable customer insights that can help businesses improve customer retention, encourage repeat purchases, and develop targeted marketing strategies.

## Objectives

- Analyze customer purchasing behavior using transaction data.
- Perform data cleaning, feature engineering, and exploratory data analysis (EDA).
- Develop customer-level features using RFM concepts and additional behavioral indicators.
- Apply K-Means clustering to identify distinct customer segments.
- Visualize and interpret the resulting clusters.
- Recommend business strategies for each customer segment.

## Dataset

**Dataset:** Online Retail

The dataset contains e-commerce transaction records, including invoice details, product information, quantities, prices, customer IDs, and countries.

The data was cleaned and aggregated to create customer-level profiles for segmentation.

## Tools and Technologies

- **Programming:** Python
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Techniques:** EDA, Feature Engineering, Log Transformation, StandardScaler, K-Means Clustering, PCA

## Methodology

### 1. Data Cleaning
- Handled missing customer identifiers.
- Removed invalid transactions, including negative quantities and non-positive prices.
- Prepared transaction data for customer-level analysis.

### 2. Feature Engineering

Created six customer-level features:

- **Recency:** Days since the customer's last purchase.
- **Number of Orders:** Number of orders placed by the customer.
- **Total Spending:** Total amount spent by the customer.
- **Total Quantity:** Total quantity of products purchased.
- **Unique Products:** Number of distinct products purchased.
- **Average Order Value:** Average spending per order.

### 3. Exploratory Data Analysis

Analyzed the distributions of customer spending, order frequency, purchase quantity, product variety, average order value, and recency to understand customer behavior and identify skewed features.

### 4. Data Preprocessing

Applied log transformation to skewed purchasing features and used StandardScaler to standardize the features before clustering.

### 5. Customer Segmentation

Applied the K-Means clustering algorithm to group customers based on their purchasing behavior. The Elbow Method and Silhouette Score were used to evaluate different values of K.

Four clusters were selected to explore more detailed, business-oriented customer segments.

### 6. Visualization and Interpretation

Used Principal Component Analysis (PCA) to project the scaled customer features into two dimensions for visualization. Cluster profiles were analyzed to understand differences between the customer groups.

## Customer Segments and Business Recommendations

The four segments were interpreted as follows:

| Customer Segment | Business Recommendation |
|---|---|
| High-Value Loyal Customers | Offer loyalty rewards, exclusive benefits, and personalized recommendations. |
| Regular Customers | Encourage repeat purchases through cross-selling and loyalty programs. |
| Low-Value Customers | Use relevant product recommendations, affordable bundles, and targeted promotions. |
| Inactive/At-Risk Customers | Run re-engagement campaigns with personalized offers and reminders. |

These labels are interpretations of the observed customer profiles and purchasing behavior.

## Model Evaluation

The Elbow Method and Silhouette Score were used to assess clustering quality.

The highest Silhouette Score among the tested values was obtained for **K = 2 (0.3578)**. However, **K = 4** was selected for the final business-oriented segmentation to explore more detailed customer groups.

This represents a trade-off between cluster separation and the practical usefulness of the segments.

## Key Findings

- The analysis grouped **4,338 unique customers** into four customer segments.
- Customers showed differences in spending, order frequency, product variety, and recency.
- High-Value Loyal Customers demonstrated the strongest purchasing activity.
- Inactive/At-Risk Customers had the longest average time since their last purchase.
- The segments provide a basis for developing targeted marketing and customer retention strategies.

