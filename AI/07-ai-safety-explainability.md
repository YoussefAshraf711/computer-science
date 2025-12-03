[العربي](./07-ai-safety-explainability_ar.md)

# <a name="-7-ai-safety-explainability"></a>🤖 Chapter 7: AI Safety & Explainability

## 1. What is it?
AI Safety & Explainability covers methods and practices that make AI systems safer, more robust, interpretable, and aligned with human values and regulatory requirements.

## 2. What does the specialist do?
They run robustness and adversarial tests, implement interpretability methods (SHAP, LIME), measure fairness and bias, deploy privacy-preserving techniques, and build monitoring/governance processes.

## 3. Sub-domains
- Explainable AI (local & global explanations)  
- Robustness & adversarial ML  
- Fairness and bias mitigation  
- Privacy-preserving ML (differential privacy, secure aggregation)

## 4. Expanded Key Concepts
- Feature attributions (SHAP, LIME), counterfactual explanations  
- Adversarial attacks and defenses (FGSM, PGD, adversarial training)  
- Fairness metrics (statistical parity, equalized odds)  
- Privacy budgets and differential privacy concepts

## 5. Expanded Tools & Technologies
- SHAP, LIME, Captum for interpretability  
- CleverHans, Foolbox for adversarial testing  
- TensorFlow Privacy, Opacus for DP  
- RobustBench for benchmarks

## 6. In-Depth Workflow (example: auditing a credit scoring model)
1. Define stakeholder explanation needs and regulatory requirements.  
2. Compute global and local explanations (SHAP) for representative samples.  
3. Run fairness audits across protected groups and measure gaps.  
4. Apply mitigation strategies and document trade-offs.  
5. Set up ongoing monitoring for fairness and robustness.

## 7. Common Job Roles
- Responsible AI Engineer  
- AI Safety Researcher  
- Model Auditor

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Adversarial Example`** | An input to an AI model that is intentionally designed to cause the model to make a mistake. |
| **`Captum`** | A library for model interpretability in PyTorch. |
| **`Counterfactual`** | An explanation that describes what would have happened if something had been different. |
| **`Differential Privacy (DP)`** | A system for publicly sharing information about a dataset by describing the patterns of groups within the dataset while withholding information about individuals in the dataset. |
| **`Fairness`** | The property of an AI model that its predictions are not biased towards or against certain groups of people. |
| **`Foolbox`** | A library for creating adversarial examples. |
| **`LIME`** | Local Interpretable Model-agnostic Explanations, a technique for explaining the predictions of any classifier in an interpretable and faithful manner. |
| **`Robustness`** | The ability of an AI model to maintain its performance on unseen data. |
| **`SHAP`** | SHapley Additive exPlanations, a game theoretic approach to explain the output of any machine learning model. |

</details>

[⬆️ Back to Table of Contents](./README.md)
