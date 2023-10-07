# Mathematics

## Matrices

### Introduction to matrices

#### Definition of a matrix

A matrix is an array of mathematical elements

If a matrix has 2 rows and 3 columns it is a 2x3 matrix:

$$
  A = \begin{bmatrix}
    a & b & c\\
    d & e & f
  \end{bmatrix}
$$

If a matrix has 3 rows and 2 columns it is a 3x2 matrix:

$$
  A = \begin{bmatrix}
    a & b \\
    c & d \\
    e & f
  \end{bmatrix}
$$

These are both rectangular matrices

A square matrix has the same number of rows as columns:

$$
  A = \begin{bmatrix}
    a & b \\
    c & d
  \end{bmatrix}
$$

If either the number of rows or columns is 1, the matrix is a vector

If the number of rows is 1 it is a row vector:

$$
  A = \begin{bmatrix}
    a & b & c
  \end{bmatrix}
$$

If the number of columns is 1 it is a column vector:

$$
  A = \begin{bmatrix}
    a \\
    b \\
    c
  \end{bmatrix}
$$

The general notation for an MxN matrix is:

$$
  A = \begin{bmatrix}
    a_{11} & a_{12} & \dots  & a_{1n} \\
    a_{21} & a_{22} & \dots  & a_{2n} \\
    \vdots & \vdots & \ddots & \vdots \\
    a_{m1} & a_{m2} & \dots  & a_{mn}
  \end{bmatrix}
$$

#### Addition and multiplication

Matrices of the same size can be added element by element:

$$
  \begin{bmatrix}
    a & b \\
    c & d
  \end{bmatrix} + \begin{bmatrix}
    e & f \\
    g & h
  \end{bmatrix} = \begin{bmatrix}
    a+e & b+f \\
    c+g & d+h
  \end{bmatrix}
$$

Matrices which are not the same size cannot be added

Multiplying a matrix by a scalar is also element by element:

$$
  \begin{bmatrix}
    a & b \\
    c & d
  \end{bmatrix} \times e = \begin{bmatrix}
    ae & be \\
    ce & de
  \end{bmatrix}
$$

The matrix can be any size when multiplying by a scalar

Multiplying two matrices requires multiplying across the rows of the first matrix, and down the columns of the second and summing the result:

$$
  \begin{bmatrix}
    a & b \\
    c & d
  \end{bmatrix} \times \begin{bmatrix}
    e & f \\
    g & h
  \end{bmatrix} = \begin{bmatrix}
    ae+bg & af+bh \\
    ce+dg & cf+dh
  \end{bmatrix}
$$

The order of the matrices in the multiplication is important (they do not commute):

$$
  \begin{bmatrix}
    e & f \\
    g & h
  \end{bmatrix} \times \begin{bmatrix}
    a & b \\
    c & d
  \end{bmatrix} = \begin{bmatrix}
    ea+fc & eb+fd \\
    ga+hc & gb+hd
  \end{bmatrix}
$$

Because the rows of the first matrix are multiplied by the columns of the second, the first matrix must have the same number of rows as the second's number of columns

The general formula for the multiplication of matrices is:

$$
C = A B
$$

$$
\ c_{ij} = \sum_{k=1}^{n} 2^{-n} = a_{ik} b_{kj}
$$

#### Special matrices

The zero matrix is one where all elements are equal to zero:

$$
  0 = \begin{bmatrix}
    0 & 0 \\
    0 & 0
  \end{bmatrix}
$$

The identity matrix is a matrix where diagonal elements are equal to 1, and all other elements are 0:

$$
  I = \begin{bmatrix}
    1 & 0 \\
    0 & 1
  \end{bmatrix}
$$

The identity matrix does commute:

$$
AI = IA
$$

Diagonal matrices have non-zero elements only on the diagonal:

$$
  D = \begin{bmatrix}
    d_{11} & 0 \\
    0 & d_{22}
  \end{bmatrix}
$$

Banded matrices have non-zero elements on the bands parallel to the diagonal

For example, a tridiagonal banded matrix has three bands:

$$
  B = \begin{bmatrix}
    b_{11} & b_{12} & 0 \\
    b_{21} & b_{22} & b_{23} \\
    0 & b_{32} & b_{33}
  \end{bmatrix}
$$

Triangular matrices have elements either above or below the diagonal

An upper diagonal matrix:

