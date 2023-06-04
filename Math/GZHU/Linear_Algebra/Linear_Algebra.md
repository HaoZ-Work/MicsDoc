# Ch1：Geometric interpretation of linear equations
### 1、Two pictures of the linear equations.e,g:
> 2x-y=0
>-x+2y=3
- #### row picture:The main idea is to find a point which satisfy the two equations.The form is Ax=b.(A is the coefficient matrix ,b,x are the vectors.)
> $\begin{bmatrix}
2 & -1\\
-1 & 2 \\
\end{bmatrix}$$\begin{bmatrix}x \\ y
\end{bmatrix}$ = $\begin{bmatrix}0 \\ 3\end{bmatrix}$

- #### column picture:The important idea.We use two vectors to make a new vector.
> x $\begin{bmatrix}2 \\ -1 \end{bmatrix}$ + y$\begin{bmatrix} -1 \\ 2\end{bmatrix}$ = $\begin{bmatrix} 0 \\ 3\end{bmatrix}$

### 2、A simple example for linear equations Ax=b
> $\begin{bmatrix} 2 & 5\\1 & 3 \end{bmatrix}$$\begin{bmatrix} 1 \\2 \end{bmatrix}$=1 $\begin{bmatrix} 2 \\ 1\end{bmatrix}$+2$\begin{bmatrix} 5 \\ 3\end{bmatrix}$=$\begin{bmatrix} 7 \\ 12\end{bmatrix}$





# 2、Elimination Matrix
### 2.1、A simple example for elimination.
> ##### Step1:From these equations we can get a matrix
> x + 2y + z = 2
> 3x + 8y + z = 12
> 4y + z = 2

> $\begin{bmatrix}  1 & 2 & 1 \\ 3&8 & 1 \\ 0 & 4 & 1\end{bmatrix}$ -->$\begin{bmatrix}  1 & 2 & 1 \\ 0&2 & -2 \\ 0 & 4 & 1\end{bmatrix}$ --> $\begin{bmatrix}  1 & 2 & 1 \\ 0&2 & -2 \\ 0 & 0 & 5\end{bmatrix}$ ,

> ##### Step2:Back substitution: In this step,we use the augmented matrix to get the x,y,z.
> $\begin{bmatrix}  1 & 2 & 1 &2\\ 3&8 & 1 & 12\\ 0 & 4 & 1 &2\end{bmatrix}$ --> $\begin{bmatrix}  1 & 2 & 1 & 2\\ 0&2 & -2 & 6 \\ 0 & 0 & 5 & -10\end{bmatrix}$ -->
x+2y+z =2
> 2y-z =6
> 5z=-10
than we solve the equations and get x,y,z.
#### When elimination fails?
> ##### If we get the zero but nothing below it, e,g:$\begin{bmatrix}  1 & 2 & 1 \\ 0&2 & -2 \\ 0 & 0 & 0\end{bmatrix}$ We can not get the field of x,y,z.

### 2.2、Elimination matrixes
##### In elimination ,we can use the elementary matrix in each step.
> ##### Step 1
> $\begin{bmatrix}  1 &  0 & 0 \\ -3&1 & 0 \\ 0 & 4 & 1\end{bmatrix}$ $\begin{bmatrix}  1 & 2 & 1 \\ 3&8 & 1 \\ 0 & 0 & 1\end{bmatrix}$ = $\begin{bmatrix}  1 & 2 & 1 \\ 0&2 & -2 \\ 0 & 4 & 1\end{bmatrix}$
> ##### $\begin{bmatrix}  1 &  0 & 0 \\ -3&1 & 0 \\ 0 & 4 & 1\end{bmatrix}$ This matrix is elementary matrix which means we subtract 3 times row_1 from row_2.
> ##### The first row in E means we take one row_1 and do nothing.Row_1 one can change the first row in the matrix which on its right.$E_{[11]}$ indicates how many row_1 we take,$E_{[12]}$ mean the row_2.and so do the $E_{[13]}$ .

> ##### Step 2
> $\begin{bmatrix}  1 & 0 & 0 \\ 0&1 & 0 \\ 0 & -2 & 1\end{bmatrix}$ $\begin{bmatrix}  1 & 2 & 1 \\ 0&2 & -2 \\ 0 & 4 & 1\end{bmatrix}$= $\begin{bmatrix}  1 & 2 & 1 \\ 0&2 & -2 \\ 0 & 0 & 5\end{bmatrix}$

####  How can we do this all in one step?
> ##### $E_{[32]}$($E_{[21]}$A)=U

### 2.3、Permutation matrix
#### The permutation matrix can change  raws or columns in other matrix.
> $\begin{bmatrix}  0 & 1 \\ 1 &0 \end{bmatrix}$$\begin{bmatrix}  a& b \\ c &d \end{bmatrix}$= $\begin{bmatrix}  c & d \\ a &b \end{bmatrix}$

