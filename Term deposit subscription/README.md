Term Deposit Subscription Prediction

Objective
To predict whether a bank customer will subscribe to a term deposit (yes / no) using Logistic Regression, and to evaluate the model using metrics beyond accuracy due to class imbalance.

Why Not Just Accuracy?
The dataset is highly imbalanced (~11–12% positive class).
False Positives → Unnecessary marketing cost
False Negatives → Loss of potential customers
Hence, we focus on:
- Precision
- Recall (Sensitivity)
- F1-score
- Specificity
- ROC-AUC

Dataset
- Source: UCI Machine Learning Repository
- Dataset: Bank Marketing
- Accessed via: ucimlrepo
- Records: 45,211
- Features: 16
- Target: y → subscription (yes / no)

Tools & Libraries
- Python
- Pandas, NumPy
- scikit-learn
- Matplotlib
- ucimlrepo

Data Preprocessing
- Combined features and target into a single DataFrame
- Handled missing categorical values by replacing them with "unknown"
- Encoded target variable (yes → 1, no → 0)
- One-Hot Encoding for categorical features
- Standard Scaling for numerical features
- Stratified train-test split (75% / 25%)

Exploratory Data Analysis (EDA)
Key insights:
- Customers with higher balance and higher education are more likely to subscribe
- Longer call duration strongly correlates with subscription (post-call feature)
- Too many campaign contacts reduce success rate
- Dataset imbalance makes accuracy misleading

Model
Algorithm: Logistic Regression
Pipeline:
- ColumnTransformer
- StandardScaler (numerical features)
- OneHotEncoder (categorical features)

Model Evaluation (Threshold = 0.5)
- Precision: High
- Recall: Low (misses many potential subscribers)
- ROC-AUC: ~0.90 → strong separability

Threshold Optimization
- Optimal threshold found using F1-score maximization
- Improved recall significantly
- Balanced trade-off between precision and recall

ROC Curve
- ROC curve plotted to visualize classifier performance
- Demonstrates strong model discrimination capability

Output
- probabilities.csv
- Record ID
- Probability of subscription
- Final predicted label

Practical Limitation
- Feature duration is only available after the call
- Including it improves performance but reduces real-world deployability

Conclusion
- Logistic Regression performs well with proper preprocessing
- Threshold tuning is critical for business-oriented ML problems
- ROC-AUC is a better performance indicator than accuracy for imbalanced data
