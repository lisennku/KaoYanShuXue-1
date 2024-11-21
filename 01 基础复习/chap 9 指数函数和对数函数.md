# 1. 基础知识

## 1.1 指数函数

> 形如$f(x) = a^x　a > 0$的函数被称为指数函数

- 指数函数法则：

    - $a^0 = 1$

    - $a^1 = a$

    - $a^xa^y = a^{x+y}$

    - $\frac {a^x} {a^y} = a^{x-y}$

    - $(a^x)^y = a^{xy}$

- 指数函数图像 恒在$x$轴上方

    - 当$a > 1$时
        - <img src="chap 9 指数函数和对数函数.assets/image-20241121093513247.png" alt="image-20241121093513247" style="zoom:50%;" />
    - 当$a = 1$时
        - 恒为$y=1$
    - 当$0 < a < 1$时
        - <img src="chap 9 指数函数和对数函数.assets/image-20241121093540036.png" alt="image-20241121093540036" style="zoom: 57%;" />

## 1.2 对数函数

> 形如$f(x) = log_a(x)　a > 0 且 a \ne 1, x > 0$的函数称为对数函数

- 对数函数法则：

    - $log_a(1) = 0$

    - $log_a(a) = 1$

    - $log_a(xy) = log_a(a) + log_a(b)$

    - $log_a(x/y) = log_a(x) - log_a(y)$

    - $log_a(x^y) = ylog_a(x)$

    - <font size = 4>$log_a(x) = \frac {log_c(x)} {log_c(a)}$</font>

- 对数函数图像 恒在$y$轴右侧

    - 当$a > 1$时
        - <img src="chap 9 指数函数和对数函数.assets/image-20241121093619639.png" alt="image-20241121093619639" style="zoom:50%;" />
    - 当$0 < a < 1$时
        - <img src="chap 9 指数函数和对数函数.assets/image-20241121093648453.png" alt="image-20241121093648453" style="zoom:50%;" />

# 2. 关于自然底数$e$的两个重要极限

> - <font size = 4>$\displaystyle \lim_{n \to \infty} (1 + \frac x n)^{n} = e^x$</font>
>
> - <font size = 4>$\displaystyle \lim_{h \to 0}(1 + hx)^{\frac 1 h} = e^x$</font>



# 3. 对数函数和指数函数求导

> <font size=4>$f(x)=log_a(x)$</font>的导数为<font size=4>$\frac 1 {xln(a)}$</font>
>
> <font size=4>$f(x)=a^x$</font>的导数为<font size=4>$a^xln(a)$</font>

<img src="chap 9 指数函数和对数函数.assets/image-20241120153256636.png" alt="image-20241120153256636" style="zoom:70%;" />

- 例， 求$y=e^{x^2}log_3(5^x-sin(x))$的导数

    <img src="chap 9 指数函数和对数函数.assets/image-20241120162027368.png" alt="image-20241120162027368" style="zoom: 50%;" />

# 4. 对数函数和指数函数的极限

## 4.1 指数函数

### 4.1.1 指数趋于0时的极限

>  指数函数$a^x$当$x$趋近于0时，函数极限为1，也即$\displaystyle \lim_{x \to 0} a^x = 1$

>  需要注意的时，类似三角函数判断是大数还是小数一样，不能单纯的依靠$x \to 0$或$x \to \infty$来判断指数趋近于0，而是要依靠==指数的表达式的结果==

因此当指数函数==本身作为乘法或除法的因子==时，可利用该极限进行拆分以便于计算

但是当指数函数作为加减项时，则一般情况下无法拆分，可考虑其他方法

- 重要极限：

    - > $\displaystyle \lim_{x \to 0}\frac {a^x - 1} x = ln(a)$
        >
        > 特别的，如果$a = e$，则有
        >
        > $\displaystyle \lim_{x \to 0}\frac {e^x - 1} x = 1$

    - 证明

        <img src="chap 9 指数函数和对数函数.assets/image-20241121100147532.png" alt="image-20241121100147532" style="zoom: 67%;" />

### 4.1.2 指数趋于$\pm \infty$的极限

- $x \to \infty$

    $\displaystyle \lim_{x \to \infty} r^x = \begin{cases}  \infty & \ r > 1\\ 1 & \ r = 1 \\ 0 &  0 \le r < 1  \end{cases} $

- $x \to -\infty$

    $\displaystyle \lim_{x \to -\infty} r^x = \begin{cases}  0 & \ r > 1\\ 1 & \ r = 1 \\ 0 &  \infty \le r < 1  \end{cases} $

### 4.1.3 指数函数与$x^n$在无穷位置的增长率

- 结论1：
    - 不论$n$有多大，指数函数的趋于无穷的速度都快于多项式函数，也即形如$x^n$的函数

- 结论2：
    - 不论$n$有多大，$\displaystyle \lim_{x \to \infty} \frac {x^n} {a^x} = 0$

- 结论3：
    - $\displaystyle \lim_{x \to \infty} \frac {多项式函数} {指数为正的 大的多项式型的指数函数} = 0$

## 4.2 对数函数 *以下对数函数的底数默认大于1*

### 4.2.1 对数函数在1附近的极限

