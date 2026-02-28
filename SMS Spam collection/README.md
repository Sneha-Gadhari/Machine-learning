# SMS Spam Classification using Ensemble Learning

## Project Overview

This project implements and compares multiple classification strategies for SMS spam detection using ensemble learning techniques. The objective is to evaluate how combining classifiers (Voting and Stacking) performs compared to individual base models and a boosting method (AdaBoost with decision stumps).

The task focuses on understanding weak learners, boosting, classifier combination strategies, and model evaluation using cross-validation.

---

## Dataset

Source: UCI Machine Learning Repository – SMS Spam Collection Dataset  

The dataset contains 5,572 SMS messages labeled as:

- Ham (0) – Legitimate messages  
- Spam (1) – Unwanted promotional messages  

The original dataset is a tab-separated text file with two columns:
- 'label'
- 'message'

---

## Methodology

### Text Preprocessing
- Label encoding (ham = 0, spam = 1)
- TF-IDF vectorization
- English stop-word removal

### Base Models
- Multinomial Naive Bayes  
- Logistic Regression  
- Linear SVM (Calibrated for probability estimation)

### Ensemble Methods
- Hard Voting Classifier  
- Soft Voting Classifier  
- Stacking Classifier (Meta-learner: Logistic Regression)  
- AdaBoost using Decision Stumps (DecisionTreeClassifier with max_depth = 1)

---

## Evaluation Strategy

- Stratified 5-Fold Cross Validation  
- Performance Metrics:
  - Precision
  - Recall
  - F1-score
  - ROC-AUC
  - Confusion Matrix

---

## Results Summary

Among all evaluated models, **Stacking** achieved the best overall performance with the highest F1-score and balanced precision-recall tradeoff.

Soft Voting performed better than Hard Voting due to probability averaging.

AdaBoost with decision stumps showed lower recall, indicating that shallow trees are too weak for high-dimensional TF-IDF text features.

---

## Output Files

- 'ensemble_comparison.csv' – Model-wise performance comparison  
- 'final_model_predictions.csv' – Predictions with probabilities  

---

## Conclusion

Stacking is recommended as the most effective combining strategy for this SMS spam classification task. It successfully leverages the complementary strengths of multiple classifiers and provides strong generalization performance compared to individual models and boosting with weak stumps.
