# Random Forest Algorithm

The word ‘Forest’ in the term suggests that it will contain a lot of trees. The algorithm contains a bundle of decision trees to make a classification and it is also considered a saving technique when it comes to overfitting of a decision tree model. A decision tree model has high variance and low bias which can give us pretty unstable output unlike the commonly adopted logistic regression, which has high bias and low variance. That is the only point when Random Forest comes to the rescue. 


Moreover, a random forest technique has a capability to focus both on observations and variables of a training data for developing individual decision trees and take maximum voting for classification and the total average for regression problem respectively.  It also uses a bagging technique that takes observations in a random manner and selects all columns which are incapable of representing significant variables at the root for all decision trees. In this manner, a random forest makes trees only which are dependent on each other by penalising accuracy. We have a thumb rule which can be implemented for selecting sub-samples from observations using random forest. If we consider 2/3 of observations for training data and p be the number of columns then 

1.  For classification, we take sqrt(p) number of columns
2.  For regression, we take p/3 number of columns.

**The above thumb rule can be tuned in case you like increasing the accuracy of the model.**

Let us interpret both bagging and random forest technique where we draw two samples, one in blue and another in pink.

![image](https://user-images.githubusercontent.com/30498799/115809396-9cb4c980-a41e-11eb-8f9f-407950242a25.png)

From the above diagram, we can see that the Bagging technique has selected a few observations but all columns. On the other hand, Random Forest selected a few observations and a few columns to create uncorrelated individual trees.


A sample idea of a random forest classifier is given below


![image](https://user-images.githubusercontent.com/30498799/115809432-b0603000-a41e-11eb-85ca-faa9b6eba3b5.png)

