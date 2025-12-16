# SmartChurn — Predicting & Understanding Customer Churn

> *“What if the discounts meant to keep customers actually made them leave?”*  

SmartChurn predicts which energy customers are likely to churn, explains **why**, and simulates **discount-based retention strategies** (5%, 10%, 20%) to guide data-driven decisions.


## Key Impact

- **3× more churners identified** after threshold tuning  
- **Optimal discount** (~10%) for retention without harming ROI  
- Data-driven insights for **personalized retention and engagement**

## How It Works

1. **Predict** churn with XGBoost + SMOTE  
2. **Explain** predictions using SHAP  
3. **Simulate** discount effects on churn & ROI  
4. **Generate** actionable retention strategies

## Churn Prediction Results

| Metric | Default Threshold (0.5) | Tuned Threshold (0.24) |
|--------|--------|-------|
| Recall (Churners) | 15% | **33%** |
| Accuracy | 91% | 87% |
| ROC-AUC | 0.68 | **0.70** |

## What Drives Churn?

- **Contract Origin & Renewal Timing** — biggest churn predictors  
- **Engagement Channels** — effective for retention  
- **Price & Margin** — secondary to experience

## Discount Simulation Insights

| Discount | Churn Effect | ROI |
|----------|-------------|-----|
| 5% | small reduction | neutral |
| 10% | **~8.5% reduction** | optimal |
| 20% | limited | negative |

*Moderate incentives work best; aggressive discounts can **backfire**.*
