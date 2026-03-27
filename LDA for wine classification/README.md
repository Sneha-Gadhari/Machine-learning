# Wine Classification

## Overview
- Machine learning project to classify wine samples into different categories
- The code loads the dataset, performs preprocessing, and scales features
- Applies Linear Discriminant Analysis (LDA) to reduce dimensions
- Trains a classification model and evaluates its accuracy
- Originally developed in Google Colab, compatible with Jupyter Notebook

## Files
- `Wine_classification (1).ipynb`  
  - Contains the full workflow
- `lda_projection.csv`  
  - LDA-transformed dataset

## Steps
- Load dataset
- Preprocess data
- Apply LDA
- Train model
- Evaluate results

## What is LDA?
- LDA (Linear Discriminant Analysis) is a dimensionality reduction technique
- It reduces features while preserving class separability
- Uses class labels to maximize the distance between different classes
- Helps in better visualization and improved model performance

## Requirements
- Python 3
- numpy
- pandas
- matplotlib
- scikit-learn
- Jupyter Notebook

## How to Run
- Install required libraries
- Open the notebook in Jupyter Notebook or JupyterLab
- Run all cells step by step

## Note
- The notebook was created in Google Colab
- It will work in Jupyter with minor adjustments:
  - Update file paths if needed

## Output
- Classification results
- Model accuracy
- LDA projection data
