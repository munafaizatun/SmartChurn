# SmartChurn — Discount Impact & Explainable ROI

> *“Discounts intended to keep customers may actually push them away.”*

SmartChurn analyzes how retention discounts affect customer churn and revenue using **XGBoost** and **SHAP (explainable AI)**. Instead of blindly offering incentives, it quantifies **who is at risk, why, and how price changes influence loyalty**.

## Key Insights

- **All tested discounts (5%, 10%, 20%) increased churn.**  
- **ROI was negative for all discount levels**, showing that blanket price cuts can hurt revenue.  
- **Customer perception drives behavior**: SHAP revealed price variance, contract timing, and engagement channels as main factors.  
- **Targeted retention matters more than discounts**: personalized strategies based on risk and engagement are more effective than uniform offers.

## What I Did

- Predicted churn probabilities with **XGBoost**.  
- Explained feature importance and discount impact with **SHAP**.  
- Simulated multiple discount scenarios to evaluate **churn and ROI trade-offs**.  
- Generated actionable recommendations to **protect revenue and customer trust**.

## Takeaways for Business

1. Discounts are not universally beneficial — they can backfire.  
2. Engage customers **before contract expiry** and prioritize high-risk segments.  
3. Use **explainable AI insights** to design stable pricing and retention strategies.
