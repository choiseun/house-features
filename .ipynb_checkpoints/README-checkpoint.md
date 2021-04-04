# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Predicting House Sale Prices

---

## Technology & Skills

**Technology:** Python, Jupyter Notebook, GitHub, Git

**Python Libraries:** Pandas, numpy, sklearn, matplotlib, seaborn, scipy

**Technical Skills:** Regression, data cleaning, exploratory data analysis (EDA), data visualization, machine learning, bias-variance tradeoff, imputation method, model validation, statistics, feature engineering, regularization, ensemble models, k-means clustering, pipeline, gridsearch, transfer learning

**Models:** Multiple linear regression, ridge regression, LASSO regression, k-nearest neighbors regressor, random forest regressor, extra trees regressor, support vector regressor, XGBoost regressor, principal components regression

---

## Overview

This project will cover the following sections:

- Problem Statement
- Executive Summary
- Conclusion
- Data Sources
- Data Dictionary

---

## Problem Statement

My goal for this project is to build a regression model that can predict the actual sale price of houses in Ames, Iowa within 25,000 USD. The main metrics I will use to evaluate the accuracy of my model include the root mean squared error (RMSE) and the coefficient of determination (R-squared). The RMSE represents the average distance between the predicted and actual sale prices in USD, and the R-squared represents the variability in sale price that can be explained by the features I incorporate in my model. A limitation of the RMSE is that it is heavily affected by outliers, which I expect to be present in the data.

As a data scientist consulting a real estate agency on house prices, I hope to use my insights to inform real estate agents and homeowners on the expected sale price of their houses and the features that contribute the most value to sale price so that the homeowners can selectively renovate certain features prior to selling.

---

## Executive Summary

In the problem statement, I stated that my goals are to build a regression model capable of predicting actual housing sale prices in Ames, Iowa within 25,000 USD and to identify the features that are most important in determining sale price. Through multiple rounds of model tuning, I identified at least one model that adequately achieves this goal. Of the ten models I have explored, Model 4 is the most suitable to be my production model. While Model 10 performs the best at prediction, the model does not offer much interpretability of the features it is using. Model 4, on the other hand, meets both criteria set out in the problem statement. Despite the limitations of outliers on RMSE and the high number of potential features, I have built a model that is typically 24,410 USD off from the actual sale price and can explain 90.8% of the variability in sale price using 14 features. For this reason, Model 4 is an excellent choice for the production model.

---

## Conclusion

The results indicate that no single feature had the biggest effect on sale price. Rather, the synergies created between interaction terms contributed the most value to sale price. Based on my production model, the top 5 interaction terms include: (1) neighborhood and total basement square footage, (2) living area above ground and full bath, (3) living area above ground and kitchen quality, (4) overall quality and living area above ground, and (5) neighborhood and living area above ground. Unfortunately, many of these features cannot be changed in a practical way for homeowners. Thus, I would recommend that real estate agents and homeowners focus their efforts on renovating the kitchen because a higher rating on kitchen quality can create synergies capable of increasing the sale price.

**Note:** I exclude many features in my recommendation because features like living area above ground are not something that can be altered once the house is built.

---

## Data Sources

One csv file was used for this project. The dataset can be found [here](https://www.kaggle.com/c/dsir-lancelot-project-2-regression-challenge/data).
- train.csv: This file contains all the data for my model.

---

## Data Dictionary

The data dictionary can be found [here](https://www.kaggle.com/c/dsir-lancelot-project-2-regression-challenge/data).
