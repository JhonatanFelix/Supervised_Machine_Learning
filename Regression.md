# Introduction to Linear Regression

The equation of a first order linear Regression is simply $$y_\beta = \beta_0 + \beta_1x$$

![Figure 1](https://github.com/JhonatanFelix/Supervised_Machine_Learning/blob/main/images/LinearRegressionExample.png)

The Linear Regression is the line that minimizes the cost function. By that, we have that LR is the line that best fit the points we got on our experiment. We can see an example in the Figure 1, the line that best fits the Budget vs Box Office.


As a method of prediction we need some metrics to evaluate if our model is good or not. For tha we calculate the **residuals**, as follows $$R_{(i)} = y_\beta (x_{obs}^{(i)}) - y_{obs}^{(i)}  $$ In this formula we have that that $y_\beta(x_{obs}^{(i)})$ is our predicted value, and $y_{obs}^{i}$ is our observed value. We can see in the figure bellow what we can visualize as residuals with the distance between the points and the line.
![Figure 2](https://github.com/JhonatanFelix/Supervised_Machine_Learning/blob/main/images/Residuals.png)

Now we can utilize some metrics to evaluate, using residuals as follows. For instance, we can utilize the metric os **Mean Absolute Error(MAE)**





$$ MAE = \frac{1}{n} \sum\limits_{i=1}^{n} \lvert y_\beta (x_{obs}^{(i)}) - y_{obs}^{(i)}\rvert$$ 

or utilizes the metric of **Mean Squared Error(MSE)**

$$ MSE = \frac{1}{n} \sum\limits_{i=1}^{n}(y_\beta (x_{obs}^{(i)}) - y_{obs}^{(i)} )^2 $$



### MAE
The mean absolute error (MAE) is the simplest regression error metric to understand. We’ll calculate the residual for every data point, taking only the absolute value of each so that negative and positive residuals do not cancel out. We then take the average of all these residuals. Effectively, MAE describes the typical magnitude of the residuals. Mathematically we can see as the mean of the $\mathbb{L}^1$ norm.

The Mean Absolute Error (MAE) is a metric that provides an intuitive measure of the difference between the actual data and the predictions made by a model. It quantifies the absolute difference without considering the direction of the errors. By taking the absolute value of the residuals, the MAE does not indicate whether the model underperforms or overperforms (*i.e.*, whether it consistently underestimates or overestimates the actual data). Each residual contributes proportionally to the total error, so larger errors have a linear impact on the overall error. A small MAE suggests that the model is highly accurate in its predictions, while a large MAE indicates potential issues in certain areas. It's important to note that achieving a MAE of 0, meaning a perfect prediction, is extremely rare.

Although the MAE is easy to interpret, using the absolute value of the residuals may not always be the preferred approach. Depending on how you want your model to handle outliers or extreme values in the data, you may want to give more emphasis to these outliers or downplay their impact. The presence of outliers can significantly affect the choice of an appropriate error metric.

### MSE
The mean square error (MSE) is just like the MAE, but squares the difference before summing them all instead of using the absolute value. We can see this difference in the equation below. Mathematically we can see as the mean of the $\mathbb{L}^2$ norm.

When we square the difference between the data and the model's predictions, the result is the Mean Squared Error (MSE), which tends to be larger than the Mean Absolute Error (MAE). Due to this squaring operation, direct comparison between the MSE and MAE is not meaningful. Instead, we compare the error metrics of our model with those of competing models.

The impact of the squared term in the MSE equation becomes more pronounced when dealing with outliers in the data. While each residual in the MAE contributes proportionally to the total error, the error in the MSE grows quadratically. Consequently, outliers have a much greater influence on the total error in the MSE compared to the MAE. Moreover, the model is more heavily penalized for making predictions that significantly deviate from the corresponding actual values. In other words, large differences between actual and predicted values are punished more severely in the MSE than in the MAE.
