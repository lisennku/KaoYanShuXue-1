# 1. 向量的概念及线性运算

## 1.1 向量的定义

> 由$n$个数$a_1, a_2, \cdots, a_n$组成的有序数组$\alpha = (a_1, a_2, \cdots, a_n)$，称为向量，此时称向量$\alpha$为$n$维向量
>
> - 其中，
>     - 数$a_i$称为向量的第$i$个分量
>     - 分量的个数，称为向量的维数

> $n$维向量，分为行向量和列向量
>
> - 行向量：有序数组排列成行的形式，是一个$1 \times n$的矩阵
> - 列向量：有序数组排列成列的形式，是一个$n \times 1$的矩阵

- 零向量

    > 所有分量全为$0$的向量，记为$0$

- 负向量

    > 将每个分量都取相反数得到的向量

- 向量的转置

    > 类比矩阵的转置

- 向量的相等

    > 两个同种类型的向量相等$\Leftrightarrow$相同位置的分量相等

## 1.2 向量的线性运算

> 向量的加法运算和数乘，称之为向量的线性运算

- 向量的加减

    > 设两个$n$维向量，$\alpha = (a_1, a_2, \cdots, a_n),\; \beta = (b_1, b_2, \cdots, b_n)$
    >
    > - 则向量$\alpha$和$\beta$的加法定义为：$\alpha + \beta = (a_1+b_1, a_2+b_2, \cdots, a_n+b_n)$
    >
    > - 则向量$\alpha$和$\beta$的减法定义为（结合向量加法和负向量）：$\alpha - \beta = (a_1-b_1, a_2-b_2, \cdots, a_n-b_n)$

- 向量的数乘

    > 设向量$\alpha = (a_1, a_2, \cdots, a_n)$，$k$是一个常数，则数$k$与向量$\alpha$的乘法定义为
    >
    > $k\alpha = (ka_1, ka_2, \cdots, ka_n)$

- 向量线性运算满足的规律

    > 设$\alpha, \beta, \gamma$为同型的$n$维向量，$0$为同型零向量，$k, l$为实数

    - 交换律：$\alpha + \beta = \beta + \alpha$
    - 结合律：$(\alpha + \beta) + \gamma= \alpha + (\beta + \gamma)$
    - $\alpha + 0 = 0+\alpha = \alpha$
    - $\alpha + (-\alpha) = (-\alpha)+\alpha = 0$
    - $1 \cdot \alpha = \alpha$
    - $(kl)\alpha = k(l\alpha)=l(k\alpha)$
    - $k(\alpha + \beta) = k\alpha + k\beta$
    - $(k+l)\alpha = k\alpha + l\alpha$

# 2. 向量的线性组合与线性表示

## 2.1 向量的线性组合与线性表示的定义

> 设$\alpha_1, \alpha_2, \cdots, \alpha_m$是一组$n$维向量，$k_1, k_2, \cdots, k_m$是一组常数，则称
>
> $k_1\alpha_1 + k_2\alpha_2 + \cdots + k_m\alpha_m$为向量组$\alpha_1, \alpha_2, \cdots, \alpha_m$的一个线性组合
>
> $k_1, k_2, \cdots, k_m$称为组合系数

> 设$\beta,\alpha_1, \alpha_2, \cdots, \alpha_m$是$n$维向量，若存在常数$k_1, k_2, \cdots, k_m$，使得关系式
>
> $\beta = k_1\alpha_1 + k_2\alpha_2 + \cdots + k_m\alpha_m$成立，则称$\beta$是向量组$\alpha_1, \alpha_2, \cdots, \alpha_m$的线性组合，也称，$\beta$可由向量组$\alpha_1, \alpha_2, \cdots, \alpha_m$==线性表示==

## 2.2 向量的线性组合与线性表示的判定

