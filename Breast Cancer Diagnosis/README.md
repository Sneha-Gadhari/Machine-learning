****Breast Cancer Diagnosis Prediction using Machine Learning****

**Problem Statement**
This project aims to build a supervised machine learning classification pipeline to predict whether a breast tumor is Malignant (M) or Benign (B) using the Breast Cancer Wisconsin (Diagnostic) Dataset.
The project demonstrates the complete machine learning workflow:
- Problem framing
- Data preprocessing
- Model training
- Model evaluation
- Generalization error analysis

**Dataset**
- Source: UCI Machine Learning Repository
- Dataset: Breast Cancer Wisconsin (Diagnostic)
- Link: https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic
The dataset contains 569 samples with 30 numerical features extracted from digitized images of breast mass cell nuclei.

**Data Preprocessing**
Removed non-informative column (id)
Encoded target variable:
- Malignant (M) → 1
- Benign (B) → 0
Checked for missing values (none present)
Performed feature scaling using StandardScaler

**Train–Test Split**
Dataset split into training and testing sets
Default test size: 20%
Random state fixed for reproducibility

**Models Trained**
Logistic Regression (Baseline Linear Classifier)
Decision Tree Classifier (Non-linear Model)

**Model Evaluation Metrics**
For the test dataset, the following metrics are reported:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
Additionally:
- Training error and Test error are reported
- Generalization gap is analyzed

**Performance Analysis**
Comparison between training vs testing performance
Identification of:
- Overfitting (high training accuracy, lower test accuracy)
- Underfitting (low accuracy on both training and test sets)
Discussion of generalization error

**Machine Learning Issues Discussed**
- Feature scaling importance (especially for Logistic Regression)
- Class imbalance considerations
- Feature correlation in medical datasets
- Data leakage prevention during preprocessing

**Conclusion**
The project analyzes whether the trained models generalize well to unseen data by comparing training and test performance. Logistic Regression serves as a strong baseline, while the Decision Tree highlights the risk of overfitting if not regularized.

**Technologies Used**
- Python
- Google Colab
- NumPy
- Pandas
- Scikit-learn
- Matplotlib / Seaborn
