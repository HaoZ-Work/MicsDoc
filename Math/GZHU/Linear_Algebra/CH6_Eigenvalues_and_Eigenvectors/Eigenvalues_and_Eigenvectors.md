## 6.1、Introduction to Eigenvalues
### 6.1.1、Eigenvalues and Eigenvector
> #### if Ax parallel to x $$Ax= \lambda x $$
> - ##### $\lambda\  is\ Eigenvalue  $
> - ##### $x\ here\  is\ Eigenvector  $
#### two properties of Eigenvalue
> - ##### The sum of $\lambda$ (there are normally more than one $\lambda$)
>$$\lambda_1+\lambda_2+...\lambda_n = a_{11}+a_{22}+a_{33}+...a_{nn}$$
> - ##### $$detA=\lambda_1 \lambda_2 ...\lambda_n$$

### 6.1.2、How to find the Eigenvalue and Eigenvector?(How to solve $Ax=\lambda x$)
> ##### $$Ax=\lambda x \\ (A-\lambda I)x=0 \\ \because (A-\lambda I)x=0,x \neq 0 \\ \therefore (A-\lambda x)\ is\ singular \\ \therefore det(A-\lambda I)=0$$
> ##### then we first get $\lambda$ and then get the x
#### e,g:
> $$A=\begin{bmatrix} 3&1 \\ 1 &3\end{bmatrix} $$
> ##### Step 1:get the $\lambda$
> $$det(A-\lambda I)= \left|\begin{array}{cccc}
3-\lambda &1 \\ 1 &3-\lambda\end{array}\right|
=(3-\lambda)^2-1=0$$
> $$\therefore \lambda_1=4,\lambda_2=2$$
> ##### Step 2: get the $x$
> $$\lambda_1 = 4 \\ A-4I = \begin{bmatrix} -1&1 \\ 1 &-1\end{bmatrix}=0 \\ \therefore x_1=\begin{bmatrix} 1 \\ 1\end{bmatrix}$$
> $$\lambda_2 = 2 \\ A-2I = \begin{bmatrix} 1&1 \\ 1 &1\end{bmatrix}=0 \\ \therefore x_2=\begin{bmatrix} -1 \\ 1\end{bmatrix}$$

#### there are also normally more than one vector x.
#### sometimes the $\lambda$ is complex numbers
