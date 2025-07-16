# 🛡 Fraud Detection System

A machine learning project to detect fraudulent transactions using a real-world anonymized dataset.

## 📂 Dataset

The dataset (data.csv) is an anonymized collection of financial transactions, containing both normal and fraudulent activities. Each transaction includes several numerical features derived from PCA transformations, as well as a Class label indicating fraud (1) or legitimate (0).

## 📊 Features

- 28 PCA-transformed features: V1 to V28
- Time: Seconds elapsed between this transaction and the first transaction in the dataset
- Amount: Transaction amount
- Class: Target variable (1 for fraud, 0 for legitimate)

## 🧠 Model Pipeline

1. *Data Preprocessing*
   - Standard scaling of Amount and Time
   - Handling imbalanced classes using techniques like SMOTE or undersampling

2. *Modeling*
   - Algorithms: Logistic Regression, Random Forest, XGBoost, etc.
   - Cross-validation and hyperparameter tuning using GridSearchCV

3. *Evaluation Metrics*
   - Accuracy, Precision, Recall, F1-Score, ROC-AUC
   - Confusion Matrix visualization

## 📈 Results

The Random Forest model achieved:

- *Accuracy*: ~94.8%
- *Precision*: ~91.0%
- *Recall*: ~87.0%
- *F1 Score*: ~89.0%
- *AUC*: ~98.0%

> Note: Due to class imbalance, we prioritize *Recall* to minimize false negatives (missed frauds).

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/Ritam200/Fraud_detection_app.git
cd fraud-detection

# Install dependencies
pip install -r requirements.txt

# Run the script
python fraud_detection.py 
