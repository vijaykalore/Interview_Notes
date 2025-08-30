# Python Snippets for Machine Learning Interviews

This document contains useful Python snippets that are commonly used in machine learning interviews. These snippets cover various tasks such as data manipulation, model training, evaluation, and visualization.

## Data Manipulation

### Importing Libraries
```python
import pandas as pd
import numpy as np
```

### Loading Data
```python
# Load a CSV file into a DataFrame
df = pd.read_csv('data.csv')
```

### Data Exploration
```python
# Display the first few rows of the DataFrame
print(df.head())

# Get summary statistics
print(df.describe())

# Check for missing values
print(df.isnull().sum())
```

### Data Cleaning
```python
# Fill missing values
df.fillna(df.mean(), inplace=True)

# Drop duplicates
df.drop_duplicates(inplace=True)
```

## Feature Engineering

### One-Hot Encoding
```python
# One-hot encode categorical variables
df = pd.get_dummies(df, columns=['category_column'])
```

### Normalization
```python
# Normalize a feature
from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler()
df['normalized_feature'] = scaler.fit_transform(df[['feature']])
```

## Model Training

### Train-Test Split
```python
from sklearn.model_selection import train_test_split

X = df.drop('target', axis=1)
y = df['target']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

### Model Training
```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier()
model.fit(X_train, y_train)
```

## Model Evaluation

### Predictions
```python
# Make predictions
y_pred = model.predict(X_test)
```

### Accuracy Score
```python
from sklearn.metrics import accuracy_score

accuracy = accuracy_score(y_test, y_pred)
print(f'Accuracy: {accuracy:.2f}')
```

## Visualization

### Plotting with Matplotlib
```python
import matplotlib.pyplot as plt

# Plot feature importance
importances = model.feature_importances_
plt.barh(range(len(importances)), importances)
plt.xlabel('Feature Importance')
plt.ylabel('Features')
plt.title('Feature Importance from Random Forest')
plt.show()
```

### Seaborn for Visualization
```python
import seaborn as sns

# Visualize the distribution of a feature
sns.histplot(df['feature'], bins=30)
plt.title('Feature Distribution')
plt.show()
```

## Conclusion

These snippets provide a quick reference for common tasks in machine learning using Python. Familiarity with these can help streamline the coding process during interviews.