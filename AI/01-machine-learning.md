[العربي](./01-machine-learning_ar.md)

# <a name="-1-machine-learning"></a>🤖 Chapter 1: Machine Learning (ML)

## 1. What is it?
Machine Learning (ML) is the field of designing algorithms and statistical models that allow systems to learn patterns from data and make predictions or decisions without being explicitly programmed for each task.

## 2. What does the specialist do?
The ML specialist frames problems as predictive or descriptive tasks, collects and cleans datasets, engineers features, selects and trains models (from linear models to ensemble methods), evaluates models using appropriate metrics, and documents models for handoff or deployment. They aim for reproducibility and explainability.

## 3. Sub-domains
- Supervised learning (classification, regression)  
- Unsupervised learning (clustering, density estimation)  
- Semi-supervised learning  
- Ensemble methods (bagging, boosting)  
- Anomaly detection  
- Online / incremental learning

## 4. Expanded Key Concepts
- Data lifecycle: collection, cleaning, train/val/test split  
- Feature engineering and representation  
- Model selection and cross-validation  
- Bias–variance trade-off and regularization (L1/L2)  
- Evaluation metrics (accuracy, precision/recall, F1, ROC-AUC, RMSE)  
- Handling class imbalance and calibration

## 5. Expanded Tools & Technologies
- Languages & basics: Python, SQL, Jupyter  
- Libraries: scikit-learn, XGBoost, LightGBM, CatBoost, pandas, numpy  
- Experiment tracking: MLflow, Weights & Biases  
- Pipelines: Airflow, Prefect, Spark (for large data)

## 6. In-Depth Workflow (example: churn prediction)
1. Problem framing and success metric.  
2. Data ingestion and exploratory data analysis (EDA).  
3. Feature engineering (aggregates, encodings).  
4. Baseline models and validation strategy.  
5. Model training, tuning (Optuna/GridSearch), and calibration.  
6. Interpretation (SHAP) and documentation.  
7. Packaging model artifact and spec for deployment.

## 7. Common Job Roles
- Machine Learning Engineer (applied)  
- Data Scientist (predictive modeling)  
- ML Research Engineer (applied research)

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`AUC`** | The area under the ROC curve. |
| **`Bagging`** | A bootstrap-based ensemble technique to reduce variance. |
| **`Cross-Validation`** | A method for estimating model performance. |
| **`Decision Tree`** | A tree-like model of decisions. |
| **`Ensemble`** | A collection of multiple models. |
| **`Feature`** | An input variable to the model. |
| **`Gradient Boosting`** | A sequential ensemble method to improve errors. |
| **`Hyperparameter`** | A parameter that is set before the training process. |
| **`Imputation`** | Filling in missing values. |
| **`Loss`** | The objective function that the model tries to minimize. |
| **`Overfitting`** | Over-learning and failure to generalize. |
| **`Precision / Recall / F1`** | Important classification metrics. |
| **`Regularization`** | Mechanisms to reduce overfitting. |
| **`RMSE`** | A regression error metric. |
| **`Train/Test Split`** | Splitting data to test generalization. |
| **`Validation Set`** | A set for model and parameter selection. |

</details>

[⬆️ Back to Table of Contents](./README_AI_en.md)
