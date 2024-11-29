# 1. 用其他函数的积分来表示的函数

积分$\int_a^bf(x)dx$中的$x$只是一个虚拟变量，可以替换为其他的$s、t$等虚拟变量，如果让==积分上限==变为一个自变量，则得到了一个新的函数，该函数是以积分来表示的，此时积分中应该将虚拟变量$x$替换为其他的虚拟变量

>  $\displaystyle F(x) = \int_a^xf(t)dt$

- 函数$F(x)$所表达的含义

    ![image-20241129142221076](<chap 17 微积分基本定理.assets/image-20241129142221076.png>)

# 2. 微积分基本定理

## 2.1 第一基本定理

> 如果函数$f$在==闭区间$==[a, b]$上==连续==，定义$F$为
>
> ​	$F(x) = \displaystyle \int_a^xf(t)dt  \;\; x \in [a, b] $
>
> 则$F$在==开区间==$(a, b)$内==可导==，且$F^{\prime}(x) = f(x)$

### 2.1.1 使用微积分第一基本定理对积分求导

- 基本情况 - 对==变量在积分上限==的积分表达式进行求导

    - $\displaystyle \frac d {dx} \int_a^xf(t)dt$
    - 关键： ==将被积函数内的自变量替换为$x$即可==，不需要考虑积分下限的常数，也即不需考虑$a$，但前提是$a$必须是一个常数
    - 例
        - $\displaystyle \frac d {dz} \int_{-e}^{z}2^{cos(w^2ln(w+5))}dw = 2^{cos(z^2ln(z+5))}$

- 变形1 - 变量在积分下限

    - $\displaystyle \frac d {dx} \int_x^af(t)dt$
    - 关键：根据定积分性质，==交换积分上下限==，积分值为原积分的相反数，再将负号放到积分外，根据基本情况求解即可
    - 例
        - $\displaystyle \frac d {dx} \int_x^7 t^3cos(tln(t))dt = - x^3cos(xln(x))$

- 变形2 - 积分上限是一个函数

    - $\displaystyle \frac d {dx} \int_a^{g(x)}f(t)dt$
    - 关键：基于==链式求导法则==，令$u=g(x)$，$y=\int_a^{g(x)}f(t)dt$，则$\displaystyle \frac {dy}{dx} = \frac {dy}{du} \frac {du}{dx}$
        - $\frac {dy} {du}$表示于将$g(x)$直接带入被积函数中
        - $\frac {du} {dx}$表示对$g(x)$求导
    - 如果积分下限是函数，交换积分上下限并取反，其余正常解析即可
    - 例：
        - $\displaystyle \frac d {dq} \int_4^{sin(q)} tan(cos(a))da$
            - 令$y=\int_4^{sin(q)} tan(cos(a))da$，$u=sin(q)$
            - 则$\displaystyle \frac {dy} {dx} = \frac {dy}{du} \frac {du}{dx}$ 
                - $\displaystyle \frac {dy}{du} = tan(cos(u))=tan(cos(sin(q)))$
                - $\displaystyle \frac {du} {dx} = cos(q)$
            - 所以，$\displaystyle \frac d {dq} \int_4^{sin(q)} tan(cos(a))da = tan(cos(sin(q)))cos(q)$

- 变形3 - 积分上下限都为函数

    - $\displaystyle \frac d {dx} \int_{h(x)}^{g(x)}f(t)dt$

    - 关键：选择一个常数，将积分上下限拆开，将一个积分求导拆为两个积分和求导

    - 例：

        - $\displaystyle \frac d {dx} \int_{x^5}^{x^6}ln(t^2-sin(t)+7)dt$

            - $$
                \displaystyle
                \begin{aligned}
                =& \frac d {dx} \bigg(\int_{x^5}^0ln(t^2-sin(t)+7)dt + \int_0^{x^6}ln(t^2-sin(t)+7)dt\bigg)\\
                =& -\frac d {dx}\bigg(\int_0^{x^5}ln(t^2-sin(t)+7)dt\bigg) + \frac d {dx}\bigg(\int_0^{x^6}ln(t^2-sin(t)+7)dt\bigg)\\
                =& -5x^4(ln(x^{10}-sin(x^5)+7)) + 6x^5(ln(x^{12}-sin(x^6)+7))\\
                \end{aligned}
                $$

