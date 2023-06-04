## 1、Classification
#### if we need to solve a classification problems, for it "linear regression" is sometimes  not a good idea. It can not fit the data better.
![](assets/markdown-img-paste-2019030410521756.png)
#### compare with the linear regression the output of the Logistic regression have a range $[0,1]$
![](assets/markdown-img-paste-20190304105631674.png)
#### Actually logistic is a classification algorithm not a regression algorithm.

## 2、Hypothesis Representation
#### 2.1、The hypothesis function of logistic regression model.
### $$h_\theta(x) = g(\theta^Tx) \\ g(z)=\frac{1}{1+e^{-z}} \\ \therefore h_\theta(x)=\frac{1}{1+e^{-\theta^Tx}}$$
![](assets/markdown-img-paste-2019030411094520.png)

#### 2.2、The output of the hypothesis is actuallly a conditional probability.The case is $y = 1 $ or $ y = 0$,the condition is the trainset x
![](assets/markdown-img-paste-20190304111433492.png)

## 3、Decision Boundary
#### A simple example fot the decision boundary pf the logistic regression:
> ##### from the diagram we kown that
>  ##### $$g(z) > 0.5 z > 0 \ then\  h_0(x)=1$$
>  ##### $$g(z) < 0.5 z < 0 \ then\  h_0(x)=0$$
> ##### now zero is the decision boundary of the logistic regression.
![](assets/markdown-img-paste-20190304161831194.png)
#### The decision boundary can also be  complex.if we choose the parameters $\theta_0 =-3,\theta_1 = 1,\theta_2 = 1$,$$z=x\theta^T=-3+x_1+x_2 \\ \therefore if\ x_1+x_2 > 0,h_\theta(x)=1 \\\therefore if\ x_1+x_2 < 0,h_\theta(x)=0 $$
![](assets/markdown-img-paste-20190304160945983.png)
![](assets/markdown-img-paste-20190304161412802.png)
#### notice that:From train set we can get the  parameters ,but the decision boundary is only depend on the parameters.Once we get the parameters,there is no relationship between the decision boundary and train set.

## 4、Cost Function in logistic regression
#### We use the cost function to fit the parameters $\theta$.but the cost function we used is not the linear regression cost function. Becasue if we use it to fit the logistic ,we can not granti the Gradient descent algorithm can finally get the globle minimum. So we build a new cost function for the logistic regression.
#### $$Cost(h_\theta(x),y)=\begin{cases} -log(h_\theta(x))\ if\ y=1\\-log(1-h_\theta(x))\ if\ y=0\end{cases}$$
![](assets/markdown-img-paste-20190304164710201.png)
![](assets/markdown-img-paste-20190304164817107.png)

## 5、Simplified cost function and gradient descent
#### 5.1、The simplified cost function
> #### $$Cost(h_\theta(x),y)=-ylog(h_\theta(x))-(1-y)log(1-h_\theta(x))$$
#### 5.2、gradient descent of logistic regression.
##### The representation of gradient descent is same like the formula of linear regression ,but in fact the $h_\theta(x)$ is not same
> - ##### linear regression: $$ h_\theta(x) = \theta^Tx$$
> - ##### logistic regression: $$h_\theta(x)=\frac{1}{1+e^{-\theta^Tx}}$$
![](assets/markdown-img-paste-20190305095304943.png)

## 6、Advance optimization
#### When the train set is very large,the normal gradient descent algorithm may be have not a good performance,so we need some advance algorithm.
#### to use these algorithm,we don't need to write them, we can just use the library in octave , matlab or python.
![](assets/markdown-img-paste-20190305101811352.png)
![](assets/markdown-img-paste-20190305102817577.png)

## 7、Multi-class classification :1 vs all
#### sometimes the problem have more than two result.
![](assets/markdown-img-paste-20190305103921138.png)
![](assets/markdown-img-paste-20190305103954715.png)

#### The idea to deal with it is,we just switch it to a 2 classification problem to get the decision boundary and then we  combine them.
![](assets/markdown-img-paste-20190305104316860.png)