$$
  U = \begin{bmatrix}
    u_{11} & u_{12} & u_{13} \\
    0 & u_{22} & u_{23} \\
    0 & 0 & u_{33}
  \end{bmatrix}
$$

A lower diagonal matrix:

$$
  L = \begin{bmatrix}
    l_{11} & 0 & 0 \\
    l_{21} & l_{22} & 0 \\
    l_{31} & l_{32} & l_{33}
  \end{bmatrix}
$$

#### Transpose matrices

A transpose of a matrix is its mirror along the diagonal

When transposed, a matrix's rows become its columns and its columns its rows

$$
  A = \begin{bmatrix}
    a_{11} & a_{12} & \dots  & a_{1n} \\
    a_{21} & a_{22} & \dots  & a_{2n} \\
    \vdots & \vdots & \ddots & \vdots \\
    a_{m1} & a_{m2} & \dots  & a_{mn}
  \end{bmatrix}
$$

$$
  A^{T} = \begin{bmatrix}
    a_{11} & a_{21} & \dots  & a_{m1} \\
    a_{12} & a_{22} & \dots  & a_{m2} \\
    \vdots & \vdots & \ddots & \vdots \\
    a_{n1} & a_{2n} & \dots  & a_{mn}
  \end{bmatrix}
$$

$$
  A_{ij} = A_{ji}
$$

When transposing an MxN matrix, it becomes NxM

Transposing a transpose returns the original matrix

$$
(A^{T})^{T} = A
$$

Adding two matrices and transposing is equal to the sum of the transposes

$$
(A+B)^{T} = A^{T} + B^{T}
$$

Multiplying two matrices and transposing is equal to the reverse of the product of the transposes

$$
(AB)^{T} = B^{T} A^{T}
$$

If a matrix's transpose is equal to the matrix, it is said to be symmetric

$$
A = A^{T}
$$

If a matrix's transpose is equal to the negative of the matrix, it is said to be skew-symmetric

$$
-A = A^{T}
$$

#### Inner and outer products

The inner product is the same as the dot product

$$
  U = \begin{bmatrix}
    u_{1} \\
    u_{2} \\
    u_{3}
  \end{bmatrix},  V = \begin{bmatrix}
    v_{1} \\
    v_{2} \\
    v_{3}
  \end{bmatrix}
$$

To calculate the inner product, one matrix must be transposed

$$
U^{T} V = \begin{bmatrix}
    u_{1} & u_{2} & u_{3}
  \end{bmatrix} \begin{bmatrix}
    v_{1} \\
    v_{2} \\
    v_{3}
  \end{bmatrix} = u_{1}v_{1} + u_{2}v_{2} + u_{3}v_{3}
$$

If the inner product is equal to 0, then U and V are orthogonal

The norm of a vector is it's length

$$
\|U\| = \sqrt{U^{T} U} = \sqrt{u_{1}^2+u_{2}^2+u_{3}^2}
$$

A vector has been normalised when the norm is equal to 1

If two vectors are both orthogonal and normalised, they are orthonormal

The outer product is the inverse of the inner product

$$
U V^{T} = \begin{bmatrix}
    u_{1} \\
    u_{2} \\
    u_{3}
  \end{bmatrix} \begin{bmatrix}
    v_{1} & v_{2} & v_{3}
  \end{bmatrix} = \begin{bmatrix}
    u_{1}v_{1} & u_{1}v_{2} & u_{1}v_{3}\\
    u_{2}v_{1} & u_{2}v_{2} & u_{2}v_{3}\\
    u_{3}v_{1} & u_{3}v_{2} & u_{3}v_{3}
  \end{bmatrix}
$$

#### Inverse matrices

Not all matrices can be inverted

A matrix is only invertible when the matrix is square and:

$$
A A^{-1} = I = A^{-1} A
$$

Multiplying two matrices and inverting them is equal to the reverse of the product of the inverses

$$
(AB)^{-1} = B^{-1} A^{-1}
$$

The inverse of a transpose is equal to the transpose of an inverse:

$$
(A^{T})^{-1} = (A^{-1})^{T}
$$

Some equations are derived which can be used to calculate the inverse

$$
A A^{-1} = I
$$

$$
  \begin{bmatrix}
    a & b \\
    c & d
  \end{bmatrix} \begin{bmatrix}
    x_{1} & x_{2} \\
    y_{1} & y_{2}
  \end{bmatrix} = \begin{bmatrix}
    1 & 0 \\
    0 & 1
  \end{bmatrix}
