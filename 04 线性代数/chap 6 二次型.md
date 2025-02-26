# 1. 二次型及矩阵表示

## 1.1 二次型基本概念

### 1.1.1 二次型定义

> 设含有$n$个变量$x_1,x_2,\cdots,x_n$的==二次齐次==多项式
> $$
> \begin{align*}
> f(x_1,x_2,\cdots,x_n) = &a_{11}x_1^2 +  2a_{12}x_1x_2 + 2a_{13}x_1x_3 + \cdots + 2a_{1n}x_1x_n \\ &\quad \quad \; \; + \;a_{22}x_2^2 \quad\; + \;2a_{23}x_2x_3 + \cdots + 2a_{2n}x_2x_n \\&\quad \quad \quad \quad \quad \quad  \; \; \; \;\; + \cdots \cdots \cdots \cdots \cdots \cdots \\ & \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad  + \quad a_{nn}x_n^2
> 
> \end{align*}
> $$
> 称为$n$元二次型，简称二次型，当$a_{ij}$为实数时，称$f$为$n$元实二次型

### 1.1.2 二次型的矩阵和二次型的秩

- 考虑到$x_ix_j =  x_jx_i$，取$a_{ji} = a_{ij}$，则可将上述公式改写为如下形式
    $$
    \begin{align*}
    f(x_1,x_2,\cdots,x_n) = &a_{11}x_1^2 +  a_{12}x_1x_2 + a_{13}x_1x_3 + \cdots + a_{1n}x_1x_n \\ & + a_{21}x_2x_1 + a_{22}x_2^2+ a_{23}x_2x_3 + \cdots + a_{2n}x_2x_n \\ & + \cdots \cdots \\& + a_{n1}x_nx_1 + a_{n2}x_nx_2 + a_{n3}x_nx_3 + \cdots + a_{nn}x_n^2\\
    = & \displaystyle \sum_{i=1}^n \sum_{j = 1}^n a_{ij}x_ix_j
    \end{align*} 
    $$

- 利用矩阵乘法，上述公式又可变为
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

    - 若记$A = \begin{bmatrix} a_{11}& a_{12}& \cdots & a_{1n} \\ a_{21}& a_{22}& \cdots & a_{2n} \\ \vdots & \vdots & & \vdots \\ a_{n1}& a_{n2}& \cdots & a_{nn}\end{bmatrix}$，$x = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix}$，则第一个公式可改写为

        $f(x_1, x_2, \cdots, x_n) = x^T A x$，其中$A$是$\eqref{eq:a2}$的系数按顺序排成的==对称矩阵==

- > 称$f(x_1, x_2, \cdots, x_n) = x^T A x\;(A^T=A)$是二次型式的==矩阵表达式==
  >
  > - 实对称矩阵$A$，称为二次型$f$的矩阵
  > - 二次型$f$，称为实对称矩阵$A$的二次型
  > - *实对称矩阵$A$的秩，称为二次型$f$的秩，记为$r(f)$，即$f(f) = r(A)$*
  
  - 任给一个二次型，可以唯一确认一个实对称矩阵，反之，任给一个实对称矩阵，可以唯一确认一个二次型，因此$n$元二次型和$n$阶对称矩阵之间存在一一对应的关系
      - 二次型的矩阵，必须是对称矩阵，一般的，二次型$f=x^TAx$的矩阵为$\frac 1 2 (A+A^T)$
  - 二次型的矩阵是唯一的，可由$f$的各项系数确认
      - $a_{ii}(i = 1,2,\cdots, n)$依次是二次型中平方项$x_{i}^2$的系数
      - $a_{ij}(i \ne j)$是二次型中交叉项$x_ix_j$系数的一半
  - 二次型矩阵的阶数，等于二次型中变量的个数

### 1.1.3 二次型的标准型

> 如果二次型只含平方项$x_i^2$，不含交叉项$x_ix_j$，
>
> 即形式为$f(x_1, x_2, \cdots, x_n) = d_1x_1^2 +d_2x_2^2+ \cdots +d_nx_n^2$，则称为二次型的一个标准型，其中系数$d_1,\cdots,d_n$为任意实数

