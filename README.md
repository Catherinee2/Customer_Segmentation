## Customer Segmentation & Clustering
## Project Overview

This project focuses on customer segmentation of mall customers using unsupervised machine learning techniques, specifically K-Means clustering. The main goal is to help a marketing team better understand their target audience and design effective marketing strategies.

The analysis identifies distinct shopping groups based on demographic features such as income, age, and spending score. These insights allow the marketing team to focus resources on the most valuable customer groups.

## Problem Statement

The marketing team wants a clear understanding of their target customers to create a more strategic plan. They need to know:

1. Which customer groups exist based on age, annual income, and spending score.

2. The ideal number of customer segments.

3. Insights into how each group behaves so they can design personalized campaigns.

## Objective

The objective is to divide the mall’s customer base into approachable segments. Each segment should represent customers with similar characteristics, enabling tailored marketing strategies.

## Approach & Methodology

1. **Exploratory Data Analysis (EDA)** – Understand the dataset and variable distributions.  
2. **K-Means Clustering** – Apply the algorithm to group customers.  
3. **Summary Statistics & Visualization** – Analyze clusters with descriptive stats and plots.  
4. **Optimization** – Use the **Elbow Method** to determine the optimal number of clusters.

## Tools & Libraries Used

- Python

- Jupyter Notebook

- Pandas : data manipulation and cleaning

- Seaborn : statistical visualizations

- Matplotlib : custom visualizations and plots

- Scikit-learn (sklearn) : K-Means clustering, StandardScaler, One-Hot Encoding

## Dataset Description

The dataset contains 200 mall customers, with the following attributes:

1. CustomerID – unique ID

2. Gender – Male/Female

3. Age – in years

4. Annual Income (k$) – income in thousands of dollars

5. Spending Score (1–100) – score assigned by the mall based on spending behavior

## Exploratory Data Analysis (EDA) – Key Findings
1. Univariate Analysis

Age : Normally distributed, most customers are between 20–50 years old.

Annual Income : Average income = $60k. Distribution is close to normal, with a few high-income outliers.

Spending Score : Concentrated between 40–50.

Gender Distribution : 56% Female, 44% Male.

2. Bivariate Analysis

Annual Income vs. Spending Score : Scatter plot suggested 5 clusters.

Correlation Heatmap:

Age negatively correlated with both income and spending score.

Income slightly positively correlated with spending score.

Pairplots by Gender : Confirmed different behaviors between male and female customers.

## Clustering
1. Univariate Clustering (Income Only)

Optimal Clusters: 3 (via Elbow Method).

Insight: Lowest income group was slightly older on average.

2. Bivariate Clustering (Income + Spending Score)

Optimal Clusters: 5 (via Elbow Method).

Scatter plots revealed distinct customer groups:

Cluster 0 : Low income, high spenders (59% female).

Cluster 1 : High income, low spenders (mostly female).

Cluster 4 : High income, high spenders (avg. age ~32).

3. Multivariate Clustering (Age + Income + Spending Score + Gender)

Preprocessing:

One-hot encoding for Gender.

Standard scaling of features.

Optimal Clusters: 4.

Showed improved separation and clearer customer groups.

## Key Insights & Recommendations

Cluster 4 (High Income, High Spend) : Top priority for marketing campaigns. These customers bring the highest revenue. Balanced gender mix (53% female, 47% male).

Cluster 2 (Low Income, High Spend, Younger Age) : Opportunity for targeted promotions (e.g trending products like gaming consoles, sneakers, or seasonal sales).

Cluster 0 (Older, Lower Income) : Likely less profitable for high-spend campaigns, but may respond to discounts or loyalty programs.

Suggested future steps:

Merge customer demographics with purchase history for deeper analysis.

Build personalized recommendation systems for each segment.

## Conclusion

This project demonstrated how K-Means clustering can be used to segment mall customers and uncover actionable insights. The combination of EDA, clustering, and visualization provided the marketing team with a framework to target their most valuable customer groups.
