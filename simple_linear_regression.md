## Simple Linear Regression

### What is Simple Linear Regression?

Simple linear regression is one of the foundational concepts in statistical modeling and machine learning. It is used to explore and quantify the relationship between two variables:

- Independent Variable (Predictor): This is the variable used to predict the outcome.
- Dependent Variable (Output): This is the variable we want to predict.

The core idea of simple linear regression is to establish a linear relationship between these variables. The relationship is represented as a straight line called the regression line, defined by the equation:

```math
Yi = A * X + B
```

Where:
- Yi: Predicted value of the dependent variable for the i-th observation.
- X: Value of the independent variable.
- A: Slope of the line, representing the rate of change in Y for a one-unit increase in X.
- B: Intercept, representing the predicted value of Y when X = 0.​

This technique is widely used for predictive analysis, as it offers a simple and interpretable model for understanding the relationship between two variables.

### How Does Simple Linear Regression Work?

1. Defining the Best-Fit Line
The best-fit line minimizes the difference (error) between the actual values and the predicted values of the dependent variable. In mathematical terms, this line minimizes the sum of squared residuals.

2. Random Errors (Residuals)
Residuals are calculated as:

```math
ei = Yactual - Ypredicted
```

Where:

- ei: Residual (error) for the i-th observation.
- Yactual: Observed value.
- Ypredicted: Predicted value.

```python
if (isAwesome){
  return true
}
```

### How to Obtain the Best-Fit Line Mathematically?

To determine the parameters A (slope) and B (intercept), we use optimization techniques, specifically minimizing the Mean Squared Error (MSE).

**Mean Squared Error (MSE)**
MSE is a cost function that quantifies the average squared difference between the actual and predicted values. It is given by:

```math
MSE = (1/N) * Σ(Yactual_i - (A * Xi + B))²
```

Where:

- N: Total number of data points.
- Yactual_i: Actual value of the dependent variable for the i-th data point.
- A * Xi + B: Predicted value for the i-th data point.

**Gradient Descent**
Gradient descent is an iterative optimization algorithm used to minimize the cost function (MSE). The algorithm updates A and B as follows:

```math
A = A - α * (∂MSE/∂A)
B = B - α * (∂MSE/∂B)
```

Where:

- α: Learning rate.
- (∂MSE/∂A) and (∂MSE/∂B): Partial derivatives of the MSE with respect to A and B.

### Assumptions of Simple Linear Regression

1. Linearity:
The relationship between the independent variable and the dependent variable must be linear.

2. Independence of Residuals:
Residuals (errors) should not be correlated with each other.

3. Normality of Residuals:
Residuals should follow a normal distribution with a mean close to zero.

4. Homoscedasticity (Constant Variance):
The variance of residuals should remain constant across all levels of the independent variable.

<!-- <img src="images/dummy_thumbnail.jpg?raw=true"/> -->

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).