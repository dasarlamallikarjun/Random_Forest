# 📘 Mutation Classification using Random Forest

## Overview

This project uses the **Random Forest** classification algorithm from `scikit-learn` to predict mutation classes based on structured features from a genomic dataset. It demonstrates a complete machine learning pipeline: data preprocessing, model training, evaluation, and visualization.

## Features

- Loads and explores a dataset with Pandas
- Removes uninformative features (all-zero columns)
- Trains a Random Forest classifier
- Evaluates the model using:
  - Confusion Matrix (visualized with heatmap)
  - Classification Report (precision, recall, F1-score)

## Dataset

- **Filename**: `dataset.csv`
- **Format**: CSV file with mutation data and a `target` class label

## Machine Learning Pipeline

```
Data Loading → Preprocessing → Train/Test Split → Model Training → Evaluation → Visualization
```

- **Model**: `RandomForestClassifier`
- **Test Split**: 25%
- **Random Seed**: 42

## Visualizations Included

- Confusion Matrix using seaborn heatmap
- Classification metrics via `classification_report`

## Requirements

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## How to Run

```bash
git clone https://github.com/dasarlamallikarjun/Random_Forest.git
cd Random_Forest
jupyter notebook Final.ipynb
```
