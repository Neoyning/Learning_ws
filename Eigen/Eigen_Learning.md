# Eigen Learning Note

 ----

## Eigen Setup

 - Install Eigen [Eigen Download]
 - Using Eigen in CMake Projects [Cmake Eigen]


> Note In Eigen, indices start at 0

### Eigen Convenience typedefs

#### Matrix and Array class with 3 majar template parameters 

- Matrix: `Matrix<typename, RowsNumber, ColsNumber>`
- Array: `Array<typename, RowsNumber, ColsNumber>`

#### Matrix: 
>linear algebraic operations

 - Matrix**Nt**: `Matrix<t, N, N>`
 - Matrix**XNt**: `Matrix<type, Dynamic, N>`
 - Matrix**Xt**: `Matrix<double, Dynamic, Dynamic>`
 - Matrix**NXt**: `Matrix<type, N, Dynamic>`
 - Vector**Nt**: `Matrix<type, N, 1>`
 - RowVector**Nt**: `Matrix<type, 1, N>`

#### Array: 
>coefficient-wise(element-wise) operations
 - Array**Xt**: `Array<t,Dynamic,1> `
 - Array**Nt**: `Array<t,N,1> `
 - Array**XXt**: `Array<t,Dynamic,Dynamic> `
 - Array**NNt**: `Array<t,N,N> `

 Where: 
 - **N** can be any one of 2, 3, 4, or X(Dynamic).
 - **t** can be any one of **i**(int), **f**(float), **d**(double), **cf**(complex\<float\>), or **cd**(complex\<double\>).

For example, the statement `result = m.array() * n.array()` takes two matrices `m` and `n`, converts them both to an array, uses to multiply them coefficient-wise and assigns the result to the **matrix variable** result.
>This is legal because Eigen allows assigning(=) **array expressions** to **matrix variables**.

### Block operations

| Block operation |  Dynamic-size block  | Fixed-size block  |
| ------ | ----------- | ----------- |
| `Block of size (p,q), starting at (i,j)`   | `matrix.block(i,j,p,q);` | `matrix.block<p,q>(i,j);` |
> Indices `(i,j)` start at 0 !
> Note: Self block assignment may cause aliasing problem. Use `.eval()` for resolving.




[Eigen Download]: <https://eigen.tuxfamily.org/index.php?title=Main_Page>
[Cmake Eigen]: <https://eigen.tuxfamily.org/dox/TopicCMakeGuide.html>