- 二次型的标准型对应的矩阵为对角矩阵$\begin{bmatrix} d_1 \\ & d_2 \\  &&\ddots \\&&&d_n \end{bmatrix}$ 
- 二次型的==秩==，等于标准型中，==非零系数==的平方项的个数

### 1.1.4 二次型的规范型

> 如果二次型的标准型中，系数$d_i$只能是$1,-1,0$三个数，==且整体需要按照$1, -1, 0$的顺序出现==，则称为二次型的规范型
>
> 即形式为$z_1^2+z_2^2+\cdots +z_p^2 - z_{p+1}^2 - z_{p+2}^2 - z_r^2$
>
> 其中，$r = r(A), p \le r \le n$
>
> - 因为标准型的秩为非零系数的平方项个数

- 二次型的规范型对应的矩阵为对角矩阵，且主对角线元素为$1, -1, 0$，即

    $\begin{bmatrix} 1\\ & 1\\  &&\ddots \\&&&1 \\ &&&&-1 \\ &&&&&\ddots \\ &&&&&&-1\\ &&&&&&&0 \\ &&&&&&&& \ddots \\ &&&&&&&&& 0\end{bmatrix} = \begin{bmatrix} E_p \\ & -E_{r-p}\\  && O_{n-r} \end{bmatrix}$

### 1.1.5 二次型的惯性指数和符号差

- 正惯性指数
    - 二次型的标准型中，正系数平方项的个数$p$，称为正惯性指数
- 负惯性指数
    - 二次型的标准型中，负系数平方项的个数$q$，称为负惯性指数
- 符号差
    - 正惯性指数与负惯性指数的差，称为符号差
- 性质
    - 二次型的秩，等于正惯性指数和负惯性指数的和，即$p+q$

## 1.2 二次型的线性变换

- 线性变换

    - 设有两组变量$x_1, x_2,\cdots, x_n$和$y_1, y_2, \cdots, y_n$，关系式

        $\begin{cases} x_1 = & c_{11}y_1 + c_{12}y_2 + \cdots + c_{1n}y_n  \\ x_2 = & c_{21}y_1 + c_{22}y_2 + \cdots + c_{2n}y_n  \\ & \cdots \cdots\cdots\cdots \\x_n = & c_{n1}y_1 + c_{n2}y_2 + \cdots + c_{nn}y_n  \\  \end{cases}$

        称为由$x$到$y$的一个线性变换

    - 其矩阵形式为$x=Cy$，$C$称为线性变换的矩阵，其中，
        - $x =  \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix}$
        - $C = \begin{bmatrix} c_{11}& c_{12}& \cdots & c_{1n} \\ c_{21}& c_{22}& \cdots & c_{2n} \\ \vdots & \vdots & & \vdots \\ c_{n1}& c_{n2}& \cdots & c_{nn}\end{bmatrix}$
        - $y =  \begin{bmatrix} y_1 \\ y_2 \\ \vdots \\ y_n \end{bmatrix}$

- 逆变换

    - 若$|C| \ne 0$，则称$x=Cy$为可逆线性变换，（或满秩，非退化，非奇异），则$y=C^{-1}x$是变量$y_1, y_2,\cdots, y_n$到$x_1,x_2,\cdots,x_n$的线性变换，并称其为$x=Cy$的逆线性变换，简称逆变换

- 正交变换
    - 若$C$为正交矩阵，则称线性变换$x=Cy$为正交线性变换，简称正交变换

- 线性变换的乘积

    - 若$x=C_1y$是变量$x_1, x_2,\cdots, x_n$到$y_1, y_2, \cdots, y_n$的一个线性变换，$y=C_2z$是变量$y_1, y_2, \cdots, y_n$到$z_1, z_2, \cdots, z_n$的一个线性变换，则$x=C_1C_2z$称为由变量$x_1, x_2,\cdots, x_n$到$z_1, z_2, \cdots, z_n$的一个线性变换，并称其为$x=C_1y$和$y=C_2z$的==乘积==，对应矩阵为$C_1C_2$

    - > 线性变换乘积的矩阵，等于各线性变换矩阵的乘积，且可逆线性变换的乘积，仍为可逆线性变换

