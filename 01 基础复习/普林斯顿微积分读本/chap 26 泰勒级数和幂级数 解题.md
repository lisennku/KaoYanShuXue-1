# 1. 幂级数的收敛性

> 幂级数，指的是$\displaystyle \sum_{n=0}^{\infty}a_n(x-a)^n$形式的级数

幂级数收敛性的情形：

- 存在某数$R > 0$，该数被称为收敛半径，使得
    - 幂级数在区域$|x-a|<R$内收敛
    - 幂级数在区域$|x-a|>R$内发散
    - 在区域端点$|x-a|=R$处需要特殊讨论
- 幂级数对所有的$x$均绝对收敛，此时收敛半径为$\infty$
- 幂级数只在$x=a$处收敛，对于其他所有的$x$均发散，此时收敛半径为$0$



# 2. 合成新的泰勒级数

>  常见麦克劳林级数

> $e^x = \displaystyle \sum_{n=0}^{\infty}\frac 1 {n!}x^n = 1 + x + \frac 1 {2!}x^2 + \frac 1 {3!}x^3 + \frac 1 {4!}x^4 + \dots$
>
> 对所有实数$x$都成立

> $sin(x) = \displaystyle \sum_{n=0}^{\infty}\frac {(-1)^n} {(2n+1)!}x^{2n+1} = x - \frac 1 {3!}x^3  + \frac 1 {5!}x^5 - \frac 1 {7!}x^7 + \dots$
>
> 对所有实数$x$都成立

> $cos(x) = \displaystyle \sum_{n=0}^{\infty}\frac {(-1)^n} {(2n)!}x^{2n} = 1 - \frac 1 {2!}x^2  + \frac 1 {4!}x^4 - \frac 1 {6!}x^6 + \dots$
>
> 对所有实数$x$都成立

> $\frac 1 {1-x} = \displaystyle \sum_{n=0}^{\infty}x^n = 1 + x + x^2 + x^3 + \dots$
>
> 对$-1 < x < 1$成立

> $ln(1+x) = \displaystyle \sum_{n=1}^{\infty}-\frac {(-1)^n} {n}x^n = x - \frac 1 2 x^2 + \frac 1 3 x^3 - \frac 1 4 x^4 + \dots$
>
> 对$-1 < x \le 1$成立

> $ln(1-x) = \displaystyle \sum_{n=1}^{\infty}-\frac {1} {n}x^n = -x - \frac 1 2 x^2 - \frac 1 3 x^3 - \frac 1 4 x^4 - \dots$
>
> 对$-1 \le x < 1$成立

## 2.1 代换和泰勒级数

> 使用代换，既改变了泰勒级数，也改变了原函数，可以理解为上方等号左右两端的都发生了改变
>
> ==代换法并不是万能的，仍需考虑实际==

- 使用$x^n$代换$x$：麦克劳林级数生成新的麦克劳林级数

    > 在$f(x)$麦克劳林级数中，使用$x^n$代换$x$，可以得到$f(x^n)$的麦克劳林级数

    - 求解$e^{x^2}$的麦克劳林级数
        $$
        \begin{align*}
        & 根据e^x = \sum_{n=0}^{\infty}\frac 1 {n!}x^n = 1 + x + \frac 1 {2!}x^2 + \frac 1 {3!}x^3 + \frac 1 {4!}x^4 + \dots \\
        & 将x替换为x^2\\
        & e^{x^2} = \sum_{n=0}^{\infty}\frac 1 {n!}x^{2n} = 1 + x^2 + \frac 1 {2!}x^4 + \frac 1 {3!}x^6 + \frac 1 {4!}x^8 + \dots 
        \end{align*}
        $$

    - 求解$\frac 1 {1 + x^2}$的麦克劳林级数
        $$
        \begin{align*}
        & 根据\frac 1 {1-x} = \sum_{n=0}^{\infty}x^n = 1 + x + x^2 + x^3 + \dots \\
        & 将x换为-x^2可得\\
        & \frac 1 {1+x^2} = \sum_{n=0}^{\infty}(-1)^nx^{2n} = 1 - x^2 + x^4 - x^6 + \dots \\
        \end{align*}
        $$
        

- 使用$x-a$代换$x$：麦克劳林级数生成新的泰勒级数

    > 在$f(x)$的麦克劳林级数中，使用$x-a$代换$x$，可以得到$f(x-a)$的，关于$x=a$的泰勒级数

    -  求解$ln(x)$在$x=1$处的泰勒级数
        $$
        \begin{align*}
        & 考虑ln(x) = ln(1 + x-1)，已知ln(1+x) = \sum_{n=1}^{\infty}-\frac {(-1)^n} {n}x^n = x - \frac 1 2 x^2 + \frac 1 3 x^3 - \frac 1 4 x^4 + \dots \\
        & 将x换成x-1，则有ln(1+x-1) = ln(x) = \sum_{n=1}^{\infty}-\frac {(-1)^n} {n}(x-1)^n = (x-1) - \frac 1 2 (x-1)^2 + \frac 1 3 (x-1)^3 - \frac 1 4 (x-1)^4 + \dots
        \end{align*}
        $$

    - 求解$ln(x)$在$x=2$处的泰勒级数
        $$
        \begin{align*}
        & 考虑ln(x)=ln(2 + x - 2)=ln(2(1 + \frac {x - 2} {2}))=ln(2) + ln(1 + \frac {x - 2} {2})\\
        & 结合ln(1+x) = \sum_{n=1}^{\infty}-\frac {(-1)^n} {n}x^n，并令x= \frac {x - 2} {2}，则有\\
        & ln(x)在x=2的泰勒级数\\
        & ln(2) + \sum_{n=1}^{\infty}-\frac {(-1)^n} {n}(\frac {x - 2} {2})^n=ln(2) + \sum_{n=1}^{\infty}-\frac {(-1)^n} {n2^n}(x-2)^n
        \end{align*}
        $$

## 2.2 泰勒级数求导

## 2.3 泰勒级数求积分

## 2.4 泰勒级数加减乘除

# 3. 利用幂级数和泰勒级数求导

# 4. 利用麦克劳林级数求极限



