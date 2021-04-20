# K-Means Clustering Algorithm

It's one of the unsupervised machine learnign algorithms that groups or classifies data points, based on several similarities in the data set which allows certain patterns to evolve upon which the prediction is done.

Clustering is to group similar objects that are highly dissimilar in nature. For a better understanding of clustering, we need to differentiate the concept of **Heterogeneity between the groups and Homogeneity within the groups.**  This can be broken down by understanding the variance in the data points between the groups and the variance within the groups. The variance between the groups (also referred to as clusters) is the distance between the points from one cluster to the other. In case, two clusters are being formed from a dataset, the statistical calculation of the variance between the clusters will adhere to the rule below:

  **Sum of Squares Between the Groups > Sum of Squares within the groups i.e -----> SSB> SSW**

##### For a better understanding of clustering, a graphical representation is shown below:

![image](https://user-images.githubusercontent.com/30498799/115366678-1d45b100-a1f8-11eb-9a80-3d1c2a29f1a6.png)

#### There are few methods for measuring the variance

1.  **Ecludian Distance:** _When the Euclidean distance between 2 clusters is small, it means the features between the clusters are similar in nature._
2.  **Manhattan Distance:** _It is an extension of Euclidean distance calculation and instead of taking squares of the data points we takle in ecludian distance, we take the modulus of the difference between data points, rather than squaring them._

<u> _Statistically, it can be depicted as_: </u>

For Eg: If we have 2 points (x1, y1) and (x2, y2) = (5,4) and (1,1)

Manhattan Distance= |5-1|+|4-1|= 7

In the case of Euclidean distance calculation:

Euclidean Distance = SQRT[(5-1)^2+(4-1)^2]=5

3.  **Chebyshev Distance:** _It considers the maximum value of all the distances based on the Manhattan method._


The **“Jaccard”** method of variance calculation can be used when the variable **data type is Boolean in nature**.

##### A full reference on different distance metrics that are available for calculation:

|Identifier|Class name|args|Distance Function|
|----|-----|-------|-------|
|"euclidean"|Euclidean Distance||sqrt(sum((x – y)^2))|
|"manhattan"|Manhattan Distance||sum(mod(x – y))|
|"chebyshev"|Chebyshev Distance||max(mod(x – y))|
|"minkowski"|Minkowski Distance|p|sum(mod(x – y)^p)^(1/p)|
|"wminkowski"|WMinkowski Distance|p, w|sum(mod(w * (x – y))^p)^(1/p)|
|"seuclidean"|SEuclidean Distance|V|sqrt(sum((x – y)^2 / V))|
|"mahalanobis"|Mahalanobis Distance|V, VI|sqrt((x – y)’ V^-1 (x – y)|

## K-Means :
* It is a non-hierarchical approach to forming good clusters.
* The number of clusters needs to be determined before the model is prepared.
* These K values are measured by certain evaluation techniques once the model is run.
* K-means clustering is widely used in large dataset applications.

## How does K-means Clustering work?

### Pre-Processing of the data
1. As this algorithm is based on distance calculation from each observation to the centroids present and this being an iterative process, the data needs to be in a proper format.
2. In case the dataset has variables with different units of measures, one should undertake the process of Scaling to bring all the variables into one unit/ measure, for further algorithm processing.
3. There are 2 methods of Scaling:  Z Scaling and Min-Max Scaling
  * **Z Scaling: It is to be used when the variance between the column is very less.**
    * Features will be rescaled
    * Have the properties of a standard normal distribution (μ=0 and σ=1)
  * **Min Max Scaling: It is to be used when the variance between columns is high.**
    * The data is scaled to a fixed range – 0 to 1.
    * The cost of having this bounded range – smaller standard deviations, which can suppress the effect of outliers


#### Steps followed by K-Means Algorithm
* The first step in this model is to specify the K value.
* Based on this K value, the dataset is partitioned into initial clusters.
* Random centroids are assigned to the dataset from the initial K values which will be away from the original observations.
* Then the model calculates distances from every observation in the cluster to the random centroid. Where the distance value is less and nearer to the random centroid, every observation gets mapped to the centroid. Like this, for all the observations in the dataset, the values are calculated and the observations are assigned suitably. The Euclidean distance metric is the default measure to calculate all distance from the centroid to the observations.
* Once the distances are calculated, random clusters are formed.
* Based on these random clusters, an iterative process of assigning new centroids enables the formation of new clusters. Here the variance is calculated to every observation in the cluster from the centroid. This process runs till the time Heterogeneity between the groups is greater than Homogeneity within the groups i.e SSB > SSW.

### Model Evaluation
**Silhouette Score:**
* This method is also called Indirect model evaluation technique.
* The model helps to analyse the correctness of every observation mapped to respective clusters based on distance criteria.
**Sil_Width score= (b-a) / MAX(a,b), where** b = distance from the random observation to its neighbouring cluster,  a = distance from the random observation to its own cluster
* If the score has a positive value with a range of score between -1 to +1, the cluster mapping of the data point is correct.
* Once this is achieved, we have to get into the Silhouette Score.
* Silhouette Score is the average of Sil_Width score based on the calculation of all the observations in the dataset .
* **Conclusions drawn:**

|Value Tend to|Conclusion|
|----|-----|
|+1|The clusters formed are away from each other|
|0|The clusters are not separable|
|-1|The model has failed in forming the clusters|

#### WSS Plot (Elbow Plot):
* WSS Plot also called **“Within Sum of Squares”** is another solution under the K-Means algorithm which helps to decide the value of K (number of clusters).
* The values taken to plot the WSS plot will be the variance from each observation in the clusters to its centroid, summing up to obtain a value.
