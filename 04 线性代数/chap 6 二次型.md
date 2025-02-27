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
  > - *实对称矩阵$A$的秩，称为二次型$f$的秩，记为$r(f)$，即$r(f) = r(A)$*
  
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

        - 该过程相当于可逆线性变换，$x=Cy$
        - 情况2涉及到两次线性变换，第一次是为了凑出平方项，将$x$进行变量替换，第二次是凑出平方项后的线性变换

- 配方法的答案==不==唯一，标准型==不==唯一

- > 任何一个$n$元二次型都可以通过可逆线性变换化为标准型

- > 任何一个$n$阶实对称矩阵，都合同于一个对角矩阵

    - 因为任意一个二次型$f(x)=x^TAx$，都可以通过可逆线性变换$x=Cy$，化为标准型$g(y) = y^T\Lambda y$，其中$\Lambda=diag(d_1,d_2,\cdots,d_n)$，这样将$x=Cy$带入$f(x)=x^TAx$，得到$y^T(C^TAC)y$，这样便有$C^TAC = \Lambda$，所以有$A$和$\Lambda$合同

- 对$A$的合同对角化，就是求可逆矩阵$C$，使得$C^TAC$为对角矩阵

### 2.1.2 初等变换法

> 初等变换法化二次型为标准型，本质上就是实对称矩阵的合同对角化
>
> 基本原理：
>
> - $n$元二次型$f=x^TAx$经可逆线性变换$x=Cy$，化为标准型$y^T\Lambda y$，则$C^TAC=\Lambda$
> - 因可逆矩阵可以表示为若干个初等矩阵的乘积，即$C = C_1C_2\cdots C_s$，从而有$C_s^TC_{s-1}^T\cdots C_1^TAC_1C_2\cdots C_s = \Lambda$ ，$EC_1C_2\cdots C_s = C$
> - 因此，构建$2n \times n$矩阵$\begin{bmatrix}A \\ E\end{bmatrix}$，对==整个矩阵==施以相应于==右==乘$C_1,C_2,\cdots, C_s$的初等==列==变换，==只对$A$==施以相应于==左==乘$C_1^T,C_2^T,\cdots, C_s^T$的初等==行==变换，二者交替进行
>     - $\begin{bmatrix}A \\ E\end{bmatrix} \underset{\text{对}A\text{施以相应的初等行变换}}{\xrightarrow{\text{对整体施以相应的初等列变换}}}\begin{bmatrix}C_s^TC_{s-1}^T\cdots C_1^TAC_1C_2\cdots C_s \\ EC_1C_2\cdots C_s\end{bmatrix} = \begin{bmatrix} \Lambda \\ C\end{bmatrix} $
> - 当$A$化为对角矩阵$\Lambda$时，单位矩阵$E$化为可逆矩阵$C$，$\Lambda$是标准型的矩阵，$C$时可逆线性变换的矩阵

- 初等变换法步骤
    1. 构造$2n \times n$矩阵$\begin{bmatrix}A \\ E\end{bmatrix}$
    2. 做初等变换，求$C$和$\Lambda$
        - 对整个矩阵施以相应于==右==乘$C_1,C_2,\cdots, C_s$的初等==列==变换
        - 只对$A$施以相应于==左==乘$C_1^T,C_2^T,\cdots, C_s^T$的初等==行==变换
        - 二者交替进行
    3. 写标准型

### 2.1.3 正交变换法

> 正交变换法化二次型为标准型，本质上就是实对称矩阵的正交相似对角化

> 任何一个$n$元实二次型$f(x)=x^TAx$（$A$为实对称矩阵），都可以通过正交变换$x=Qy$（$Q$为正交矩阵）化为标准型$\lambda_1y_1^2+\lambda_2y_2^2+\cdots+\lambda_ny_n^2$，$\lambda_i$为矩阵$A$的$n$个特征值

- 步骤
    1. 求特征值
        - 写出二次型的矩阵，计算$|\lambda E -A|=0$的解
    2. 求特征向量
        - 对每个特征值$\lambda_i$，解方程组$(\lambda_i E-A)x$，计算出特征向量
    3. 改造特征向量
        - 正交化
        - 单位化
    4. 构造正交矩阵$Q$
    5. 写出标准型

## 2.2 化二次型的标准型为规范型

> 二次型的任一标准型，均可通过可逆线性变换，化为规范型

### 2.2.1 化规范型的方法

设二次型$f(x)=x^TAx$已经化为标准型：（此处的标准型是==将系数按照正负分组放置==）

