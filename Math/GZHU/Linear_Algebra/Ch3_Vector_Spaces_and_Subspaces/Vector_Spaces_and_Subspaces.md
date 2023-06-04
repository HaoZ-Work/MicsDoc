## 3.1、Vector Space and Subspace of it.
#### Vector space:$R^n$,it is a space which have all vector with n components.
> $R^2$:the space which have all vector with 2,$\begin{bmatrix} 3 & 2 \end{bmatrix}$
> $R^3$:the space which have all vector with 3,$\begin{bmatrix} 3 & 2&1 \end{bmatrix}$
#### A rule for vector space:A vector space has to te closed under multiplication and addition of vector.That means after multiplication and the addition of the vector ,the vector is still in the vector space.

#### Subspace:A part of vector space.
> subspace of $R^2$
> - all of $R^2$
> - any line through,$\begin{bmatrix} 0\\ 0 \end{bmatrix}$
> - zero vector only.

> subspace of $R^3$
> - all of $R^3$
> - any plane incuded $\begin{bmatrix} 0\\ 0 \\0\end{bmatrix}$
> - any line through,$\begin{bmatrix} 0\\0 \\0\end{bmatrix}$
> - zero vector only.

#### The most import idea:
> We use to vector $\begin{bmatrix} 1\\ 2 \\3\end{bmatrix}$ and $\begin{bmatrix} 2\\ 2 \\5\end{bmatrix}$,any combinations(opration multiplication and addition) of these two vectors build a subspace.And all of the result of combinations are in this subspace.The subspace is included by $R^3$ vector space.
> ##### We use $R^3$ because we can not image what it will be in $R^{10}$,but the situation is same.

## 3.2、
### Column space of A:solving Ax=b
> ##### We konw that not every equation Ax=b have solution,so the question is,if we want to get a solution for equation which b is satisfied?
> $\begin{bmatrix} 1&1&2 \\ 2 &1&3 \\ 3 &1 &4 \\ 4&1&5\end{bmatrix}$ $\begin{bmatrix} x_1 \\ x_2 \\x_3 \end{bmatrix}$= $\begin{bmatrix} b_1\\ b_2 \\b_3 \\ b_4\end{bmatrix}$
> ##### We can take some examples:
>if b=$\begin{bmatrix} 1\\ 2 \\3 \\ 4\end{bmatrix}$ then a= $\begin{bmatrix} 1\\ 0 \\0\end{bmatrix}$,if b=$\begin{bmatrix} 2\\ 6\\8 \\ 10\end{bmatrix}$ then a= $\begin{bmatrix} 0\\ 0 \\2\end{bmatrix}$
> ##### Now we know that if we need the equation Ax=b have solution,b must in the subspace of A

### Nullspace
#### Nullspace is a subspace.This subspace contains every x,which can solve Ax=0.
>  $\begin{bmatrix} 1&1&2 \\ 2 &1&3 \\ 3 &1 &4 \\ 4&1&5\end{bmatrix}$ $\begin{bmatrix} x_1 \\ x_2 \\x_3 \end{bmatrix}$ = $\begin{bmatrix} 0 \\ 0 \\0 \end{bmatrix}$
> ##### The x can be :$\begin{bmatrix} 0\\0\\0 \end{bmatrix}$,$\begin{bmatrix} 1 \\ 1 \\-1 \end{bmatrix}$,or$\begin{bmatrix} 2 \\ 2 \\-2 \end{bmatrix}$.We can do a summary:$C\begin{bmatrix} 1 \\ 1 \\-1 \end{bmatrix}$.And this is a the nullpsace of this equation.

## 3.3、Ax=0
### How to solve Ax=0?
> #### Step1:Elimination:A-->U
>  $A = \begin{bmatrix} 1&2&2&2 \\ 2&4&6&8\\3&6&8&10 \end{bmatrix} --> \begin{bmatrix} 1&2&2&2 \\ 0&0&2&4\\0&0&2&4 \end{bmatrix} --> \begin{bmatrix} 1&2&2&2 \\ 0&0&2&4\\0&0&0&0 \end{bmatrix} = U $

> #### Step 2:Pivot columns and free columns. In this example ,the rank of A is 2. So there are two pivot columns and 4-2=2 free columns. It does not matter which x we choosed as pivot or free column.e,g we choose $x_2 =1$, $x_4=0$ as free columns. So $x = \begin{bmatrix} x_1 \\ 1 \\ x_3 \\ 0\end{bmatrix}$

> #### Step 3: Back substitution:
>$$\begin{cases}x_1+2x_2+2x_3+2x_4=0  \\ 2x_3+4x_4=0\end{cases}$$
> ##### then  we get $x = \begin{bmatrix} -2 \\ 1 \\ 0 \\ 0\end{bmatrix}$
> #### This x is one of the solution,we can call it special solution.

