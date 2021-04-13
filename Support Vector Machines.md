# Support Vector Machine(SVM)

It is considered as black box technique as there are unknown parameters that are not so easy to interpret and assume how it works and it works on three principles.
1.  Maximum margin classifiers
2.  Support vector classifiers
3.  Support vector machines

## Maximum margin classifiers

They are often generalized with support vector machines but SVM has many more parameters compared to it. **The maximum margin classifier considers a hyperplane with maximum separation width to classify the data.** But infinite hyperplanes can be drawn in a set of data. It is indeed important to choose the ideal hyperplane for classification. 

![image](https://user-images.githubusercontent.com/30498799/114537751-25946e00-9c85-11eb-950b-ab659263ac07.png)

From the above diagram, we can assume infinite hyperplanes(left). The maximum margin classifier comes with a single hyperplane that divides the data(right). **The data touching the positive and negative hyperplanes is referred to as support vectors.**

###### The maximum margin classifier often fails in the situation of non-separable cases where it cannot allot a different hyperplane to classify _non-separable data_. For such cases, a support vector classifier comes to the rescue.

## Support Vector Classifiers

It is an extended version of the maximum margin classifier which also deals with the non-separable cases.

Let us consider a tuning parameter C. In this classifier, the high value of C can give us a robust model. A lower value of C gives us a flexible model

![image](https://user-images.githubusercontent.com/30498799/114538240-bb2ffd80-9c85-11eb-86be-8c039621c47f.png)

Let us take a look at the diagram on the left. We can see that the higher values of C delivered more errors which are regarded as a violation. The diagram on the right shows a lower value of C and does not provide a sufficient chance of violation by reducing the margin width.

## Support Vector Machine

This approach is considered during a non-linear decision and the data is not separable by a support vector classifier irrespective of the cost function.

![image](https://user-images.githubusercontent.com/30498799/114538641-2ed20a80-9c86-11eb-9c99-a34964397b0a.png)

The diagram illustrates the inseparable classes in a one-dimensional and two-dimensional space. 

When it is almost difficult to separate non-linear classes, we then apply another trick called kernel trick that helps handle the data.


![image](https://user-images.githubusercontent.com/30498799/114538853-66d94d80-9c86-11eb-911c-b25224c8f070.png)


In the above diagram, the data that was inseparable in one-dimension got separated once it was transformed into two-dimensions and after applying a polynomial kernel of the second degree. 

Now let us see how to handle the two-dimensional linearly inseparable data.

![image](https://user-images.githubusercontent.com/30498799/114538941-85d7df80-9c86-11eb-943f-ac92ff349ba4.png)


In two-dimensional data, the polynomial kernel of the second degree is applied by using a linear plane after transforming it to higher dimensions.

## Kernel Functions

Kernel functions can also be regarded as the tuning parameters in an SVM model. They are responsible for removing the computational requirement to achieve the higher dimensional vector space and deal with the non-linear separable data. There are two widely used kernel functions:
1.  Polynomial kernel
2.  Radial Basis Function (RBF) kernel

###  Polynomial Kernel

A polynomial function is used with a degree 2 to separate the non-linear data by transforming them into higher dimensions.

### Radial Basis Function (RBF) kernel

This kernel function is also known as the Gaussian kernel function. It is capable of producing an infinite number of dimensions to separate the non-linear data. It depends on a hyperparameter ‘γ'(gamma) which needs to be scaled while normalizing the data. The smaller the value of the hyperparameter, the smaller the bias and higher the variance it gives. While a higher value of hyperparameter gives a higher bias and lower variance solutions.  

## Advantages and disadvantages

### Some of the advantages of SVM are
1.  They are flexible in unstructured, structured and semi structured data.
2.  Kernel function eases the complexities in almost any data type.
3.  Overfitting is less observed compared to other models.

### disadvantages are
1.  Training time is more while computing large datasets.
2.  Hyperparameters are often challenging while interpreting their impact.
3.  Overall interpretation is difficult because of some black box approaches.


#### Though SVM is flexible in every type of data, we need to be still careful playing around with the parameters such as kernel tricks and also the hyperparameter. The business condition and its risk can be fatal if the model undergoes huge misclassification which is why parameter tuning is necessary. SVM can be used in images and text analysis but accuracy depends only on the type and condition of the data. Business domains such as banking and healthcare where misclassification can be too risky, SVM should be well tested concerning their parameters.