$$

We can make the following set of equations:

$$
\begin{align*}
a x_{1} + b y_{1} &= 1 \\
a x_{2} + b y_{2} &= 0 \\
c x_{1} + d y_{1} &= 0 \\
c x_{2} + d y_{2} &= 1
\end{align*}
$$

Therefore:

$$
\begin{align*}
y_{1} &= \dfrac{-c}{d} x_{1} \\
y_{2} &= \dfrac{-a}{b} x_{2}
\end{align*}
$$

Finding x1:

$$
\begin{align*}
a x_{1} + b y_{1} &= 1 \\
a x_{1} + b \dfrac{-c}{d} x_{1} &= 1 \\
x_{1}\left(\dfrac{ad}{d} - \dfrac{bc}{d}\right)&= 1 \\
x_{1} &= \dfrac{d}{ad-bc}
\end{align*}
$$

Finding y1:

$$
\begin{align*}
y_{1} &= \dfrac{-c}{d} x_{1} \\
y_{1} &= \dfrac{-c}{d} \dfrac{d}{ad-bc} \\
y_{1} &= \dfrac{-c}{ad-bc}
\end{align*}
$$

Finding x2:

$$
\begin{align*}
c x_{2} + d y_{2} &= 1 \\
c x_{2} + d \dfrac{-a}{b} x_{2} &= 1 \\
x_{2}\left(\dfrac{cb}{b} - \dfrac{ad}{b}\right) &= 1 \\
x_{2} &= \dfrac{b}{cb-ad} \\
x_{2} &= \dfrac{-b}{ad-bc}
\end{align*}
$$

Finding y2:

$$
\begin{align*}
y_{2} &= \dfrac{-a}{b} x_{2} \\
y_{2} &= \dfrac{-a}{b} \dfrac{-b}{ad-bc} \\
y_{2} &= \dfrac{a}{ad-bc}
\end{align*}
$$

Therefore:

$$
A^{-1} = \dfrac{1}{ad-bc} \begin{bmatrix}
    d & -b \\
    -c & a
  \end{bmatrix}
$$

And so, the determinant of the 2x2 matrix is:

$$
|A| = ad-bc
$$

If the determinant is equal to 0, then the matrix is not invertible

#### Orthogonal matrices

The inverse of an orthogonal matrix is equal to the transpose of the matrix

$$
Q^{-1} = Q^{T}
$$

Therefore:

$$
\begin{align*}
Q Q^{T} &= I \\
Q^{T} Q &= I
\end{align*}
$$

Both the rows and columns of an orthogonal matrix are orthogonal

Orthogonal matrices preserve norms; for a matrix Q and column vector x the norm is:

$$
(Q x)^{T} (Q x) = \| Qx \|^{2}
$$

We can write the first expression as:

$$
x^{T} Q^{T} Q x
$$

As $Q^{T} Q = I$, we can simplify to:

$$
x^{T} x
$$

Which becomes:

$$
\| x \|^{2}
$$

Therefore, we can prove that the orthogonal matrix Q preserves norms (lengths) because:

$$
\| x \|^{2} = \| Qx \|^{2}
$$

#### Permutation matrices

Permutation matrices are a type of orthogonal matrix

When an NxN permutation matrix is multiplied by another matrix, the rows of the matrix are permuted (rearranged)

For a 2x2 matrix, there are 2 possible permutations

The first permutation is that there is no change, this happens when the permutation matrix is the identity matrix:

$$
  \begin{bmatrix}
    1 & 0 \\
    0 & 1
  \end{bmatrix} \begin{bmatrix}
    a & b \\
    c & d
  \end{bmatrix} = \begin{bmatrix}
    a & b \\
    c & d
  \end{bmatrix}
$$

For the second permutation:

$$
  \begin{bmatrix}
    0 & 1 \\
    1 & 0
  \end{bmatrix} \begin{bmatrix}
    a & b \\
    c & d
  \end{bmatrix} = \begin{bmatrix}
    c & d \\
    a & b
  \end{bmatrix}
$$

For a 3x3 matrix, the number of possible permutations is $3! = 6$

Permutation matrices may be obtained by permuting the rows of the identity matrix:

$$
P A = (P I) A
$$

### Systems of Linear Equations

#### Gaussian elimination

Gaussian elimination is used to solve systems of linear equations

