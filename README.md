
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

## Recommended Enhancements
Consider adding the following for deeper insight:
1. **Feature Importance Plot**
```python
importances = model.feature_importances_
feat_names = X.columns
sorted_idx = importances.argsort()

plt.figure(figsize=(10, 6))
plt.barh(feat_names[sorted_idx], importances[sorted_idx])
plt.xlabel("Feature Importance")
plt.title("Random Forest Feature Importances")
plt.tight_layout()
plt.show()
```

2. **Seaborn Pairplot (for Exploratory Data Analysis)**
```python
import seaborn as sns
sns.pairplot(df, hue='target')
```

## Requirements
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## How to Run
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
jupyter notebook Final.ipynb
```

## Contact
For questions or suggestions, feel free to open an issue or reach out via email.
