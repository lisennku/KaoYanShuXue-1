# 1. 矩阵的概念

## 1.1 矩阵的概念

> 矩阵：$m \times n$个数$a_{ij}(\; i = 1,2,3,\cdots,m; j = 1,2,3,\cdots,n)$排列成一个$m$行$n$列的数表，称为一个$m \times n$矩阵

> 同型矩阵：矩阵$A$和矩阵$B$是同型矩阵$\Leftrightarrow$矩阵$A$和矩阵$B$的行数相等，列数也相等

> 矩阵相等：矩阵$A$和矩阵$B$相等$\Leftrightarrow$$A=B$$\Leftrightarrow \begin{cases} &A\text{和}B\text{是同型矩阵；}\\&\text{对应位置元素相等} \end{cases}$

## 1.2 特殊矩阵

- 方阵
    - 行数和列数相等的矩阵，相等的行列数称为阶数
        - $\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}$
- 行矩阵
    - 只有一行的矩阵，也称为行向量
        - $\begin{bmatrix} 1 & 2\end{bmatrix}$
- 列矩阵
    - 只有一列的矩阵，也称为列向量
        - $\begin{bmatrix} 1 \\ 3 \end{bmatrix}$
- 零矩阵
    - 元素全为$0$的矩阵
        - $\begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix}$
- 负矩阵
    - 将矩阵$A$的所有元素取其对应相反数后得到的矩阵，叫做$A$的负矩阵，记为$-A$
        - $A=\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}$，则$-A = \begin{bmatrix} -1 & -2 \\ -3 & -4 \end{bmatrix}$
- 上三角矩阵
    - 主对角线下方的元素全部为$0$的==方阵==
- 下三角矩阵
    - 主对角线上方的元素全部为$0$的==方阵==
- 对角矩阵
    - 即使上三角矩阵，又是下三角矩阵，也即主对角线上方，下方元素全部为$0$的==方阵==
    - 记为$diag(a_1, a_2, \dots,a_n)$
- 数量矩阵
    - 主对角线元素是同一个常数的==对角矩阵==，记为$kE$
        - 
- 单位矩阵
    - 主对角线元素全为==$1$==，其他位置元素全为$0$的==方阵==，记为$E$
        - $n$阶单位矩阵
        - $E_n = \begin{bmatrix} 1\\ & 1 \\ & & 1 \\&&&\ddots \\ &&&&1\end{bmatrix}$

# 2. 矩阵的加法、减法、数乘

## 2.1 矩阵的加减法

> 两个同型矩阵相加，就是==对应位置==的元素相加

> 两个同型矩阵相减，就是==对应位置==的元素相减

- 加减法运算规律
    - $A+B = B+A$
    - $(A+B)+C = A + (B+C)$
    - $A+O = A$
    - $A+(-A)= O$
    - $A-B=A+(-B)$
    - $A + B = C \Leftrightarrow A=C-B$

## 2.2 矩阵的数乘

> 数$k$乘以矩阵$A$，就是用数$k$乘以矩阵$A$里的每个元素

- 运算规律
    - $k(A+B) = kA+kB$
    - $(k+l)A=kA+lA$
    - $k(lA) = (kl)A$
    - $1A = A$
    - $(-1)A = -A$

# 3. 矩阵的乘法

> 两个矩阵$A$、$B$，如果$A$的列数，等于$B$的行数，则$A$、$B$可以相乘得到一个新的乘积矩阵$AB$，乘法规则定义如下：
>
> 设$A = \begin{bmatrix} a_{11} & a_{12} & \cdots & a_{1n} \\ a_{21} & a_{22} & \cdots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{m1} & a_{m2} & \cdots & a_{mn}\end{bmatrix}_{\textcolor{red}{m \times n}}$，$B = \begin{bmatrix} b_{11} & b_{12} & \cdots & b_{1s} \\ b_{21} & b_{22} & \cdots & b_{2s} \\ \vdots & \vdots & \ddots & \vdots \\ b_{n1} & b_{n2} & \cdots & b_{ns}\end{bmatrix}_{\textcolor{red}{n \times s}}$，则乘积矩阵$AB = \begin{bmatrix} c_{11} & c_{12} & \cdots & c_{1s} \\ c_{21} & c_{22} & \cdots & c_{2s} \\ \vdots & \vdots & \ddots & \vdots \\ c_{m1} & c_{m2} & \cdots & c_{ms}\end{bmatrix}_{\textcolor{red}{m \times s}}$
>
> 其中，$c_{ij} = a_{i1}b_{j1} + a_{i2}b_{j2} + \cdots + a_{in}b_{nj},\; i = 1,2,3,\cdots,m; j= 1,2,3,\cdots,s $

> 1. 只有左边矩阵的列数，等于右边矩阵的行数时，才能相乘
> 2. 乘积矩阵的行数，等于左边矩阵的行数，乘积矩阵的列数，等于右边矩阵的列数
> 3. 乘积矩阵的元素，等于左边矩阵的行，乘以右边矩阵的列
>     - 乘积矩阵的第$i$行，第$j$列元素，等于左边矩阵的第$i$行，和右边矩阵的第$j$列元素对应相乘求和

## 3.1 矩阵乘法==不满足==的规律

- 矩阵的乘法==不满足交换律==
    - 当$AB$，$BA$都有意义时，$AB$，$BA$不一定相等
    - $AB$有意义，$BA$不一定有意义
- 矩阵的乘法==不满足消去律==
    - 若$AB=AC$，且$A\ne O$，推到不出$B=C$
    - 若$BA=CA$，且$A\ne O$，推到不出$B=C$
- 两个非零矩阵的乘积可能是零矩阵
    - 若$AB=O$，推到不出$A=O$或$B=O$

## 3.2 矩阵乘法==满足==的规律或性质

- 结合律
    - $(AB)C = A(BC)$
- 分配律 *<u>注意$C$的左右位置不能动</u>*
    - $(A+B)C = AC + BC$
    - $C(A+B) = CA +CB$
- 数乘与矩阵乘积
    - $k(AB)=(kA)B=A(kB)$
- 单位矩阵与矩阵相乘  *<u>单位矩阵在矩阵乘法中相当于数乘$1$</u>*
    - $AE = EA = A$
- 数量矩阵与矩阵相乘  *<u>数量矩阵在矩阵乘法中相当于数乘</u>*
    - 数量矩阵$A= \begin{bmatrix} a & 0 & \cdots & 0\\ 0 & a & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots  \\ 0 & 0 & \cdots & a\end{bmatrix} = aE$，则有$AB = aB$
- 两个对角矩阵相乘
    - $\begin{bmatrix} a_1\\ & a_2 \\ & & a_3 \\&&&\ddots \\ &&&& a_n\end{bmatrix} \begin{bmatrix} b_1\\ & b_2 \\ & & b_3 \\&&&\ddots \\ &&&& b_n\end{bmatrix} = \begin{bmatrix} a_1b_1\\ & a_2b_2 \\ & & a_3b_3 \\&&&\ddots \\ &&&& a_nb_n\end{bmatrix}$
- 行列向量相乘  <u>*顺序不同结果不同*</u>
    - 行向量乘以列向量，结果是一个==常数==
    - 列向量乘以行向量，结果是一个==矩阵==

  