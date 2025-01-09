# 1. 导数概念

## 1.1 导数定义

- 在某点可导的定义

    > 设函数$y=f(x)$在点$x_0$的某个邻域内有定义，当自变量$x$在$x_0$处获得增量$\Delta x$，$x+\Delta x$仍在定义域内。相应的，因变量$y$取得增量$\Delta y = f(x_0 + \Delta x) - f(x_0)$，==如果当$\Delta x$趋于$0$时，$\Delta y$与$\Delta x$之比的极限存在==，则称函数$y=f(x)$在$x_0$处可导，该极限值为函数$y=f(x)$在$x_0$处的导数，记为$f^{\prime}(x_0)$，或$y^{\prime}|_{x = x_0}$，或$\frac {dy} {dx}\big|_{x = x_0}$，或$\frac {df(x)} {dx}\big|_{x = x_0}$

    > 如果当$\Delta x$趋于$0$时，$\Delta y$与$\Delta x$之比的极限不存在，则称在$x_0$处不可导，如果极限不存在的原因是因为极限趋于无穷，也称函数在点$x_0$处的导数为无穷大

    > $f^{\prime}(x_0) = \displaystyle \lim_{\Delta x \to 0} \frac {f(x_0 + \Delta x) - f(x_0)} {\Delta x} $
    >
    > $f^{\prime}(x_0) = \displaystyle \lim_{h \to 0} \frac {f(x_0 + h) - f(x_0)} {h} $
    >
    > $f^{\prime}(x_0) = \displaystyle \lim_{x \to x_0} \frac {f(x) - f(x_0)} {x - x_0} $

- 在开区间可导的定义

    > 如果函数$y=f(x)$在开区间$I$内处处可导，则称函数$y=f(x)$在开区间$I$内可导
    >
    > 在此区间内的每一个$x$，都对应函数$f(x)$的一个导数值，这样构成了一个新函数，称为原函数的导函数，记为$f^{\prime}(x)$，或$y^{\prime}(x)$，或$\frac {dy} {dx}$，或$\frac {df(x)} {dx}$

    > $f^{\prime}(x) = \displaystyle \lim_{\Delta x \to 0} \frac {f(x+ \Delta x) - f(x)} {\Delta x} $
    >
    > $f^{\prime}(x) = \displaystyle \lim_{h \to 0} \frac {f(x+ h) - f(x)} {h} $

- 在闭区间可导的定义

    - 函数$f(x)$在$x_0$处可导的充要条件是

        > 左极限$\displaystyle \lim_{h \to 0^-} \frac {f(x_0 + h) - f(x_0)} {h}$和右极限$\displaystyle \lim_{h \to 0^+} \frac {f(x_0 + h) - f(x_0)} {h}$都存在且相等

        > 左右极限被称为左右导数，记作$f_-^{\prime}(x_0)$和$f_+^{\prime}(x_0)$

    > 如果函数$y=f(x)$在开区间$I$内处处可导，且左端点的右导数，和右端点的左导数都存在，则称函数$y=f(x)$在闭区间$I$上可导

## 1.2. 导数的几何意义

- 切线

    > 设曲线$C$及$C$上的一点$M$，在点$M$外，另取$C$上一点$N$，做割线$MN$，当点$N$沿着曲线$C$趋于点$M$时，如果割线$MN$绕点$M$旋转而趋于极限位置$MT$，则直线$MT$称为曲线$C$在点$M$处的切线

    > 极限位置的含义是，只要弦长$|MN|$趋近于0，$\angle NMT$也趋于0

    <img src="chap 2 导数与微分.assets/image-20250103162904721.png" alt="image-20250103162904721" />

- 坐标系下的切线

    > 设曲线$C$为$y=f(x)$，设$M(x_0, y_0)$是曲线上一点，另取$C$上一点$N(x, y)$，割线$MN$的斜率为$tan\varphi = \frac {y - y_0} {x - x_0} = \frac {f(x) - f(x_0)} {x - x_0}$，$\varphi$为割线$MN$的倾角
    >
    > 当点$N$沿着曲线$C$趋近于$M$时，$x \to x_0$
    >
    > 如果当$x \to x_0$时$tan\varphi$存在，设为$k$，即，$k = \displaystyle \lim_{x \to x_0}\frac {f(x) - f(x_0)} {x - x_0}$存在，则$k$是切线的斜率，此时$\varphi \to \alpha$，$\alpha$是切线的倾角

    <img src="chap 2 导数与微分.assets/image-20250103163351434.png" alt="image-20250103163351434" />

- 导数的几何意义

    > 函数$y=f(x)$在点$x_0$处的导数$f^{\prime}(x_0)$在几何上表示为曲线$y=f(x)$在点$M(x_0, y_0)$处切线的斜率，即$f^{\prime}(x_0) = tan\alpha$

    > 过切点$M(x_0, y_0)$且与切线垂直的直线，叫做曲线$y=f(x)$在点$M$处的法线，如果$f^{\prime}(x_0)$不为$0$，则法线的斜率为$-\frac {1} {f^{\prime}(x_0)}$

