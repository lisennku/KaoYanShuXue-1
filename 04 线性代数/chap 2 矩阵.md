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
    - 若方阵$A$的==任意两行(列)对应成比例==，则方阵$A$可表示为$ \begin{bmatrix} *\\ * \\ \vdots \\ *\end{bmatrix}  \begin{bmatrix} * & * & \cdots & *\end{bmatrix}$

## 3.3 矩阵的可交换

> 若矩阵$A$，$B$，满足$AB=BA$，则称$A$和$B$可交换，否则为不可交换

> 可交换的矩阵，一定满足：
>
> - 一定是==同阶方阵==
>     - 不是同阶方阵一定不是可交换矩阵
> - $AB=BA$
>     - $AB$，$BA$不相等，一定不是可交互矩阵

> 单位矩阵$E$，和任一个同阶方阵可交换

> 两个同阶对角矩阵可交换

# 4. 方阵的幂

## 4.1 方阵的幂的定义

> 设$A$为方阵，$k$为正整数，则$A$的$k$次幂的定义为：
>
> $A^k = \underbrace{A \cdot A \cdot \cdots \cdot A}_{k \text{ 个}}$
>
> 规定： $A^0 = E$

## 4.2 方阵的幂的性质

- 设$A$为方阵，$k_1,k_2$为非负整数，则有

    - $A^{k_1}A^{k_2} = A^{k_1+k_2}$
    - $(A^{k_1})^{k_2} = A^{k_1k_2}$

- $(lA)^k = l^kA^k, l\text{为常数},\;k\text{为正整数}$

- 若矩阵$A$，$B$可交换，则有

    - $A^2-B^2 = (A-B)(A+B) = (A+B)(A-B)$
    - $(A+B)^2 = A^2 +2AB +B^2$
    - $(A-B)^2 = A^2 -2AB +B^2$
    - $(A-B)^3 = (A-B)(A^2 +AB +B^2)$
    - $(A+B)^3 = (A+B)(A^2 -AB +B^2)$
    - $(AB)^k = A^kB^k$

- 一般有，不要求矩阵$A$，$B$可交换

    - $(A+B)(A-B) = A^2 + BA - AB - B^2$
    - $(A+B)^2 = A^2 +AB +BA +B^2$
    - $(A-B)^2 = A^2 - AB -BA +B^2$

- 方阵多项式

    - 设$f(x) = a_mx^m + a_{m-1}x^{m-1} + \cdots + a_1x + a_0$，则有

        $f(A) = a_mA^m + a_{m-1}A^{m-1} + \cdots + a_1A + \textcolor{red}{a_0E}$

# 5. 矩阵的转置

## 5.1 转置定义

> 将矩阵$A$的各行依次变为列(或各列依次变为行)后得到的矩阵，即为$A$的转置矩阵$A^T$
>
> > $A$和$A^T$互为转置矩阵
> >
> > 若$A$为$m \times n$矩阵，则$A^T$为$n \times m$矩阵

- 转置矩阵性质

    - $(A^T)^T = A$
    - $(A+B)^T = A^T + B^T$
    - $(A-B)^T = A^T - B^T$
    - $(kA)^T = kA^T$
    - $(AB)^T = B^TA^T$
        - 可以推广到$m$个矩阵积的转置矩阵
        - $(A_1A_2\cdots A_m)^T = A_m^T \cdots A_2^TA_1^T$

    - $(A^k)^T = (A^T)^k$

## 5.2 对称矩阵与反对称矩阵

- 对称矩阵  *<u>必为方阵</u>*

    > 如果矩阵$A$满足$A = A^T$，则称矩阵$A$为对称矩阵

    > 设矩阵$A$为$n$阶方阵，$A = (a_{ij})_{n \times n}$，若$a_{ij} = a_{ji}\;i = 1,2,3,\cdots,n;\;j = 1,2,3,\cdots,n$，则称矩阵$A$为对称矩阵

    - 对称矩阵的性质

        - 若$A$，$B$为同阶对称矩阵，则$A+B$，$A-B$仍为对称矩阵

        - 若$A$为对称矩阵，则$kA$，$A^m$仍为对称矩阵，$k$为常数，$m$为正整数

        - 若$A$，$B$为同阶对称矩阵，则$AB$为对称矩阵的==充要条件==是$AB=BA$

        - 对任意$m \times n$矩阵$A$，则$A^TA, AA^T$均为对称矩阵

            - 若$A$为$m \times n$矩阵，且$AA^T = O$， 则$A = O$

                ![image-20250212162855075](chap 2 矩阵.assets/image-20250212162855075.png)

- 反对称矩阵  *<u>必为方阵</u>*

    > 如果矩阵$A$满足$A^T = -A$，则称矩阵$A$为反对称矩阵

    > 设矩阵$A$为$n$阶方阵，$A = (a_{ij})_{n \times n}$，若$a_{ij} = -a_{ji}\;i = 1,2,3,\cdots,n;\;j = 1,2,3,\cdots,n$，则称矩阵$A$为反对称矩阵

    > ==易知，反对称矩阵的主对角线上的元素均为$0$==

    - 反对称矩阵的性质
        - 若$A$，$B$为同阶反对称矩阵，则$A+B$，$A-B$仍为反对称矩阵
        - 若$A$为反对称矩阵，则$kA$仍为对称矩阵，$k$为常数
        - 若$A$为反对称矩阵，$k$为正整数，则$A^k$为$\begin{cases} \text{对称矩阵，}&k\text{偶数}\\  \text{反对称矩阵，}&k\text{奇数}\end{cases}$

# 6. 方阵的行列式

> 设$n$阶方阵$A = \begin{bmatrix} a_{11} & a_{12} & \cdots & a_{1n} \\ a_{21} & a_{22} & \cdots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{n1} & a_{n2} & \cdots & a_{nn}\end{bmatrix}$，则$A$的行列式为$|A|\begin{vmatrix} a_{11} & a_{12} & \cdots & a_{1n} \\ a_{21} & a_{22} & \cdots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{n1} & a_{n2} & \cdots & a_{nn}\end{vmatrix}$
>
> > 矩阵$A$的行列式$|A|$为一个数
> >
> > ==只有方阵才有行列式==

- 方阵行列式的性质
    - $|A^T| = |A^T|=|A|$
    - $|kA| = k^n|A|$
    - $|AB| = |A| \cdot |B|$
    - $|A^m| = |A|^m$
    - $|E| = 1$
    - 若$A$是==奇数阶==反对称矩阵，则$|A|=0$

# 7. 方阵的伴随矩阵