Gaussian elimination relies on performing operations on a matrix made up of a system of linear equations which modify the matrix without changing the solution

This includes:

- Permuting the rows
- Multiplying rows by a constant
- Summing rows which have been multiplied by a constant

These operations are performed on the matrix until an upper triangular matrix is formed

An example is used below to demonstrate the process

$$
\begin{align*}
-3x_1+2x_2-x_3&=-1\\
6x_1-6x_2+7x_3&=-7\\
3x_1-4x_2+4x_3&=-6
\end{align*}
$$

First, the system of equations are written as a matrix multiplication

$$
 \begin{bmatrix}
    -3 & 2 & -1 \\
    6 & -6 & 7 \\
    3 & -4 & 4
  \end{bmatrix} \begin{bmatrix}
    x_1 \\
    x_2 \\
    x_3
  \end{bmatrix} = \begin{bmatrix}
    -1 \\
    -7 \\
    -6
  \end{bmatrix}
$$

From this, the augmented matrix can be formed

$$
 \begin{bmatrix}
    -3 & 2 & -1 & -1\\
    6 & -6 & 7 & -7\\
    3 & -4 & 4 & -6
  \end{bmatrix}
$$

A pivot (red) is selected, and the rows below the pivot undergo operations to make any values directly below the pivot equal to zero

$$
 \begin{bmatrix}
    \color{red}{-3} & 2 & -1 & -1\\
    6 & -6 & 7 & -7\\
    3 & -4 & 4 & -6
  \end{bmatrix}
 \begin{matrix}
     \\
    + 2 \times Row 1\\
    + 1 \times Row 1
  \end{matrix} \Rightarrow  \begin{bmatrix}
    -3 & 2 & -1 & -1\\
    0 & -2 & 5 & -9\\
    0 & -2 & 3 & -7
  \end{bmatrix}
$$

A new pivot is then selected, and the same procedure is repeated

$$
\begin{bmatrix}
    -3 & 2 & -1 & -1\\
    0 & \color{red}{-2} & 5 & -9\\
    0 & -2 & 3 & -7
  \end{bmatrix}
 \begin{matrix}
   \\
   \\
    + -1 \times Row 2
  \end{matrix} \Rightarrow  \begin{bmatrix}
    -3 & 2 & -1 & -1\\
    0 & -2 & 5 & -9\\
    0 & 0 & -2 & 2
  \end{bmatrix}
$$

This matrix can now be converted back into a system of equations to be solved by back substitution

$$
\begin{align*}
-3x_1+2x_2-x_3&=-1\\
-2x_2+5x_3&=-9\\
-2x_3&=2\\
x_3 &= -1
\end{align*}
$$

$$
\begin{align*}
-2 x_2 - 5&=-9\\
-2x_2&=-4\\
x_2&=2
\end{align*}
$$

$$
\begin{align*}
-3x_1+4+1&=-1\\
-2x_1&=-6\\
x_1&=2
\end{align*}
$$

#### Reduced row echelon form

The reduced row echelon form is an expansion on Gaussian elimination

In this form, the diagonal elements of the matrix should all become one, and the values above and below them equal to zero

$$
 A = \begin{bmatrix}
    1 & 2 & 3 & 4\\
    4 & 5 & 6 & 7\\
    6 & 7 & 8 & 9
  \end{bmatrix}
$$

$$
 \begin{bmatrix}
    \color{red}{1} & 2 & 3 & 4\\
    4 & 5 & 6 & 7\\
    6 & 7 & 8 & 9
  \end{bmatrix}
 \begin{matrix}
     \\
    + -4 \times Row 1\\
    + -6 \times Row 1
  \end{matrix} \Rightarrow  \begin{bmatrix}
    1 & 2 & 3 & 4\\
    0 & -3 & -6 & -9\\
    0 & -5 & -10 & -15
  \end{bmatrix}
$$

$$
 \begin{bmatrix}
    1 & 2 & 3 & 4\\
    0 & -3 & -6 & -9\\
    0 & -5 & -10 & -15
  \end{bmatrix}
 \begin{matrix}
     \\
    \div -3\\
    \div -5
  \end{matrix} \Rightarrow  \begin{bmatrix}
    1 & 2 & 3 & 4\\
    0 & 1 & 2 & 3\\
    0 & 1 & 2 & 3
  \end{bmatrix}
$$

