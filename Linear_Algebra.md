# Matrix
Matrix is simply a multidimensional array.

- **If m != n, Rectanguar Matrix**
- **If m == n, Square Matrix**

### 1. Unit Matrix
A ***Square Matrix*** whose all Principal Diagonal matrix are equal to 1, and remaing elements are 0.

### 2. Null Matrix 
A ***Square or Non-Square*** (rectangular) matrix with all elements equal to 0 is termed as Null Or ***Zero*** matrix.

### 3. Row Matrix
Matrix having only ***1 Row***.

### 4. Column Matrix
Matrix having only ***1 Column***.

### 5. Sub-Matrix
Any matrix obtained by omitting some rows and Columns from a given, (m X n) matrix 'A', is called Sub-matrix of 'A'.

#### Principal Sub-Matrix
A ***Square Sub-matrix*** of a Square matrix 'A' is called Principal Sub-matrix, if its (sub-matrix) diagonal elements are also the diagonal elements of matrix 'A'.

### 6. Equality of Matrix
Two or more matrices are said to be Equal if they are of:
1. Same Size, order should be same.
2. The Elements in the corresponding places are same.

## Types of Square Matrix
### 1. Upper Triangular Matrix
A Square matrix, A = \[a *i j* ] is called an upper triangular matrix if a\[ i ]\[ j ] = 0, whenever i > j.

### 2. Lower Triangular Matrix
A Square matrix, A = \[a *i j* ] is called a lower triangular matrix if a\[ i ]\[ j ] = 0, whenever i < j.

- A Triangular matrix A = \[a *i j* ] *m x n* is called Strictly triangular matrix if a\[ i ]\[ i ] = 0, for i = 1, 2, ..., n.

### 3. Diagonal Matrix
A Square matrix, A = \[a *i j* ]*n x n* whose elements above and below the principal diagonal are all zero.

### 4. Scalar Matrix
A diagonal matrix whose diagonal elements are all equal is called a Scalar matrix.

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

## Subtraction of Matrices
Subtaction of Matrices is only possible when matrices are ***Conformable***, i.e Same Size.
A - B = A + (-B)

> Properties of addition also holds in Subtraction.

## Scalar multiplication of Matrix
If A = \[a *i j* ]*m x n*, then
- K * A = A * K = \[K a *i j*]*m x n*

### Properties of Scalar Multiplication
1. K * (A + B) = KA + KB
2. (P + Q) * A = PA + QA
3. P * (Q * A) = (P * Q) * A
4. (-K) * A = -(K * A) = K * (-A)

## Multiplication of Matrices
Multiplication of matrices is only possible when they are ***multiplication conformable***, that is - `number of column in first matrix should be equal to number of rows in second matrix.`
- Each element of i*th* row in first matrix is multiplied with corressponding element of i*th* column in second matrix, and the summation of each multiplication is the i*th* element of the resultant matrix. 

### Properties of matrix multiplication
1. Matrix multiplication is Associative (A * B) * C = A * (B * C)
2. Matrix multiplication is distributive with respect to addition of matrices: A * (B + C) = AB + AC
3. Matrix Multiplication is not ***Always Commutative***: AB != BA
   - If AB == BA, then the matrices 'A' and 'B' are said to **commute**.
   - If AB == -BA, then the matrices are said to be **anti-commute**.
4. The equation AB = 0, does not necessarily imply that one of the matrices 'A' and 'B' must be a Zero matrix.
   - If AB = 0, then it does not necessarily imply that BA = 0.
5. If A is an m x n matrix, I*n* denotes the n-rowed unit matrix, it can be easily seen that: A * I*n* = A = I*m* * A

## Echelon Form
A matrix A of order m x n is said to be in row echelon form if:
1. Zero rows (If any occur) then they must be below the non-zero rows.
2. The number of Zeros before the first non-zero elements in each row is less than the number of such zeros in the next non-zero row. 

**If a Matrix is in Row Echelon form then, Rank of matrix = Number of Non-Zero Rows.**

## Key Points
1. If 'A' is a square matrix of size(n x n), then r(A) <= n.
2. If 'A' is a non-square matrix of size (m x n), then r(A) <= min(m, n).
3. If a matrix a attains the maximum possible rank, then it is said to have **Full Rank**.
4. If a square matrix is non-singular, then it will have full rank.
5. Rank of a matrix = `The number of linearly independent rows == The number of linearly independent columns of the matrix`.
6. If all the rows (or Columns) of a matrix are identical or Proportional to each other, then its **Rank = 1**.













