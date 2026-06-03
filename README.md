# Simple Linear Regression From Scratch using Gradient Descent

## Overview

This project implements **Simple Linear Regression from scratch in Python** without using machine learning libraries such as Scikit-learn.
The goal of the project is to understand the mathematical foundations of machine learning, especially:

* Linear Regression
* Gradient Descent Optimization
* Loss Functions
* Parameter Updates
* Model Convergence

The model learns the relationship between an input feature and output target by minimizing prediction error using iterative optimization.

---

# Project Objective

The primary objectives of this project are:

* Build a Linear Regression model manually
* Understand how Gradient Descent works internally
* Learn how weights and bias are updated during training
* Visualize regression lines and convergence behavior
* Gain intuition behind optimization in Machine Learning

---

# Libraries Used

## 1. NumPy

```python
import numpy as np
```

### Purpose

NumPy is used for:

* Numerical computations
* Array operations
* Mathematical calculations
* Vectorized computations

### Why NumPy?

Without NumPy:

* computations become slower
* loops become inefficient
* matrix operations become difficult

NumPy enables efficient mathematical operations on arrays.

---

## 2. Matplotlib

```python
import matplotlib.pyplot as plt
```

### Purpose

Matplotlib is used for:

* plotting data points
* visualizing regression lines
* analyzing model performance visually

### Why Visualization?

Visualization helps us:

* understand how well the model fits data
* observe trends
* inspect convergence behavior

---

## 3. Random

```python
import random
```

### Purpose

The Random library initializes:

* weight
* bias

with random values.

### Why Random Initialization?

Random initialization helps:

* start optimization from arbitrary points
* avoid deterministic initialization behavior
* simulate real-world ML training methods

---

# Mathematical Foundations

## Linear Regression Equation

The prediction equation used is:


y_hat = wx + b


Where:

* y_hat = predicted value
* ( w ) = weight (slope)
* ( x ) = input feature
* ( b ) = bias/intercept

This equation represents a straight line.

---

# Loss Function

The project uses **Mean Squared Error (MSE)** as the loss function.

L = (1/2n)*​∑(y−y_hat​)

Where:

* ( y ) = actual value
* ( y_hat ) = predicted value
* ( n ) = number of samples

---

## Why Mean Squared Error?

MSE is used because:

* it penalizes larger errors heavily
* it is differentiable
* it works efficiently with Gradient Descent
* it provides smooth optimization

---

# Gradient Descent Optimization

The model learns by minimizing the loss function using Gradient Descent.

---

## Weight Gradient

∂w/∂L​=−(1/n)​∑(y−y_hat​)x

This determines how the weight should change to reduce error.

---

## Bias Gradient

∂b/∂L​=−(1/n)∑(y−y_hat​)

This determines how the bias should change.

---

# Parameter Update Rules

The parameters are updated iteratively:

## Weight Update

w = w+η⋅(1/n)​∑(y−y_hat​)x

## Bias Update

b = b +η⋅(1/n)​∑(y−y^​)x

Where:

* ( η(neta) ) = learning rate

---

# Why Gradient Descent?

Gradient Descent helps:

* minimize prediction error
* improve model accuracy
* optimize parameters iteratively

It is the foundation of:

* Neural Networks
* Deep Learning
* Logistic Regression
* Modern AI Optimization

---

# Project Workflow

## Step 1: Initialize Parameters

Randomly initialize:

* weight
* bias

---

## Step 2: Make Predictions

Use:


y_hat = wx + b


to predict outputs.

---

## Step 3: Calculate Error


error = y - y_hat


---

## Step 4: Compute Gradients

Calculate gradients for:

* weight
* bias

---

## Step 5: Update Parameters

Adjust parameters using Gradient Descent.

---

## Step 6: Repeat Until Convergence

Training stops when:

* loss stabilizes
* maximum iterations are reached

---

# Features of the Project

* Linear Regression implemented completely from scratch
* No ML frameworks used
* Gradient Descent optimization
* Early stopping mechanism
* Visualization of regression line
* Loss tracking during training
* Educational implementation for understanding ML internals

---

# Observations

## 1. Loss Decreases Gradually

During training:

* prediction error decreases
* model improves continuously

This confirms that Gradient Descent successfully optimizes parameters.

---

## 2. Learning Rate is Critical

### Small Learning Rate

* slower convergence
* more stable training

### Large Learning Rate

* faster learning
* may overshoot optimal solution

Choosing the correct learning rate is important.

---

## 3. Model Converges Efficiently

The early stopping condition:

```python
if np.abs(curr_loss - prev_loss) < threshold:
```

prevents unnecessary computation once convergence is achieved.

---

## 4. Visualization Improves Understanding

Plotting:

* original data points
* regression line

helps visually verify model accuracy.

---

# Outcome of the Project

After training:

* the model successfully learns the best-fit line
* prediction error reduces significantly
* regression line closely fits the dataset

The project demonstrates:

* understanding of machine learning fundamentals
* mathematical implementation skills
* optimization concepts
* practical Python programming

---

# Sample Output

The model produces:

* optimized weight
* optimized bias
* decreasing loss curve
* fitted regression line

---

# Future Improvements

Possible future enhancements:

* Multiple Linear Regression
* Polynomial Regression
* Mini-Batch Gradient Descent
* Stochastic Gradient Descent
* Regularization (L1/L2)
* R² Score Evaluation
* Train-Test Split
* Feature Scaling
* Interactive Visualizations

---

# Applications of Linear Regression

Linear Regression is widely used in:

* price prediction
* sales forecasting
* stock market analysis
* weather prediction
* trend analysis
* recommendation systems

---

# Conclusion

This project provides a deep understanding of:

* how Linear Regression works internally
* how optimization algorithms train ML models
* how mathematical concepts translate into code

Building ML algorithms from scratch strengthens understanding far beyond using prebuilt libraries and creates a strong foundation for advanced Machine Learning and Deep Learning concepts.

---