$$
 \begin{bmatrix}
    1 & 2 & 3 & 4\\
    0 & \color{red}{1} & 2 & 3\\
    0 & 1 & 2 & 3
  \end{bmatrix}
 \begin{matrix}
    + -2 \times Row 2 \\
    \\
    + -1 \times Row 2
  \end{matrix} \Rightarrow  \begin{bmatrix}
    1 & 0 & -1 & -2\\
    0 & 1 & 2 & 3\\
    0 & 0 & 0 & 0
  \end{bmatrix}
$$

$$
RREF(A) = \begin{bmatrix}
    1 & 0 & -1 & -2\\
    0 & 1 & 2 & 3\\
    0 & 0 & 0 & 0
  \end{bmatrix}
$$

#### Computing inverses

The reduced row echelon form can be used to find inverses of matrices

$$
A = \begin{bmatrix}
-3 & 2 & -1 \\
6 & -6 & 7 \\
3 & -4 & 4
\end{bmatrix}
$$

For a matrix to be invertible:

$$
\begin{align*}
A A^{-1} &= I \\
A a_{i}^{-1} &= e_i
\end{align*}
$$

We combine the identity matrix and the original matrix for the augmented matrix:

$$
\begin{bmatrix}
-3 & 2 & -1 & 1 & 0 & 0\\
6 & -6 & 7 & 0 & 1 & 0\\
3 & -4 & 4 & 0 & 0 & 1
\end{bmatrix}
$$

And calculate the reduced row echelon form:

$$
\begin{bmatrix}
\color{red}{-3} & 2 & -1 & 1 & 0 & 0\\
6 & -6 & 7 & 0 & 1 & 0\\
3 & -4 & 4 & 0 & 0 & 1
\end{bmatrix}
\begin{matrix}
{}\\
{}+ 2 \times Row 1\\
{}+ 1 \times Row 1
\end{matrix} \Rightarrow  \begin{bmatrix}
-3 & 2 & -1 & 0 & 0 & 0\\
0 & -2 & 5 & 2& 1 & 0\\
0 & -2 & 3 & 1 & 0 & 1
\end{bmatrix}
$$

$$
\begin{bmatrix}
-3 & 2 & -1 & 0 & 0 & 0\\
0 & \color{red}{-2} & 5 & 2& 1 & 0\\
0 & -2 & 3 & 1 & 0 & 1
\end{bmatrix}
\begin{matrix}
{}+ 1 \times Row 2\\
{}\\
{}+ -1 \times Row 2
\end{matrix} \Rightarrow  \begin{bmatrix}
-3 & 0 & 4 & 3 & 1 & 0\\
0 & -2 & 5 & 2& 1 & 0\\
0 & 0 & -2 & -1 & -1 & 1
\end{bmatrix}
$$

$$
\begin{bmatrix}
-3 & 0 & 4 & 3 & 1 & 0\\
0 & -2 & 5 & 2& 1 & 0\\
0 & 0 & \color{red}{-2} & -1 & -1 & 1
\end{bmatrix}
\begin{matrix}
{}+ 2 \times Row 3\\
{}+ 2.5 \times Row 3\\
{}
\end{matrix} \Rightarrow  \begin{bmatrix}
-3 & 0 & 0 & 1 & -1 & 2\\
0 & -2 & 0 & -\frac{1}{2} & -\frac{3}{2} & \frac{5}{2}\\
0 & 0 & -2 & -1 & -1 & 1
\end{bmatrix}
$$

$$
\begin{bmatrix}
-3 & 0 & 0 & 1 & -1 & 2\\
0 & -2 & 0 & -\frac{1}{2} & -\frac{3}{2} & \frac{5}{2}\\
0 & 0 & -2 & -1 & -1 & 1
\end{bmatrix}
\begin{matrix}
\div -3\\
\div -2\\
\div -2
\end{matrix} \Rightarrow  \begin{bmatrix}
1 & 0 & 0 & -\frac{1}{3} & \frac{1}{3} & -\frac{2}{3}\\
0 & 1 & 0 & \frac{1}{4} & \frac{3}{4} & -\frac{5}{4}\\
0 & 0 & 1 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2}
\end{bmatrix}
$$

Therefore the inverse is:

$$
A=
\begin{bmatrix}
1 & 0 & 0 & -\frac{1}{3} & \frac{1}{3} & -\frac{2}{3}\\
0 & 1 & 0 & \frac{1}{4} & \frac{3}{4} & -\frac{5}{4}\\
0 & 0 & 1 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2}
\end{bmatrix}
$$

