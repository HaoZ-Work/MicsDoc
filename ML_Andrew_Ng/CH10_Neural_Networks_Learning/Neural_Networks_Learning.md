## 1、Cost Function
#### 1.1、 some new number
> - ##### $L$:the number of the layers
> - ##### $s_j$(or $K$):The number of unit(not counting bias unit) in layer $l$
![](assets/markdown-img-paste-20190308150606248.png)
#### 1.2、Cost Function
$$J(\Theta) = -\frac{1}{m}[\sum^m_{i=1}\sum^{K}_{k=1}y^{(i)}_{k}log(h_\theta(x^{(i)}))_{k}+(1-y_{k}^{(i)})log(1-(h_{\theta}(x^{(i)}))_{k})]-\frac{\lambda}{2m}\sum^{L-1}_{l=1}\sum^{s_j}_{i=1}\sum^{s_{j+1}}_{j=1}(\Theta^{(l)}_{ji})^2$$
![](assets/markdown-img-paste-20190308151355430.png)

## 2、Backpropagation algorithm
#### 2.1、Now we need to build the algorithm to minimize the $J(\Theta)$,the Gradient Descent algorithm need us compute two values for it
> - ##### $J(\Theta)$
> - ##### $ \frac{\partial}{\partial  \Theta^{(l)}_{ij}}J(\Theta)$
![](assets/markdown-img-paste-20190308153940874.png)
#### 2.2、From Error $\delta^{(l)}_j$ to Gradient Descent Algorithm
> #### We define $\delta^{(l)}_j = a^{(l)}_j - y_j$,it represents the error beteen the $y_j$(the real data from the train set) and $a^{(l)}_j$(the feature we got from the neural network)
> #### So the right order to minimize $J(\Theta)$ is
> - ##### 1st step: Run forward propagation to get the output and ervery a in hidden layers.
> - ##### 2nd step:Run backpropagation from the output layer to the input layer ,then we got $\delta^{(l)}_j$
> - ##### 3rd step:Use $\delta^{(l)}_j$ to compute $ \frac{\partial}{\partial  \Theta^{(l)}_{ij}}J(\Theta)$，because $$\frac{\partial}{\partial  \Theta^{(l)}_{ij}}J(\Theta)=a^{(l)}_j\delta^{(l+1)}_i$$
> - ##### 4th step :Run Gradient Descent to minimize $J(\Theta)$

#### 2.3、The implementation details of backpropagation algorithm and the Gradient Descent algorithm.
![](assets/markdown-img-paste-20190308155428380.png)
![](assets/markdown-img-paste-20190308160057828.png)

## 3、Backpropagation intuition
![](assets/markdown-img-paste-20190308190519222.png)

## 4、implementation note:Unrolling parameters
#### Unrolling parameters means:we unroll them form parameters matrices into parameters vectors.Because the result of cost function ($\theta$ and $dervative$)is represented as matrix.But if we need to use the fminunc(),the inpit of it must be vector.So we need to unroll parameters.
![](assets/markdown-img-paste-20190310192851474.png)
#### Example:
![](assets/markdown-img-paste-2019031019312713.png)
![](assets/markdown-img-paste-20190310193407996.png)
![](assets/markdown-img-paste-20190310193418509.png)
![](assets/markdown-img-paste-20190310193622119.png)
![](assets/markdown-img-paste-20190310193741104.png)

## 5、Gradient check
#### A reason for gradient check is sometimes the backpropagation can run with bugs and the error will be very large.gradient check can make sure the backpropagation algorithm run correctly
> #### The main idea is computing the dervative of $J(\theta)$  and then compare to the $\theta$ in $DVec$.If the values are very similar or same,backpropagation algorithm run correctly
![](assets/markdown-img-paste-20190310195903199.png)
#### The way to compute the dervative of $J(\theta)$
![](assets/markdown-img-paste-20190310195832645.png)
![](assets/markdown-img-paste-20190310200233497.png)

## 6、Random initialization
#### Zero initialization for $\theta$ is not a bad idea in logistic regression.But if we set $\theta = 0$ in neural network,every feature will in same value. So,we need the Random initialization for $\theta$.
![](assets/markdown-img-paste-20190310203249835.png)
#### implementation:Just use this formula we can make every $\theta$ between $[-\epsilon,\epsilon]$
![](assets/markdown-img-paste-20190310203527399.png)

## 7、Putting it together
![](assets/markdown-img-paste-20190310204725337.png)
![](assets/markdown-img-paste-20190310205113136.png)
![](assets/markdown-img-paste-20190310205324193.png)
