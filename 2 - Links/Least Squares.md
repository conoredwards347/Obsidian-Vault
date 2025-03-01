- 19-01-25 01:17
- Sources: [[Least Squares - Wikipedia]], [[Ordinary Least Squares Regression - Victor Powell and Lewis Lehe]]
---

**Definition**: In regression analysis, least squares is a parameter estimation method based on minimising the sum of the squares of the residuals (a residual being the difference between an observed value and the fitted value provided by a model) made in the results of each individual equation. (More simply, least squares is a mathematical procedure for finding the best-fitting curve to a given set of points by minimising the sum of the squares of the offsets ("the residuals") of the points from the curve.).

---

**Example**: To predict height from hand size, Ordinary Least Squares (OLS) regression identifies the best-fit line through data points. It works as follows:

1. Start with a trial line.
2. Measure the vertical errors (differences) between data points and the line.
3. Square the errors to ensure all differences are positive.
4. Adjust the line to minimise the total squared error.

The result is a regression equation, e.g., $\text{Height} = 5 + 0.8 × \text{Hand Size}$, where 5 is the intercept (predicted height when hand size is zero) and 0.8 is the slope (height increase per unit of hand size). OLS generalises to multiple variables by minimising errors relative to a plane or higher-dimensional surface.

![[Ordinary Least Squares (OLS) Regression.png]]