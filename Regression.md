# Introduction to Linear Regression

The equation of a first order linear Regression is simply $$y_\beta = \beta_0 + \beta_1x$$


As a method of prediction we need some metrics to evaluate if our model is good or not. For tha we calculate the **residuals**, as follows $$R_{(i)} = y_\beta (x_{obs}^{(i)}) - y_{obs}^{(i)}  $$ In this formula we have that that $y_\beta(x_{obs}^{(i)})$ is our predicted value, and $y_{obs}^{i}$ is our observed value.

Now we can utilize some metrics to evaluate, using residuals as follows. For instance, we can 
$$ MAE = \frac{1}{n} \sum\limits_{i=1}^{n}|y_\beta (x_{obs}^{(i)}) - y_{obs}^{(i)} | $$
$$ MSE = \frac{1}{n} \sum\limits_{i=1}^{n}(y_\beta (x_{obs}^{(i)}) - y_{obs}^{(i)} )^2 $$