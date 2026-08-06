# LLM-API-Cost-Prediction-Routing-Optimization-
# LLM Cost Intelligence: Diagnosing Spend & Predicting High-Cost Requests

## Business Problem
[1-2 sentences — same as your notebook intro]

## Key Findings
- GPT-4.1 drives 53% of total cost despite being only 25% of requests
- No cost-aware routing exists — model usage is flat across all task types
- ~15% of total spend ($33) is avoidable by routing simple tasks to cheaper models

## Approach
1. EDA on cost drivers (model, task type, language)
2. Identified and fixed a broken target column (`budget_exceeded`)
3. Built a leakage-free classifier to predict high-cost requests pre-routing
4. Compared Logistic Regression, Random Forest, and XGBoost

## Results
| Model | Precision | Recall |
|---|---|---|
| Logistic Regression | 0.25 | 0.79 |
| Random Forest | 0.23 | 0.96 |
| XGBoost | 0.23 | 0.95 |

## Tools
Python · pandas · scikit-learn · XGBoost · matplotlib

## Repo Structure
[paste the tree above]

## How to Run
git clone this repo → pip install -r requirements.txt → open notebooks/LLM_cost_intelligence.ipynb
