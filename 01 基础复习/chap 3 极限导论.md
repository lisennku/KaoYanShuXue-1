# 1. 极限

## 1.1 极限的定义

### 1.1.1 自变量趋近于有限值时函数的极限

> 定义1：
>
> 当$f(x)$在点$x_0$的去心邻域内有定义，如果存在常数$L$，使得任意给定的正数$\epsilon > 0$，都存在$\delta > 0$，使得不等式
>
> $|f(x) - L| < \epsilon \qquad |x-x_0| \in (0, \delta)$
>
> 恒成立，则常数$L$就叫做函数$f(x)$当$x \to x_0$时的极限，记作$\displaystyle \lim_{x \to x_0} f(x) = L$

- $\delta$的选择，依赖于$\epsilon$的选择

- 定义1可以理解为，只要$x$距离$x_0$不超过$\delta$，则$f(x)$的值距离$L$就不会超过$\epsilon$

    - $|f(x) - L| < \epsilon$ 可以表示为函数值距离水平线$y = L$的距离
    - $|x-x_0|$可以表示为$x$距离$x_0$的距离

- 换句话说，只要给定了一个和$L$的距离$\epsilon$，就一定可以在接近$x_0$的距离$\delta$内，找到一点，使得函数值和$L$的距离小于给定的$\epsilon$

    ![image-20241112123254848](<chap 3 极限导论.assets/image-20241112123254848.png>)

### 1.1.2 自变量趋近于无穷时函数的极限

> 定义2：
>
> 设函数$f(x)$，当$|x|$大于某一正数时有定义，如果存在常数$L$，使得任意给定的正数$\epsilon > 0$，总存在正数$M$，使得不等式
>
> $|f(x) - L| < \epsilon \qquad |x| > M $
>
> 恒成立，则常数$L$就叫做函数$f(x)$当$x$趋近于$\infty$时的极限，记作$\displaystyle \lim_{x \to \infty} f(x) = L$

- 定义2对于正负无穷都成立

- 定义2可以理解为，只要有$|x| > M$，就有函数值和$L$的距离小于给定的$\epsilon$，也即位于区间$[L-\epsilon, L+\epsilon]$

    ![image-20241112123347094](<chap 3 极限导论.assets/image-20241112123347094.png>)

### 1.1.3 左右极限

- 左极限

> 定义3：
>
> 当$f(x)$在点$x_0$的左邻域内有定义，如果存在常数$L$，使得任意给定的正数$\epsilon > 0$，都存在$\delta > 0$，使得不等式
>
> $|f(x) - L| < \epsilon \qquad x_0 - \delta < x < x_0$
>
> 恒成立，则常数$L$就叫做函数$f(x)$当$x \to x_0$时的极限，记作$\displaystyle \lim_{x \to x_0^-} f(x) = L$

- 右极限

> 定义4：
>
> 当$f(x)$在点$x_0$的右邻域内有定义，如果存在常数$L$，使得任意给定的正数$\epsilon > 0$，都存在$\delta > 0$，使得不等式
>
> $|f(x) - L| < \epsilon \qquad x_0 < x < x_0 +\delta $
>
> 恒成立，则常数$L$就叫做函数$f(x)$当$x \to x_0$时的极限，记作$\displaystyle \lim_{x \to x_0^+} f(x) = L$

# 2. 极限的四则运算

> 要求参与运算的函数的极限==存在且有限==，也即非无穷

- 和差运算
    - 当两个函数$f$和$g$，在$x \to a$时有分别有$f(x) \to L$和$g(x) \to M$，那么当$x \to a$时，有$f(x) + g(x) \to L + M$
    - 当两个函数$f$和$g$，在$x \to a$时有分别有$f(x) \to L$和$g(x) \to M$，那么当$x \to a$时，有$f(x) - g(x) \to L - M$
- 乘法运算
    - 当两个函数$f$和$g$，在$x \to a$时有分别有$f(x) \to L$和$g(x) \to M$，那么当$x \to a$时，有$f(x)g(x) \to LM$
- 除法运算
    - 当两个函数$f$和$g$，在$x \to a$时有分别有$f(x) \to L$和$g(x) \to M$，那么当$x \to a$时，有$\frac{f(x)} {g(x)} \to \frac L M$，$M$不为0

# 3. 夹逼定理的证明

> 夹逼定义， aka 三明治定理 Squeeze Theorem/ Sandwich Theorem
>
> 如果两个函数$f(x)$和$g(x)$在某一点$c$附近有同一个极限，也即$\displaystyle \lim_{x \to c} f(x) = \lim_{x \to c} g(x) = L$
>
> ==并且==在点$c$附近，另一个函数$h(x)$总是介于$f(x)$和$g(x)$之间，也即$f(x) \leq h(x) \leq g(x)$
>
> 那么$h(x)$在点$c$附近也有极限，并且极限是$L$

![38895cf5646657a075bd1cd74ae6873](<chap 3 极限导论.assets/38895cf5646657a075bd1cd74ae6873.jpg>)

# 4. 其他性质

## 4.1 某点的极限与该点的函数值

>  某点的极限值，与该函数在该点的函数值是无关的

极限值描述的自变量接近某值时，函数的趋近值

可以考虑函数$f(x) = \begin{cases}  x - 1 & \ x \neq 2 \\ 3 &  x = 2  \end{cases} $ 在$x \to 2$时的极限是1，而非$f(2)$的值3

## 4.2 极限存在的充要条件

> 当且仅当函数$f(x)$在某点$a$的左右极限都存在，且相等时，该函数在点$a$附近存在极限

## 4.3 垂直渐近线

> 如果函数$f(x)$在$x=a$处有一条垂直渐近线，意味着左极限$\displaystyle \lim_{x\to a^-} f(x)$和右极限$\displaystyle \lim_{x\to a^+} f(x)中至少有一个极限是$+\infty$或$-\infty$

## 4.4 水平渐近线

> 如果函数$f(x)$在$y=L$处有一条右侧水平渐近线， 则$\displaystyle \lim_{x\to \infty} f(x) = L$
>
> 如果函数$f(x)$在$y=L$处有一条左侧水平渐近线， 则$\displaystyle \lim_{x\to -\infty} f(x) = L$

## 4.5 渐近线说明

> 1. 一个函数不一定要在左右两边有相同的水平渐近线，如$f(x) = tan^{-1}(x)$
>
>     ![image-20241112142807899](<chap 3 极限导论.assets/image-20241112142807899.png>)
>
> 2. 一个函数可以和其水平渐近线相交，如函数$f(x) = \frac {sin(x)} x$
>
>     ![image-20241112142726050](<chap 3 极限导论.assets/image-20241112142726050.png>)

# 5. 附录

## 5.1 三角不等式证明

> 三角不等式：
>
> 对于任意的实数$a, b$，有$|a+b| \leq |a| + |b|$

![017f98181d866a5f82da0add4b207f1](<chap 3 极限导论.assets/017f98181d866a5f82da0add4b207f1.jpg>)



