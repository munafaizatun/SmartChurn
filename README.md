# SmartChurn — Predicting, Explaining, and Simulating Customer Churn  
---
>*What if the very discounts meant to keep customers loyal actually made them leave faster?*  
SmartChurn explores this paradox through data science — combining predictive modeling, explainable AI, and scenario simulation to reveal how pricing, contracts, and engagement channels shape customer churn in the energy sector.


## Overview  

Customer churn directly impacts profitability. Retaining existing customers is often **5x cheaper** than acquiring new ones — yet many retention programs fail because they rely on blanket discounts that don’t address *why* customers leave.  

**SmartChurn** bridges the gap between *prediction* and *action*:  
it identifies who is likely to churn, explains why, and tests how different discount strategies affect both churn and ROI.  


## Objectives  

- Predict which customers are **most likely to churn**  
- Explain **why** they churn using **SHAP (Explainable AI)**  
- Simulate **discount-based retention strategies** (5%, 10%, 20%)  
- Evaluate **ROI and churn trade-offs** to guide data-driven retention  


## Workflow  

| Stage | Description |
|-------|--------------|
| **Data Preparation** | Cleaned and processed 14K+ customer records with behavioral and contractual attributes. |
| **Modeling** | Built churn classifier using **XGBoost + SMOTE** to handle class imbalance (only 10% churners). |
| **Explainability** | Used **SHAP** to reveal which features drive churn probability. |
| **Simulation** | Applied **ΔSHAP** analysis to simulate customer response to discounts. |
| **Business Insights** | Translated model findings into strategic recommendations for retention. |


## Modeling Results  

| Metric | Default Threshold (0.5) | Tuned Threshold (0.24) |
|--------|--------------------------|------------------------|
| Accuracy | 0.91 | 0.87 |
| Recall (Churn Detection) | 0.15 | **0.33** |
| ROC-AUC | 0.68 | **0.70** |

*By tuning the decision threshold, recall improved by 3× — enabling earlier identification of churners without sacrificing accuracy.*


## Explainable Insights (SHAP)  

| Feature Group | Key Drivers | Interpretation |
|----------------|-------------|----------------|
| **Contract Origin** | `origin_up_*` | Onboarding source strongly predicts churn risk. |
| **Renewal Tenure** | `months_renewal` | Customers nearing renewal are most likely to churn. |
| **Engagement Channels** | `channel_*` | Certain communication channels increase retention. |
| **Pricing & Margin** | `margin_gross_pow_ele`, `price_peak/offpeak` | Pricing sensitivity exists but is secondary to engagement. |

*Customer experience and renewal timing matter more than price.*

## Discount Simulation (ΔSHAP Scenarios)  

To understand how pricing changes influence churn, SmartChurn simulates **5%, 10%, and 20% discount offers** and measures their SHAP-driven impact on churn probability and ROI.  

| Scenario | Description | Churn Impact | ROI Implication |
|-----------|--------------|---------------|-----------------|
| **5% Discount** | Light incentive | Small churn drop | Safe but limited ROI gain |
| **10% Discount** | Balanced offer | **~8.5% churn reduction** | Best ROI balance |
| **20% Discount** | Aggressive pricing | Diminishing churn benefit | ROI decreases |

*Moderate incentives (around 10%) achieve optimal retention efficiency, while excessive discounts harm profit.*

## Strategic Takeaways  

| Insight | Meaning | Business Action |
|----------|----------|-----------------|
| **Contract Origin** | Top churn driver | Strengthen onboarding & channel quality |
| **Renewal Timing** | Predicts loyalty | Proactively engage before contract end |
| **Discount Sensitivity** | Non-linear effect | Personalize offers; avoid blanket discounts |


## Business Impact  

- Early identification of churn-prone customers
- 3× higher churn recall after threshold optimization
- Actionable SHAP insights for engagement and pricing
- Discount ROI simulation for targeted retention strategies  
