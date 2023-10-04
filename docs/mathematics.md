# Mathematics

## Fundamentals

### Algebra

### Trigonometry

### Calculus

### Complex numbers

## Matrices

### Introduction

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

Multiplying a matric by a scalar is also element by element:

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

Multiplying two matrices requires multiplying across the rows of the first matrixs, and down the columns of the second and summing the result:

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

Because the rows of the first matrix are multiplied by the columns of the second, the first matric must have the same number of rows as the second's number of columns

The general formula for the matricplication of matrices is:

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
a x_{1} + b y_{1} = 1 \\
a x_{2} + b y_{2} = 0 \\
c x_{1} + d y_{1} = 0 \\
c x_{2} + d y_{2} = 1
$$

Therefore:

$$
y_{1} = \dfrac{-c}{d} x_{1} \\
y_{2} = \dfrac{-a}{b} x_{2}
$$

Finding x1:

$$
a x_{1} + b y_{1} = 1 \\
a x_{1} + b \dfrac{-c}{d} x_{1} = 1 \\
x_{1}\left(\dfrac{ad}{d} - \dfrac{bc}{d}\right)= 1 \\
x_{1} = \dfrac{d}{ad-bc}
$$

Finding y1:

$$
y_{1} = \dfrac{-c}{d} x_{1} \\
y_{1} = \dfrac{-c}{d} \dfrac{d}{ad-bc} \\
y_{1} = \dfrac{-c}{ad-bc}
$$

Finding x2:

$$
c x_{2} + d y_{2} = 1 \\
c x_{2} + d \dfrac{-a}{b} x_{2} = 1 \\
x_{2}\left(\dfrac{cb}{b} - \dfrac{ad}{b}\right)= 1 \\
x_{2} = \dfrac{b}{cb-ad} \\
x_{2} = \dfrac{-b}{ad-bc}
$$

Finding y2:

$$
y_{2} = \dfrac{-a}{b} x_{2} \\
y_{2} = \dfrac{-a}{b} \dfrac{-b}{ad-bc} \\
y_{2} = \dfrac{a}{ad-bc}
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
Q Q^{T} = I \\
Q^{T} Q = I
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

As $$Q^{T} Q = I$$, we can simplify to:

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
-3x_1+2x_2-x_3=-1\\
6x_1-6x_2+7x_3=-7\\
3x_1-4x_2+4x_3=-6
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
    \color{red}-3 & 2 & -1 & -1\\
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
    0 & \color{red}-2 & 5 & -9\\
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
-3x_1+2x_2-x_3=-1\\
-2x_2+5x_3=-9\\
-2x_3=2
$$

$$
x_3 = -1
$$

$$
-2 x_2 - 5=-9\\
-2x_2=-4\\
x_2=2
$$

$$
-3x_1+4+1=-1\\
-2x_1=-6\\
x_1=2
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
    \color{red}1 & 2 & 3 & 4\\
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
    0 & \color{red}1 & 2 & 3\\
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

#### Elementary matrices

#### LU decomposition

### Vector spaces

#### Vector spaces

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

## Differential equations

### First-order differential equations

### Homogeneous linear differential equations

### Inhomogeneous linear differential equations

### The laplace transform and series solution methods

### Systems of differential equations

### Partial differential equations

## Vector calculus

### Vectors

### Differentiation

### Integration and curbvilinear coordinates

### Line and surface integrals

### Fundamental theorems

## Statistics and probability

### Descriptive statistics

### Basic probability

### Random variables

### Damplins and confidence intervals

### Hypothesis testing
