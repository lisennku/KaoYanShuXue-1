# 1. 线性方程组的表示法

## 1.1 一般形式

> 含有$n$个未知数，$m$个方程的线性方程组
>
> $\begin{cases} & a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n = b_1 \\& a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n = b_2 \\ & \cdots \cdots \\& a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n = b_n \end{cases}$

- 系数矩阵$A = \begin{bmatrix} a_{11} & a_{12} & \cdots & a_{1n} \\ a_{21}&a_{22}& \cdots & a_{2n}\\\vdots & \vdots && \vdots \\ a_{m1} &a_{m2} & \cdots & a_{mn} \end{bmatrix}_{m \times n}$
- 增广矩阵$\overline{A} = \begin{bmatrix} a_{11} & a_{12} & \cdots & a_{1n}  & b_1\\ a_{21}&a_{22}& \cdots & a_{2n} & b_2\\\vdots & \vdots && \vdots & \vdots \\ a_{m1} &a_{m2} & \cdots & a_{mn}  & b_n\end{bmatrix} = (A, b)$
- 未知数列向量$x = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix}_{\textcolor{red}{n} \times 1}$
- 常数项列向量$b = x = \begin{bmatrix} b_1 \\ b_2 \\ \vdots \\ b_m \end{bmatrix}_{\textcolor{red}{m} \times 1}$

> 当常数项<font style="font-weight: bold;">$b$</font>均为$0$时，称为齐次线性方程组
>
> 当常数项<font style="font-weight: bold;">$b$</font>不全为$0$时，称为非齐次线性方程组

## 1.2 矩阵形式

> $Ax =b $

## 1.3 向量形式

> 将系数矩阵分为==列向量组==，$A = (\alpha_1, \alpha_2, \cdots, \alpha_n)$
>
> $\alpha_1x_1 + \alpha_2x_2 + \cdots+ \alpha_nx_n = b$

- 若使用向量形式表示齐次线性方程组，则向量组的组合系数即为方程组的解

# 2. 线性方程组解的判定

## 2.1 非齐次线性方程组的判定

> $n$元非齐次线性方程组有解的充分必要条件是，$r(A) = r(\overline{A})$
>
> 且当有解时
>
> - 若$r(A) = r(\overline{A}) = n$，有唯一解
> - 若$r(A) = r(\overline{A}) < n$，有无穷多解

## 2.2 齐次线性方程组的判定