$d_1y_1^2+d_2y_2^2+\cdots +d_py_p^2 - d_{p+1}y_{p+1}^2-\cdots-d_{r}y_{r}^2$

其中，$p \le r \le n,\; d_i>0(i = 1,2,\cdots,r)$，$r$是$f(x_1,x_2,\cdots,x_n)$的秩

再令：$\begin{cases}y_i =& \frac {1}{\sqrt{d_i}}z_i \\ y_j=&z_j\end{cases}\; (i=1,2,\cdots,r;\;j=r+1,\cdots,n)$

### 2.2.2 惯性定理

> 任意一个$n$元二次型$f(x)=x^TAx$，一定可以经过线性变换，化为规范型
>
> $z_1^2+z_2^2+\cdots+z_p^2-z_{p+1}^2-z_{p+2}^2-\cdots-z_{r}^2$
>
> 其中$p$是二次型的正惯性指数，$r$是二次型的秩，$p,r$由二次型矩阵唯一确认

> 任一$n$阶实对称矩阵$A$，一定合同于对角矩阵$\begin{bmatrix} E_p \\ & -E_{r-p}\\  && O \end{bmatrix}$
>
> 其中，$r$是$A$的秩，$p$是$A$的正惯性指数

> 实对称矩阵$A$和$B$合同的充要条件是，他们有相同的秩和相同的正惯性指数

- 等价说法
    - 有相同的秩和负惯性指数
    - 有相同的正惯性指数和相同的负惯性指数
    - 有相同的规范型
    - 正负特征值个数相等

- 推论：
    - 若实对称矩阵$A$与$B$相似，则$A$与$B$合同

# 3. 二次型和对称矩阵的有定性

## 3.1 有定性的概念

- 正定/负定

    > 设$n$元二次型$f(x)=x^TAx\;(A=A^T)$，如果对于==任意====非零==列向量$x=(x_1,x_2,\cdots,x_n)^T \ne 0$，恒有$f(x)x^TAx > 0(\text{或}<0)$，则<u>称二次型$f(x)=x^TAx$为正/负定二次型，称对称矩阵$A$为正/负定矩阵</u>

- 半正定/半负定

    > 设$n$元二次型$f(x)=x^TAx\;(A=A^T)$，如果对于==任意==列向量$x=(x_1,x_2,\cdots,x_n)^T$，恒有$f(x)x^TAx \ge 0(\text{或}\le 0)$，且存在==非零==列向量$x_0=(x_1^0,x_2^0,\cdots,x_n^0)^T \ne 0$，使得$f(x_0)=x_0^TAx_0 = 0$，则<u>称二次型$f(x)=x^TAx$为半正/负定二次型，称对称矩阵$A$为半正/负定矩阵</u>

- 二次型，或矩阵，的正定/负定，半正定/半负定，统称为二次型或矩阵的有定性，不具备有定性的二次型或矩阵，称为不定的

- 二次型$f(x_1, x_2, \cdots, x_n) = a_1x_1^2 +a_2x_2^2+ \cdots +a_nx_n^2$正定的充要条件是$a_i > 0\; (i = 1,2,\cdots,n)$
- 对角矩阵正定的充要条件是主对角线上的元素都大于$0$

## 3.2 正定二次型和正定矩阵的判别

> 正定二次型，经过任一可逆线性变换，仍为正定二次型

- 可逆线性变换不改变二次型的定性

- 若$A,B$是两个合同的实对称矩阵，则$A,B$具有相同的定性

- 正定的必要条件

    > 若对称矩阵$A$正定，则$|A| > 0$

### 3.2.1 判别法

1. 标准型法

    > $n$元二次型$f(x)=x^TAx$正定的充分必要条件是，它的标准型为$d_1y_1^2 +d_2y_2^2 +\cdots+ d_ny_n^2$，其中，$d_i > 0$

2. 惯性指数法

    > $n$元二次型$f(x)=x^TAx$正定的充分必要条件是，它的正惯性指数为$n$

3. 规范型法

    > $n$元二次型$f(x)=x^TAx$正定的充分必要条件是，它的规范型为$y_1^2+y_2^2 +\cdots+y_n^2$

4. 与$E$结合法

    > $n$阶对称矩阵$A$正定的充分必要条件是，$A \simeq E$，即存在可逆矩阵$C$，使得$C^TAC=E$

5. 矩阵分解法

    > $n$阶对称矩阵$A$正定的充分必要条件是，存在可逆矩阵$C$，使得$A = C^C$

