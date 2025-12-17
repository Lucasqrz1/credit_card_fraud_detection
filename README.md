# Credit Card Fraud Detection

Machine learning project for detecting fraudulent credit card transactions using the public dataset from **ULB (Université Libre de Bruxelles)**. This dataset is widely used for research on classification under highly imbalanced conditions.

## 📌 Objective

Build a classifier capable of identifying fraudulent transactions, even when they represent less than 0.2% of all records.

## 📂 Dataset

* Source: ULB + Worldline
* Records: 284,807 transactions
* Fraud cases: 492
* Extremely imbalanced
* Features transformed using PCA for privacy reasons

The dataset **is not stored in this repository** due to GitHub’s 100 MB limit.

## 🧠 Project Steps

1. Load dataset (local file)
2. Exploratory Data Analysis (EDA)
3. Preprocessing:

   * StandardScaler
   * Outlier handling
   * Train/test split
4. Handling class imbalance:

   * Undersampling
   * Oversampling (SMOTE)
5. Modeling:

   * Logistic Regression
   * Random Forest
   * XGBoost
6. Evaluation:

   * AUC-ROC
   * Precision / Recall
   * Confusion Matrix
   * Precision-Recall Curve (more relevant for imbalance)
7. Interpretation and comparison of methods

## 🏗️ Project Structure

```
credit_card_fraud_detection/
│
├── data/
│   ├── raw/            # Original dataset (gitignored)
│   └── processed/      # Cleaned datasets
│
├── notebooks/
│   └── cc_fraud_analysis.ipynb
├── .gitignore
├── requirements.txt
└── README.md
```

## 🚀 How to Run

1. Install dependencies:

```
pip install -r requirements.txt
```

2. Place the dataset file here:

```
data/raw/creditcard.csv
```

3. Run the notebooks or scripts:

```
python src/modeling.py
```

## 📈 Expected Results

* AUC-ROC > 0.94
* High recall to minimize false negatives
* Comparison between balancing strategies

## 🛑 Note

The dataset contains anonymized data. Do not attempt to reverse PCA features or re-identify individuals.

## 📚 References

* Carcillo et al. — ULB Machine Learning Group
* Worldline & ULB Credit Card Fraud Dataset
