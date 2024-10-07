# Credit Analysis

## Overview
Credit analysis is an important process used by financial institutions and lenders to evaluate the creditworthiness of individuals or businesses applying for loans or credit. It involves assessing the applicant's ability to repay borrowed funds by analyzing various financial indicators such as income, debt levels, credit history, and financial stability. The goal of credit analysis is to minimize the risk of default and ensure that loans are extended to reliable borrowers.

The first stage in the credit lifecycle is the credit granting process, where credit is granted based on a thorough assessment of the applicant’s creditworthiness. This involves evaluating the individual's or company's financial situation, including income, debt, and overall financial health. Lenders typically use credit scoring models to predict the likelihood of default. The goal of this work is to build a Credit Scoring Model using logistic regression.

The dataset used in this project is provided by the course from [ **"Preparatório para Entrevistas em Dados (PED)"**](https://renatabiaggi.com/ped/).

## Project Structure

**notebooks/:** Jupyter notebooks used for the exploratory analysis, preprocessing, data preparation, and Probability of Default estimation

**report/:** The presentation slides that outline findings from the data analysis

**README.md:** Project overview and instructions (this file)

## Key Objectives

**Exploratory Data Analysis (EDA):**

- Perform a thorough EDA to understand the structure of the dataset
- Identify trends, patterns, and outliers in the data
- Analyze missing values

**Preprocessing:**

- Treat features containing missing values
- Transform date type feature

**Data Preparation:**

- Evaluate multicollinearity analysis
- Apply Weight of Evidence (WOE) transformation to convert categorical variables into dummy features allowing for better performance in logistic regression

### Data
The dataset used in this project contains 10,738 observations and 81 features (78 features anonymized)

## Tools and Technologies

- **Pandas and Numpy:** For data manipulation
- **Matplotlib & Seaborn:** For creating graphs and charts during EDA
- **Scikit-learn:** For splitting data, and model evaluation metrics like AUC, Gini, and KS statistics
- **Statsmodels:** To perform Logistic Regression
- **Jupyter Notebook:** To document and run the analysis


## Insights

Findings during the analysis:

- Anonymized Features: The majority of features in the dataset were anonymized, limiting the ability to interpret their meanings

- Handling Missing Values: After filtering for missing data, we discovered that 75% of the features had more than 37.81% of missing values. Missing values were handled as follows:

  - Features with ≤50% missing values: These features were assigned to a "Missing" category during the Fine and Coarse Classing process, allowing them to be considered without removing them from the model
  - Features with >50% missing values: These features (38 in total) were excluded from the analysis to avoid model performance degradation

- Multicollinearity: Multicollinearity was detected among certain features. To address this, we removed correlated features to ensure that the model could make independent predictions based on distinct variables

## Future Work
To further improve the analysis, future steps may include:

- Outliers: Understand the outliers to handle the best treatment. Through interquartile range (IQR) method, we observed that 71 of 78 (91.02%) independent features present outliers

- Missing Values: Understanding the nature of missing values is very important, in many cases, missing data may carry intrinsic meaning

- Gini coefficient and KS statistics: both metrics showed that the model is performing well, but it could be refined. It can be done by adding new features, transforming existing ones, or trying different algorithms such as random forests or gradient boosting

- Loss Given Default (LGD), Exposure at Default (EAD), and Expected Loss (EL): as we don’t know the meaning of the features it wasn’t possible to calculate LGD, EAD, and EL

## Acknowledgements
Part of the methodology used in this project, including techniques for logistic regression and credit risk modeling, was inspired by concepts and examples provided in both the PED and EBA courses by [Renata Biaggi](https://renatabiaggi.com/), as well as the ["Credit Risk Modeling in Python"](https://www.udemy.com/course/credit-risk-modeling-in-python/learn/lecture/15585764?start=450#overview) course on Udemy.

## Contributing
Contributions are welcome! If you have additional data, corrections, or suggestions, feel free to contact me. Please ensure that your contributions align with the project's goals and maintain a respectful tone. 