> $\begin{bmatrix}  a& b \\ c &d \end{bmatrix}$$\begin{bmatrix}  0 & 1 \\ 1 &0 \end{bmatrix}$= $\begin{bmatrix}  b& a \\ d &c \end{bmatrix}$

#### multiply on the left side -->rows operation
#### multiply on the right side -->column operation

# CH3
## 1、The Rules for matrix multiplication
> e,g : $\begin{bmatrix}  A_1 & A_2 \\ A_3 & A_4 \end{bmatrix}$$\begin{bmatrix}  B_1 & B_2 \\ B_3 & B_4 \end{bmatrix}$= $\begin{bmatrix}  A_1B_1+A_2B_2 & A_1B_2+A_2B_4 \\ A_3B_1+A_4B_3 & A_3B_2+A_4B_4 \end{bmatrix}$
> There is a rule: The number of columns in left matrix must equal the number of rows in right matrix.
## 2、invertible matrix
#### We use $A^{-1}$ sto indicate the inverse matrix of A.
> $AA^{-1}=I$
> $A^{-1}=I$
#### How we get the inverse matrix of A?
> Gauss-Tordam:
> A=$\begin{bmatrix} 1 & 3\\ 2 &7 \end{bmatrix}$,$A^{-1}$=$\begin{bmatrix}  a& b \\ c &d \end{bmatrix}$
> now we make a augmented matrix :AI=$\begin{bmatrix} 1 & 3 & 1 & 0\\ 2 &7&0&1 \end{bmatrix}$ -->elimination -->  $\begin{bmatrix} -1 & 3 & 1 & 0\\ 0 &1&-2&1  \end{bmatrix}$ --> $\begin{bmatrix} 1 & 0 & 7 & -3\\ 0 &1&-2&1 \end{bmatrix}$=$IA^{-1}$,
> $A^{-1}$=$\begin{bmatrix}  7 & -3\\ -2&1 \end{bmatrix}$
#### Why we can do this?
> We use E(elimination matrix), E[AI] = [$IA^{-1}$]
> because if EA=I,then E is $A^{-1}$,and then,EI=$A^{-1}$

# CH4:A=LU,Factorization of a matrix
#### We use a E (elimination matrix) help A to get U.Thas is EA=U.e,g
> $\begin{bmatrix} 1 & 0 \\-4 &1 \end{bmatrix}$$\begin{bmatrix} 2 &1 \\8&7 \end{bmatrix}$=$\begin{bmatrix} 2 &1 \\0&3 \end{bmatrix}$
#### If we use the form A=LU,it will be:$A=E^{-1}U=LU$
> $\begin{bmatrix} 2 &1 \\8&7 \end{bmatrix}$=$\begin{bmatrix} 1 & 0 \\4 &1 \end{bmatrix}$$\begin{bmatrix} 2 &1 \\0&3 \end{bmatrix}$
> from E to $E^{-1}$ we just need change 4 to -4.

#### Now n =2,let's talk about the situation n = 3
> $E_{32}E_{31}E_{21}A=U$ --> $A=E_{21}^{-1}E_{31}^{-1}E_{32}^{-1}U=LU $

#### Q:Why we use A=LU instead of EA=U
> (1)E on the left of A need more operation than L, so we use L.
> (2)L can keep the multipliers in matrix.If no row exchanges,mutlipliers go directly into L.

#### Some basic information for Permutation matrix.
> ##### we list all of the permutation matrix.e,g:n=3
> $\begin{bmatrix} 1 & 0 & 0\\0&1&0 \\0& 0&1 \end{bmatrix}$ ,$\begin{bmatrix} 0 & 1 & 0\\1&0&0 \\0& 0&1 \end{bmatrix}$,$\begin{bmatrix} 0 & 0 & 1\\0&1&0 \\1& 0&0 \end{bmatrix}$ ,$\begin{bmatrix} 1 & 0 & 0\\0&0&1 \\0& 1&0 \end{bmatrix}$ ,$\begin{bmatrix} 0 & 1 & 0\\0&0&1 \\1& 0&0 \end{bmatrix}$ ,$\begin{bmatrix} 0 & 0 & 1\\1&0&0 \\0& 1&0 \end{bmatrix}$
> ##### A fact of permutation is ,the inverses matrix are the transposes.


# Day5:
## 1、Permutation and transpos
### Permutation
#### With P(Permutation matrix) we can exchange the rows in A,if 0 in the pivot pisition,then we need do use P.
> A=LI --> PA = LU
#### Some matrix have rule:
> $P^{-1}=P^T$-->$P^TP=I$

### Transpose matrix
#### $(A^T)_{ij}=A_{ji}$
> $\begin{bmatrix} 1 & 3\\ 2&3 \\4&1 \end{bmatrix}$ --> $\begin{bmatrix} 1&2&4 \\ 3&3&1 \end{bmatrix}$

#### Symmetrix matrix:if $A^T=A$,we call it symmetric.

#### one rule:$A A^T = $ Symmetric matrix
> becaus:$(A^T A)^T=A^T A$,
