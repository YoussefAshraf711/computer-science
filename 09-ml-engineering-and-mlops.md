[العربي](./09-ml-engineering-and-mlops_ar.md)

# <a name="-9-ml-engineering-and-mlops"></a>🤖 Chapter 9: ML Engineering and MLOps

## 1. What is it?

ML Engineering and MLOps is the engineering discipline that applies DevOps principles to machine learning systems. The goal is to automate and streamline the entire lifecycle of machine learning models, from data collection and model training to deployment and monitoring in a production environment, all in a reliable and repeatable way.

Simply put, if the data scientist "invents" the smart model, the ML engineer "builds the factory" that produces and operates this model at scale.

## 2. What does the specialist do?

An ML engineer is the bridge between the experimental data science world and the real production environment. Their tasks include:

* Turning models into products: Taking the experimental code (often from a Jupyter Notebook) from the data scientist, refactoring it, and turning it into robust, production-ready software.
* Building automated pipelines: Creating automated systems for continuously collecting data, processing it, and training models (known as CI/CD/CT).
* Model Deployment: Building APIs to serve model predictions and deploying them as scalable and reliable services.
* Monitoring models in production: Building systems to monitor model performance over time and detect any degradation in its accuracy (a phenomenon called Model Drift).
* Managing ML infrastructure: Building and managing the systems on which the models run, such as Kubernetes clusters equipped with GPUs.

## 3. Sub-domains

* ML Infrastructure: Focuses on building and managing the hardware and software needed to train and serve models.
* ML Automation: Focuses on building CI/CD/CT pipelines for continuous training and deployment.
* Model Serving: Specializes in deploying models to achieve the lowest possible latency and handle a high number of requests (High Throughput).
* Model Monitoring: Focuses on building systems to track model accuracy, data drift, and other performance metrics in real-time.

## 4. Expanded Key Concepts

* `MLOps Lifecycle`: The machine learning lifecycle, which is a continuous loop: Data Collection → Data Validation → Feature Engineering → Model Training → Model Analysis → Model Serving → Model Monitoring → (and back to the beginning).
* `Reproducibility`: The ability to re-run any part of the process (data preparation, training) and get the exact same results. This is crucial for debugging and regulatory compliance.
* `CI/CD/CT`:
  * `Continuous Integration`: Continuously testing the code.
  * `Continuous Delivery`: Continuously preparing a deployable release after CI succeeds.
  * `Continuous Training`: Automatically retraining the model on new data.
* `Experiment Tracking`: Recording everything about each training run: parameters, code version, data version, and results.
* `Model Registry`: A central repository for storing, versioning, and managing trained models.
* `Feature Store`: A central repository for production-ready engineered features that can be shared among different models.
* `Model Drift`: The degradation of a model's performance over time because the characteristics of live production data have changed from the training data.

## 5. Expanded Tools & Technologies

* Pipeline Orchestration: Kubeflow, Apache Airflow.
* Experiment Tracking and Model Registry: MLflow, Weights & Biases (W&B).
* Data and Feature Versioning: DVC (Data Version Control), Feast.
* Model Serving: TensorFlow Serving, TorchServe, KServe.
* Monitoring: Prometheus, Grafana, Evidently AI.
* Infrastructure: Docker, Kubernetes (K8s).
* Cloud Platforms: Amazon SageMaker, Google Vertex AI, Azure Machine Learning.

## 6. In-Depth Workflow

Project: Turn the "Customer Churn Prediction Model" into a real product.

 1. Containerize Training: The MLOps engineer takes the data scientist's code, refactors it into clean Python scripts, and creates a Dockerfile to package the training code and all dependencies into a container.
 2. Build a CI/CT Pipeline (using GitHub Actions and Kubeflow):
     * Trigger: The pipeline runs automatically on a new code merge or on a schedule (e.g., weekly).
     * Data Validation: The first step is to pull new data and validate its format. If the data schema changes, the pipeline fails and alerts the team.
     * Model Retraining: The training container is run on a Kubernetes cluster.
     * Experiment Tracking: All model parameters and evaluation metrics (like accuracy) are automatically logged in MLflow.
     * Model Registration: The new model's performance is compared to the currently deployed model. If it's better, it is "promoted" and saved in the MLflow Model Registry.
 3. Build a CD Pipeline (Continuous Deployment):
     * Trigger: Promoting a new model in the registry triggers the deployment pipeline.
     * Create a Serving API: A FastAPI service is built that loads the new model from the registry and exposes a prediction endpoint. This service is also containerized using Docker.
     * Canary Deployment: The pipeline deploys the new model container to production, initially directing only a small percentage of traffic (e.g., 5%) to it.
 4. Monitoring:
     * The engineer monitors the new model's performance (like response time and error rate) using Prometheus and Grafana.
     * They use a tool like Evidently AI to compare the distribution of live production data with the training data to detect Data Drift.
     * If the new model is stable, traffic is gradually shifted to 100%. If it fails, it is automatically rolled back to the previous version.

## 7. Common Job Roles

* ML Engineer (Machine Learning Engineer)
* MLOps Engineer
* AI Platform Engineer (builds the infrastructure for AI teams).

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`CI/CD/CT`** | Continuous Integration / Continuous Delivery / Continuous Training. |
| **`Concept Drift`** | A type of model drift where the relationship between features and the target changes. |
| **`Data Drift`** | A type of model drift where the distribution of the input data itself changes. |
| **`DVC`** | Data Version Control, like `Git` but for data. |
| **`Experiment Tracking`** | The process of logging all parameters and results of model training experiments. |
| **`Feature Store`** | A central repository for production-ready features. |
| **`Inference`** | The process of using a trained model to make predictions on new data. |
| **`Kubeflow`** | An open-source platform for making ML workflows on `Kubernetes` simple and portable. |
| **`MLflow`** | An open-source platform for managing the entire machine learning lifecycle. |
| **`Model Drift`** | The degradation of a model's performance over time. |
| **`Model Registry`** | A central repository for managing versions of trained models. |
| **`Orchestration`** | Organizing and coordinating a complex workflow composed of multiple steps. |
| **`Reproducibility`** | The ability to replicate results exactly. |
| **`Serving`** | The process of making a model available to receive prediction requests. |

</details>

[⬆️ Back to Table of Contents](README.md)

