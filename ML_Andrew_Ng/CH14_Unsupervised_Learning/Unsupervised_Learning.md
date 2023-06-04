## 1、Unsupervised learning Introuction
### In nsupervised learning,we just have the data without the labels.We need to let the learning algorithm find the data structur of data set by itself.
![](assets/markdown-img-paste-20190315101152933.png)
## 2、K-means algorithm
### 2.1、These pictures can show what the k-means algorithm do.
- > #### 1st step:Set the cluster centroids randomly
![](assets/markdown-img-paste-20190315101945375.png)
- > #### 2nd step: cluster assignment.We assign each point to the different cluster which is closest to this point.

![](assets/markdown-img-paste-20190315102043770.png)
- > #### 3rd step:Move cluster centroids.We compute the means of the distance which is between the cluster centroids and each points belong it. We move the cluster centroids to the pisotion which we find by the means.
![](assets/markdown-img-paste-20190315102114442.png)

- > #### repeat the step2 and step3 until the position of cluster centroids don't change.

> ##### iteration 2![](assets/markdown-img-paste-20190315102142974.png)![](assets/markdown-img-paste-20190315102213501.png)

> ##### iteration 3![](assets/markdown-img-paste-20190315102240690.png)![](assets/markdown-img-paste-20190315102252669.png)

### 2.2、Implementation
#### Input:
- ##### K:number of clusters,set the pisotion of it randomly.
- ##### Train set: without labels
![](assets/markdown-img-paste-20190315102513772.png)
![](assets/markdown-img-paste-2019031510424060.png)

## 3、Optimization objective
### 3.1、Cost Function $J$
- > #### $c^{(i)}$
- > #### $\mu_{k}$
- > #### $\mu_{c^{(i)}}$
$$J(c^{(1)}...c^{(m)},\mu_1...\mu_K)=\frac{1}{m}\sum_{i=1}^m ||x^{(i)}-\mu_{c^(i)}||^2$$
![](assets/markdown-img-paste-20190315134655530.png)
### 3.2、Algorithm
![](assets/markdown-img-paste-20190315135055951.png)

## 4、Random initialization
### 4.1、How to Random initialization?
> #### Randomly pcik K training examples as cluster centroids.
![](assets/markdown-img-paste-20190315144330275.png)
### The problem is,if we randomly initialization may be the cost function can not get the global minimum
![](assets/markdown-img-paste-20190315144602217.png)
![](assets/markdown-img-paste-2019031514513944.png)

## 5、Choosing the number of clusters
### There is not a very commom standard to choose the number of cluster.One of it is:Elbow method
> #### We just test every number and observe the picture of the $Cost/K$.Take the number on "Elbow".But sometimes the picture will like the right one.
![](assets/markdown-img-paste-20190315150819358.png)
### So we can also choose K that basic on the problem
