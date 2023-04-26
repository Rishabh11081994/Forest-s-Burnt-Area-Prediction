# Forest-s-Burnt-Area-Prediction
The aim in the project is to predict the burn area in forest fire


Objective: The objective of the jupyter notebook is to build good model to predict how much area would be burn during fire.
The data can be used for both classification and regression task. Several data scientist converted the target variable which is 
continous in nature into binary categorial variable to perform the classification task in order to predict whether there would be burnt or not. However, our approach have been first to visualize the data and later perform regression task.


#Conclusion
The purpose of the project was to predict the value of burnt area
Which is impacted by various features like month, ISI index, temperature
Rain etc.

There was some duplicated values in the data set that has been removed
The null values was not present in the data

While performing hypothesis test like spearman to find the significance of
Correlation between numerical independent and response variable it was observed
There was very weak correlation between independent and response feature (area)
.It was improved using log(x+1) transformation

ANOVA test shows that month is significant variables that affects the area while days
Do not. Post hoc analysis accomplished with Dunn’s test conveys that pair of month
Like dec and oct, dec and march, and aug and dec impacts the area significantly.

Severals models were built and evaluated using mean squared error.OLS methods
Depicts that with log(x+1) transformation we can explain the variance of 40% with a simple model. This is the simple model where wald test confirms only four feature were significant
To predict burnt area, the four feature namely are FFM, ISI index , wind and temperature 


Later we tuned the Gradient Boosted Regressor where features were selected using
Recursive feature elimination.  The best performance was obtained with max depth =2
And minimum split = 14

Bayesian regressor was attempted on the model. The performance was good in test data
Not on training data which indicate the presence of high bias in the model. 

Finally we can select OLS best logistic regression model for predictive modelling as it is light
And performing similar to ensemble model.  

All model are showing high biases, this is because the response variables contains almost
50% of the data with zero area, if somehow more  records are taken containing different values other than zero, the model will perform good. 


