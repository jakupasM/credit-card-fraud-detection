# 💳 Credit Card Fraud Detection

A machine learning project that detects fraudulent credit card transactions using Logistic Regression and Random Forest.

## 📌 Project Overview

Credit card fraud detection is a highly imbalanced classification problem because fraudulent transactions represent only a very small percentage of all transactions.

The goal of this project is to identify fraudulent transactions while reducing false alarms.

## 📊 Dataset

- Total transactions: 284,807
- Fraudulent transactions: 492
- Features: 30
- Target:
  - `0` = Legitimate transaction
  - `1` = Fraudulent transaction

The dataset contains anonymized PCA-transformed features `V1` through `V28`, along with `Time`, `Amount`, and `Class`.

## ⚠️ Dataset Setup

The dataset is not included in this repository because it exceeds GitHub's file-size limit.

1. Download `creditcard.csv` from the Kaggle Credit Card Fraud Detection dataset.
2. Place it inside:

```text
data/creditcard.csv
```

3. Open and run:

```text
notebooks/credit_card_fraud_detection.ipynb
```

## 🧹 Data Preprocessing

- Checked the dataset shape and missing values
- Analyzed the class distribution
- Split the original dataset into training and testing sets
- Preserved the original class imbalance in the test set
- Applied random under-sampling only to the training set
- Standardized the `Time` and `Amount` features using `StandardScaler`

## 🤖 Machine Learning Models

- Logistic Regression
- Random Forest Classifier

## 📈 Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC-AUC

## 🏆 Results

| Model | Accuracy | ROC-AUC |
|---|---:|---:|
| Logistic Regression | 0.9603 | 0.9759 |
| Random Forest | 0.9666 | 0.9768 |

### Confusion Matrices

**Logistic Regression**

```text
[[54612 2252]
 [    8   90]]
```

**Random Forest**

```text
[[54968 1896]
 [    9   89]]
```

Random Forest reduced the number of false positives, while Logistic Regression detected one additional fraudulent transaction.

## ⭐ Feature Importance

The most important Random Forest features were:

- V14
- V12
- V10
- V17
- V4

Because the dataset was anonymized using PCA, the original meaning of these features is not publicly available.

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook
- Visual Studio Code

## 📂 Project Structure

```text
credit-card-fraud-detection/
├── data/
│   └── creditcard.csv
├── images/
├── notebooks/
│   └── credit_card_fraud_detection.ipynb
├── .gitignore
├── requirements.txt
└── README.md
```

## 🚀 Future Improvements

- Compare random under-sampling with SMOTE
- Tune model hyperparameters
- Test XGBoost and LightGBM
- Optimize the classification threshold
- Add Precision-Recall and ROC curves

## 👨‍💻 Author

Mario Jakupas  
M.S. Computer Science  
Interested in Data Science, Machine Learning, and Artificial Intelligence
