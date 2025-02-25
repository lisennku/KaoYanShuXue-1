# 1. 二次型及矩阵表示

## 1.1 二次型基本概念

- 二次型定义

    > 设含有$n$个变量$x_1,x_2,\cdots,x_n$的==二次齐次==多项式
    > $$
    > \begin{align*}
    > f(x_1,x_2,\cdots,x_n) = &a_{11}x_1^2 +  2a_{12}x_1x_2 + 2a_{13}x_1x_3 + \cdots + 2a_{1n}x_1x_n \\ &\quad \quad \; \; + \;a_{22}x_2^2 \quad\; + \;2a_{23}x_2x_3 + \cdots + 2a_{2n}x_2x_n \\&\quad \quad \quad \quad \quad \quad  \; \; \; \;\; + \cdots \cdots \cdots \cdots \cdots \cdots \\ & \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad  + \quad a_{nn}x_n^2
    > 
    > \end{align*} \tag{1} \label{eq:poly}
    > $$
    > 称为$n$元二次型，简称二次型，当$a_{ij}$为实数时，称$f$为$n$元实二次型

- 二次型的矩阵和二次型的秩

    - 考虑到$x_ix_j =  x_jx_i$，取$a_{ji} = a_{ij}$，则可将$\eqref{eq:poly}$的公式改写为如下形式
        $$
        \begin{align*}
        f(x_1,x_2,\cdots,x_n) = &a_{11}x_1^2 +  a_{12}x_1x_2 + a_{13}x_1x_3 + \cdots + a_{1n}x_1x_n \\ & + a_{21}x_2x_1 + a_{22}x_2^2+ a_{23}x_2x_3 + \cdots + a_{2n}x_2x_n \\ & + \cdots \cdots \\& + a_{n1}x_nx_1 + a_{n2}x_nx_2 + a_{n3}x_nx_3 + \cdots + a_{nn}x_n^2\\
        = & \displaystyle \sum_{i=1}^n \sum_{j = 1}^n a_{ij}x_ix_j
        \end{align*} \tag{2} \label{eq:poly_aligns}
        $$

    - 利用矩阵乘法，$\eqref{eq:poly_aligns}$又可变为
        $$
        \begin{align*}
        f(x_1,x_2,\cdots,x_n) = & x_1(a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n) \\
        & + x_2(a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n) \\
        & + \cdots \cdots \\
        & + x_n(a_{n1}x_1 + a_{n2}x_2 + \cdots + a_{nn}x_n) \\
        =& (x_1, x_2, \cdots, x_n)\begin{bmatrix} a_{11}x_1& a_{12}x_2& \cdots & a_{1n}x_n \\ a_{21}x_1& a_{22}x_2& \cdots & a_{2n}x_n \\ &\cdots \cdots \cdots \\ a_{n1}x_1& a_{n2}x_2& \cdots & a_{nn}x_n\end{bmatrix} \\
        =& (x_1, x_2, \cdots, x_n)\begin{bmatrix} a_{11}& a_{12}& \cdots & a_{1n} \\ a_{21}& a_{22}& \cdots & a_{2n} \\ \vdots & \vdots & & \vdots \\ a_{n1}& a_{n2}& \cdots & a_{nn}\end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} \\
        \end{align*}
        $$

        - 若记$A = \begin{bmatrix} a_{11}& a_{12}& \cdots & a_{1n} \\ a_{21}& a_{22}& \cdots & a_{2n} \\ \vdots & \vdots & & \vdots \\ a_{n1}& a_{n2}& \cdots & a_{nn}\end{bmatrix}$，$x = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix}$，则$\eqref{eq:poly}$可改写为

            $f(x_1, x_2, \cdots, x_n) = x^T A x$，其中$A$是$\eqref{eq:poly_aligns}$的系数按顺序排成的==对称矩阵==

    - > 称$f(x_1, x_2, \cdots, x_n) = x^T A x\;(A^T=A)$是二次型式$\eqref{eq:poly}$的矩阵表达式

        