# 范畴

1. $x \to a$时的有理函数
2. $x \to a$时涉及平方根的函数
3. $x \to \infty$时的有理函数
4. $x \to \infty$时的多项式型函数
5. $x \to -\infty$时的有理函数和类多项式函数
6. 涉及绝对值的函数

# 1. $x \to a$时的有理函数

>  有理函数，是形如$f(x)=\frac {p(x)} {q(x)}$，且$p(x), q(x)$均为多项式函数，则此时$f(x)$是有理函数

- 针对$\displaystyle \lim_{x \to a} \frac {p(x)} {q(x)}$的极限求解，可直接将$x=a$带入到$f(x)$中，根据计算后的分子分母的情况，分为三类讨论

1. 分母不为零，则计算后的结果即为极限值

2. 如果为不定式，也即分母为0

    1. 若分子为0，则需要先将$f(x)$进行分解后再次计算

    2. 若分子不为0，那么此时会涉及到在$x=a$处的一条垂直渐近线，具体结果需要结合$f(x)$在$x=a$两边的符号

        - 左极限为$\infty$，右极限为$\infty$，则双侧极限为$\infty$
        - 左极限为$-\infty$，右极限为$-\infty$，则双侧极限为$-\infty$
        - 左极限为$-\infty$，右极限为$\infty$，则双侧极限为不存在 Does Not Exist DNE
        - 左极限为$\infty$，右极限为$-\infty$，则双侧极限为不存在 Does Not Exist DNE

        ![image-20241112172050554](<chap 4 求解多项式极限的问题.assets/image-20241112172050554.png>)

# 2. $x \to a$时涉及平方根的函数

> 带有根号的函数进行极限求解

分子分母需要同时乘以某个的共轭表达式

> $\sqrt a + \sqrt b$根号的共轭表达式是$\sqrt a - \sqrt b$，可通过平方差公式计算后得到$a-b$

# 3. $x \to \infty$时的有理函数

> 1. 多项式性质： 当$x$很大时，首项决定一切
>
> 2. 定理：
>
>     对于任意的$n > 0 \qquad n \in \mathbb N$， $\displaystyle \lim_{x \to \infty} \frac C {x_n} = 0$
>

- 针对$\displaystyle \lim_{x \to \infty} \frac {p(x)} {q(x)}$的极限求解的一般思路是，对于分子分母中的每个多项式，如果多项式是多于一项的，那么就将其除以首项再乘以首项，也即，对于每个多项式$p(x)$，有$\frac {px} {p(x)的首项} p(x)的首项$

- 可以结合$p(x)$和$q(x)$的首项的次数，对结果进行初步判断
    - 若次数相同，则极限是有限且非领
    - 若分母次数高于分子次数，则极限是零
    - 若分母次数小于分子次数，则极限为$\infty$或$-\infty$

# 4. $x \to \infty$时的多项式型函数

> 类多项式型函数指的是函数自变量的次幂是分数或者n次根，其不符合多项式函数定义，但是形如多项式函数

针对该类型函数的极限求值的一般解法，是通过乘以共轭表达式，或者类似$x \to \infty$时的有理函数时进行的除以乘以首项的做法

# 5. $x \to -\infty$时的有理函数和类多项式函数

- 有理函数化简到最后需要注意符号问题

- 类多项式型函数要注意对开根号后的负号问题

    - > 如果$x < 0$，并且需要写$\sqrt[n]{x^{某次幂}}=x^m$，那么需要在$x^m$前加负号的唯一情形是$n$为偶数且$m$为奇数

# 6. 涉及绝对值的函数

- 根据绝对值内部的符号来考虑多个区间，查看是否存在左右极限，以及是否相等以确认是否存在双侧极限