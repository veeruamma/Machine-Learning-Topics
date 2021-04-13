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








