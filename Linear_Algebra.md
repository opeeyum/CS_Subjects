# Matrix
Matrix is simply a multidimensional array.

- **If m != n, Rectanguar Matrix**
- **If m == n, Square Matrix**

### Unit Matrix
A ***Square Matrix*** whose all Principal Diagonal matrix are equal to 1, and remaing elements are 0.

### Null Matrix 
A ***Square or Non-Square*** (rectangular) matrix with all elements equal to 0 is termed as Null Or ***Zero*** matrix.

### Row Matrix
Matrix having only ***1 Row***.

### Column Matrix
Matrix having only ***1 Column***.

### Sub-Matrix
Any matrix obtained by omitting some rows and Columns from a given, (m X n) matrix 'A', is called Sub-matrix of 'A'.

#### Principal Sub-Matrix
A ***Square Sub-matrix*** of a Square matrix 'A' is called Principal Sub-matrix, if its (sub-matrix) diagonal elements are also the diagonal elements of matrix 'A'.

### Equality of Matrix
Two or more matrices are said to be Equal if they are of:
1. Same Size, order should be same.
2. The Elements in the corresponding places are same.


## Addition of Matrices
Addition of Matrices is only possible when matrices are ***Conformable***, i.e Same Size.

### Properties of Addition
1. Commutative: A + B = B + A
2. Associative: (A + B) + C = A + (B + C)
3. Existence of additive ***identity***: A + 0 = 0 + A
4. Existence of additive ***inverse***: -A + A = 0 = A + (-A)
5. Cancellation law:
   - A + B = A + C -> B = C
   - B + A = C + A -> B = C

## Substraction of Matrices
Substaction of Matrices is only possible when matrices are ***Conformable***, i.e Same Size.
A - B = A + (-B)

> Properties of addition also holds in Subtraction.

## Scalar multiplication of Matrix
If A = \[a*ij*]*m x n*, then
- K * A = A * K = \[K a*ij*]*m x n*

### Properties of Scalar Multiplication
1. K * (A + B) = KA + KB
2. (P + Q) * A = PA + QA
3. P * (Q * A) = (P * Q) * A
4. (-K) * A = -(K * A) = K * (-A)

## Multiplication of Matrices
Multiplication of matrices is only possible when they are ***multiplication conformable***, that is  - number of column in frist matrix should be equal to number of rows in second matrix.

### Properties of matrix multiplication
1. Matrix multiplication is Associative (A * B) * C = A * (B * C)
2. Matrix multiplication is distributive with respect to addition of matrices: A * (B + C) = AB + AC
3. Matrix Multiplication is not ***Always Commutative***: AB != BA
   - If AB == BA, then the matrices 'A' and 'B' are said to **commute**.
   - If AB == -BA, then the matrices are said to be **anti-commute**.
4. The equation AB = 0, does not necessarily imply that one of the matrices 'A' and 'B' must be a Zero matrix.
   - If AB = 0, then it does not necessarily imply that BA = 0.
















