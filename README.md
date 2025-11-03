# SmartChurn — Predicting & Explaining Customer Churn  

What if discounts meant to retain customers actually made them leave faster?  
SmartChurn explores this paradox using predictive modeling and explainable AI — revealing how pricing, contracts, and engagement channels drive customer churn in the energy sector.

## Objectives
- Predict customers at risk of churn using **XGBoost**
- Explain **why** they churn with **SHAP**
- Simulate **discount-based retention scenarios** (5%, 10%, 20%)
- Identify the **optimal strategy** balancing retention and ROI

## Workflow
1. **Data Prep:** 14K records; handled imbalance (10% churn) with SMOTE  
2. **Modeling:** XGBoost + threshold tuning (Precision–Recall F1 optimization)  
3. **Explainability:** SHAP values → top drivers (`origin_up_*`, `months_renewal`, `channel_*`)  
4. **Scenario Testing:** Discount simulations → churn, revenue, and ΔSHAP shifts  

## Key Insights
| Insight | Interpretation | Implication |
|----------|----------------|--------------|
| **Contract Origin** | Top churn driver | Improve onboarding channels |
| **Renewal Months** | Loyalty indicator | Engage before contract expiry |
| **Discounts** | Raise churn risk | Avoid blanket discounts |

## Impact
Discounts >10% **increase churn probability** and reduce ROI.  
Customer **engagement** and **tenure stability** matter more than monetary incentives.
