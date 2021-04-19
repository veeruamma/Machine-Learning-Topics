# Machine-Learning-Topics
Projects worked on machine learning algorithms

_**Bias**_ : Error generated on the training data 

_**Variance**_ : Error generated on the testing or unseen data 

## Underfitting and Overfitting

While fitting the model, there can be 2 events which will lead to the bad performance of the model. These events are
1. **Underfitting** : Where the model couldn't fit the data well enough. This model gives lower accuracy and is unbale to capture the relationship between input and output variables. It can be avoided by using more data or by optimising the parameters of the model.
**Higher Error on both train and test data i.e High Bias and High Variance**

2. **Overfitting** : When the model predicts very well on training data and is not able to predict well on test data or validation data. the main reason for this could be memorising the training data and unable to generalize the test or unseen data. It can be avoided by using regularisation techniques such as drop out or by propser features selection.
**Higher Error only on test data i.e Low Bias and High Variance**

![image](https://user-images.githubusercontent.com/30498799/114488493-0de8c580-9c44-11eb-801b-af238541efae.png)

## R-squared and Adjusted R-squard
In case of regression models, apart form the accuracy and loss, there are other metrics to evaluate the performance of the model such as R-squared and Adjusted R-squared.

**R-square may work well in simple linear regression but in case of multiple linear regression, every time you add a independent variable to the model, the R-Squared value increases, even if the independent variavle is insignificant. It never decreass. Whereas Adjusted R-squared values increases only when the independent variable is significant and affects dependent varibale .**

**Adjusted R-squared value will be always less than or equal to R-squared value** 


## Linear Regression 
It is a method used to find the relationship between the outcome variable also known as the dependent variable, and one or more variable often called as independent variables. This method is mostly used for forecasting. There are different rehression techniques based on the number of independent varibales and the type of realtionship between varibales.

Regression 
* Performed when the type of dependent or target varibale is continuous and independent variable could be continuous or categorical or nominal. 
* Tries to find the best fit line, which shows the relationship between dependent and independent variables with least error.

**The impact of change in independent varibales on the dependent variable can be described using the best fit line.**

Best fit line equation for linear regression is **y= mx + c**,  where m is slope and c is intercept or constant

#### Simple Linear Regression : If there is only input/independent varibale. y = mx + c, trying to find the best m and c values for y and x. Just a line
#### Multiple Linear Regression : If there are more than one input/independent varibale. y = m1x1 + m2x2 + ... +c, trying to find the best set of m and c values. It's a plane

![image](https://user-images.githubusercontent.com/30498799/114487189-c06b5900-9c41-11eb-8278-c3a77dd6a158.png)


### Assumptions for Linear Regression models
1. Linearity : should have linear relationship b/w input and output variables.
2. Multicollinearity : two or more input variables shouldn't be highly correlated
3. Homoscedasticity : residuals should be homoscedasticity that means variance of error are constant across input variables
4. Multivariate Normality : residuals should be normally distributed.
5. Categorical data : categorical data should be converted into dummy variables.
6. Minimum records : at least of 20 records of input variables needed.

#### Polynomial Regression : It is a non-linear regression and relationship of output variable is fitted to nth degree of the input variable.

#### Ridge and Lasso Regression
These regression techniques are used when there is a overfitting behavior of the model. Ideally, the model should be well generalized and able to perform well on unseen data but in case of overfitting the model performance will be bad on unseen data. Hence to avoid this kind of overfitting in lineaer regression, we use Ridge and Lasso Regression techniques.

Genearalized model will have as much as low bias and low variance, but the overfitted model will have low bias but high variance hence the Ridge and Lasso techniques will lower the variance with the help of additional parameters in cost function such as alpha and squared slope in case of Ridge and magnitude of the slope in case of Lasso. 
Lasso helps in lowering the variance and also important feature selection by removing the low slope values.

#### Advantages of Using Linear Regression
1.  Linear Regression method is very easy to use. If the relationship between the variables (independent and dependent) is known, we can easily implement the regression method accordingly (Linear Regression for linear relationship).
2.  Linear Regression provides the significance level of each attribute contributing to the prediction of the dependent variable. With this data, we can choose between the variables which are highly contributing/ important variables. 
3.  After performing linear regression we get the best fit line, which is used in prediction, which we can use according to the business requirement.

#### Limitations of Linear Regression
 1. The main limitation of linear regression is that its performance is not up to the mark in the case of a nonlinear relationship.
 2. Linear regression can be affected by the presence of outliers in the dataset.
 3. The presence of high correlation among the variables also leads to the poor performance of the linear regression model.

## Logistic Regression 

## Decision Tree

## Support Vector Machine(SVM) 

## Naive Bayes 

## K-nearest neighbour

## K-means 

## Random Forest

## Gradient Boosting algorithms
1.  GBM
2.  XGBoost
3.  LightGBM
4.  CatBoost