#### Elementary matrices and LU decomposition

Gaussian elimination returns a matrix $A$ as an upper triangular matrix

This cal also be expressed as an upper triangular matrix $U$ multiplied by a lower triangular matrix $L$

This is referred to as a matrix decomposition

$$
A = \begin{bmatrix}
-3 & 2 & -1 \\
6 & -6 & 7 \\
3 & -4 & 4
\end{bmatrix}
$$

$$
\begin{bmatrix}
\color{red}{-3} & 2 & -1 \\
6 & -6 & 7 \\
3 & -4 & 4
\end{bmatrix}
\begin{matrix}
{} \\
{} + 2 \times Row 1\\
{}
\end{matrix} \Rightarrow  \begin{bmatrix}
-3 & 2 & -1 \\
0 & -2 & 5 \\
3 & -4 & 4
\end{bmatrix} = M_1 A
$$

As we added $2\times$ the first row to the second, the first elementary matrix is:

$$
M_1 = \begin{bmatrix}
1 & 0 & 0 \\
2 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

$$
\begin{bmatrix}
\color{red}{-3} & 2 & -1 \\
0 & -2 & 5 \\
3 & -4 & 4
\end{bmatrix}
\begin{matrix}
{} \\
{} \\
{} + 1 \times Row 1
\end{matrix} \Rightarrow  \begin{bmatrix}
-3 & 2 & -1 \\
0 & -2 & 5 \\
0 & -2 & 3
\end{bmatrix} = M_2 M_1 A
$$

And so the second elementary matrix becomes:

$$
M_2 = \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
1 & 0 & 1
\end{bmatrix}
$$

$$
\begin{bmatrix}
-3 & 2 & -1 \\
0 & \color{red}{-2} & 5 \\
0 & -2 & 3
\end{bmatrix}
\begin{matrix}
{} \\
{} \\
{} + -1 \times Row 2
\end{matrix} \Rightarrow  \begin{bmatrix}
-3 & 2 & -1 \\
0 & -2 & 5 \\
0 & 0 & -2
\end{bmatrix} = M_3 M_2 M_1 A = U
$$

And the third elementary matrix:

$$
M_3 = \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & -1 & 1
\end{bmatrix}
$$

Where:

$$
M_3 M_2 M_1 A = U
$$

$$
\therefore A = M_1^{-1} M_2^{-1} M_3^{-1} U
$$

The inverses of the elementary matrices are found:

$$
M_1 = \begin{bmatrix}
1 & 0 & 0 \\
2 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix} M_2 = \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
1 & 0 & 1
\end{bmatrix} M_3 = \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & -1 & 1
\end{bmatrix}
$$

$$
M_1^{-1} = \begin{bmatrix}
1 & 0 & 0 \\
-2 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix} M_2^{-1} = \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
-1 & 0 & 1
\end{bmatrix} M_3^{-1} = \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 1 & 1
\end{bmatrix}
$$

The elementary matrices are then multiplied:

$$
M_1^{-1} M_2^{-1} = \begin{bmatrix}
1 & 0 & 0 \\
-2 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix} \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
-1 & 0 & 1
\end{bmatrix} = \begin{bmatrix}
1 & 0 & 0 \\
-2 & 1 & 0 \\
-1 & 0 & 1
\end{bmatrix}
$$

$$
(M_1^{-1} M_2^{-1}) M_3^{-1} = \begin{bmatrix}
1 & 0 & 0 \\
-2 & 1 & 0 \\
-1 & 0 & 1
\end{bmatrix} \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 1 & 1
\end{bmatrix} = \begin{bmatrix}
1 & 0 & 0 \\
-2 & 1 & 0 \\
-1 & 1 & 1
\end{bmatrix}
$$

And a lower triangular matrix is produced:

$$
L = \begin{bmatrix}
1 & 0 & 0 \\
-2 & 1 & 0 \\
-1 & 1 & 1
\end{bmatrix}
$$

$$
\therefore A = L U
$$

### Vector spaces

#### Introduction to vector spaces

#### Linear independence

#### Span, basis, and dimension

#### Gram-Schmidt process

#### Null space

#### Column space

#### Row space, left null space, and rank

#### Orthogonal projections

#### The least-squares problem