### Matrix R: Reduced row echelon form:Zero above and below pivots.
> ##### a example:U --> R
> $U=\begin{bmatrix} 1&2&2&2 \\ 0&0&2&4\\0&0&0&0 \end{bmatrix} -- > \begin{bmatrix} 1&2&0&-2 \\ 0&0&2&4\\0&0&0&0 \end{bmatrix} --> \begin{bmatrix} 1&2&0&-2 \\ 0&0&1&2\\0&0&0&0 \end{bmatrix}=R$

### We look another  example to show  how to compluting some basic question of Ax=0.
> $A=\begin{bmatrix} 1&2&3 \\ 2&4&6 \\2&6&8 \\2&8&10\end{bmatrix} -- > \begin{bmatrix} 1&2&3 \\ 0&2&2 \\0&0&0 \\0&0&0\end{bmatrix} = U$

#### (1) special solution of Ax=0
> The rank of A is 2 which means two pivot columns and one free column.We set $x_3 = 1$,and back substitution $$\begin{cases}x_1+2x_2+3x_3=0  \\ 2x_2+2x_3=0\end{cases}$$,we get $x = \begin{bmatrix} -1 \\ -1 \\ 1\end{bmatrix}$

#### (2) Nullspace of Ax=0
> The nullspace contains all the combinations of the special solutions.The nullspace can be $x = c\begin{bmatrix} -1 \\ -1 \\ 1\end{bmatrix}$,a line in $R^3$ space.c is a number.

#### (3) Basis of the nullspace
> basis of the nullpsace means this vector: $x = \begin{bmatrix} -1 \\ -1 \\ 1\end{bmatrix}$
#### (4) Matrix R of Ax=0
> $\begin{bmatrix} 1&2&3 \\ 0&2&2 \\0&0&0 \\0&0&0\end{bmatrix}--> \begin{bmatrix} 1&0&1 \\ 0&1&1 \\0&0&0 \\0&0&0\end{bmatrix} -- >\begin{bmatrix} I & F \\0 & 0\end{bmatrix}$(F is free column)
#### (5) Matrix N:Nullspace matrix,this is a matrix which the columns in it are special solutions
> So RN=0,if $R=\begin{bmatrix} I & F \\0 & 0\end{bmatrix}$,$N=\begin{bmatrix}-F \\I\end{bmatrix}$ or $N=c\begin{bmatrix}-F \\I\end{bmatrix}$

## 3.4 Ax=b
### First we take a example to show how can we get the complete solution of Ax=b
> $Ax=b -- > \begin{bmatrix} 1&2&2&2 &b_1 \\ 2&4&6&8 &b_2 \\ 3 &6&8 &10 & b_3\end{bmatrix} -- >\begin{bmatrix} 1&2&2&2 &b_1 \\ 0&0&2&4 &b_2-2b_1 \\ 0 &0&0 &0 & b_3-b_2-b_1\end{bmatrix}$
from the row3 we see that $b_3-b_2-b_1=0$,We just suppose that b is $b = \begin{bmatrix} 1 \\ 5 \\ 6\end{bmatrix}$
> the augmented matrix is $\begin{bmatrix} 1&2&2&2 &1\\ 0&0&2&4 &3 \\ 0 &0&0 &0 & 0\end{bmatrix}$,
> #### Step 1:Set all free variables to zero ,to find a particular solution
> we set $x_2=x_4=0$ then we get the equations $$\begin{cases}x_1+2x_3=1  \\ 2x_3=3\end{cases}$$,so a particular solution of Ax=b is $\begin{bmatrix} -2\\ 0\\1.5\\0\end{bmatrix}$
> #### Step 2:Get the nullspace of Ax=b,and plus it to the particular solution.because:
$$X_p+X_n = all\ the\ solutions$$
### Question:The solvability of Ax=b (if it have solution what the condition must b satify? )
> #### When b is in the column space of A.

###  The relationship between the rank and the number of solutions
#### (1)Full column rank:r=n<m
> $A=\begin{bmatrix}1&3 \\2&1 \\ 6&1 \\ 5&1 \end{bmatrix} --> R = \begin{bmatrix}1&0 \\0&1 \\ 0&0 \\ 0&0 \end{bmatrix}= \begin{bmatrix}I \\0 \end{bmatrix}$
> From matrix R we know that there are no free column, so the Nullspace of A have only zero vector and Ax=b have also only one particular solution.

#### (2)Full row rank: r=m<n
> $A=\begin{bmatrix}1 &2&6&5 \\ 3 &1&1&1 \end{bmatrix} --> R = \begin{bmatrix}1 &0&F&F \\ 0 &1&F&F \end{bmatrix}= \begin{bmatrix}I &F \end{bmatrix}$
> The number of pivot variables: r=m, free variables n-r (n-m)
The number of the solution is $\infty$,because the Free variables,we can set any number to free variables,so we have many particular solutions and many vectors in nullspace.

#### (3)Full rank:r=m=n
> $A=\begin{bmatrix}1 &3 \\3 &1\end{bmatrix} -- > R=I$
> this situation have only one solution for Ax=b. It just like a normal equation,such as 5 equations to solve 5 unknowns.

#### (4) r<m ,r<n
> $R=\begin{bmatrix}I & F\\ 0 &0\end{bmatrix}$,this sitution equal the sitution1 union sitution2 so,it have 0 or $\infty$ solutions.