## 1.3. 可导性和连续性的关系

> 函数在某点可导，则必在该点连续
>
> 函数在某点连续，则未必在该点可导

在某点连续，需要三个条件： ①函数在该点有定义②当$x \to x_0$时函数极限存在③极限和函数值相等

在某点可导，充要条件是左右导数，也即左右极限，存在且相等

需要注意的是，二者中的极限形式不同

- 连续的极限，是$\displaystyle \lim_{x \to x_0}f(x)-f(x_0) = 0$
- 可导的极限，是$\displaystyle \lim_{x \to x_0}\frac {f(x) - f(x_0)} {x - x_0}$

# 2. 函数的求导法则

## 2.1 导数的四则运算

> 如果函数$u=u(x)$和$v=v(x)$在点$x$处均具有导数，则其和、差、积、商(分母为零的点除外)都在$x$处具有导数，且
>
> $[u(x) \pm v(x)]^{\prime} = u^{\prime}(x) \pm v^{\prime}(x)$
>
> $[u(x)\cdot v(x)]^{\prime}=u^{\prime}(x)v(x) + u(x)v^{\prime}(x)$
>
> $[\frac {u(x)} {v(x)}]^{\prime} = \frac {u^{\prime}(x)v(x) - u(x)v^{\prime}(x)}{v^2(x)}$

> 和差积运算可以推广到任意有限个可导函数的情形

## 2.2 反函数导数

> 如果函数$x = f(y)$在区间$I_y$内单调、可导且$f^{\prime}(y) \ne0$，那么它的反函数$y=f^{-1}(x)$在区间$I_x = {x|x=f(y), y \in I_y}$内也可导，且
>
> $[f^{-1}(x)]^{\prime} = \frac {1} {f^{\prime}(y)}$
>
> > 简单来说，反函数的导数是其原函数的导数的倒数，但原函数的导数是以$y$表示而非$x$	
>
> > 对于以$y=f(x)$方式给出的原函数，先以$x=f(y)$表示，然后求出$f^{\prime}(y)$，再以$y=f^{-1}(x)$的形式表示反函数，再按照公式写出$[f^{-1}(x)]^{\prime} = \frac {1} {f^{\prime}(y)}$，再找出$f^{\prime}(y)$和$x=f(y)$之间的关系，最终以$x$表示反函数的导数

<img src="chap 2 导数与微分.assets/febd88079afbea247774c74dc2cf74e2.jpg" alt="febd88079afbea247774c74dc2cf74e2" style="zoom: 25%;" />

## 2.3 复合函数的导数

> 如果函数$u=g(x)$在点$x$处可导，而函数$y=f(u)$在点$u=g(x)$处也可导，则复合函数$f[g(x)]$在点$x$处也可导，且其导数为
>
> $\frac {dy} {dx} = f^{\prime}(u) \cdot g^{\prime}(x)$，或，$\frac {dy} {dx} = \frac {dy}{du} \frac {du} {dx}$

# 3. 高阶导数

> 一般的，函数$f(x)$的导数$f^{\prime}(x)$仍是$x$的函数，则$f^{\prime}(x)$的导数称为函数$f(x)$的二阶导数，记作$f^{\prime\prime}(x)$或$\frac {d^2y}{dx^2}$

> 类似的，$n-1$阶导数的导数，称为$f(x)$的$n$阶导数，记作$f^{(n)}(x)$，或$\frac {d^ny} {dx^n}$

> 如果函数$f(x)$具有$n$阶导数，也称为函数$n$阶可导

- 常见函数的$n$阶导数
    - $[sin(x)]^{(n)} = sin(x + n \cdot \frac {\pi} {2})$
    - $[cos(x)]^{(n)} = cos(x + n \cdot \frac {\pi} {2})$
    - $[ln(1+x)]^{(n)} = (-1)^{n-1} \cdot \frac {(n-1)!} {(1+x)^n}$
    - $[x^{\mu}]^{(n)} = \mu(\mu-1)(\mu-2)\cdots (\mu-n+1)x^{\mu-n}$
- $n$阶导数的和、差、积
    - $(u \pm v)^{(n)} = u^{(n)} \pm v^{(n)}$
    - $(uv)^{(n)} = \displaystyle \sum_{k=0}^nC_n^ku^{(n-k)}v^{()}$


# 4. 隐函数 和 参数方程的导数

- 隐函数，相对于显函数而言

    > 显函数，可以使用一个带有自变量的表达式，来表示因变量
    >
    > 隐函数，使用一个方程来表示自变量/因变量之间的关系的函数

    > 隐函数求导方法
    >
    > ==对一切求关于$x$的导==，需要注意的是，涉及到$y$的求导，因其是关于$x$的函数，==所以需要使用使用链式求导法则，乘积求导法则以及商求导法则==，最终将求出$\frac {dy}{dx}$的表达式