- 二次型的可逆线性变换

    > 二次型的可逆线性变换，是指，将二次型$f(x)=x^TAx$，通过由$x$到$y$的可逆线性变换$x=Cy$，将二次型从关于$x$的函数变为关于$y$的二次型$g(y)$

    - 方法一：
        - 按照线性变换的对照关系，将二次型的方程组中的$x_i$替换为线性变换中的对应线性表达
    - 方法二：
        - 按照二次型的矩阵表达式，将其中的$x^T$和$x$，换为线性变换中的$x=Cy$，即$g(y) = y^T(C^TAC)y$

    > 二次型经过可逆线性变换，得到的仍是二次型，且秩不变

- > 若二次型$f(x) = x^TAx$经可逆线性变换$x=Cy$化为二次型$y^TBy$，$B=C^TAC$，则$A$与$B$合同

    > 若二次型$f(x) = x^TAx$经正交变换$x=Qy$化为二次型$y^TBy$，$B=Q^TAQ=Q^{-1}AQ$，则$A$与$B$合同，且相似

## 1.3 合同矩阵和合同变换

> 二次型的可逆变换中，涉及到$g(y) = y^TBy,\; B = C^TAC$，其中$B= C^TAC$即为合同

- 合同矩阵

    > 设$A, B$是$n$阶矩阵，若存在可逆矩阵$C$，使得$C^TAC=B$，则称矩阵$A$与$B$合同，记为$A\simeq B$，并称由$A$到$B$的变换为合同变换，$C$称为合同变换的矩阵

    - 基本性质
        - 反身性，对于任意矩阵$A$，有$A \simeq A$
        - 对称性，若$A \simeq B$，则$B \simeq A$
        - 传递性，若$A \simeq B, B \simeq C$，则$A \simeq C$
    - 重要性质
        - 若$A \simeq B$，则$r(A) = r(B)$，$A \cong B$
        - 若$A \simeq B$，则$A = A^T$的充要条件是$B=B^T$
        - 若$A \simeq B$，则$A,B$可逆性相同，当$A,B$都可逆时，$A^{-1} \simeq B^{-1}$
        - 若$A \simeq B$，则$A^T \simeq B^T$

# 2. 化二次型为标准型

> 任何一个二次型经过适当的可逆线性变换，都可化为标准型

## 2.1 化二次型为标准型

### 2.1.1 配方法

> 基本原理类似于将二次多项式进行配方
> $$
> \begin{align*}
> ax^2+bx+c = & a(x^2+\frac b a x) + c\\
> &= a(x^2 +2 \times \frac {b} {2a}x + ( \frac {b} {2a})^2) - a( \frac {b} {2a})^2 + c\\
> &= a(x +  \frac {b} {2a})^2 + \frac {4ac-b^2} {4a}
> \end{align*}
> $$

- 配方法步骤

    1. 配方

        - 情况1，如果二次型含有平方项
            - 直接利用完全平方公式，==一次一个变量，逐个配方==

        - 情况2，如果二次型只含有交叉项，没有平方项
            - 先做辅助变换$\begin{cases}x_i = &y_i + yj \\ x_j =&y_i - y_j \\ x_k =&y_k\;(k \ne i,j)\end{cases}$使其产生平方项，再按照情况1进行配方

    2. 用另外一个变量，代替配方出的每一个平方项里的内容

        - 该过程相当于可逆线性变换

- 配方法的答案==不==唯一，标准型==不==唯一

- > 任何一个$n$元二次型都可以通过可逆线性变换化为标准型

- > 任何一个$n$阶实对称矩阵，都合同于一个对角矩阵

    - 因为任意一个二次型$f(x)=x^TAx$，都可以通过可逆线性变换$x=Cy$，化为标准型$g(y) = y^T\Lambda y$，其中$\Lambda=diag(d_1,d_2,\cdots,d_n)$，这样将$x=Cy$带入$f(x)=x^TAx$，得到$y^T(C^TAC)y$，这样便有$C^TAC = \Lambda$，所以有$A$和$\Lambda$合同

- 对$A$的合同对角化，就是求可逆矩阵$C$，使得$C^TAC$为对角矩阵

### 2.1.2 初等变换法

### 2.1.3 正交变换法