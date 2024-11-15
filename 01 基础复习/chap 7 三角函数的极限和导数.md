# 1. 三角函数的极限

对于三角函数求极限，需要判断是在非常小的数上==取==三角函数，如，$\displaystyle \lim_{x \to 0}\frac {sin(5x)} x$，还是在非常大的数上==取==三角函数，如，$\displaystyle \lim_{x \to \infty}\frac {sin(5x)} x$

> 需要注意的是，非常大和非常小是==相对于三角函数里的数字==而言，并不能依靠$x \to 0$,$x \to \infty$来简单判断是非常小或非常大
>
> 如：
>
> $\displaystyle \lim_{x \to 0}xsin(\frac 5 x)$ 当$x \to 0$时，$sin$内是非常大的数
>
> $\displaystyle \lim_{x \to \infty}xsin(\frac 5 x)$ 当$x \to \infty$时，$sin$内是非常小的数

## 1.1 小数的情况

> 重要极限(红色)：
>
> <font color=red>$\displaystyle \lim_{x \to 0} \frac {sin(x)} x = 1$</font> $\qquad$ $\displaystyle \lim_{x \to 0} sin(x) = 0$
>
> <font color=red>$\displaystyle \lim_{x \to 0} \frac {tan(x)} x = 1$</font> $\qquad$ $\displaystyle \lim_{x \to 0} tax(x) = 0$
>
> $\displaystyle \lim_{x \to 0} \frac {cos(x)} x = DNF$ $\qquad$ <font color=red>$\displaystyle \lim_{x \to 0} cos(x)= 1$</font>
>
> <font color=red>$\displaystyle \lim_{x \to 0} \frac {1-cos(x)} x = 0$</font> $\qquad$ $\displaystyle \lim_{x \to 0} \frac {1-cos(x)} {x^2} = 1/2$       

### 1.1.1 $\displaystyle \lim_{x \to 0} \frac {sin(x)} x = 1$

- 说明了一个重要的情况，虽然当$x \to 0$时，$sin(x)$和$x$都趋近于0，但是两者趋近程度是类似的，所以虽然$\frac {sin(x)} x$不等于1，但其极限值为1

    > 当$x$非常小时，$sin(x)$表现的就像$x$，==这个情况只在乘积或商的情形下才成立==
    >
    > - 对于$x+sin(x)$或$x-sin(x)$时不能认为两者相等然后认为表达式为0

- 证明

    以半径为1绘制圆，取圆心角为$x$，以弧度计量，延长OA，并做点B的切线，与延长线相交于D，过A做垂直于OB的垂线，垂足为C

    前置知识点：

    > $S_{扇} = \frac x {2\pi} \pi r^2 = \frac {xr^2} 2$

    ![image-20241115093813482](<chap 7 三角函数的极限和导数.assets/image-20241115093813482.png>)

    <img src="chap 7 三角函数的极限和导数.assets/3175e91dc933637a718bb293c4cb9e6.jpg" alt="3175e91dc933637a718bb293c4cb9e6" style="zoom:33%;" />

- 重要不等式

    > $sin(x) < x < tan(x)$

### 1.1.2 $\displaystyle \lim_{x \to 0} \frac {tan(x)} x = 1$

- 证明

    <img src="chap 7 三角函数的极限和导数.assets/image-20241115102429521.png" alt="image-20241115102429521" style="zoom:50%;" />

### 1.1.3 $\displaystyle \lim_{x \to 0} \frac {1-cos(x)} x = 0$

- 证明

    <img src="chap 7 三角函数的极限和导数.assets/image-20241115102452172.png" alt="image-20241115102452172" style="zoom:50%;" />

## 1.2 大数情况

- 对于大数情况，要考虑三角函数所处的位置

    - 如果在多项式中，仅仅是==加减==一个$sin(x)$或$cos(x)$，可以看做他们比$x$的==任意正次幂次==数要低，可以忽略并按照多项式的方法求解极限，唯一的例外是如果多项式中其他的最高次幂是0的时候
    - 如果在多项式中，$sin(x)$或$cos(x)$是$x$的系数，那么此时三角函数非常重要，一般通过==夹逼定理==进行极限的求取

- > 一般性原理，对于任意的==正==指数$\alpha$，有
    >
    > $\displaystyle \lim_{x \to \infty} \frac {sin(任何东西)} {x^{\alpha}} = 0$
    >
    > $\displaystyle \lim_{x \to \infty} \frac {cos(任何东西)} {x^{\alpha}} = 0$

- 求$\displaystyle \lim_{x \to \infty} x sin(\frac 5 x)$的极限

    <img src="chap 7 三角函数的极限和导数.assets/image-20241115112956969.png" alt="image-20241115112956969" style="zoom:50%;" />

## 1.3 其他情况

前面提到的都是$x \to 0$或$x \to \infty$的情况，那么如果是其他情况，要怎么计算三角函数的极限呢

> 一般采取==换元法==
>
> 也即，如果是$x \to \frac {\pi} 2$，那么令$t = x - \frac {\pi} 2$，则可以从$x$趋近于$\frac {\pi} 2$，改为$t$趋近于$0$
>
> 然后再结合==三角恒等式==进行计算

# 2. 三角函数的导数

## 2.1 三角函数的导数

### 2.1.1 导数

- $f(x) = sin(x)$的导数

    > $f^{\prime} = cos(x)$ 

- $f(x) = cos(x)$的导数

    > $f^{\prime} = -sin(x)$

- $f(x) = tan(x)$的导数

    > $f^{\prime} = sec^2(x) = \frac 1 {cos^2(x)}$

- $f(x) = sec(x)$的导数

    > $f^{\prime} = sec(x)tan(x) = \frac 1 {cos(x)}tan(x) = \frac {sin(x)} {cos^2(x)}$ 

- $f(x) = csc(x)$的导数

    > $f^{\prime} = -csc(x)cot(x) = - \frac {1} {sin(x)} cot(x) = - \frac {cos(x)} {sin^2(x)}$

- $f(x) = cot(x)$的导数

    > $f^{\prime} = -csc^2(x) = - \frac 1 {sin^2(x)}$

### 2.1.2 证明

- $f(x) = sin(x)$

    <img src="chap 7 三角函数的极限和导数.assets/image-20241115141828125.png" alt="image-20241115141828125" style="zoom:50%;" />

- $f(x) = cos(x)$

    <img src="chap 7 三角函数的极限和导数.assets/image-20241115141922796.png" alt="image-20241115141922796" style="zoom: 50%;" />

- $f(x) = tan(x)$

    <img src="chap 7 三角函数的极限和导数.assets/image-20241115143037280.png" alt="image-20241115143037280" style="zoom:80%;" />

- $f(x) = sec(x)$

    <img src="chap 7 三角函数的极限和导数.assets/image-20241115143106747.png" alt="image-20241115143106747" style="zoom:50%;" />

- $f(x) = csc(x)$

    <img src="chap 7 三角函数的极限和导数.assets/image-20241115143130248.png" alt="image-20241115143130248" style="zoom:50%;" />

- $f(x) = cot(x)$

    <img src="chap 7 三角函数的极限和导数.assets/image-20241115143307296.png" alt="image-20241115143307296" style="zoom:80%;" />