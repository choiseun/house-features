# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Renovating the Features of a House That Matter

---

## Overview

This project will cover the following:

- Problem statement
- Data dictionary
- Summary of analysis
- Conclusion
- Data sources

---

## Problem Statement

My goal for this project is to create a regression model that can predict the actual sale price of houses in Ames, Iowa within 25,000 USD. The main metrics I will use to evaluate the accuracy of my model include the root mean squared error (RMSE) and the coefficient of determination (R-squared). The RMSE represents the average distance between the predicted and actual sale prices in USD, and R-squared represents the variability in sale price that can be explained by the features I incorporate in my model. A limitation of the RMSE that will play an important role in determining the robustness of my model is that the RMSE is heavily affected by outliers, and I expect outliers to be present in the data. In order to construct a model that reflects mostly signal as opposed to noise, I will utilize a minimal number of features to build my model.

As a data scientist consulting a real estate agency on house prices, I hope to use my insights to inform real estate agents and homeowners who are looking to sell their houses of the features that contribute the most value to sale price so that they can selectively renovate certain features prior to selling.

---

## Data Dictionary

The link to Kaggle's data dictionary can be found [here](https://www.kaggle.com/c/dsir-lancelot-project-2-regression-challenge/data).

---

## Summary of Analysis

In the problem statement, I stated that my goal is to build a regression model capable of predicting actual housing sale prices in Ames, Iowa within 25,000 USD. Through multiple rounds of model tuning, I identified at least one model - i.e. Model 4 - that adequately achieves this goal. Of the five models I have explored, the ridge regression model with 14 features performs the best under my evaluation metrics. Despite the limitations of outliers on RMSE and the high number of potential features, I have built a model that is typically 24,410 USD off from the actual sale price and can explain 90.8% of the variability in sale price using 14 features. For this reason, Model 4 is an excellent choice for the production model.

---

## Conclusion

The results indicate that no single feature had the biggest effect on sale price. Rather, the synergies created between interaction terms contributed the most value to sale price. Based on my production model, the top 5 interaction terms include: (1) neighborhood and total basement square footage, (2) living area above ground and full bath, (3) living area above ground and kitchen quality, (4) overall quality and living area above ground, and (5) neighborhood and living area above ground. Unfortunately, many of these features cannot be changed in a practical way for homeowners. Thus, I would recommend that real estate agents and homeowners focus their efforts on renovating the kitchen because a higher rating on kitchen quality can create synergies capable of increasing the sale price.

**Note:** I exclude many features in my recommendation because features like living area above ground are not something that can be altered once the house is built.

---

## Data Sources

Three files were used for this project. The link to the files has been added [here](https://www.kaggle.com/c/dsir-lancelot-project-2-regression-challenge/data).
- train.csv: This file contains all of the training data for my model.
- test.csv: This file contains the test data for my model. The target variable, sale price, has been removed from the test set.
- sample_sub_reg.csv: This file contains an example of a properly formatted submission.

---
