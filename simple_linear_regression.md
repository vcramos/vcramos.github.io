## Simple Linear Regression

### What is Simple Linear Regression?

Simple linear regression is one of the foundational concepts in statistical modeling and machine learning. It is used to explore and quantify the relationship between two variables:

- Independent Variable (Predictor): This is the variable used to predict the outcome.
- Dependent Variable (Output): This is the variable we want to predict.

The core idea of simple linear regression is to establish a linear relationship between these variables. The relationship is represented as a straight line called the regression line, defined by the equation:

$$ Y_i = A * X + B $$

Where:
- $$ Y_i $$: Predicted value of the dependent variable for the i-th observation.
- X: Value of the independent variable.
- A: Slope of the line, representing the rate of change in Y for a one-unit increase in X.
- B: Intercept, representing the predicted value of Y when X = 0.​

This technique is widely used for predictive analysis, as it offers a simple and interpretable model for understanding the relationship between two variables.

### How Does Simple Linear Regression Work?

1. Defining the Best-Fit Line
The best-fit line minimizes the difference (error) between the actual values and the predicted values of the dependent variable. In mathematical terms, this line minimizes the sum of squared residuals.

2. Random Errors (Residuals)
Residuals are calculated as:

$$ e_i = Y_{actual} - Y_{predicted} $$

Where:

- $$ e_i $$: Residual (error) for the i-th observation.
- $$ Y_{actual} $$: Observed value.
- $$ Y_{predicted} $$: Predicted value.

### How to Obtain the Best-Fit Line Mathematically?

To determine the parameters A (slope) and B (intercept), we use optimization techniques, specifically minimizing the Mean Squared Error (MSE).

**Mean Squared Error (MSE)**

MSE is a cost function that quantifies the average squared difference between the actual and predicted values. It is given by:

$$ MSE = (1/N) * \sum(Y_{actual_i} - (A * X_i + B)) ^ 2 $$

Where:

- N: Total number of data points.
- $$ Y_{actual_i} $$: Actual value of the dependent variable for the i-th data point.
- $$ A * X_i + B $$: Predicted value for the i-th data point.

**Gradient Descent**

Gradient descent is an iterative optimization algorithm used to minimize the cost function (MSE). The algorithm updates A and B as follows:

$$ A = A - \alpha * (\partial{MSE} / \partial{A}) $$

$$ B = B - \alpha * (\partial{MSE} / \partial{B}) $$

Where:

- $$ \alpha $$: Learning rate.
- (\partial{MSE} / \partial{A}) and (\partial{MSE} / \partial{B}): Partial derivatives of the MSE with respect to A and B.

### Assumptions of Simple Linear Regression

1. Linearity:
The relationship between the independent variable and the dependent variable must be linear.

2. Independence of Residuals:
Residuals (errors) should not be correlated with each other.

3. Normality of Residuals:
Residuals should follow a normal distribution with a mean close to zero.

4. Homoscedasticity (Constant Variance):
The variance of residuals should remain constant across all levels of the independent variable.

### Evaluating the Performance of Simple Linear Regression

1. Coefficient of Determination (R²):
The coefficient of determination, R², measures the proportion of the variance in the dependent variable that is predictable from the independent variable. It is defined as:

$$ R² = 1 - (Σ(Residuals²) / Σ(Total Sum of Squares)) $$

Where:

Σ(Residuals²): Sum of squared residuals.
Σ(Total Sum of Squares): Total variance in the dependent variable.
2. Root Mean Squared Error (RMSE):
RMSE is the square root of the mean squared error, representing the average error magnitude:

```math
RMSE = √MSE
```

Where:

MSE: Mean Squared Error, as defined earlier.

---

*Montgomery, D. C., Peck, E. A., & Vining, G. G. (2021). Introduction to Linear Regression Analysis (6th ed.). Wiley.*

*Draper, N. R., & Smith, H. (1998). Applied Regression Analysis (3rd ed.). Wiley.*

*Kutner, M. H., Nachtsheim, C. J., Neter, J., & Li, W. (2005). Applied Linear Statistical Models (5th ed.). McGraw-Hill Education.*

<!-- <img src="images/dummy_thumbnail.jpg?raw=true"/> -->