- 参数方程

    > 一般的，若参数方程
    >
    > $\begin {cases}x = \varphi(t) \\ \\y=\psi(t) \end{cases}$
    >
    > 确定了$y$和$x$之间的函数关系，则称，此函数关系所表达的函数，是由参数方程所确定的函数

    - 求导
        - $\frac {dy} {dx} = \frac {\psi^{\prime}(t)} {\varphi^{\prime}(t)}$
        - $\frac {d^2y} {dx^2} = \frac {\psi^{\prime\prime}(t) \varphi^{\prime}(t) - \varphi^{\prime\prime}(t) \psi^{\prime}(t)} {\varphi^{\prime 3}(t)}$

# 5. 函数的微分

## 5.1 微分的概念

- 函数在某点的可微

    > 设函数$y=f(x)$在某区间内有定义，$x_0$及$x_0+\Delta x$都在该区间内，如果函数的增量
    >
    > $\Delta y = f(x_0+\Delta x) - f(x_0)$
    >
    > 可以表示为
    >
    > $\Delta y = A\Delta x +o(\Delta x)$，其中$A$是不依赖于$\Delta x$的常数，
    >
    > 那么称函数$y=f(x)$在点$x_0$是<u>**可微**</u>的，
    >
    > $A\Delta x$称为函数$y=f(x)$在点$x_0$相应于自变量增量$\Delta x$的微分，记作==$dy$==

- 在某点$x_0$可微的充分必要条件

    > 函数在点$x_0$可微的充要条件是，函数在点$x_0$可导

    > 如果函数在点$x_0$可微，那么该微分一定是$dy = f^{\prime}(x_0) \Delta x$

- $\Delta y$和$dy$的关系

    - 当$f^{\prime} \ne 0$，通过极限$\displaystyle \lim_{\Delta x \to 0} \frac {\Delta y} {dy} = \lim_{\Delta x \to 0} \frac {\Delta y} {f^{\prime}(x_0)\Delta x} = \frac {1} {f^{\prime}(x_0)} \cdot \lim_{\Delta x \to 0}\frac {\Delta y} {\Delta x} = 1$可知，==$\Delta y$和$dy$是等价无穷小==
    - 由等价无穷小的定理可知，==$\Delta y=dy + o(dy)$==，所以$dy$是$\Delta y$的主部，又因为$dy = f^{\prime}(x_0)\Delta x$，所以当$f^{\prime}(x_0) \ne 0$时，$dy$又称为$\Delta y$的线性主部
    - 当$f^{\prime}(x_0) \ne 0$时，若以微分$dy = f^{\prime}(x_0)\Delta x$代替增量$\Delta y=f(x_0+\Delta x) - f(x_0)$，其误差为$o(dy)$
        - 因此当$|\Delta x|$很小时，近似有$\Delta y \approx dy$

- 函数的微分

    - 函数$y=f(x)$在任意点的微分，称为函数的微分，记作$dy$或$df(x)$，有$dy = f^{\prime}(x) \Delta x$
    - 通常将自变量$x$的增量$\Delta x$称为自变量的微分，记作$dx$，因此函数的微分可记为$dy = f^{\prime}(x)dx$，也即$\frac {dy} {dx} = f^{\prime}(x)$

## 5.2 微分的几何意义

<img src="chap 2 导数与微分.assets/image-20250109134526435.png" alt="image-20250109134526435" style="float: left; margin-right: 10px;"/>

- 点$M$是曲线上顶点，坐标为$(x_0, y_0)$，当自变量$x$有微小增量$\Delta x$时，得到曲线上另外一点$N$，坐标为$(x_0+\Delta x, y_0+\Delta y)$
    - 故有，$MQ = \Delta x$，$NQ = \Delta y$
- 过点$M$做$MT$，其倾角为$\alpha$，则有$PQ = MQ \cdot tan(\alpha) = f^{\prime}(x_0) \cdot \Delta x = dy$
- 因此
    - 对于可微函数$y=f(x)$而言，当$\Delta y$是曲线$y=f(x)$上点的纵坐标增量时，$dy$是曲线切线上的点的纵坐标的相应增量
    - 当$|\Delta x|$很小时，$|\Delta y - dy|$比$|\Delta x|$小得多，因此点$M$附近可以使用切线段来近似代替曲线段

## 5.3 微分在近似计算中的应用

- 计算$\Delta y$
    - $\Delta y = f^{\prime}(x_0) \cdot \Delta x$
- 计算$f(x_0 + \Delta x)$
    - $f(x_0 + \Delta x) = f(x_0) + f^{\prime}(x_0) \cdot \Delta x$
- 计算$f(x)$
    - $f(x) \approx f(x_0) + f^{\prime}(x_0) (x - x_0)$

