<p align="center">
  <img src="chart_images/btc banner.png" alt="Bitcoin Price Direction Prediction Banner" width="100%">
</p>

<h1 align="center">₿ Bitcoin Price Direction Prediction using Machine Learning</h1>

<p align="center">
Predicting the next-day direction of Bitcoin prices using supervised machine learning algorithms, feature engineering, and financial market analysis.
</p>

<p align="center">

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?style=for-the-badge&logo=scikitlearn)
![XGBoost](https://img.shields.io/badge/XGBoost-Ensemble-success?style=for-the-badge)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-black?style=for-the-badge&logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-blueviolet?style=for-the-badge&logo=numpy)

</p>

---

# 📖 Project Overview

Bitcoin is one of the world's most volatile financial assets, making the prediction of its price movements a challenging problem in financial analytics and machine learning. Instead of forecasting the exact future price, this project focuses on predicting whether the price of Bitcoin will move **up or down on the next trading day**.

A complete end-to-end machine learning workflow was implemented, beginning with data preprocessing and exploratory data analysis, followed by feature engineering, model training, and comprehensive performance evaluation. Historical Bitcoin market data was transformed into informative predictors that capture market behaviour and improve the learning capability of the models.

Six supervised machine learning algorithms were trained and compared using multiple evaluation metrics, including Accuracy, Precision, Recall, F1-Score, and ROC-AUC. The project demonstrates how different machine learning techniques perform on a real-world financial prediction task while highlighting the importance of feature engineering and model evaluation in quantitative finance.

---

## 🎯 Key Highlights

- 📈 Predicts the next-day direction of Bitcoin prices.
- 🤖 Compares six supervised machine learning algorithms.
- 📊 Performs Exploratory Data Analysis (EDA).
- ⚙️ Applies feature engineering to financial market data.
- 📉 Evaluates models using multiple classification metrics.
- 📚 Demonstrates a complete end-to-end machine learning workflow.

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook
-                

# 🎯 Business Problem

Bitcoin is one of the most actively traded cryptocurrencies in the world, characterised by high price volatility and rapidly changing market conditions. Accurately predicting short-term market movements remains a significant challenge due to the complex and non-linear behaviour of financial markets.

Rather than forecasting the exact future price of Bitcoin, this project addresses a binary classification problem by predicting whether the next day's closing price will be **higher or lower** than the current day's closing price. Such predictions can provide valuable insights for traders, investors, and researchers seeking to understand market behaviour and evaluate data-driven trading strategies.

This project investigates whether supervised machine learning algorithms can identify meaningful patterns from historical market data and engineered financial features to improve the prediction of Bitcoin price direction.

# 🎯 Project Objectives

The primary objectives of this project are to:

- Develop an end-to-end machine learning pipeline for Bitcoin price direction prediction.
- Perform exploratory data analysis to understand the characteristics of the dataset.
- Engineer informative financial features from historical Bitcoin market data.
- Train multiple supervised machine learning models for binary classification.
- Compare model performance using multiple evaluation metrics.
- Identify the strengths and limitations of each machine learning algorithm.
- Provide recommendations for improving predictive performance in future work.
# 📂 Dataset

The dataset consists of historical Bitcoin market data containing daily trading information. Each observation includes the following market variables:

- Date
- Open Price
- High Price
- Low Price
- Close Price
- Adjusted Close Price
- Trading Volume

Additional predictive variables were generated through feature engineering to capture market behaviour more effectively. These engineered features provide the machine learning models with additional information beyond the original market variables.
# 🔄 Project Workflow

```text
Historical Bitcoin Market Data
            │
            ▼
     Data Preprocessing
            │
            ▼
Exploratory Data Analysis
            │
            ▼
    Feature Engineering
            │
            ▼
      Train-Test Split
            │
            ▼
 Machine Learning Models
            │
            ▼
   Performance Evaluation
            │
            ▼
    Model Comparison
            │
            ▼
  Best Performing Model
```
# 📊 Exploratory Data Analysis (EDA)

Before training the machine learning models, exploratory data analysis (EDA) was performed to understand the characteristics of the dataset, identify relationships between variables, and uncover patterns that could influence model performance.

The analysis focused on data quality, target distribution, feature relationships, and the statistical behaviour of the engineered financial variables.
## 📈 Class Distribution

<p align="center">
  <img src="chart_images/Target Distributon.png" width="700">
</p>

### Observation

The target variable exhibits a relatively balanced distribution between upward and downward Bitcoin price movements. This balanced class distribution reduces the likelihood of model bias towards a single class and allows evaluation metrics such as Accuracy, Precision, Recall, and F1-Score to provide meaningful performance comparisons.
## 🔥 Correlation Heatmap

<p align="center">
  <img src="chart_images/Feature correlation.png" width="700">
</p>

### Observation

The correlation heatmap illustrates the relationships among the numerical variables within the dataset. Strong positive correlations were observed between the Open, High, Low, Close, and Adjusted Close prices, reflecting their shared dependence on daily market movements. These insights informed the feature engineering process by highlighting which variables contain complementary information for predicting Bitcoin price direction.

# 📉 Confusion Matrix Analysis

Confusion matrices were used to evaluate how each machine learning model classified Bitcoin price movements. Unlike accuracy alone, confusion matrices provide detailed insight into true positives, true negatives, false positives, and false negatives, helping to identify model biases and classification behaviour.

---

## Logistic Regression

<p align="center">
  <img src="chart_images/confusionmatlog.png" alt="Logistic Regression Confusion Matrix" width="500">
</p>

**Observation**

The Logistic Regression model predicted every validation sample as the positive class (Class 1), resulting in an overall accuracy of **54.14%**. However, it failed to correctly classify any negative-class observations, indicating poor class discrimination despite its higher accuracy.

---

## Support Vector Machine (Polynomial)

<p align="center">
  <img src="chart_images/confusionmatsv.png" alt="Support Vector Machine Confusion Matrix" width="500">
</p>

**Observation**

The Support Vector Machine exhibited behaviour nearly identical to Logistic Regression, predicting all samples as the positive class. While achieving the same overall accuracy (**54.14%**), the model was unable to distinguish between the two classes effectively.

---

## XGBoost

<p align="center">
  <img src="chart_images/confusionmatxg.png" alt="XGBoost Confusion Matrix" width="500">
</p>

**Observation**

Unlike the previous models, XGBoost successfully predicted both positive and negative classes. Although its overall accuracy (**48.25%**) was lower, the confusion matrix shows a more balanced classification pattern, demonstrating the model's ability to learn decision boundaries for both classes rather than predicting a single outcome.
### Observation

The confusion matrix provides a detailed summary of the classification performance by comparing predicted labels with the actual outcomes. It highlights the number of correctly classified observations alongside false positives and false negatives, enabling a deeper assessment of the model beyond overall accuracy.
# 📊 Model Performance Comparison

The three machine learning models were evaluated using multiple classification metrics to compare their ability to predict the next-day direction of Bitcoin prices.

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|--------|---------:|----------:|--------:|----------:|---------:|
| Logistic Regression | **54.14%** | 0.29 | 0.54 | 0.38 | **0.5210** |
| Support Vector Machine (Polynomial) | **54.14%** | 0.29 | 0.54 | 0.38 | 0.4885 |
| XGBoost | 48.25% | **0.51** | 0.48 | **0.44** | 0.4953 |

# 🏆 Model Ranking

The models were ranked based on their overall predictive performance while considering the balance between Accuracy, Precision, Recall, F1-Score, and ROC-AUC.

| Rank | Model | Remarks |
|------|-------|---------|
| 🥇 | Logistic Regression | Highest ROC-AUC and tied highest accuracy, but predicted only one class. |
| 🥈 | Support Vector Machine (Polynomial) | Similar behaviour to Logistic Regression with slightly lower ROC-AUC. |
| 🥉 | XGBoost | Lower accuracy but demonstrated better balance by correctly identifying both classes. |

# 💬 Discussion of Results

The evaluation revealed that **Logistic Regression** and **Support Vector Machine (Polynomial Kernel)** achieved the highest overall accuracy of **54.14%**. However, a closer inspection of the confusion matrices and classification reports showed that both models predicted every validation sample as the positive class. As a result, neither model successfully identified any observations belonging to the negative class, leading to zero precision, recall, and F1-score for that class.

Although **XGBoost** achieved a lower overall accuracy (**48.25%**), it demonstrated a more balanced classification performance by correctly identifying observations from both classes. This behaviour resulted in improved weighted precision and F1-score compared to the other models.

These findings demonstrate that **accuracy alone is insufficient when evaluating classification models**, particularly in financial prediction tasks. Metrics such as Precision, Recall, F1-Score, ROC-AUC, and the confusion matrix provide a more comprehensive understanding of model behaviour and should be considered alongside accuracy when selecting the most appropriate model.
# 💻 Installation

Clone the repository:

```bash
git clone https://github.com/Liquidfingers/Bitcoin-Price-Direction-Prediction.git
```

Navigate to the project directory:

```bash
cd Bitcoin-Price-Direction-Prediction
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```
