[العربي](./08-data-science_ar.md)

# <a name="-8-data-science"></a>🔬 Chapter 8: Data Science

## 1. What is it?

Data Science is an interdisciplinary field that uses scientific methods, processes, algorithms, and systems to extract knowledge and insights from structured and unstructured data. It doesn't just describe the past; it aims to predict the future and discover hidden patterns that cannot be seen through traditional analysis.

If the data analyst is the "detective," the data scientist is the "scientist in the lab" who forms hypotheses, runs experiments on data using advanced statistics and machine learning, and discovers new principles. They answer questions like, "What will happen?" and "How can we make something happen?".

## 2. What does the specialist do?

 * Formulating problems: Transforming complex business problems (like "How do we reduce customer churn?") into clear statistical or machine learning problems (like "Build a classification model to predict customers at risk of churning").
 * Data collection and exploration (EDA): Exploratory data analysis to understand its properties, distributions, and the relationships between its variables.
 * Feature Engineering: Creating and engineering new variables (features) from raw data to help the model learn better.
 * Building and training models: Building Machine Learning Models and training them on historical data to predict future outcomes.
 * Evaluating models: Measuring the accuracy and performance of models using precise statistical metrics.
 * Communicating results: Explaining the model's results and their business impact to non-technical stakeholders in an understandable way.

## 3. Sub-domains

 * Predictive Modeling: Building models to predict future outcomes (e.g., sales forecasting, stock price prediction).
 * Natural Language Processing (NLP): Dealing with and analyzing text data (e.g., sentiment analysis, chatbots).
 * Computer Vision: Dealing with image and video data (e.g., object recognition, image classification).
 * Recommendation Systems: Building systems that suggest products or content to users (like Netflix and Amazon recommendations).
 * Causal Inference: Using statistics to determine cause-and-effect relationships, not just correlation.

## 4. Expanded Key Concepts

 * `Machine Learning`: The data scientist's primary toolkit. It includes:
     * `Supervised Learning`: Training on data that has correct "answers" (Labels). It is divided into Classification and Regression.
     * `Unsupervised Learning`: Training on data that has no answers, with the goal of discovering the internal structure (like Clustering).
 * `Modeling Process`:
     * `Train/Validation/Test Split`: Dividing the data into 3 sets: for training, for tuning the model, and for its final test.
     * `Cross-Validation`: A technique for more reliably evaluating a model by splitting the data into multiple parts and using them for training and testing interchangeably.
     * `Hyperparameter Tuning`: The process of finding the best internal settings for a model to achieve the highest performance.
 * `Overfitting vs. Underfitting`:
     * `Overfitting`: When the model memorizes the training data excessively (including noise), leading to poor performance on new data.
     * `Underfitting`: When the model is too simple and fails to capture the underlying pattern in the data.
 * `Deep Learning`: Using deep neural networks to solve complex problems, especially in the fields of NLP and Computer Vision.

## 5. Expanded Tools & Technologies

 * Programming Languages: Python (dominant, with Pandas, NumPy, Scikit-learn, Matplotlib libraries), R.
 * Machine Learning and Deep Learning Frameworks: Scikit-learn (for traditional machine learning), TensorFlow, PyTorch, Keras (for deep learning).
 * Work Environments: Jupyter Notebook, Google Colab.
 * Big Data Tools: Spark (especially PySpark).
 * Cloud Machine Learning Platforms: Google Vertex AI, Amazon SageMaker, Azure Machine Learning.

## 6. In-Depth Workflow

Project: Build a model to predict customer churn.

 1. Problem Formulation: In collaboration with the business team, "Churn" is precisely defined (e.g., a user who has not logged in for 30 days). The problem is a "Binary Classification."
 2. Data Collection and Exploration (EDA): The scientist queries the data warehouse for historical data on user behavior. Using a Jupyter Notebook, they visualize the data to look for relationships (Are users who contact customer service more likely to churn?).
 3. Feature Engineering and Preprocessing: They create new features (like "average session duration," "days since last login"). They handle missing values and scale numerical variables.
 4. Model Training: They split the data into a training set and a test set. They train several models (like Logistic Regression, Random Forest, Gradient Boosting) on the training data using Scikit-learn.
 5. Model Evaluation: They use the trained models to make predictions on the test data (which the model has not seen before). They evaluate their performance using metrics like Accuracy, Precision, Recall, and F1-Score.
 6. Hyperparameter Tuning: They choose the best model (e.g., Gradient Boosting) and tune its internal settings to get the best possible performance.
 7. Interpretation and Communication: They analyze the model to understand why it makes certain decisions (using techniques like Feature Importance). They present the results to management: "Our model can predict churn with 85% accuracy. The most important factors are days since last login and the number of contacts with customer service."
 8. Handover for Deployment: The scientist hands over the final trained model and feature engineering logic to an ML Engineer to deploy it in the production environment.

## 7. Common Job Roles

 * Data Scientist
 * Machine Learning Scientist (often more focused on research and developing new algorithms).
 * NLP Scientist: A scientist specializing in natural language processing.
 * Computer Vision Engineer: An engineer specializing in computer vision.

## 8. A-Z Glossary
<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Accuracy`** | The ratio of correct predictions to the total number of predictions. |
| **`Algorithm`** | A set of rules and steps that a model follows to learn. |
| **`Classification`** | A machine learning task to classify data into specific categories (e.g., "Spam" or "Not Spam"). |
| **`Clustering`** | An unsupervised learning task to group similar data together. |
| **`Cross-Validation`** | A technique for reliably evaluating a model. |
| **`Confusion Matrix`** | A table used to describe the performance of a classification model. |
| **`Ensemble Methods`** | Techniques that combine several models to get a better prediction (e.g., `Random Forest`). |
| **`Feature`** | An input variable used by the model to make a prediction (a column in the dataset). |
| **`Feature Engineering`** | The art and science of creating new features from raw data. |
| **`F1-Score`** | A metric that balances `Precision` and `Recall`. |
| **`Hyperparameter`** | An external setting for a model that is tuned before the training process. |
| **`Label`** | The "answer" or target value that the model tries to predict in supervised learning. |
| **`Model`** | The mathematical output of the process of training an algorithm on data. |
| **`Overfitting`** | When a model learns the training data too well and fails with new data. |
| **`Precision`** | In classification, the ratio of true positive predictions to the total number of positive predictions. |
| **`Recall`** | The ratio of true positive predictions that the model was able to capture. |
| **`Regression`** | A machine learning task to predict a continuous numerical value (like price). |
| **`Scikit-learn`** | The most popular library in Python for traditional machine learning. |
| **`Supervised Learning`** | Where the model is trained on labeled data. |
| **`TensorFlow`** | An open-source framework from Google for deep learning. |
| **`Train/Test Split`** | Splitting the data into a set for training and another for testing. |
| **`Underfitting`** | When a model is too simple to capture the pattern in the data. |

</details>

[⬆️ Back to Table of Contents](README.md)