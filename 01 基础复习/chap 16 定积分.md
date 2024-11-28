# 1. 定积分定义及性质

## 1.1 定积分概念

> 形如$\displaystyle \int_a^bf(x)dx$的是定积分，表示的是==函数$f(x)$对$x$从$a$到$b$的积分==
>
> 从函数图像来看，是由曲线$y=f(x)$，两条垂线$x=a$，$x=b$和$x$轴围成的有向面积
>
> 有向指的是面积有正有负
>
> > $f(x)$为被积函数
> >
> > 垂线位置的$a$、$b$为积分端点
> >
> > $dx$表示的是对水平轴的积分

- 基本定积分计算

    - 线性函数定积分，也即$f(x)=kx+b$的定积分$\displaystyle \int_a^bf(x)dx$，可以通过三角形面积或者梯形面积计算

    - 常数定积分，也即$\displaystyle \int_a^bCdx$，其结果等于$C(b-a)$

    - 如果函数$f$为奇函数，则对称区间的积分为0，也即$\displaystyle \int_a^{-a}f(x)dx=0$

## 1.2 定积分定义

> ==黎曼积分==定义
>
> $\displaystyle \int_a^bf(x)dx = \lim_{mesh \to 0}\sum_{j=1}^nf(c_j)(x_j - x_{j-1})$

- 其中，

    - $\displaystyle \sum_{j=1}^n f(c_j)(x_j - x_{j-1})$称为黎曼和
    - $a = x_0<x_1 <\cdots<x_{n-1}<x_n=b $是对区间$[a, b]$的一个划分，基本采取等长划分

    - $mesh$表示的是最大区间的长度，也即$(x_1-x_0),(x_2-x_3)\cdots(x_n-x_{n-1})$中最大的值，如果是等长划分其实这些值都相等

    - $c_j$是区间$[x_{j-1}, x_j]$中的任意值
        - 如果$c_j$选择的是使函数$f(x)$在区间$[x_{j-1}, x_j]$取最大值的点，那么此时为黎曼和的上和
        - 如果$c_j$选择的是使函数$f(x)$在区间$[x_{j-1}, x_j]$取最小值的点，那么此时为黎曼和的下和

- 如果函数$f$是有界的，即使有有限个不连续的点，该函数也是可积的，如果有无穷多个不连续点，则不属于黎曼积分，属于勒贝格积分

- 如果函数$f$是无界的，也可能是可积的，因为可能存在一条垂直渐近线

### 1.2.1 使用定积分定义计算$\displaystyle \int_0^2 x^2dx$

<img src="chap 16 定积分.assets/image-20241128163720505.png" alt="image-20241128163720505" style="zoom:80%;" />

## 1.3 定积分性质

1. 调换积分上下限，其值为相反数

    $\displaystyle \int_a^bf(x)dx = - \displaystyle \int_b^af(x)dx$

2. 如果积分上下限相同，积分为0

​	$\displaystyle \int_a^af(x)dx = 0$

3. 对于任何可积函数$f$和常数$a、b、c$，有

​	$\displaystyle \int_a^bf(x)dx = \displaystyle \int_a^cf(x)dx + \displaystyle \int_c^bf(x)dx$

4. 常数可以移到积分表达式的外边

    $\displaystyle \int_a^bCf(x)dx = C\displaystyle \int_a^bf(x)dx$

5. 和或差的积分等于积分的和或差

    $\displaystyle \int_a^b(f(x) \pm g(x))dx = \displaystyle \int_a^bf(x)dx \pm \displaystyle \int_a^bg(x)dx$

# 2. 定积分求面积

## 2.1 求通常的面积

> 通常的面积指的是无向面积，也即不认为各个部分围成的在$x$轴下方的面积为负数，将其作为正数的面积
>
> 关键点在于找到被积函数与$x$轴的交点，也即求解$f(x) = 0$的，在积分区间内的所有解

- 基本步骤

    1. 找出被积函数在积分区间内，满足函数值为0的所有$x$的值
    2. 以原被积函数$f(x)$而非其绝对值形式进行分段积分，第一个分段从$a$到第一个使函数值为0的$x$值进行积分，第二个分段从第一个使函数值为0的$x$值到下一个进行积分，直到最后一个分段，从最后一个使函数值为0的$x$的值到$b$的积分
    3. 分别计算每个积分值
    4. 对积分值取绝对值并相加即可

- 例题

    - 计算$f(x) = -x^2 -2x + 3$的，在$x \in [0, 2]$的普通面积

        <img src="chap 16 定积分.assets/image-20241128171047908.png" alt="image-20241128171047908" style="zoom:67%;" />

## 2.2 求两条曲线之间的实际面积

> 两个函数$f$和$g$之间的面积为$\displaystyle \int_a^b |f(x)-g(x)|dx$

# 3. 积分的估算

> 如果对于在$[a, b]$区间内所有$x$都有$f(x) \leq g(x)$，则有$\displaystyle \int_a^bf(x)dx \leq \displaystyle \int_a^bg(x)dx$

> 如果对于在$[a, b]$区间内所有$x$都有$m \leq f(x) \leq M$，则有$\displaystyle m(b-a) \leq \displaystyle \int_a^bf(x)dx \leq M(b-a)$

# 4. 积分的平均值与积分中值定理

> 函数$f$在区间$[a, b]$内的平均值=$\frac 1 {b-a}\displaystyle \int_a^bf(x)dx$

> 积分中值定理
>
> 如果函数$f$在闭区间$[a, b]$上连续，那么在开区间$(a, b)$内总有一点$c$，满足$f(c) = \frac 1 {b-a}\displaystyle \int_a^bf(x)dx$