- 通过线性方程组判定

  > 判断$\beta$是否是向量组$\alpha_1, \alpha_2, \cdots, \alpha_n$的线性组合，等同于判断一个线性方程组是否有解，且有解时，该解即为组合系数

  - 线性方程组：$x_1\alpha_1 + x_2\alpha_2 + \cdots + x_n\alpha_n = \beta$
      - 当$\beta,\alpha_1, \alpha_2, \cdots, \alpha_n$是行向量时，则系数矩阵$A = \alpha_1^T, \alpha_2^T, \cdots, \alpha_n^T$，方程组可写为$Ax=\beta^T$

      - 当$\beta,\alpha_1, \alpha_2, \cdots, \alpha_n$是列向量时，则系数矩阵$A = \alpha_1, \alpha_2, \cdots, \alpha_n$，方程组可写为$Ax=\beta$

  - $\beta$是$\alpha_1, \alpha_2, \cdots, \alpha_n$的线性组合 $\Leftrightarrow$ 方程组$x_1\alpha_1 + x_2\alpha_2 + \cdots + x_n\alpha_n = \beta$有解
  - $\beta$不是$\alpha_1, \alpha_2, \cdots, \alpha_n$的线性组合 $\Leftrightarrow$ 方程组$x_1\alpha_1 + x_2\alpha_2 + \cdots + x_n\alpha_n = \beta$无解

- 通过秩

  - 若$\beta,\alpha_1, \alpha_2, \cdots, \alpha_n$是行向量，记矩阵$A = (\alpha_1^T, \alpha_2^T, \cdots, \alpha_n^T)$，$B = (\alpha_1^T, \alpha_2^T, \cdots, \alpha_n^T, \beta^T)$

  - 若$\beta,\alpha_1, \alpha_2, \cdots, \alpha_n$是列向量，记矩阵$A = (\alpha_1, \alpha_2, \cdots, \alpha_n)$，$B = (\alpha_1, \alpha_2, \cdots, \alpha_n, \beta)$

  > $\beta$是$\alpha_1, \alpha_2, \cdots, \alpha_n$的线性组合 $\Leftrightarrow$ $r(A) = r(B)$
  >
  > $\beta$不是$\alpha_1, \alpha_2, \cdots, \alpha_n$的线性组合 $\Leftrightarrow$ $r(A) \ne r(B)$


## 2.3 向量的线性组合与线性表示的结论

- 零向量是任意向量组的线性组合

- 向量组$\alpha_1, \alpha_2, \cdots, \alpha_n$中的任一向量$\alpha_i \; (1 \le i \le n)$，均可由本向量组线性表示

- 任一$n$维向量$\alpha = (a_1, a_2, \cdots, a_n)$，都可由$n$维基本单位向量组线性表示，且表示方式唯一，组合系数即为对应的分量

    > $n$维基本单位向量组$\varepsilon_1 = (1, 0,0,\cdots, 0), \varepsilon_2 = (0,1,0,\cdots, 0), \cdots, \varepsilon_n = (0,0,0,\cdots, 1)$

# 3. 向量组的等价

## 3.1 向量组等价的定义

> 设有两个向量组$A = \alpha_1, \alpha_2, \cdots, \alpha_n,\; \beta = \beta_1, \beta_2, \cdots, \beta_n$，若向量组$A$中的每个向量都可用向量组$B$线性表示，则称向量组$A$可由向量组$B$线性表示，若向量组$A$与向量组$B$能够==互相线性表示==，则称向量组$A$和向量组$B$==等价==

## 3.2 向量组等价的性质

- 反身性：任一向量组与其本身等价
- 对称性：若向量组$A$等价于向量组$B$，则向量组$B$等价于向量组$A$
- 传递性：若向量组$A$等价于向量组$B$，向量组$B$等价于向量组$C$，则向量组$A$等价于向量组$C$
- 若$A,B,C$均为$n$阶方阵，且$AB=C$，则有
    - $C$的==列==向量组可由==$A$的列==向量组表示，当$B$可逆时，二者等价
    - $C$的==行==向量组可由==$B$的行==向量组表示，当$A$可逆时，二者等价

## 3.3 向量组等价的判定

- 由向量组$A : \alpha_1, \alpha_2, \cdots, \alpha_m$和 $ B : \beta_1, \beta_2, \cdots, \beta_n$构造矩阵
    - 行向量：$A=(\alpha_1^T, \alpha_2^T, \cdots, \alpha_m^T)$， $ B = (\beta_1^T, \beta_2^T, \cdots, \beta_n^T)$
    - 列向量：$A=(\alpha_1, \alpha_2, \cdots, \alpha_m)$， $ B = (\beta_1, \beta_2, \cdots, \beta_n)$

> 向量组$ B : \beta_1, \beta_2, \cdots, \beta_n$可由向量组$A : \alpha_1, \alpha_2, \cdots, \alpha_m$线性表示$\Leftrightarrow$矩阵$A$的秩等于矩阵$(A,B)$的秩，即$r(A) = r(A,B)$