#### Do a summary:The rank tells every about the number of solutions
| rank      | r=m=n        | r=n<m    | r=m<n    | r<m,r<n        |
| --------- | ------------ | -------- | -------- | -------------- |
| solutions | one solution | 0 or one | $\infty$ | 0 or  $\infty$ |

## 3.5 Independence, Basis and Dimension
### Independence
> ##### Independence is used to describe a bunch of vector.$$vector :x_1 ,x_2, ...x_n$$ are independence if there are no combination of them gives zero.which means $$c_1x_1+c_2x_2+...c_nx_n \neq 0 \ (c \neq 0)$$
> ##### In a other word is:vector are combination of A,if they are independence ,the nullspace of A have only zero vector.
> ##### In a other word is:each vector is not equal to the combinations of another vectors.

#### How to know whether if the vectors are indepnedence?
> ##### if rank =0,no free variables-->independence
> ##### if rank < 0, have free variables. dependence.

### Spanning:Vectors span a Space
> #### vectors $v_1,v_2,....v_n$ span a space.this means ,vector build a space,and this space consists all of the combinations of thede vectors.

### Basis
> #### Basis is a sequence of vectors like $v_1,v_2....v_d$.It have 2 main properties:
$$\begin{cases}They \ are \ independence.  \\ They\ can\ span\ the\ whole\ space.\end{cases}$$
> #### e,g. $R^3$ space. one of the basis can be
$$x_1=\begin{bmatrix} 1 \\ 0 \\ 0\end{bmatrix},x_2=\begin{bmatrix} 0 \\ 1 \\ 0\end{bmatrix},x_1=\begin{bmatrix} 0 \\ 0 \\ 1\end{bmatrix}$$
> #### another can be
$$x_1=\begin{bmatrix} 1 \\ 1 \\ 2\end{bmatrix},x_2=\begin{bmatrix} 2 \\ 2 \\ 5\end{bmatrix},x_1=\begin{bmatrix} 2 \\ 3 \\ 8\end{bmatrix}$$

### Dimension
#### (1) Question:We konw that if too many vector in basis may be there are dependence,but if too less they can not describe the whole space. So how many vectors should in a basis?
> ##### e,g:basis of  $R^n$ space.If the matrix is n * n and invertible. To describe this space we need n vectors in a basis.The number of vectors in basis is same with the number rank.
#### We call this number Dimension.
#### (2) A important fact of getting a basis
> #### if we know the dim(A)=n.We can take n vectors,and if they are independence.These vector is a basis of space A.
#### (3) Something important between rank and dimension.
> ##### rank is used to described a matrix.
> ##### dimension is used to described a space.

#### (4) What is the dimension of nullspace?
> ##### This is depend on matrix A. dim N(A) is the number of free variables in A.

## 3.6、Dimension of four Subspaces.
#### 3.6.1、four fundamental subspaces:
> - column space:$C(A)$
> - null psace:$N(A)$
> - row space :all combinations of rows of A. we use $C(A^T)$ to represent it.
> - Null space of row space:$N(A^T)$
#### if A is m * n
> - $C(A)\ is\ in\ R^m$
> - $N(A)\ is\ in\ R^n$
> - $C(A^T)\ is\ in\ R^n$
> - $N(A^T)\ is\ in\ R^m$
> ##### dimension:
> - $dim\ C(A)=r$
> - $dim\ C(A^T)=r$
> - $dim\ N(A)=n-r$
> - $dim\ N(A^T)=m-r$

#### 3.6.2、Row space
##### How to get the basis of $C(A^T)$?
> Basis for row spacc is first r rows of matrix R
> $A=\begin{bmatrix} 1&2&3&1\\ 1&1&2&1 \\ 1&2&3&1\end{bmatrix}-->\begin{bmatrix} 1&0&1&1\\ 0&1&1&0 \\ 0&0&0&0\end{bmatrix}=R$
> from R we know that r = 2, the first and second row can be the basis of $C(A)$
> Basis:$\begin{bmatrix} 1&0&1&1\end{bmatrix}$,$\begin{bmatrix} 0&1&1&0\end{bmatrix}$

#### 3.6.3、Null space $N(A^T)$
##### How to get the basis of left null space?
> ##### Use $EA=R$ to find a vector which can make the combination of rows in A to 0.
> e,g:$EA=R -->EA=\begin{bmatrix}-1&2&0 \\ 1&-1&0\\-1 &0&1 \end{bmatrix} \begin{bmatrix} 1&2&3&1\\ 1&1&2&1 \\ 1&2&3&1\end{bmatrix}--> \begin{bmatrix} 1&0&1&1\\ 0&1&1&0 \\ 0&0&0&0\end{bmatrix}=R$
> ##### In this example, the last row in E,$\begin{bmatrix}-1&0&1\end{bmatrix}$,make matrix A to 0 in R. So this is a basis of left null space.
> ##### That means we need first do elimination to A ,then we get the R and E.Last we get the basis of the $N(A^T)$
