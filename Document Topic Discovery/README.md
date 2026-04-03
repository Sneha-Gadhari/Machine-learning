# SVD for Document Topic Discovery (Latent Semantic Analysis)

## Overview
This project implements **Latent Semantic Analysis (LSA)** using **Singular Value Decomposition (SVD)** on text data. The goal is to reduce high-dimensional sparse text features into a lower-dimensional semantic space and analyze how well these representations support clustering and classification tasks.

---

## Dataset
- Dataset used: 20 Newsgroups (via scikit-learn)
- Categories selected:
  - sci.space
  - rec.autos
  - talk.politics.misc

- Preprocessing:
  - Removed headers, footers, and quotes to avoid bias
  - Converted raw text into numerical features using TF-IDF

---

## Methodology

### 1. Text Vectorization
- Used TF-IDF Vectorizer
- Removed stopwords
- Applied:
  - `max_features = 5000`
  - `min_df = 5`
  - `max_df = 0.5`

### 2. Dimensionality Reduction
- Applied Truncated SVD (LSA)
- Component values used:
  - 50
  - 100
  - 200

### 3. Normalization
- Applied L2 normalization on reduced features
- Improves clustering performance

### 4. Clustering
- Algorithm: K-Means
- Evaluated using Silhouette Score

### 5. Classification
- Model: Logistic Regression
- Evaluated using Accuracy Score

### 6. Topic Interpretation
- Extracted top 10 terms for 5 topics
- Based on SVD components

---

## Results

| Components | Silhouette Score | Accuracy |
|-----------|----------------|----------|
| 50        | 0.0469         | 0.8381   |
| 100       | 0.0293         | 0.8481   |
| 200       | 0.0205         | 0.8427   |

### Observations
- Accuracy improves as components increase up to 100
- Slight drop at 200 due to noise/overfitting
- Silhouette score decreases with higher dimensions
- Indicates clusters are more distinct in lower dimensions

---

## Files Included

- `SVD for Document Topic Discovery.ipynb` → Complete implementation
- `svd_results.csv` → Performance metrics
- `lsa_topic_terms.txt` → Extracted topics

---

## Key Learnings

- SVD effectively reduces dimensionality of sparse text data
- Helps uncover latent semantic structure
- Improves performance in classification tasks
- Provides interpretable topic representations
- Trade-off exists between dimensionality and clustering quality

---

## Conclusion

SVD (LSA) successfully transforms high-dimensional TF-IDF features into a compact semantic space. The reduced representations improve classification performance and allow meaningful topic extraction. However, increasing dimensions may reduce clustering quality due to loss of separability. Overall, SVD is a powerful technique for text-based dimensionality reduction and analysis.

---

## How to Run

1. Install dependencies:
- pip install scikit-learn numpy pandas


2. Run the notebook:
- Open notebook in Jupyter/Colab
- Execute all cells

---