> 向量组$ B : \beta_1, \beta_2, \cdots, \beta_n$可由向量组$A : \alpha_1, \alpha_2, \cdots, \alpha_m$线性表示，则$r(B) \le r(A)$

> 向量组$ B : \beta_1, \beta_2, \cdots, \beta_n$和向量组$A : \alpha_1, \alpha_2, \cdots, \alpha_m$等价 $\Leftrightarrow$$r(A)=r(B)=r(A,B)$

# 4. 向量组的线性相关性



## 4.1 向量组的线性相关/无关的定义

> 给定向量组$\alpha_1, \alpha_2, \cdots, \alpha_n$，如果存在==不全为$0$==的数$k_1, k_2, \cdots, k_n$，
>
> 使得$k_1\alpha_1+k_2\alpha_2+ \cdots+k_n\alpha_n = \textcolor{red}{0}$成立
>
> 则称向量组$\alpha_1, \alpha_2, \cdots, \alpha_n$线性相关，$k_1, k_2, \cdots, k_n$称为一组相关系数，否则，称向量组线性无关

## 4.2 向量组的线性相关/无关的性质与结论

1. 一个向量$\alpha$线性相关$\Leftrightarrow$$\alpha = 0$，一个向量$\alpha$线性无关$\Leftrightarrow \alpha = 0$
    - 若向量$\alpha$线性相关，意味着有非零的$k$，使得$k\alpha = 0$，所以只能有$\alpha = 0$
    - 若向量$\alpha$线性无关，意味着只有当$k=0$时，$k\alpha = 0$，所以只能有$\alpha \ne 0$
2. 两个向量线性相关$\Leftrightarrow$两个向量对应的分量成比例
    - $k_1\alpha + k_2\beta = 0 \Rightarrow \frac {\alpha} {\beta} = -\frac {k_2} {k_1}$
3. 如果向量组中有一部分向量（称为部分组）线性相关，则该向量组线性相关
    - 可令不在部分组内的向量的系数为$0$
4. 若向量组中有两个向量成比例，则向量组必线性相关
    - 结合性质$2$和性质$3$易知
5. 若向量组线性无关，则其任一部分组也不线性相关
6. 含有零向量的向量组必线性相关
    - 令零向量的系数为$1$，其他向量的系数为$0$
7. $n$维单位坐标向量必线性无关
8. 设$r$维向量$\alpha_1, \alpha_2, \cdots, \alpha_m$线性无关，$\beta_1, \beta_2, \cdots, \beta_m$是$\alpha_1, \alpha_2, \cdots, \alpha_m$的$r+l$维接长向量，则$\beta_1, \beta_2, \cdots, \beta_m$线性无关
9. 设$\alpha_1, \alpha_2, \cdots, \alpha_m$是$r$维向量，$\beta_1, \beta_2, \cdots, \beta_m$是$\alpha_1, \alpha_2, \cdots, \alpha_m$的$r+l$维接长向量，若$\beta_1, \beta_2, \cdots, \beta_m$线性相关，则$\alpha_1, \alpha_2, \cdots, \alpha_m$也线性相关

## 4.3 向量组的线性相关/无关的判定

- 定义法

    > 向量组$\alpha_1, \alpha_2, \cdots, \alpha_n$线性相关$\Leftrightarrow$齐次线性方程组$x_1\alpha_1 + x_2\alpha_2 +\cdots + x_n\alpha_n = 0$有非零解

    > 向量组$\alpha_1, \alpha_2, \cdots, \alpha_n$线性无关$\Leftrightarrow$齐次线性方程组$x_1\alpha_1 + x_2\alpha_2 +\cdots + x_n\alpha_n = 0$只有零解

- 矩阵秩法

    > 设向量组$\alpha_1, \alpha_2, \cdots, \alpha_n$，构造矩阵$A$，并求出矩阵$A$的秩
    >
    > 如果$r(A) < n$，则向量组线性相关，
    >
    > 如果$r(A) = n$，则向量组线性无关，
    >
    > 其中$n$为向量组内向量的个数
    >
    > - 若$\alpha_1, \alpha_2, \cdots, \alpha_n$为行向量，则$A = (\alpha_1^T, \alpha_2^T, \cdots, \alpha_n^T)$
    > - 若$\alpha_1, \alpha_2, \cdots, \alpha_n$为列向量，则$A = (\alpha_1, \alpha_2, \cdots, \alpha_n)$