6. 特征值法

    > $n$阶==实==对称矩阵$A$正定的充分必要条件是，$A$的特征值全大于$0$

7. 顺序主子式法

    > 从二次型或对称矩阵本身直接判定

    - 顺序主子式定义

        - 设$n$阶矩阵$A=(a_{ij})_{n \times n}$，由$A$的第$1,2,\cdots,k$行，及第$1,2,\cdots,k$列交叉位置上的元素构成的$k$阶子式

            $\begin{vmatrix} a_{11} & a_{12} & \cdots & a_{1k}\\ a_{21} & a_{22} & \cdots & a_{2k}\\ \vdots & \vdots && \vdots\\ a_{k1} & a_{k2} & \cdots & a_{kk}\\ \end{vmatrix}\;k=1,2,\cdots,n$

            称为$A$的$k$阶顺序主子式，记为$|A_k|$，本质为一个行列式

    - 顺序主子式判别

        > $n$阶==实==对称矩阵$A$正定的充分必要条件是，$A$的各阶顺序主子式全大于$0$

## 3.3 正定矩阵的性质

1. 若$A$为正定矩阵，则$A$必为对角矩阵
2. 若$A$为正定矩阵，则$A$的主对角线元素都大于$0$
3. 若$A$为正定矩阵，则$|A| > 0$
4. 若$A$为正定矩阵，则$A$为可逆矩阵
5. 若$A$为正定矩阵，则$A^T, A^{-1}, A^{\ast},kA(k>0), A^k(k\text{为正整数})$均为正定矩阵
6. 若$A$为正定矩阵，$B$是同阶正定或半正定矩阵，则$A+B$也是正定矩阵

## 3.4 负定二次型或矩阵的判定

设$n$元二次型$f(x)=x^TAx(A^T=A)$，则

$f(x)$或$A$负定

$\Leftrightarrow$ $-f(x)$或$-A$正定

$\Leftrightarrow$ 标准型为$d_1y_1^2 +d_2y_2^2 +\cdots+ d_ny_n^2$，其中，$d_i < 0$

$\Leftrightarrow$ 规范型为$-y_1^2-y_2^2 -\cdots-y_n^2$

$\Leftrightarrow$ 负惯性指数为$n$

$\Leftrightarrow$ $A$与$-E$合同，即$A \simeq -E$

$\Leftrightarrow$ $A$的所有特征值均小于零

$\Leftrightarrow$ $A$的所有奇数阶顺序主子式小于零，所有偶数阶顺序主子式大于零

## 3.5 半正定二次型或矩阵的判定

设$n$元二次型$f(x)=x^TAx(A^T=A)$，则

$f(x)$或$A$半正定

$\Leftrightarrow$  标准型为$d_1y_1^2 +d_2y_2^2 +\cdots+ d_ny_n^2$，其中，$d_i \ge 0$，且至少有一个$d_i=0$

$\Leftrightarrow$  规范型为$y_1^2+y_2^2 +\cdots+y_\textcolor{red}{r}^2$，其中$r$为秩，$r \le n$

$\Leftrightarrow$  正惯性指数等于秩，且小于$n$

$\Leftrightarrow$  $A$与$\begin{bmatrix}E_r \\ & O \end{bmatrix}$合同，其中$r$为秩

$\Leftrightarrow$  $A$的所有特征值均大于或等于零，且至少有一个特征值为零

$\Leftrightarrow$  $A$的所有主子式均大于或等于零

## 3.6 半负定二次型或矩阵的判定

设$n$元二次型$f(x)=xTAx(AT=A)$，则

$f(x)$或$A$半负定

$\Leftrightarrow$  标准型为$d_1y_1^2 +d_2y_2^2 +\cdots+ d_ny_n^2$，其中，$d_i \le 0$，且至少有一个$d_i=0$

$\Leftrightarrow$  规范型为$-y_1^2-y_2^2 -\cdots-y_\textcolor{red}{r}^2$，其中$r$为秩，$r \le n$

$\Leftrightarrow$  负惯性指数等于秩，且小于$n$

$\Leftrightarrow$  $A$与$\begin{bmatrix}-E_r \\ & O \end{bmatrix}$合同，其中$r$为秩

$\Leftrightarrow$  $A$的所有特征值均小于或等于零，且至少有一个特征值为零

$\Leftrightarrow$  $A$的所有奇数阶主子式均小于或等于零，所有偶数阶主子式均大于或等于零
