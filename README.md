
# Real Estate Price Prediction using Regression Models

**Foundations of Machine Learning – Assignment 1**

## Abstract

This comprehensive report presents a data-driven analysis and modeling of real estate prices using a housing dataset from Taiwan. The report walks through all essential stages of the machine learning workflow including data cleaning, visualization, hypothesis testing, correlation analysis, and linear regression. Particular attention is given to explaining the impact of each variable on house pricing, visualizing important patterns, and interpreting results from statistical tests and models.

## Introduction

Real estate valuation is a cornerstone of economic development, affecting investment, taxation, and personal finance decisions. With the growing availability of data, predictive modeling has become a vital tool to support property assessment. In this study, we analyze a dataset that includes housing features and transaction details to identify factors that influence house price per unit area and to develop a predictive regression model.

## Dataset Description and Preprocessing

### Data Overview

The dataset includes 414 observations and 7 key features:

- `X1 transaction date`: Time of sale  
- `X2 house age`: Age of the house in years  
- `X3 distance to MRT station`: Proximity to public transport  
- `X4 number of convenience stores`: Nearby store count  
- `X5 latitude`, `X6 longitude`: Geographical coordinates  
- `Y house price of unit area`: Target variable  

### Data Cleaning

- All column names were standardized for consistency.  
- Verified data types and ensured no missing values.  
- Created a new variable `Age_Group` by comparing house age to the median.  

## Exploratory Data Analysis

### Distribution of Features

Visualizing the distribution of each feature helps understand the spread and skewness.  
![Normalized Distributions](latex_figures/normalized_distribution.png)

### Correlation Matrix

Pairwise Pearson correlations show strong and weak linear relationships.  
![Correlation Heatmap](latex_figures/correlation_heatmap.png)

### Key Relationship: Price vs MRT Distance

As seen below, distance to MRT station is inversely correlated with price.  
![Regression Plot](latex_figures/regression_plot.png)

## Statistical Hypothesis Testing

### Test 1: Price by House Age Group

- **$H_0$**: Mean price per unit area is equal across age groups.  
- **$H_1$**: Mean price differs.  

Result: Newer homes are priced significantly higher.  

### Test 2: Price by Convenience Stores

- **$H_0$**: Mean price is the same across different store counts.  
- **$H_1$**: At least one group differs.  

ANOVA showed significance: more stores = higher value.  

### Test 3: Association Between Categorical Variables

A chi-square test showed that binned distance and age are not independent, supporting compound effects on price.

## Regression Modeling

### Model Training and Evaluation

A simple linear regression model using MRT distance showed:

- **Negative coefficient**: More distance = lower price  
- **R² ~ 0.52**: Good predictive power with one feature  

### Interpretation

Each meter further from the MRT reduces price by ~0.007 per unit area — a real economic insight.

## Conclusion

- MRT distance is the strongest pricing factor  
- Convenience stores and house age also matter  
- Regression modeling validated visual and statistical insights  
- Future work: multiple features, regularization, advanced models  

---

© 2025 – Foundations of Machine Learning  