- 变形4 - 伪装成极限的导数

    - $\displaystyle \lim_{h \to 0} \frac 1 h \int_x^{x+h}f(t)dt$

    - 关键：极限表达式其实就是$F(x)$($f$的反导数)在$x$的导数

        - 令$F(x) = \int_a^xf(t)dt$

        - 则有

            - $$
                \displaystyle
                \begin{aligned} \\
                &F(x+h) - F(x)  \\ 
                = & \int_a^{x+h}f(t)dt - \int_a^xf(t)dt \\
                = & \int_a^xf(t)dt + \int_x^{x+h}f(t)dt - \int_a^xf(t)dt \\
                = & \int_x^{x+h}f(t)dt \\
                & 所以有： \lim_{h \to 0} \frac 1 h \int_x^{x+h}f(t)dt \\
                & = \lim_{h \to 0}\frac {F(x+h) - F(x)} h \\
                & = F^{\prime}(x) \\
                & = f(x) \\
                \end{aligned} \\
                $$

    - 例

        - $\displaystyle \lim_{h \to 0}\frac 1 h \int_x^{x+h}log_3(cos^6(t) + 2)dt $

            $=log_3(cos^6(x) + 2)$

##  2.2 第二基本定理

> 如果函数$f$在闭区间$[a, b]$上是连续的，$F$为$f$的任意一个关于$x$的反导数，也即原函数，则有
>
> $\displaystyle \int_a^bf(x)dx = F(b) - F(a) $
>
> 或记为
>
> $\displaystyle \left. \int_a^bf(x)dx = f(x) \right |_a^b $

### 2.2.1 不定积分

- 不定积分，在积分符号中没有上下限，形如$\int f(x)dx$，表示的是$f(x)$的所有反导数的集合，这些反导数之间的差异只体现在常数项不同

- 定积分是有上下限的，形如$\int_a^bf(x)dx$，表示的是具体的一个数值，图像上来看，是$y=f(x)$，$x=a$，$x=b$以及$x$轴所谓成的图形的面积

- 不定积分

    > 如果$\frac d {dx}F(x) = f(x)，则有不定积分$$\displaystyle \int f(x)dx = F(x) + C $

- 不定积分性质

    - 函数和差的不定积分，等于不定积分的和差

        > $\displaystyle \int (f(x) \pm g(x))dx = \int f(x)dx \pm  \int g(x)dx$

    - 常数倍函数的不定积分，等于常数倍的不定积分

        > $\displaystyle \int cf(x)dx = c \int f(x)dx$

### 2.2.2 使用微积分第二基本定理计算定积分

计算定积分，通常==先==根据对应的不定积分，==求出被积函数的反导数==函数(是否带有常数项都可)，再将积分上下限带入反导数，计算$F(b) - F(a)$

- 常见不定积分

    - $\displaystyle \int x^a dx = \frac {x^{a+1}} {a+1} + C\;\;a \neq -1$

    - $\displaystyle \int \frac 1 xdx = ln(|x|) + C$

    - $\displaystyle \int e^x dx = e^x + C $

    - $\displaystyle \int b^x dx = \frac {b^x} {ln(b)} + C$

    - $\displaystyle \int cos(x) dx = sin(x) + C$

    - $\displaystyle \int sin(x) dx = -cos(x) + C $

    - $\displaystyle \int sec^2(x) dx = tan(x) + C $

    - $\displaystyle \int sec(x)tan(x) dx = sec(x) + C $

    - $\displaystyle \int csc^2(x) dx = -cot(x) + C $

    - $\displaystyle \int csc(x)cot(x) dx = -csc(x) + C $

    - $\displaystyle \int \frac 1 {\sqrt{1-x^2}} dx = sin^{-1}(x) + C $

    - $\displaystyle \int \frac 1 {1+x^2} dx = tan^{-1}(x) + C $

    - $\displaystyle \int \frac 1 {|x|\sqrt{x^2 - 1}} dx = sec^{-1}(x) + C $

    - $\displaystyle \int cosh(x) dx = sinh(x) + C$

    - $\displaystyle \int sinh(x) dx = cosh(x) + C $

- 如果$x$的系数不是$1$，暂记为$a$，则求不定积分时需要将不定积分乘以$\frac 1 a$

- 计算定积分

    - $\displaystyle \int_{-1}^2 x^4dx$
    - $\displaystyle \int_{-e^2}^{-1} \frac 4 x dx$
    - $\displaystyle \int_0^{\pi/3} \big(sec^2(x)-5sin(\frac x 2)\big) dx$
    - $\displaystyle \int_4^9 \frac 1 {x\sqrt{x}} dx$
    - $\displaystyle \int_0^{1/6} \frac 1 {\sqrt{1-9x^2}} dx$



 