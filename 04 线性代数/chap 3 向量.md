# 1. 向量的概念及线性运算

- 向量的定义

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

- 向量的线性运算

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

# 3. 向量组的等价

# 4. 向量组的线性相关性

# 5. 极大线性无关组

# 6. 向量组的秩