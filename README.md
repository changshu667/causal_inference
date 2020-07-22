# Customer Churn Analysis

## Project Type
Course Project
## Problem
This project aims to evaluate the effectiveness of a discount market offer to decrease the probability of customers opting out from a telecom company.
## Approach
Several variables that could impact customers’ churn decisions are not included in the dataset, such as income. So, I first merged an external dataset of income from the UC Census Bureau 2020 American Community Survey to solve this external validity problem. And then propensity score matching was conducted to check and ensure there isn’t a baseline difference between the control group and treatment group. After matching, I fit a weighted least-square model including the treatment variables and covariates to investigate the impact of treatment variables in customers’ churn. Outcome: Customer with discount market offer appear to have 0.7 lower probability of churning with statistical significance.
## Key Techniques
Backwards Design, Propensity Score Matching, Weighted Least Square Regression Model
## Language
Python
