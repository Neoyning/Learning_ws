# Neoy SLAM Programming Learning Space

----

> This learning space is aim for concrete study of SLAM-related Programming skills!

### NOTE: Clone remote github repositories and edit it locally

 - Create a New repository from your github page [Github]
 - Install VS Code in your Computer [VS Code Download]
 - Add Python and C++ Extension in VS Code [VS Keyboard Shortcut]
 - Clone a repository locally [Intro to Git in VS Code]

## IDE

| IDE | Usage | 
| ------ | ----------- |
| Eclipse C++  | C++ programming and coding reading |
| Pycharm  | Python programming and debugging |
| VS Code  | Source coding upload to git and doxygen edit  |

### Eclipse C++ Eigen Setup
1. Project Properties -> C/C++ General -> Paths and Symbols -> (GNU C++) Source Location -> Link Folder -> check "Link to folder..." -> Browse -> select eingen3 folder(eg. /usr/include/eigen3) -> OK -> Apply
2. `Project Properties -> C/C++ General -> Paths and Symbols ->` (GNU C++) Includes -> Add -> Workspace -> select "eigen3" -> OK -> Apply
3. Click OK and close the Properties window.

## Learning-based TOOLs

| Package | Description | 
| ------ | ----------- |
| Pytorch   | NN Model Building, Training ,Testing and Evaluation|


## Model-based TOOLs

| Package or Library | Description |
| ------ | ----------- |
| Eigen   | Matrix Operation |
| Ceres   | Computer vision specified optimizatiopn tool | 

In Eigen, indices start at 0

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


[Github]: <https://github.com/>
[VS Code Download]: <https://code.visualstudio.com/download>
[VS Keyboard Shortcut]: <https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf>
[Intro to Git in VS Code]: <https://code.visualstudio.com/docs/sourcecontrol/intro-to-git>