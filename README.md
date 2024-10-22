![Claims_photo](https://github.com/user-attachments/assets/be70a1e2-d004-466d-9781-5a94008c8830)

# Claims Prediction and Cost Analysis in Insurance

## Introduction
Accurately predicting insurance claim amounts is critical for insurance companies to maintain financial stability, optimize claims handling, and offer competitive pricing. The goal of this project is to develop a predictive model that forecasts insurance claim amounts based on customer demographics, policy details, and claims history. The analysis also aims to uncover the key factors influencing claim costs, providing insights that help insurers better manage risk, set premiums, and allocate reserves effectively.

In an industry where claim variability poses a significant challenge, understanding the drivers of claim costs can empower insurers to anticipate expenses and refine their financial strategies. This project is particularly important for insurers seeking to reduce the impact of unexpectedly high claims while avoiding excessive premium increases that could deter customers.

## Project Overview
This project examines various economic and demographic factors affecting insurance claim amounts across multiple datasets. The primary dataset includes information about policy details, customer demographics, and claims history. The analysis aims to deliver actionable insights for insurers by developing a predictive model to estimate claim amounts and identifying the most influential factors associated with higher claim costs.

## Key Research Questions
1. What factors are most associated with higher insurance claim amounts?
2. How can predictive modeling be used to forecast total claim amounts with reasonable accuracy?
3. How can insights into claim cost drivers inform better claims handling and pricing strategies for insurers?

## Datasets
**Primary Dataset:** Insurance Claims

**Description:** This dataset contains detailed information on insurance claims, including:

* **Policy Details:** Coverage amount, deductible, policy state.
* **Customer Information:** Age, demographics, income level.
* **Claims Breakdown:** Total claim amount, injury claims, property claims.
* **Other Attributes:** Fraud status, incident details.
* **Relevance:** This dataset serves as the foundation for building the predictive model, as it contains the target variable (total claim amount) and numerous features for analysis.

**Secondary Dataset:** Case Study Worksheet

**Description:** Contains supplementary financial or scenario-specific data that may help validate the predictive model's performance and refine the analysis.

* **Policy Information:** Policy state, policy type.
* **Incident Details:** Type of incident, incident severity.
* **Fraud Indicator:** Whether the claim was marked as fraudulent or not.
* **Relevance:** Provides additional context for evaluating model predictions against real-world scenarios.

![Datasets Table](https://github.com/user-attachments/assets/449ec104-4a96-475b-afdb-fa49cbfc3885)

## Major Insights
### Insight 1: Key Predictors of Claim Amounts
**Narrative:** The feature importance analysis identified certain variables as the most influential in predicting insurance claim amounts. This insight highlights which factors have the greatest impact, allowing insurers to prioritize these variables when assessing risks and pricing policies.

**Key Findings:**
* "Premium Amount" emerged as the most significant predictor, accounting for approximately 34.8% of the model's importance scores. This indicates that the amount paid by policyholders for coverage is strongly correlated with claim costs.
* Other important predictors include "Income Level" (7.6%), "Coverage Amount" (7.5%), and "Location" (7.5%). This suggests that financial characteristics and regional factors play substantial roles in determining claim amounts.
* "Credit Score" (7.1%) also showed significant importance, implying that customers with different credit histories may exhibit varying levels of risk.

![Top 10 Features](https://github.com/user-attachments/assets/b82f44f9-b5e6-45db-8875-59e3265c4aab)


### Insight 2: The Role of Financial Characteristics in Claims
**Narrative:** While the relationship between deductibles and claim sizes did not yield meaningful insights due to imputed values, we can still draw conclusions based on the impact of premiums and coverage amounts. The importance of these variables suggests that policyholders with higher premiums and coverage limits tend to have higher claim costs.

**Key Findings:**
* The "Premium Amount" being the top predictor aligns with the expectation that higher premiums, which often indicate higher coverage levels or risk, are associated with larger claims.
* "Coverage Amount" also shows that policies with larger coverage amounts are correlated with higher claim payouts, reflecting the higher financial exposure insurers face when offering more extensive coverage.

### Insight 3: Geographic Variations in Claim Costs
**Narrative:** The correlation heatmap provided insights into how different numerical features relate to each other. Identifying correlated features can help refine the model and improve the accuracy of predictions.

**Key Findings:**
* There were noticeable correlations between financial features such as "Premium Amount," "Coverage Amount," and "Income Level." These relationships suggest that individuals with higher income levels are likely to choose policies with higher premiums and coverage amounts.
* Some weaker correlations between other features suggest potential interactions that could be further explored in future modeling (e.g., "Credit Score" and "Claim History").

![Correlation Heatmap](https://github.com/user-attachments/assets/7d15f10a-1abf-44ac-9cee-1153ba1095f0)

## Methodology
### Data Pre-Processing
* Cleaned the data by handling missing values, removing duplicates, and standardizing numeric features.
* Applied label encoding for binary categories and one-hot encoding for multi-class variables.

### Exploratory Data Analysis (EDA):
* Conducted descriptive statistics, univariate analysis (histograms, bar charts), and bivariate analysis (scatter and box plots).
* Used a correlation heatmap to identify feature relationships and applied PCA to assess dimensionality.

### Model Development:
* Chose the Random Forest Regressor due to its suitability for non-linear data and feature importance analysis.
* Split the data into training and testing sets, performed hyperparameter tuning, and evaluated using RMSE and R² metrics.

## Implications
### For Risk Management and Policy Pricing
**Pricing Optimization:** Insights into the relationship between premiums and claim amounts can inform more accurate premium calculations.
**Risk-Based Adjustments:** Understanding the influence of income level and location on claims allows for tailored pricing strategies.
**Deductible Strategies:** Lower deductibles correlate with higher claim amounts, suggesting that insurers may benefit from offering incentives for higher deductibles.

## For Geographic Strategy Development
Regional variations in claim costs indicate that insurers can benefit from location-based adjustments to premiums and coverage options.

## Conclusion
This study developed a predictive model to forecast insurance claim amounts and identified the main factors influencing claim costs. The analysis revealed that Premium Amount, Income Level, Coverage Amount, and Location are the most significant predictors, emphasizing the importance of financial characteristics and policy details in determining claim sizes. The Premium Amount emerged as the top factor, suggesting that pricing strategies should closely reflect the relationship between premiums and expected claim costs.

The model demonstrated reasonable accuracy in predicting claim amounts, supporting the use of data-driven approaches for pricing optimization and risk management. Correlation analysis also highlighted relationships among financial features, which can inform further model refinement. While the imputation of the "Total Claim Amount" may have impacted some insights, the findings provide a solid foundation for improving claims handling and pricing strategies.

## Future Directions
**Explore Advanced Models:** Consider models like Gradient Boosting or Neural Networks for potentially improved accuracy.
**Conduct Regional Pricing Analysis:** Further investigate geographic variations in claims for location-based risk assessment.
**Incorporate Additional Data Sources:** Include other relevant datasets, such as macroeconomic indicators or lifestyle factors, to enhance predictive capabilities.

## References
1. **Primary Dataset: Insurance Claims Data**

* **insurance_claims.csv** - This dataset, sourced from Mendeley Data, contains information on individual insurance claims, including policy details, customer demographics, and claim amounts. It serves as the foundation for the predictive modeling in this project.
* **Link:** [Mendeley Data](https://data.mendeley.com/datasets/992mh7dk9y/2)

2. **Secondary Dataset: Case Study Worksheet**

* **Insurance Fraud Detection** - Sourced from Kaggle, this dataset includes data related to insurance fraud detection. Although not used in the final analysis, it was considered for supplementary validation.
* **Link:** [Kaggle](https://www.kaggle.com/datasets/arpan129/insurance-fraud-detection)


## Appendix: Code and Data

* [Data Wrangling Model](https://github.com/uvray46/Insurance-Claims-Prediction-Cost-Analysis/blob/main/Data%20Wrangling%20Model)
* [EDA Model](https://github.com/uvray46/Insurance-Claims-Prediction-Cost-Analysis/blob/main/EDA%20Model)
* [Pre-Processing & Modeling](https://github.com/uvray46/Insurance-Claims-Prediction-Cost-Analysis/blob/main/Pre-Processing%20%26%20Modeling)