> $\displaystyle \lim_{x \to 0} \frac {log_a(x + 1)} x = \frac 1 {ln(a)}$
>
> 特别的，如果$a = e$，则有
>
> $\displaystyle \lim_{x \to 0} \frac {ln(x + 1)} x = 1$
>
> > 证明关键点在于 1) $log_a(1) = 0$ 2) 求极限实际为求导数

### 4.2.2 对数函数在无穷附近的极限

> $\displaystyle \lim_{x \to \infty}log_ax = \infty$

因为对数函数在$y$轴右侧，所以不需要考虑$-\infty$的情况

### 4.2.3 函数与$x^n$在无穷位置的增长率

- 结论1：
    - 无论$a$有多小，只要$a > 0$，对数函数趋于无穷的速度都要慢于$x^a$
- 结论2：
    - 无论$a$有多小，都有 $\displaystyle  \lim_{x \to \infty} \frac {log_c(x)} {x^a} = 0$
- 结论3： 
    - 无论$a$有多小，都有 $\displaystyle \lim_{x \to \infty} \frac {任何正的多项式型的对数函数} {具有正次幂的多项式型} = 0$

### 4.2.4 对数函数在0附近的极限

- 结论
    - 对数函数在0附近的增长率较慢，无论$a$有多小，只要$a > 0$，都有 $\displaystyle \lim_{x \to 0^+} x^aln(x) = 0$
    - 也即，无论$a$有多小，都有 $\displaystyle \lim_{x \to 0^+} (任何真数趋于0的对数函数) (具有正次幂的非常小的多项式型) = 0$

## 5. 取对数求导法

取对数求导，是指针对于形如$y=f(x)^{g(x)}$的函数，或者，涉及到幂函数和指数函数的积和商的函数，进行求导，基本步骤为：

1. 对等式两边进行取(自然)对数，这样指数位置的$g(x)$可以移下来
2. 对等号两边进行隐函数求导，左边的结果总是$\frac 1 y \frac {dy} {dx}$，右边则是乘积法则，或链式求导法则
3. 对等号两边同时乘以$y$，得到单独的$\frac {dy} {dx}$，并用原始的$f(x)^{g(x)}$替换$y$

- 例1，求$\frac {d((1 + x^2)^{\frac 1 {x^3}})} {dx}$

    <img src="chap 9 指数函数和对数函数.assets/image-20241121135422819.png" alt="image-20241121135422819" style="zoom:50%;" />

- 例2，若<font size=4>$y = \frac {(x^2-3)^{100}3^{sec(x)}} {2x^5(log_7(x) - cot(x))^9}$</font>，求<font size=4>$\frac {dy} {dx}$</font>

    <img src="chap 9 指数函数和对数函数.assets/image-20241121140953936.png" alt="image-20241121140953936" style="zoom:67%;" />


# 5. 双曲函数

- 双曲函数

    - 正弦双曲函数
        - $sinh(x) = \frac {e^x - e^{-x}} 2$
    - 余弦双曲函数
        - $cosh(x) = \frac {e^x + e^{-x}} 2$
    - 正割双曲函数
        - $sech(x) = \frac 2 {e^x + e^{-x}} $
    - 余割双曲函数
        - $csch(x) = \frac 2 {e^x - e^{-x}}$
    - 正切双曲函数
        - $tanh(x) = \frac {e^x - e^{-x}} {e^x + e^{-x}}$
    - 余切双曲函数
        - $coth(x) = \frac {e^x + e^{-x}} {e^x - e^{-x}}$

- 双曲函数等式

    - $cosh^2(x) - sinh^2(x) = 1$
    - $1 - tanh^2(x) = sech^2(x)$

- 双曲函数导数

    - 正弦双曲函数

        - $\frac d {dx}sinh(x) = cosh(x)$

    - 余弦双曲函数

        - $\frac d {dx}cosh(x) = sinh(x)$

    - 正割双曲函数

        - $\frac d {dx}sech(x) = -sech(x)tanh(x)$

    - 余割双曲函数

        - $\frac d {dx}csch(x) = -csch(x)coth(x)$

    - 正切双曲函数

        - $\frac d {dx}tanh(x) = sech^2(x)$

    - 余切双曲函数

        - $ \frac d {dx}coth(x)=-csch^2(x)$

    - 证明过程

        <img src="chap 9 指数函数和对数函数.assets/cfba1b61d6436cbb565b13095929ec01.jpg" alt="cfba1b61d6436cbb565b13095929ec01" style="zoom: 33%;" />

- 双曲函数图像

    - 正弦双曲函数
        - <img src="chap 9 指数函数和对数函数.assets/image-20241121153104420.png" alt="image-20241121153104420" style="zoom:50%;" />
    - 余弦双曲函数
        - <img src="chap 9 指数函数和对数函数.assets/image-20241121153044695.png" alt="image-20241121153044695" style="zoom:50%;" />
    - 正割双曲函数
        - ![image-20241121153158098](<chap 9 指数函数和对数函数.assets/image-20241121153158098.png>)
    - 余割双曲函数
        - ![image-20241121153209921](<chap 9 指数函数和对数函数.assets/image-20241121153209921.png>)
    - 正切双曲函数
        - ![image-20241121153128904](<chap 9 指数函数和对数函数.assets/image-20241121153128904.png>)
    - 余切双曲函数
        - ![image-20241121153146106](<chap 9 指数函数和对数函数.assets/image-20241121153146106.png>)
