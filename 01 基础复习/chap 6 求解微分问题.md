# 1. 根据定义求导

导数的定义如下：

> $f^{\prime}(x) = \frac {dy} {dx} = \displaystyle \lim_{\Delta x \to 0} \frac {f(x+\Delta x) - f(x)} {\Delta x}$

那么一般情况下可以根据导数定义进行导函数的求解

需要注意的是，当$\Delta x \to 0$时，带入定义后可能出现不定式，也即*出现$\frac 0 0$或$\frac c 0　c \neq 0$的场景，此时不能简单的将$\Delta x$消掉*

- 例，求$f(x) = \sqrt x + x^2$的导数

- 解

    <img src="chap 6 求解微分问题.assets/b122706155293b46801df1537c3b4b5.jpg" alt="b122706155293b46801df1537c3b4b5" style="zoom:33%;" />

    

# 2. 更好的求导方法

## 2.1 函数的常数倍的导数

常数倍函数的导数，是指形如$f(x)=C g(x)　Ｃ为常数$的函数

> $f(x)=Cg(x)$的导数为$f{\prime} = Cg^{\prime}$

## 2.2 函数和与函数差的导数

> $f(x) = u(x) + v(x)$的导数为$f^{\prime} = u^{\prime} + v^{\prime}$
>
> $f(x) = u(x) - v(x)$的导数为$f^{\prime} = u^{\prime} - v^{\prime}$

## 2.3 根据乘积法则求积函数的导数

- 乘积法则 - 以函数形式体现

    > 设$f(x) = h(x)g(x)$，则
    >
    > ​	$f^{\prime} = h^{\prime}(x)g(x) + f(x)g^{\prime}(x)$

- 乘积法则 - 以$dx$形式体现

    > 设$y=uv$，$u$和$v$是关于$x$的函数，则
    >
    > ​	<font size=4>$\frac y x = \frac {du} {dx}v + u\frac {dv} {dx}$</font>

- 如果函数乘积多于两个，速记方法，以$dx$形式体现

    > 乘积出现几次，就将乘积相加几次，然后逐个替换乘积中的函数为其导数

    - 例子

        - 设$y = uvw$，$u$$v$$w$是关于$x$的函数，则

            <font size=4>$\frac {dy} {dx} = \frac {du} {dx} vw + u\frac {dv} {dx} w + uv\frac {dw} {dx} $</font>

## 2.4 根据商法则求商函数的导数

- 商法则 - 以函数形式体现

    > 设<font size =3>$f(x) = \frac {h(x)} {g(x)}$</font>，则
    >
    > ​	<font size =4>$f^{\prime} = \frac {h^{\prime}(x)g(x) - f(x)g^{\prime}(x)} {(g(x))^2}$</font>

- 商法则 - 以$dx$形式体现

    > 设$y=\frac u v$，$u$和$v$是关于$x$的函数，则
    >
    > ​	<font size = 5>$\frac {dy} {dx} = \frac {\frac {du} {dx} v - \frac {dv} {dx} u} {v^2}$</font>

## 2.5 通过链式求导法则求复合函数的导数

- 链式求导法则 - 以函数形式体现

    > 设$f(x) = h(g(x))$， 则
    >
    > ​	$f^{\prime} = h^{\prime}(g(x)g^{\prime}(x)$

- 链式求导法则 - 以$dx$形式体现

    > 设$y$是$u$的函数，$u$是$x$的函数，则
    >
    > ​	<font size=5>$\frac {dy} {dx} = \frac {dy} {du} \frac {du} {dx}$</font>

- 链式求导法则可以看成按照函数复合的逆方向进行逐个求导并乘积，外层求导时内部函数不变

    - 例 求函数$y = \sqrt {x^3 -7x}$的导数

        ![image-20241114141935224](<chap 6 求解微分问题.assets/image-20241114141935224.png>)

## 2.6 复杂函数求导例题

- 函数<font size =5>$f(x) = \frac {3x^7 + x^4 \sqrt {2x^5 +15x^{4/3} -23x +9}} {6x^2 -4}$</font>的导数

    解：<img src="chap 6 求解微分问题.assets/79d3a5f68a448d8398852d01377673e.jpg" alt="79d3a5f68a448d8398852d01377673e" style="zoom: 33%;" />

# 3. 求解切线方程

1. 先求解出给定函数的导函数，带入给定的点，计算出斜率
2. 再根据给定的点和函数，算出切线上的点
3. 根据切线过的点和斜率，即可算出切线方程

# 4. 分段函数的导数

> 检验分段函数在分段点上，以及如果包含绝对值，要考虑绝对值中分段的点，是否可导，需要做以下校验：
>
> - 分段函数在检验点上是否相等 $\Rightarrow$ 验证连续性
> - 分段函数的导数在检验点上是否相等 $\Rightarrow$ 验证可导性

- 例  判断如下函数在分段点上是否可导

    <font size=4>$ y= \begin{cases} |x^2 - 4|\quad &x\leq 1\\ -2x + 5 \quad &x>0 \end{cases}$</font>

- 解<img src="chap 6 求解微分问题.assets/dfcc1455246ac58451fe2fe0f21560c.jpg" alt="dfcc1455246ac58451fe2fe0f21560c" style="zoom:33%;" />

    



