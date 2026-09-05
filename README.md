# Customer Churn Prediction

A machine learning project that predicts whether a customer is likely to **churn or stay** based on customer-related features.

The project explores data preprocessing, feature engineering, classification models, model evaluation, and threshold tuning to improve churn detection.

## 📌 Project Overview

Customer churn is an important business problem because identifying customers who are likely to leave can help companies take proactive retention actions.

In this project, different machine learning approaches are used to predict the `Customer_Status` target variable, which contains two classes:

* **Churned**
* **Stayed**

The notebook includes data preprocessing, exploratory analysis, model training, evaluation, and comparison between multiple classification models.

## 📊 Dataset

The dataset contains **6,418 customer records** with numerical and categorical customer-related features.

The target variable is:

```text
Customer_Status
```

The dataset is obtained through Kaggle within the notebook.

> **Note:** The raw dataset is not included in this repository.

## 🤖 Machine Learning Models

The project evaluates the following models:

### 1. Logistic Regression

A baseline classification model used to establish an initial performance benchmark.

### 2. Random Forest

An ensemble learning model consisting of multiple decision trees. It is evaluated against Logistic Regression to compare classification performance.

### 3. Tuned Random Forest

The Random Forest model is further tuned to improve its ability to identify customers who are likely to churn.

### 4. Threshold-Tuned Random Forest

The classification threshold is adjusted to **0.58** in order to improve the balance between precision and recall for churn detection.

## 📈 Model Performance

The main evaluation results obtained in the notebook are:

| Model                     | Accuracy | Precision (Churn) | Recall (Churn) | F1-Score (Churn) |   ROC-AUC |
| ------------------------- | -------: | ----------------: | -------------: | ---------------: | --------: |
| Logistic Regression       |     0.75 |              0.53 |           0.81 |             0.64 |     0.857 |
| Random Forest             |     0.82 |              0.69 |           0.58 |             0.63 |     0.858 |
| Tuned Random Forest       |     0.79 |              0.59 |           0.73 |             0.65 |     0.861 |
| Tuned RF — Threshold 0.58 |     0.78 |              0.58 |           0.77 |         **0.66** | **0.861** |

### Key Observations

* **Random Forest** achieved the highest accuracy at **82%**.
* **Logistic Regression** achieved a high churn recall of **81%**, making it effective at identifying customers who churn.
* **Tuned Random Forest** improved the balance between precision and recall.
* Adjusting the Random Forest decision threshold to **0.58** produced the highest churn F1-score of **0.66**.
* The tuned models achieved a ROC-AUC of **0.861**, indicating strong overall classification ability.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook / Google Colab
* Kaggle Dataset

## 🔄 Project Workflow

```text
Data Collection
      ↓
Data Exploration
      ↓
Data Preprocessing
      ↓
Feature Preparation
      ↓
Train/Test Split
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Random Forest Tuning
      ↓
Threshold Optimization
      ↓
Model Comparison
```

## 📂 Repository Structure

```text
customer-churn-prediction/
│
├── Customer_Churn_Prediction.ipynb
└── README.md
```

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Marokhaled/customer-churn-prediction.git
```

### 2. Open the notebook

Open:

```text
Customer_Churn_Prediction.ipynb
```

You can run it using **Google Colab** or **Jupyter Notebook**.

### 3. Run the cells

Execute the notebook cells from top to bottom to reproduce the preprocessing, model training, evaluation, and results.

## 🎯 Project Goals

The main objectives of this project are to:

* Predict customer churn using machine learning.
* Compare different classification algorithms.
* Evaluate models using accuracy, precision, recall, F1-score, and ROC-AUC.
* Improve Random Forest performance through model tuning.
* Explore how changing the classification threshold affects churn prediction.
* Demonstrate a complete end-to-end machine learning workflow.