- 行列式法 <u>*适用于向量组中，向量个数等于维度数的场景*</u>

    > 设$\alpha_1, \alpha_2, \cdots, \alpha_n$为$n$个$n$维向量，
    >
    > - 若$\alpha_1, \alpha_2, \cdots, \alpha_n$为行向量，则$A = (\alpha_1^T, \alpha_2^T, \cdots, \alpha_n^T)$
    > - 若$\alpha_1, \alpha_2, \cdots, \alpha_n$为列向量，则$A = (\alpha_1, \alpha_2, \cdots, \alpha_n)$
    >
    > 可知$A$为$n$阶方阵，则
    >
    > $|A| = 0$时，向量组线性相关
    >
    > $|A| \ne 0$时，向量组线性无关

## 4.4 矩阵的行/列向量组的线性相关与矩阵的秩的关系

> 设$A$为$m \times n$阶矩阵，则
>
> - 行向量组
>     - 线性相关 $\Leftrightarrow r(A)< m$
>     - 线性无关 $\Leftrightarrow r(A) = m$
> - 列向量组
>     - 线性相关 $\Leftrightarrow r(A)< n$
>     - 线性无关 $\Leftrightarrow r(A) = n$

> 设$A$为$n$阶方阵，则
>
> - $A$的行/列向量组线性相关$\Leftrightarrow r(A) < n \Leftrightarrow |A| = 0 \Leftrightarrow A$不可逆
> - $A$的行/列向量组线性无关$\Leftrightarrow r(A) = n \Leftrightarrow |A| \ne 0 \Leftrightarrow A$可逆

## 4.5 向量组的线性相关、线性无关与线性表示的关系

> 向量组$\alpha_1, \alpha_2, \cdots, \alpha_m\;(m \ge 2)$线性==相关==的充要条件是，其中，至少有一个向量，是其他$m-1$个向量的线性组合

> 向量组$\alpha_1, \alpha_2, \cdots, \alpha_m\;(m \ge 2)$线性==无关==的充要条件是，向量组中任一向量，都不能由其他$m-1$个向量线性表示

> 若向量组$\alpha_1, \alpha_2, \cdots, \alpha_m$线性无关，而向量组$\alpha_1, \alpha_2, \cdots, \alpha_m,\beta$线性相关，则$\beta$可由向量组$\alpha_1, \alpha_2, \cdots, \alpha_m$线性表示，且表示法唯一

> 若向量组$\alpha_1, \alpha_2, \cdots, \alpha_m$线性无关，而向量$\beta$不能由向量组$\alpha_1, \alpha_2, \cdots, \alpha_m$线性表示，则向量组$\alpha_1, \alpha_2, \cdots, \alpha_m,\beta$线性无关

> 设有两个向量组：$(I)\; \alpha_1, \alpha_2, \cdots, \alpha_r$，$(II)\; \beta_1, \beta_2, \cdots, \beta_s$，若向量组$(I)$线性无关，且向量$(I)$可由向量组$(II)$线性表示，则$r \le s$

> 设有两个向量组：$(I)\; \alpha_1, \alpha_2, \cdots, \alpha_r$，$(II)\; \beta_1, \beta_2, \cdots, \beta_s$，若向量组$(I)$可由向量组$(II)$线性表示，且$r > s$，则向量组$(I)$必线性相关

- > 若$(I),(II)$均线性无关，且$(I),(II)$可互相线性表示，则$r = s$

- > 若向量组所含向量的个数大于向量的维数，则该向量组线性相关

# 5. 极大线性无关组

## 5.1 定义

> 如果向量组$\alpha_1, \alpha_2, \cdots, \alpha_s$的部分组$\alpha_{i_{1}}, \alpha_{i_{2}},\cdots, \alpha_{i_{r}}$满足：
>
> 1. $\alpha_{i_{1}}, \alpha_{i_{2}},\cdots, \alpha_{i_{r}}$线性无关
> 2. 向量组$\alpha_1, \alpha_2, \cdots, \alpha_s$中任一向量都可由$\alpha_{i_{1}}, \alpha_{i_{2}},\cdots, \alpha_{i_{r}}$线性表示
>     - 条件$2$可更换为
>         - 向量组中任一$r+1$个向量（如果有的话）都线性相关
>         - 向量组中任意多于$r$个向量（如果有的话）都线性相关

