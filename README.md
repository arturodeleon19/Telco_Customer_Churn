# Telco_Customer_Churn
Telecom Customer Churn Prediction &amp; Retention ROI Engine

## Executive Summary

This repository delivers an end-to-end churn prediction and financial optimization framework designed to mitigate customer attrition in the telecommunications sector. By shifting from blanket retention efforts to a precision-targeted intervention model, the framework optimizes decision thresholds based on economic loss matrices rather than arbitrary statistical cutoffs. Based on current model projections, deploying this targeted campaign successfully identifies high-risk accounts to generate $140,500 in gross revenue saved against a campaign expenditure of $14,050, yielding a net business value of $126,450—vastly outperforming untargeted or baseline retention strategies.

## Key Insights

* Primary Churn Drivers: Month-to-month contracts and bank withdrawal payment methods represent the highest-risk behavioral segments for customer defection.
* Onboarding Vulnerability: Customer tenure is a critical predictor, with the initial onboarding window (0–6 months) posing the highest acute churn risk (53% attrition rate).
* Service Friction: Internet service features—specifically Fiber Optic technology—strongly correlate with lower customer satisfaction scores (~2.94 mean satisfaction) and heavily drive negative sentiment compared to DSL or Cable alternatives.
* Statistical Validation: Kruskal-Wallis testing confirms that internet service type and configuration variance are statistically significant drivers of churn propensity ($p < 0.001$).

  ## Directory & File Overview
  
  * Kaggle/: Houses raw data extracts and exploratory workspace files used for initial modeling iterations.(https://www.kaggle.com/datasets/alfathterry/telco-customer-churn-11-1-3/data)
  * notebooks/: Features a clean, reproducible Jupyter notebook walking through database-level SQL data exploration (including analytical queries), step-by-step EDA, preprocessing pipelines, statistical visualization, and the transition from  XGBoost to an CatBoost classification model.
 
## Methodology & Next Steps

* Model Pipeline: Built using robust preprocessing steps handled seamlessly within sklearn pipelines (including OneHotEncoder and StandardScaler) paired with the high-performance CatBoost architecture to resolve tabular complexity and classification issues.
* Financial Optimization: Integrates a custom evaluation function incorporating Customer Lifetime Value (CLV) and incentive costs to discover the profit-maximizing decision threshold. (Note: The current CLV integration is a baseline directional assumption built on estimated figures and should be refined with actual historical customer tier valuations).
* Strategic Recommendations: Future iterations aim to audit feature spaces for potential target leakage, implement probability calibration for real-world uncertainty, and adjust financial projections using conservative conversion compliance rates (e.g., modeling 20–30% successful retention conversions instead of assuming absolute compliance).
