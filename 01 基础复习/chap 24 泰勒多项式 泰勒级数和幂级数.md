# 1. 泰勒多项式

> <font size=4>**泰勒近似定理**</font>
>
> <font color=blue size=4>若$f$在$x=a$处光滑，则在所有次数为$N$或者更低次数的多项式中，==在$x=a$附近时==，==最近似于==$f(x)$的多项式是</font>
>
> <font color=blue size=4>$P_N(x)=f(a) + f^{\prime}(a)(x-a) + \frac{f^{\prime\prime}(a) } {2}(x-a)^2 + \dots + \frac {f^N(a)}{N!}(x-a)^N$</font>
>
> <font size=4>使用求和符号表示为</font>
>
> <font color=blue size=4>$\displaystyle P_N(x)=\sum_{n=0}^{N}\frac {f^{(n)}(a)} {n!}(x-a)^n$</font>
>
> - 其中，零阶导为$f(a)$本身
>
> <font color=blue size=4>$P_N(x)$称为$f(x=)$==在$x=a$处==的==$N$阶==泰勒多项式</font>
>
> - 注意，实际的次数可能小于$N$

> <font size=4>泰勒多项式性质：</font>
>
> <font color=blue size=4>对所有的$x = 0, 1, 2,\dots, N$，有$P^{(n)}_N(a) = f^{(n)}(a)$</font>
>
> 也即，当$x=a$时，$P_N$的所有$N$阶及以下的导数值都和$f$对应的导数值相同

# 2. 泰勒定理

> $N$阶误差项
>
> 又称为$N$阶余项，指的是使用在$x=a$处的$N$阶泰勒多项式$P_N(x)$来预估$f(x)$的值时产生的误差
>
> $R_N(x) = f(x) - P_N(x)$

> <font size=4>泰勒定理</font>
>
> <font size=4 color=blue>关于$x=a$的$N$阶余项：</font>
>
> <font size=4 color=blue>$R_N(x) = \frac {f^{(N+1)(a)}} {(N+1)!} (x-a)^{N+1}$</font>
>
> - $c$是介于$x$和$a$之间的一个数
>     - 注意：$x$可能大于$a$，也可能小于$a$，所以说$c$介于两者
> - ==$c$依赖于$x$和$N$==

# 3. 幂级数

- 在$x=a$处的幂级数

    > <font color=blue size=4>$x=a$处的幂级数的一般表达式为$a_0 + a_1(x-a) + a_2(x-a)^2 +\dots + a_n(x-a)^n + \dots$</font>
    >
    > <font color=blue size=4>使用求和公式表示为$\displaystyle \sum_{n=0}^{\textcolor{red}{\infty}}a_n(x-a)^n$</font>
    >
    > - 其中$a_n$是确定的常数
    > - ==数$a$称为幂级数的中心==，因为当$x=a$时级数收敛于$a_0$

- 在$x=0$处的幂级数

    > <font color=blue size=4>$x=0$处的幂级数的一般表达式为$a_0 + a_1x + a_2x^2 +\dots + a_nx^n + \dots$</font>
    >
    > <font color=blue size=4>使用求和公式表示为$\displaystyle \sum_{n=0}^{\textcolor{red}{\infty}}a_nx^n$</font>
    >
    > - 其中$a_n$是确定的常数

    > 在$x=0$处的特殊幂函数
    >
    > $\displaystyle e^x = \frac {x^0} {0!} + \frac {x^1} {1!} + \frac {x^2} {2!} + \frac {x^3} {3!} + \dots = \sum_{n=0}^{\textcolor{red}{\infty}}\frac 1 {n!}x^n$

# 4. 泰勒级数和麦克劳林级数

- 泰勒级数

    > <font color=blue size=4>$f$关于$x=a$的泰勒级数为</font>
    >
    > <font color=blue size=4>$\displaystyle \sum_{n=0}^{\textcolor{red}{\infty}} \frac {f^{(n)}(a)} {n !}(x-a)^n = f(a) + f^{\prime}(a)(x-a) + \frac {f^{\prime\prime}(a)} {2!} (x-a)^2 + \frac {f^{(3)}(a)} {3!} (x-a)^3 + \dots +  \frac {f^{(n)}(a)} {n !}(x-a)^n + \dots$</font>
    >
    > - 可见，泰勒多项式$P_N(x)$是泰勒级数的$N$项部分和
    >
    > 

- 麦克劳林级数

    > 麦克劳林级数，就是$f$关于$x=0$的泰勒级数
    >
    > <font color=blue size=4>$\displaystyle \sum_{n=0}^{\textcolor{red}{\infty}} \frac {f^{(n)}(a)} {n !}x^n = f(a) + f^{\prime}(a)x + \frac {f^{\prime\prime}(a)} {2!}x^2 + \frac {f^{(3)}(a)} {3!} x^3 + \dots +  \frac {f^{(n)}(a)} {n !}x^n + \dots$</font>

- 泰勒级数的收敛性

    > 为了证明一个函数在某些数$x$处，等于它的泰勒级数，可尝试证明当$n \to \infty$时，$R_N(x) \to \infty$

- 常见的麦克劳林级数

    - > 也即在$x=0$的泰勒级数

    - $\displaystyle e^x = \sum_{n=0}^{\textcolor{red}{\infty}}\frac 1 {n!}x^n = 1 + x + \frac 1 {2!}x^2 + \frac 1 {3!}x^3 +\dots$

    - $\displaystyle sin(x) = \sum_{n = 0}^{\textcolor{red}{\infty}}\frac {(-1)^n} {(2n+1)!}x^{2n+1}$
    - $\displaystyle cos(x) = \sum_{n = 0}^{\textcolor{red}{\infty}}\frac {(-1)^n} {(2n)!}x^{2n}$