## 5.2 极大线性无关组的性质和结论

1. 零向量组没有极大线性无关组
2. 线性无关的向量组，其极大线性无关组为向量组本身
3. 向量组的极大线性无关组可能不唯一
4. 向量组和它的任一极大线性无关组等价
5. 同一向量组的两个极大线性无关组等价， 且所含向量个数相等
6. 若向量组$(I)$可由向量组$(II)$线性表示，则向量组$(I)$的极大线性无关组可由向量组$(II)$的极大线性无关组线性表示
7. 等价的向量组，其极大线性无关组也等价

## 5.3 极大线性无关组的求法 - 矩阵初等变换法

> 求向量组$\alpha_1, \alpha_2, \cdots, \alpha_s$的一个极大线性无关组，并将其余向量用极大线性无关组表示出来，其步骤如下：

1. 构造矩阵$A$
    - 若$\alpha_1, \alpha_2, \cdots, \alpha_s$为列向量，则矩阵$A = (\alpha_1, \alpha_2, \cdots, \alpha_s)$
    - 若$\alpha_1, \alpha_2, \cdots, \alpha_s$为列向量，则矩阵$A = (\alpha_1^T, \alpha_2^T, \cdots, \alpha_s^T)$
2. 对矩阵$A$进行初等行变换，化为行阶梯矩阵$B$，则$B$的==首非零元素所在的列==，==对应于向量组$\alpha_1, \alpha_2, \cdots, \alpha_s$中的向量==，即为向量组$\alpha_1, \alpha_2, \cdots, \alpha_s$的一个极大线性无关组
3. 再对行阶梯矩阵$B$进行初等行变换，化为行简化阶梯矩阵$C$，则$C$中列向量的线性关系即为$A$中列向量的线性关系，也即$\alpha_1, \alpha_2, \cdots, \alpha_s$的线性关系

# 6. 向量组的秩

## 6.1 向量组秩的定义

> 向量组$\alpha_1, \alpha_2, \cdots, \alpha_s$的任一极大线性无关组中所含向量的个数，称为向量组$\alpha_1, \alpha_2, \cdots, \alpha_s$的秩，记为$r(\alpha_1, \alpha_2, \cdots, \alpha_s)$

- 规定，零向量组的秩为$0$

## 6.2 向量组秩的性质和结论

1. 向量组的秩是唯一的，等于极大线性无关组中所含向量个数

2. 向量组$\alpha_1, \alpha_2, \cdots, \alpha_s$线性无关$\Leftrightarrow r(\alpha_1, \alpha_2, \cdots, \alpha_s) = s$ 因为行阶梯矩阵没有零行，所以根据矩阵初等变换求向量组的极大线性无关组，此时全部变量都属于极大线性无关组

    向量组$\alpha_1, \alpha_2, \cdots, \alpha_s$线性相关$\Leftrightarrow r(\alpha_1, \alpha_2, \cdots, \alpha_s) < s$

3. 若向量组$(I)$可由向量组$(II)$线性表示，则$r(I) \le r(II)$

4. 等价的向量组的秩相等

5. 向量组的秩$\le$向量的个数；

    向量组的秩$\le$向量的维数

6. 若向量组的秩为$r$，则向量组中必有$r$个向量线性无关，而任意多于$r$个向量都线性相关

7. 若向量组的秩为$r(r > 0)$，则任意含$r$个向量的线性无关的部分组都是向量组的极大线性无关组

## 6.3 向量组秩的求法

> 根据矩阵的秩等于其行向量组的秩，也等于其列向量组的秩，将求向量组的秩转为求矩阵的秩

1. 构造矩阵$A$

    - 若$\alpha_1, \alpha_2, \cdots, \alpha_s$为列向量，则矩阵$A = (\alpha_1, \alpha_2, \cdots, \alpha_s)$

    - 若$\alpha_1, \alpha_2, \cdots, \alpha_s$为列向量，则矩阵$A = (\alpha_1^T, \alpha_2^T, \cdots, \alpha_s^T)$

2. 求矩阵$A$的秩$r(A)$，而$r(A) = r(\alpha_1, \alpha_2, \cdots, \alpha_s)$ 