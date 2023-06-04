## 5.1 The Properties of Determinants
### 5.1.1、3 basic properties
#### (1) $Det\ I = 1$
> $$
\left|\begin{array}{cccc}
1 &0 \\ 0 &1\end{array}\right|
=1$$
#### (2) $exchange\ the\ rows,\ resverse\ the\ sign\ of\ the\ det\ .$
#### (3)
> $$\left|\begin{array}{cccc}
ta &tb \\ c &d\end{array}\right|=t\left|\begin{array}{cccc}
a &b \\ c &d\end{array}\right| $$
$$\left|\begin{array}{cccc}
a+a' &b+b' \\ c &d\end{array}\right|= \left|\begin{array}{cccc}
a &b \\ c &d\end{array}\right| +\left|\begin{array}{cccc}
a' &b' \\ c &d\end{array}\right| $$

### 5.1.2、other 4-10 properties which come from the basic 3.
#### (4) $if\ det\ have\ two\ equal\ rows,\ -->det=0$
#### (5) $subtract\ l*row_i\ from\ row_k\ the\ det\ dose\ not\ change$
> $$\left|\begin{array}{cccc}
a &b \\ c-la &d-lb\end{array}\right|=\left|\begin{array}{cccc}
a &b \\ c &d\end{array}\right|-l\left|\begin{array}{cccc}
a &b \\ a &b\end{array}\right|=\left|\begin{array}{cccc}
a &b \\ c &d\end{array}\right|-0=\left|\begin{array}{cccc}
a &b \\ c &d\end{array}\right|$$
#### (6)$if\ det\ have\ one\ zeros\ row\ -->det = 0$
#### (7)
> $$U = \left|\begin{array}{cccc}
d_1 & &&& \\  0&d_2 \\ 0&0&d_3\\0&0&0&... \\0&0&0&0&d_n\end{array}\right| = d_1 * d_2 * d_3....* d_n $$

#### (8)
> $$\begin{cases} detA= 0\ exactly\ when\ A\ is\ singular(no invertible) \\ detA \neq 0\ when\ A\ is\ invertible\end{cases}$$
#### (9)$detAB= detA * detB $
> - $$ det A^{-1} = \frac{1}{det A} \\ \because A^{-1}A=I,detI=(detA^{-1})(detA)=1$$
> - $$det A^2 = (detA)^2$$
> - $$det 2A= 2^n * detA$$
#### (10) $det A^T=det A$:This means all properties for rows are also for columns.
> $$\left|\begin{array}{cccc}
a &b \\ c &d\end{array}\right|=\left|\begin{array}{cccc}
a &c \\ b &d\end{array}\right|=ad-bc$$


## 5.2、Cofactors

## 5.3 Cramer's Rule, Inverses, and Volumes
### 5.3.1、Formula for $A^{-1}$
> #### $$A^{-1}= \frac{1}{detA}C^T \\ \begin{bmatrix} a & b \\c &d\end{bmatrix}^{-1}=\frac{1}{ad-bc}\begin{bmatrix} C_{11} & C_{12} \\C_{21} &C_{22}\end{bmatrix}=\frac{1}{ad-bc}\begin{bmatrix} d & -b \\-c &a\end{bmatrix}$$

### 5.3.2、
> #### $$x=A^{-1}b=\frac{1}{detA}C^Tb$$
