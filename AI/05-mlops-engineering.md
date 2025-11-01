[العربي](./05-mlops-engineering_ar.md)

# <a name="-5-mlops-ml-engineering"></a>🤖 Chapter 5: MLOps & ML Engineering

## 1. What is it?
MLOps applies DevOps and software engineering best practices to the ML lifecycle: reproducible training, CI/CD for models, deployment, monitoring, and governance.

## 2. What does the specialist do?
An MLOps engineer designs reproducible pipelines, automates training and deployment, manages model/version registries, implements monitoring and drift detection, and ensures governance and reproducibility.

## 3. Sub-domains
- CI/CD and pipelines orchestration (Airflow, Argo)  
- Experiment tracking and model registry (MLflow, W&B)  
- Data versioning and feature stores (DVC, Feast)  
- Monitoring, observability, and retraining triggers

## 4. Expanded Key Concepts
- Reproducibility: data/code/config versioning  
- Lineage and provenance for traceability  
- Canary & blue/green deployments and rollback strategies  
- Drift detection (covariate & concept) and automated retraining

## 5. Expanded Tools & Technologies
- Docker, Kubernetes, Helm, GitOps tools (ArgoCD)  
- MLflow, Weights & Biases, DVC, LakeFS, Feast  
- Prometheus, Grafana, ELK Stack for monitoring

## 6. In-Depth Workflow (example: production ML pipeline)
1. Data ingestion with scheduled workflows (Airflow/Prefect).  
2. Training triggered by CI pipeline; track experiments in MLflow.  
3. Package model in Docker and push to registry.  
4. Deploy to Kubernetes with canary rollouts and health checks.  
5. Monitor SLOs/SLIs, set retraining triggers based on drift.

## 7. Common Job Roles
- MLOps Engineer  
- ML Platform Engineer  
- Production ML Engineer

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Canary Deployment`** | A technique to reduce the risk of introducing a new software version in production by slowly rolling out the change to a small subset of users before rolling it out to the entire infrastructure. |
| **`DVC`** | Data Version Control, a tool for data versioning. |
| **`Feature Store`** | A central repository for features. |
| **`Lineage`** | The data life cycle that includes the data's origins and where it moves over time. |
| **`MLflow`** | An open-source platform for managing the end-to-end machine learning lifecycle. |
| **`Prometheus`** | An open-source systems monitoring and alerting toolkit. |
| **`Retraining Trigger`** | A trigger that automatically retrains a model when a certain condition is met. |

</details>

[⬆️ Back to Table of Contents](./README_AI_en.md)
