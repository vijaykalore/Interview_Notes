# Math Formulas for Machine Learning

This document provides a comprehensive list of essential mathematical formulas used in Machine Learning. Understanding these formulas is crucial for grasping the underlying principles of various algorithms and techniques.

## 1. Linear Algebra

### Vectors and Matrices
- **Vector Addition**: 
  If **a** and **b** are vectors, then:
  **c** = **a** + **b**

- **Dot Product**: 
  For vectors **a** and **b**:
  **a** · **b** = Σ(a_i * b_i)

- **Matrix Multiplication**: 
  If **A** is an m x n matrix and **B** is an n x p matrix:
  **C** = **A** * **B** where C_ij = Σ(A_ik * B_kj)

### Eigenvalues and Eigenvectors
- For a square matrix **A**:
  **A** **v** = λ **v**
  where λ is the eigenvalue and **v** is the eigenvector.

## 2. Calculus

### Derivatives
- **Gradient**: 
  For a function f(x), the gradient is:
  ∇f(x) = [∂f/∂x_1, ∂f/∂x_2, ..., ∂f/∂x_n]

### Optimization
- **Gradient Descent Update Rule**:
  **θ** = **θ** - α * ∇J(θ)
  where α is the learning rate and J(θ) is the cost function.

## 3. Probability and Statistics

### Basic Probability
- **Bayes' Theorem**:
  P(A|B) = [P(B|A) * P(A)] / P(B)

### Distributions
- **Normal Distribution**:
  f(x) = (1 / (σ√(2π))) * e^(-(x - μ)² / (2σ²))
  where μ is the mean and σ is the standard deviation.

### Expected Value and Variance
- **Expected Value**:
  E[X] = Σ[x * P(x)]

- **Variance**:
  Var(X) = E[X²] - (E[X])²

## 4. Machine Learning Metrics

### Classification Metrics
- **Accuracy**:
  Accuracy = (TP + TN) / (TP + TN + FP + FN)

- **F1 Score**:
  F1 = 2 * (Precision * Recall) / (Precision + Recall)

### Regression Metrics
- **Mean Squared Error (MSE)**:
  MSE = (1/n) * Σ(y_i - ŷ_i)²

- **R² Score**:
  R² = 1 - (SS_res / SS_tot)
  where SS_res is the sum of squares of residuals and SS_tot is the total sum of squares.

## 5. Common Algorithms

### Linear Regression
- **Cost Function**:
  J(θ) = (1/2m) * Σ(hθ(x_i) - y_i)²

### Logistic Regression
- **Sigmoid Function**:
  σ(z) = 1 / (1 + e^(-z))

### Support Vector Machines
- **Hinge Loss**:
  L(y, f(x)) = max(0, 1 - y * f(x))

## Conclusion

This cheatsheet serves as a quick reference for the mathematical concepts and formulas that are fundamental to understanding and implementing machine learning algorithms. Mastery of these concepts will greatly enhance your ability to tackle machine learning problems effectively.