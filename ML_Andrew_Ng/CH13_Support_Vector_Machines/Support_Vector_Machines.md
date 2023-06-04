## 1、Optimization objective
#### The Optimization objective of the SVM is the Cost function of it.
#### 1.1、Now  we just have a review of the logistic Regression and from the Cost function of logistic Regression we get the Cost Function of SVM
![](assets/markdown-img-paste-20190313090241860.png)
![](assets/markdown-img-paste-20190313090849229.png)
#### 1.2、The Cost Function
![](assets/markdown-img-paste-20190313092443319.png)
#### $cost_1(\theta^Tx^{(i)})$,$cost_2(\theta^Tx^{(i)})$ is this
![](assets/markdown-img-paste-20190313093007450.png)
![](assets/markdown-img-paste-20190313091738302.png)
#### and $C$ is used to adjust the weight of $A$
#### 1.3、Tht output of $h_{\theta}$ is $0$ and $1$
![](assets/markdown-img-paste-20190313091835869.png)

## 2、Large Margin Intution
#### If we need to minimize the Cost Function we just make $CA=0$,which means $A=0$.
![](assets/markdown-img-paste-20190313093859975.png)
![](assets/markdown-img-paste-20190313094105529.png)
#### The SVM Separate the examples which a large margin.That means, it will choose a Decision Boundary which have the large margin between the negative value and the positive value.
![](assets/markdown-img-paste-20190313094415101.png)

## 3、The mathmatics behind large margin classification
![](assets/markdown-img-paste-20190313100837792.png)
![](assets/markdown-img-paste-20190313101656670.png)

## 4、Kernels I
#### If we need to fit a Non-liear Decision Boundary,the Polynomial may be is not a good idea,because when the data is large ,use Polynomial is too expensive.
![](assets/markdown-img-paste-20190314155552297.png)
#### So we use a new algorithm to fit it.
> ##### 1st landmarks:Some points
> ##### 2nd similarity function:This a a function which can evalute the similarity between $x$ and $l^{(1)}$.The function compute the distance between $l$ and $x$.
> - ##### if the distance goes to 0 , $f_1$ get to 1
> - ##### if the distance is very large , $f_1$ get to 0
![](assets/markdown-img-paste-20190314160934564.png)
![](assets/markdown-img-paste-20190314161756197.png)
#### An example:The picture of the similarity function.
> ##### If $\sigma^2$ is small,when we push $x$ away from  $l$,the value of similarity function will quickly goes down.But if $\sigma^2$ is large,it will be slow.
![](assets/markdown-img-paste-20190314162427878.png)

#### Finally,the $h_{\theta}$ which made of similarity function $f_1,f_2,f_3$ can also give us a good prediction.
#### $$h_{\theta} = \theta_0+\theta_1f_1+\theta_2f_2+\theta_3f_3$$
![](assets/markdown-img-paste-20190314163200213.png)

#### BUT there is still a qestion:How to choose $\sigma^2$ and the points $l$?

## 5、Kernels II
#### 5.1、Choosing the landmarks:
> ##### In fact we use the every $x$ in train set as $l$.
![](assets/markdown-img-paste-20190314212810784.png)
#### 5.2、SVM with kernels function $f$
> ##### SVM with kernels means,we don't use the $x$ as the input of the $cost()$ in SVM function,instead ,we use the $f$($f$ is a matrix which come from $f_i = similarity(x,l^{(i)})$),So $\theta^Tx-->\theta^Tf$
![](assets/markdown-img-paste-20190314213244697.png)
![](assets/markdown-img-paste-20190314214137420.png)
#### 5.3、The parametrs of SVM:$\lambda$ and $\sigma^2$
![](assets/markdown-img-paste-2019031421444550.png)

## 6、Using an SVM
#### If we need use SVM,some parametrs need us to specify
- > ##### Parametrs $C$,the weight.
- > ##### kernel or without kernel(linear kernel),if we choose to use the kernel function,we alse need to specify the $\sigma^2$
![](assets/markdown-img-paste-20190315085434465.png)
#### kernel function:if we have many features ,don't forget to scaling the values.
![](assets/markdown-img-paste-20190315085903775.png)
#### Question:Which model we should use?
| n and m           | model                                                 |
| ----------------- | ----------------------------------------------------- |
| n>>m              | logistic Regiession/SVM without kernel                |
| n<m(intermediate) | SVM with G kernel                                     |
| n<<m              | add features ->logistic Regiession/SVM without kernel |
#### n:features, m train examples
![](assets/markdown-img-paste-20190315091444152.png)
- > ##### logistic regiession $\approx$ SVM wichout kernel.
- > ##### ![](assets/markdown-img-paste-20190315093646445.png)
