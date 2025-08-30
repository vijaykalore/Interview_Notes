# Machine Learning Coding Questions

This document contains a collection of coding questions that are commonly asked in machine learning interviews. Each question is accompanied by a brief description, potential approaches to solve it, and key concepts to consider.

## 1. Implement Linear Regression from Scratch

**Description:**  
Create a simple linear regression model without using any libraries. Implement the gradient descent algorithm to optimize the weights.

**Key Concepts:**  
- Cost function (Mean Squared Error)
- Gradient descent
- Feature scaling

**Approach:**  
1. Initialize weights and bias.
2. Define the cost function.
3. Implement the gradient descent algorithm.
4. Update weights iteratively until convergence.

---

## 2. K-Nearest Neighbors (KNN) Algorithm

**Description:**  
Write a function to implement the KNN algorithm for classification. The function should take a dataset and a test instance and return the predicted class.

**Key Concepts:**  
- Distance metrics (Euclidean, Manhattan)
- Voting mechanism
- Handling ties

**Approach:**  
1. Calculate the distance between the test instance and all training instances.
2. Sort the distances and select the top K neighbors.
3. Perform majority voting to determine the predicted class.

---

## 3. Decision Tree Implementation

**Description:**  
Implement a decision tree classifier from scratch. Include methods for fitting the model and making predictions.

**Key Concepts:**  
- Gini impurity and entropy
- Recursive splitting
- Pruning techniques

**Approach:**  
1. Define a function to calculate impurity.
2. Recursively split the dataset based on the feature that provides the best split.
3. Create leaf nodes for terminal conditions.

---

## 4. Cross-Validation Technique

**Description:**  
Write a function to perform k-fold cross-validation on a given dataset and model.

**Key Concepts:**  
- Overfitting and underfitting
- Model evaluation metrics
- Stratified sampling

**Approach:**  
1. Shuffle the dataset and split it into k folds.
2. For each fold, train the model on k-1 folds and validate on the remaining fold.
3. Average the performance metrics across all folds.

---

## 5. Implementing a Neural Network

**Description:**  
Create a simple feedforward neural network with one hidden layer. Implement forward propagation and backpropagation.

**Key Concepts:**  
- Activation functions (ReLU, Sigmoid)
- Loss functions (Cross-entropy)
- Backpropagation algorithm

**Approach:**  
1. Initialize weights and biases for each layer.
2. Implement forward propagation to compute the output.
3. Use backpropagation to update weights based on the loss gradient.

---

## 6. Feature Selection Techniques

**Description:**  
Write a function to perform feature selection using Recursive Feature Elimination (RFE).

**Key Concepts:**  
- Importance of features
- Model performance metrics
- Iterative feature removal

**Approach:**  
1. Train the model on the full feature set.
2. Evaluate feature importance.
3. Remove the least important feature and repeat until the desired number of features is reached.

---

## 7. Time Series Forecasting

**Description:**  
Implement a simple time series forecasting model using ARIMA.

**Key Concepts:**  
- Autoregressive and moving average components
- Stationarity
- ACF and PACF plots

**Approach:**  
1. Check for stationarity and difference the series if necessary.
2. Fit the ARIMA model to the data.
3. Generate forecasts and evaluate performance.

---

## Conclusion

These coding questions cover a range of fundamental machine learning concepts and algorithms. Practicing these problems will help solidify your understanding and prepare you for technical interviews in data science and machine learning roles.