### Eigenvalues and eigenvectors

#### Two by two and three by thee determinants

#### Laplace expansion

#### Leibniz formula

#### Properties of a determinant

#### The eigenvalue problem

#### Finding eigenvalues and eigenvectors

#### Matrix diagonalisation

#### Powers of a matrix

---

## Differential equations

### First-order differential equations

#### Euler method

#### Seperable equations

#### Linear first order equations

### Homogeneous linear differential equations

#### Euler method for higher order ODEs

#### The principle of superposition

#### The wronskian

#### Homogeneous second order ODE with constant coefficients

#### Distinct real roots

#### Complex conjugate roots

#### Repeated roots

### Inhomogeneous linear differential equations

#### Inhomogeneous second order ODE

#### Inhomogeneous term: exponential function

#### Inhomogeneous term: sine or cosine

#### Inhomogeneous term: polynomials

#### Resonance

### The laplace transform and series solution methods

#### Definition of the laplace transform

#### Laplace transform of a constant coefficient ODE

#### Solution og an initial value problem

#### The heaviside step function

#### The dirac delta function

#### Solution of a discontinuous inhomogeneous term

#### Solution of an impulsive inhomogeneous term

#### The series solution method

#### Series solution of the Airy's equation

### Systems of differential equations

#### Systems of homogeneous linear first order ODEs

#### Distinct real eigenvalues

#### Complex-conjugate eigenvalues

#### Phase portraits

#### Stable and unstable nodes

#### Saddle points

#### Spirals

#### Coupled oscillators

#### Normal modes (eigenvalues)

#### Normal modes (eigenvectors)

### Partial differential equations

#### Fourier series

#### Fourier sine and cosine series

#### The diffusion equation

#### Solution of the diffusion equation: separation of variables

#### Solution of the diffusion equation: eigenvalues

#### Solution of the diffusion equation: Fourier series

---

## Vector calculus

### Vectors

#### Introduction to vectors

#### Cartesian coordinates

#### Dot product

#### Cross product

#### Quaternions

#### Analytic geometry of lines

#### Analytic geometry of planes

#### Kronecker delta and Levi-Civita symbol

#### Vector identities

#### Scalar triple product

#### Vector triple product

#### Scalar and vector fields

### Differentiation

#### Partial derivatives

#### The method of least squares

#### Chain rule

#### Triple product rule

#### Gradient

#### Divergence

#### Curl

#### Laplacian

#### Vector derivative identities

### Integration and curvilinear coordinates

#### Double and triple integrals

#### Polar coordinates (gradient)

#### Polar coordinates (divergence and curl)

#### Polar coordinates (laplacian)

#### Central force

#### Change of variables (single integral)

#### Change of variables (double integral)

#### Cylindrical coordinates

#### Spherical coordinates

### Line and surface integrals

#### Line integral of a scalar field

#### Arc length

#### Line integral of a vector field

#### Work-energy theorem

#### Surface integral of a scalar field

#### Surface area of a sphere

#### Surface integral of a vector field

#### Flux integrals

### Fundamental theorems

#### Gradient theorem

#### Conservative vector fields

### Arithmetic

#### Conservation of energy

#### Divergence theorem

#### Continuity equation

#### Green's theorem

#### Stokes' theorem

#### Meaning of the divergence and the curl

---

## Statistics and probability

### Descriptive statistics

#### Defining data

#### Histograms and skewness

#### Mean, median, variance, and standard deviation

#### Boxplots

#### Categorical data

#### Hierarchical data

#### Pareto charts

### Basic probability

#### Probability

#### Law of complements

#### Mutually exclusive and independent events

#### Conditional probability

#### Law of total probability and Bayes' rule

### Random variables

#### Introduction to random variables

#### Mean, variance, and standard deviation of a random variable

#### Mean, variance, and standard deviation for a sum of random variables

#### Binomial random variable

#### Poisson random variable

#### Normal random variable

#### Central limit theorem

#### Z scores

### Sampling and confidence intervals

#### Populations and samples

#### Point estimation of a population mean and proportion

#### The standard normal

#### Confidence interval estimation

#### Sample size determination

#### The finite correction factor

### Hypothesis testing

#### Defining hypotheses

#### Type I and type II error

#### One sample z-test

#### One sample t-test

#### Single sample test for population proportion

#### Testing equality of variances

#### Testing the difference between two population means

#### Chi-squared test for independence
