# Customer-Churn-Prediction-LR-SVM

## Table of Contents
- [Project Overview](#project-overview)
- [Project Structure](#project-structure)
- [Dataset](#dataset)
  - [Data Overview](#data-overview)
  - [Data Cleaning](#data-cleaning)
  - [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
  - [Logistic Regression](#logistic-regression)
  - [Support Vector Machine](#support-vector-machine)
- [Evaluation Metrics](#evaluation-metrics)
---
## Project Overview
This project is dedicated to predicting customer churn using **Logistic Regression (LR)** and **Support Vector Machine (SVM)** models. Customer churn prediction is a crucial task for businesses looking to improve retention by identifying potential churners early. The project was developed as a final project for my Foundations of Artificial Intelligence course, applying machine learning techniques to a practical, real-world problem.

The notebook includes comments and explanations at each step, guiding the user through data processing, model selection, evaluation, and analysis of results, making it suitable for both technical and non-technical audiences.

---

## Project Structure
- **CustomerChurnPrediction.ipynb**: Main Jupyter notebook containing all project stages, from data preprocessing to model evaluation. The notebook is structured and includes comments for clarity.
- **README.md**: Documentation of the project.

--- 

## Dataset

### Data Overview
This project uses the **IBM Telco Customer Churn** dataset, which provides information on a fictional telecommunications company’s customer base in California. The dataset includes 7,043 customers and contains various features such as:
- **Demographic information**: age, gender, etc.
- **Subscription details**: tenure, subscription type, monthly charges, total charges, etc.
- **Customer activity**: engagement metrics, support interactions, and historical usage patterns.

The target variable indicates whether a customer has churned (left the service) or not.

#### Dataset Links
- **About the Dataset**: [IBM Telco Customer Churn Overview](https://community.ibm.com/community/user/businessanalytics/blogs/steven-macko/2019/07/11/telco-customer-churn-1113)
- **Download the Dataset**: [Kaggle - IBM Telco Dataset](https://www.kaggle.com/datasets/sindhukotla/ibm-telco-dataset/data?select=Telco_customer_churn_demographics.xlsx)

### Data Cleaning: 
- Checked for missing values and appropriately assigned a value 
- Deleted duplicate rows

### Feature Engineering:
- Removed irrelevant features like ‘Customer ID’, ‘Country’, ‘State’, ‘Lat Long’
- Removed features that are directly associated with the target churn like ‘Churn Category’, ‘Churn Reason’, ‘Churn Score’, ‘Customer Status’ to prevent Data Leakage
- Handled categorical features using Label and One Hot Encoding to convert them into numerical
- Handled numerical features by scaling them as required for the model

Each step is thoroughly documented in the notebook, with comments explaining the rationale behind feature engineering choices.

---

## Modeling

### Logistic Regression
**Logistic Regression from sklearn** is used as a baseline model for churn prediction. It’s a widely used algorithm for binary classification due to its simplicity and interpretability. 

After the baseline model, we implement **Logistic Regression from scratch** to understand the inner workings of the algorithm. This includes a detailed explanation of the following mathematical concepts: Sigmoid Function, Log-Loss (Binary Cross-Entropy), Gradient Descent.

![image](https://github.com/user-attachments/assets/7108d7ba-51ff-496c-b67e-d20beb44c0f3)

### Support Vector Machine
**Support Vector Machine (SVM) from sklearn** is implemented as a more complex model that can capture non-linear relationships through kernel functions. 

After the library model, we implement **SVM from scratch** to understand the inner workings of the algorithm. This includes a detailed explanation of the following mathematical concepts: Objective Function, Hinge Loss, and Gradient Descent.

![image](https://github.com/user-attachments/assets/a69f6a23-8db2-4380-b65c-c56d9f151139)

---

## Evaluation Metrics
To measure the effectiveness of each model, several metrics are used:
- **Accuracy**: The overall correctness of predictions.
- **Precision and Recall**: Especially relevant for understanding model performance on churners (positive class).
- **F1 Score**: Balances precision and recall to provide a single metric for comparison.
- **Confusion Matrix**: Visual representation of true vs. predicted classes.
---
