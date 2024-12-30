#  1. 映射和函数

## 1.1 映射

- 映射

    > **设$X$、$Y$是两个非空集合，如果存在一个法则$f$，使得对$X$中每个元素$x$，按照法则$f$，在$Y$中有唯一确定的元素$y$与之对应，则称$f$为从$X$到$Y$的一个映射，记作：**
    >
    > **$f:X \to Y$**

    > - 其中：
    >
    >     - 元素$y$称为元素$x$在映射$f$下的==像==，记作$f(x)$，也即$y=f(x)$
    >
    >     - 元素$x$称为元素$y$在映射$f$下的==原像==
    >     - 集合$X$，集合$Y$，和映射法则$f$是构成映射的三大要素
    >
    > - 定义域：
    >     - 集合$X$称为映射$f$的定义域，记作$D_f$，也即$D_f=X$
    > - 值域：
    >     - *$X$中所有元素的像组成的集合*称为映射$f$的值域，记作$R_f$或$f(X)$
    >     - 也即，$R_f = f(X) = {f(x)| x\in X}$
    >     - 注意，$R_f \subset Y$，不一定$R_f=Y$
    > - 

- 映射的类型

    - 满射

        > 设$f$是从集合$X$到集合$Y$的一个映射，如果$R_f=Y$，也即，$Y$中任一个元素$y$都是$X$中某个元素的像，则称$f$是从$X$到$Y$==上==的映射，也称为==满射==

    - 单射

        > 设$f$是从集合$X$到集合$Y$的一个映射，若对集合$X$中任意两个不同元素$x_1 \neq x_2$，他们的像$f(x_1) \neq f(x_2)$，则称$f$为$X$到$Y$的==单射==

    - 双射

        > 若一个映射$f$即是单射，又是满射，则称为一一映射或==双射==

- 逆映射

    > 设$f$是$X$到$Y$的==单射==，则有定义可知，对于每个$y \in R_f$，有唯一的$x \in X$，适合$f(x) = y$，于是，可以定义一个新的映射$g$，即
    >
    > $g: R_f \to X$
    >
    > 对每个$y \in R_f$，规定$g(y)=x$，$x$瞒住$f(x)=y$，则新映射$g$称为$f$的逆映射，记作$f^{-1}$
    >
    > 定义域$D_{f^{-1}}=R_f$，值域$R_{f^{-1}}=X$
    >
    > - <u>只有单射才有逆映射，否则从$g(y)=x$可能出现多个$x$值，导致不符合映射定义</u>

- 复合映射

    > 设有两个映射，
    >
    > $g: X \to Y_1$，$f:Y_2 \to Z$，其中$Y_1 \subset Y_2$
    >
    > 则由映射$g\text{和}f$确定了一个从$X \to Z$的映射，该映射称为复合映射，表示将每个$x \in X$，映射为$f(g(x)) \in Z$
    >
    > 复合映射记为$f \circ g$，也即$f \circ g:X \to Z, \; (f \circ g)(x)=f(g(x)),\; x \in X$
    >
    > - 构成复合映射的条件：$\circ$符号右侧映射的值域，在符号左侧映射的定义域内
    > - 复合映射的书写顺序与映射实际顺序相反，即，如果是$f \circ g \circ h$，则先是映射$h(x)$，再是$g(h(x))$，最后是$f(g(h(x)))$

## 1.2 函数

1. 函数的定义

    > 设数集$D \subset R$，则称映射$f:D \to R$为定义在数集$D$上的==函数==，记为$y=f(x),\;x \in D$
    >
    > - $x$称为自变量，$y$称为因变量，$D$称为定义域，记为$D_f$，也即$D = D_f$
    > - 构成函数的要素：定义域$D_f$和对应法则$f$
    >     - 因为函数本身是从实数集映射到实数集的映射

    > 函数的定义中，每个$x \in D$，按照对应法则$f$，总有唯一确定的值$y$与$x$对应，这个值称为函数$f$在$x$处的函数值，记为$f(x)$，也即$y=f(x)$
    >
    > 函数值$f(x)$的全体所构成的集合称为函数$f$的值域，记作$R_f$或$f(D)$

    > 符号$f$与$f(x)$
    >
    > - 通常来说，$f$表示自变量和因变量之间的对应法则，$f(x)$表示与自变量$x$对应的函数值
    > - 但通常为了叙述方便，常用$y=f(x) \;\; x \in D$来表示定义在数集$D$上的函数，此时$f(x)$表示由它确定的函数$f$

2. 函数的性质

    - 有界性

        > 设函数$f(x)$的定义域为$D$，数集$X \subset D$
        >
        > 如果存在数$K_1$，使得$f(x) \le K_1$对任意的$x \in X$都成立，则称函数$f(x)$在$X$上有==上界==，$K_1$是函数$f(x)$在$X$上的一个上界
        >
        > 如果存在数$K_2$，使得$f(x) \ge K_2$对任意的$x \in X$都成立，则称函数$f(x)$在$X$上有==下界==，$K_2$是函数$f(x)$在$X$上的一个下界
        >
        > 如果存在正数$M$，使得$|f(x)| \le M$对任意的$x \in X$都成立，则称函数$f(x)$在$X$上有界
        >
        > 如果对于任意正数$M$，总存在$x_1 \in X$使得$|f(x)| > M$，则称函数$f(x)$在$X$上无界

        > 如果对于整个定义域，上述成立，则成为全局有界/无界

        > 函数$f(x)$在$X$上有界 $\Leftrightarrow$ $f(x)$在$X$上既有上界又有下界

    - 单调性

        > 设函数$f(x)$的定义域为$D$，区间$I \subset D$，如果对于区间$I$上任意两点$x_1, x_2$
        >
        > 当$x_1 < x_2$时，恒有$f(x_1) < f(x_2)$，那么称函数$f(x)$在区间$I$上是==单调递增==的
        >
        > 当$x_1 < x_2$时，恒有$f(x_1) > f(x_2)$，那么称函数$f(x)$在区间$I$上是==单调递减==的

        > 单调，特指不包含等于
        >
        > 单调递增函数和单调递减函数统称为单调函数

    -  奇偶性

        > 设函数$f(x)$的定义域为$D$==关于原点对撑==
        >
        > 如果对于任意$x \in D$，有$f(-x) = f(x)$恒成立，则称$f(x)$为偶函数，关于$y$轴对称
        >
        > 如果对于任意$x \in D$，有$-f(x) = f(-x)$恒成立，则称$f(x)$为奇函数，关于原点对称

        > *奇偶性不具有可加性*

    - 周期性

        > 设函数$f(x)$的定义域为$D$，如果存在一个正数$l$，使得对于任意$x \in D$，有$x \pm l \in D$，且$f(x + l) = f(x)$恒成立
        >
        > 则称函数$f(x)$为周期函数，$l$称为函数$f(x)$的周期

        > 通常周期函数的周期，指的是最小正周期
        >
        > - 并非每个函数都有最小正周期
        >     - 狄利克雷函数，$D(x) = \begin{cases}1, & x \in Q\\0,& x \in Q^C \end{cases}$
        >         - 任何正有理数$r$都是周期，故而不存在最小正周期

3. 反函数和复合函数

    - 反函数

        > 设函数$f:D \to f(D)$是单射，则存在逆映射$f^{-1}:f(D) \to D$，称$f^{-1}$为函数$f$的反函数
        >
        > 对于每个$y \in f(y)$，有唯一的$x \in D$，有$f^{-1}(y) = x$

        > 反函数和其直接函数，关于$y=x$对称

        > **若直接函数是单调函数，则其反函数也是单调函数，且单调性相同**

    - 复合函数

        > 设函数$y=f(x)$的定义域为$D_f$，函数$u=g(x)$的定义域为$D_g$，且其值域$R_g \subset D_f$，则下式确定的函数
        >
        > $y=f[g(x)],\;\; x \in D_g$
        >
        > 称为由函数$u=g(x)$和函数$y=f(x)$构成的复合函数，定义域为$D_g$

        > 构成复合函数的条件是，$\circ$右侧的函数的值域，在$\circ$左侧的函数的定义域内
        >
        > $f \circ g$要求$R_g \subset D_f$

        > $f \circ g$表示由函数$g(x)$和函数$f(x)$复合而来，按照先$g$后$f$的次序复合

4. 初等函数

    - 基本初等函数

        - 幂函数，$y=x^{\mu}, \mu \in R\text{是常数}$
        - 指数函数，$y=a^x,\; a > 0 \text{且}a\ne1$
        - 对数函数，$y=log_a(x),\; a > 0\text{且}a \ne 1$
        - 三角函数，$trig(x)$
        - 反三角函数，$arctrig(x)$或$trig^{-1}(x)$

    - 初等函数

        > 通过基本初等函数，和常数，经过有限次的四则运算，和有限次的函数复合所构成，并可用一个式子表示的函数，称为初等函数

# 2. 数列的极限

## 2.1 数列极限的定义

> 数列
>
> 如果按照==某一法则==，对每个$n \in N_+$，对应一个确定的实数$x_n$，将这些实数按照下标从小到大的顺序排列得到的序列，称为数列，记为$\{x_n\}$
>
> $x_n$称为一般项或通项，通常用公式表示

> 数列的极限
>
> 设$\{x_n\}$是一个数列，如果存在常数$a$，对于任意给定的正数$\varepsilon$(不论多么小)，总存在正整数$N$，使得$n > N$时，不等式
>
> $|x_n -a | < \varepsilon$
>
> 都成立，那么就称**常数$a$是数列$\{x_n\}$的极限**，记为$\displaystyle \lim_{n \to \infty}x_n = a$，或**称$\{x_n\}$收敛于$a$**，记为$x_n \to a\;(n \to \infty)$
>
> - 如果不存在这样的常数$a$，则说明数列$\{x_n\}$是发散的，或$\displaystyle \lim_{n \to \infty}x_n$不存在$DNE$
> - 正数$\varepsilon$可以任意给定是重要前提，这样$|x_n - a|<\varepsilon$才可以表达出$x_n$与$a$==无限接近==的意思
> - 正整数$N$是和$\varepsilon$相关的，随着$\varepsilon$的给定而确定

- $|x_n -a | < \varepsilon$表示的内容
    - 极限表示的是$\{x_n\}$无限接近值$a$，也即两者相差<u>几乎</u>为$0$，所以$|x_n-a|$任意小，因此可以使用$\forall \varepsilon >0, \;|x_n -a|<\varepsilon$

> 数列极限符号表达
>
> $\displaystyle \lim_{n \to \infty}x_n = a \Leftrightarrow \forall \varepsilon > 0 \text{，} \exists \text{正整数}N \text{，当}n > N \text{时，有} |x_n - a| < \varepsilon$

> 数列极限的几何意义
>
> 当$n > N$时，所有的$x_n$的点都落在数轴上的开区间$(a - \varepsilon, a + \varepsilon)$内

## 2.2 收敛数列的性质

1. 极限的唯一性

    > 如果数列$\{x_n\}$收敛，那么极限唯一

    <img src="chap 1 函数与极限.assets/image-20241225085824203.png" alt="image-20241225085824203" style="zoom: 60%;" />

2. 收敛数列的有界性

    > 如果数列$\{x_n\}$收敛，那么数列$\{x_n\}$一定有界

    - 数列有界的定义

        > 对于数列$\{x_n\}$，如果存在一个正整数$M$，使得对于一切$\{x_n\}$都满足不等式
        >
        > $|x_n| \le M$
        >
        > 则称数列$\{x_n\}$有界，如果这样的正整数$M$不存在，则称数列$\{x_n\}$无界

3. 收敛数列的保号性

    > 如果数列$\{x_n\}$收敛于$a$，或$\displaystyle \lim_{n \to \infty}x_n = a$，且$a > 0(\text{或}a < 0)$，则存在正整数$N$，当$n > N$时，都有$x_n > 0(\text{或}x_n < 0)$

    > 保号性推论
    >
    > 如果数列$\{x_n\}$从某项起有$x_n \ge 0(\text{或}x_n \le 0)$，且数列$\{x_n\}$收敛于$a$，那么有$a \ge 0 (\text{或} a \le 0)$

4. 收敛数列与其子数列间的关系

    > 如果数列$\{x_n\}$收敛于$a$，那么他的任一子数列也收敛，且也收敛于$a$
    >
    > - 如果一个数列$\{x_n\}$的两个子数列收敛于不同值，则可知原数列$\{x_n\}$是发散的
    > - 如果数列$\{x_n\}$是发散的，但其子数列可能是收敛的

    - 子数列定义

        > 从数列$\{x_n\}$中任意抽取无限多项，且保持这些项在原数列$\{x_n\}$中的先后次序，这样得到的新数列，就称为原数列$\{x_n\}$的子数列

# 3. 函数的极限

## 3.1 函数极限的定义

- 自变量$x$趋于有限值$x_0$

    > 设函数$f(x)$在点$x_0$的某一***去心邻域***内有定义，如果存在常数$A$，对任意给定的正数$\varepsilon$(不论他多么小)，总存在正数$\delta$，使得当$x$满足$0 < |x - x_0| < \delta$时，对应的函数值$f(x)$**都**满足不等式
    >
    > $|f(x) - A| < \varepsilon$
    >
    > 则常数$A$叫做函数$f(x)$，当$x \to x_0$时的极限，记作$\displaystyle \lim_{x \to x_0}f(x) = A$，或$f(x) \to A,\; \text{当}x \to x_0\text{时}$

    - 定义中指明$0 < |x - x_0| < \delta$，说明

        - $x \ne x_0$，<span style="text-decoration: underline double;">这说明函数在$x_0$处有没有极限，和$f(x)$在$x_0$处有无定义没有关系</span>
        - $\delta$表示的是$x_0$邻域半径，<span style="text-decoration: underline double;">表示了$x$和$x_0$的接近程度</span>

    - $|f(x)-A | < \varepsilon$表示的内容

        - 极限表示的是$f(x)$无限接近值$A$，也即两者相差<u>几乎</u>为$0$，所以$|f(x)-A|$任意小，因此可以使用$\forall \varepsilon >0, \;|f(x) - A|<\varepsilon$

    - $\delta$是由$\varepsilon$控制的，给定了$\varepsilon$，就可以找到一个对应的正数$\delta$，也因此，不需要要求$\delta$像$\varepsilon$那样，有**无论多小**的限制

    - $\displaystyle \lim_{x \to x_0}f(x)=A$的几何意义

        > - 对于给定的常数$A$和任意正数$\varepsilon$，在$y$轴做两条平行于$x$轴的水平线，在水平线之间的区域，就是我们希望接近于$A$的范围
        >
        > - 根据给定的范围，在点$x_0$附近可以找到一个$\delta$邻域，$(x-\delta, x+delta)$，$\color{red}此处说明\delta是由\varepsilon控制的$
        >
        > - 因此当函数$f(x)$上的点，其横坐标落到$(x-\delta, x+delta)\text{且}x \ne x_0$时，这些点的纵坐标就会落在水平线区域内，也即满足不等式$|f(x) - A | < \varepsilon$
        >
        > <img src="chap 1 函数与极限.assets/image-20241225150247565.png" alt="image-20241225150247565" />

- 单侧极限

    - 左右极限统称为单侧极限

    - 左极限

        - > 设函数$f(x)$在点$x_0$的某一***去心邻域***内有定义，如果存在常数$A$，对任意给定的正数$\varepsilon$(不论他多么小)，总存在正数$\delta$，使得当$x$满足==$-\delta < x - x_0 < 0$==时，对应的函数值$f(x)$**都**满足不等式
            >
            > $|f(x) - A| < \varepsilon$
            >
            > 则常数$A$叫做函数$f(x)$，当$x \to x_0^{\textcolor{red}{-}}$时的极限，记作$\displaystyle \lim_{x \to x_0^{\textcolor{red}{-}}}f(x) = A$，或$f(x) \to A,\; \text{当}x \to x_0^{\textcolor{red}{-}}\text{时}$

    - 右极限

        - > 设函数$f(x)$在点$x_0$的某一***去心邻域***内有定义，如果存在常数$A$，对任意给定的正数$\varepsilon$(不论他多么小)，总存在正数$\delta$，使得当$x$满足==$0 < x - x_0 < \delta$==时，对应的函数值$f(x)$**都**满足不等式
            >
            > $|f(x) - A| < \varepsilon$
            >
            > 则常数$A$叫做函数$f(x)$，当$x \to x_0^{\textcolor{red}{+}}$时的极限，记作$\displaystyle \lim_{x \to x_0^{\textcolor{red}{+}}}f(x) = A$，或$f(x) \to A,\; \text{当}x \to x_0^{\textcolor{red}{+}}\text{时}$

- 函数$f(x)$，在$x \to x_0$时极限存在的充要条件是：<font color=red>**左右极限存在且相等**</font>

- 自变量$x$的绝对值$|x|$趋于无穷大

    - > 设函数$f(x)$当$|x|$大于某一正数时有定义，如果存在常数𝐴，对任意给定的正数𝜀(不论他多么小)，总存在正数$X$，使得当$|x|>X$时，对应的函数值$f(x)$都满足不等式
        >
        > $|f(x) - A| < \varepsilon$
        >
        > 那么常数$A$叫做函数$𝑓(𝑥)$，当$x \to \infty$时的极限，记作$\displaystyle \lim_{x \to \infty}f(x) = A$，或$f(x) \to A,\; \text{当}x \to \infty\text{时}$

    - $\displaystyle \lim_{x \to \infty}f(x)=A$的几何意义

        > - 对于给定的常数$A$和任意正数$\varepsilon$，在$y$轴做两条平行于$x$轴的水平线，在水平线之间的区域，就是我们希望接近于$A$的范围
        > - 根据$\varepsilon$可以找到一个正数$X$，使得对于所有$|x| > X$，函数$f(x)$的值都会落在水平线之间的区域
        >
        > <img src="chap 1 函数与极限.assets/image-20241225160553182.png" alt="image-20241225160553182" />
        >
        > 

## 3.2 函数极限的性质

> 仅给出$\displaystyle \lim_{x \to x_0}f(x) = A$的形式，但对$\displaystyle \lim_{x \to \infty}f(x) = A$也成立

1. 函数极限唯一性

    > 如果函数极限$\displaystyle \lim_{x \to x_0}f(x) = A$存在，那么极限唯一

2. 函数极限局部有界性

    > 如果函数极限$\displaystyle \lim_{x \to x_0}f(x) = A$存在，那么存在正常数$M$和$\delta$，使得当$0<|x - x_0| < \delta$时，$|f(x)|\le M$

3. 函数极限局部保号性

    > 如果函数极限$\displaystyle \lim_{x \to x_0}f(x) = A$，且$A > 0(\text{，或}A <0)$，那么存在正常数$\delta$，使得当$0<|x - x_0| < \delta$时，$f(x) > 0\text{，或}f(x)<0$

    > 如果函数极限$\displaystyle \lim_{x \to x_0}f(x) = A$，且$A \ne 0$，那么就存在$x_0$的某一去心邻域$\stackrel {\circ} {U}(x_0)$
    >
    > 当$x \in \stackrel {\circ} {U}(x_0)$时，有$|f(x)| > \frac {|A|} 2$

    > 如果在$x_0$的某个去心邻域内$f(x) \ge 0$，或有$f(x) \le 0$，且当$x \to x_0$时，且$\displaystyle \lim_{x \to x_0}f(x) = A$，那么$A \ge 0$，或$A \le 0$

4. 函数极限与数列极限的关系

    > 如果函数极限$\displaystyle \lim_{x \to x_0}f(x) = A$存在，$\{x_n\}$为函数$f(x)$的定义域内，任意收敛于$x_0$的数列，且满足$x_n \ne x_0$
    >
    > 那么相应的函数值数列$\{f(x_n)\}$必收敛，且$\displaystyle \lim_{n \to \infty}f(x_n) = \lim_{x \to x_0}f(x)$

# 4. 无穷大和无穷小

> 无穷大/无穷小，指的均是函数，而不是具体的值

- 无穷小

    > 如果函数$f(x)$当$x \to x_0$，或$x \to \infty$时的极限为0，那么称==函数==$f(x)$==为==当$x \to x_0$，或$x \to \infty$时的==无穷小==

    - 无穷小QA

        - Q: 为什么0是无穷小而不是负数？
            - A: 根据无穷小的定义可知，是当自变量$x \to x_0 \text{或} x \to \infty$时，函数的极限为$0$，根据极限的定义，极限为$0$是指$|f(x) - 0| < \varepsilon$，也即$|f(x)| < \varepsilon$，含有绝对值，因此以$0$为无穷小的标准
        - Q: 无穷小是值还是函数？
            - A: 无穷小是函数，具体的值，无法体现对任意的$\varepsilon$，都有$|f(x)| < \epsilon$ 

    - **无穷小与极限存在**

        >  在*自变量*的*同一变化过程*$x \to x_0$，或$x \to \infty$中，==函数$f(x)$具有极限$A$的充要条件==是，$f(x) = A + \alpha$，$\alpha$是无穷小

- 无穷大

    > 设函数$f(x)$在$x_0$的某一去心邻域内有定义(或$|x|$大于某一正数时有定义)，如果对于任意给定的正数$M$(无论$M$多么大)，总存在正数$\delta$，(或正数$X$)，只要$x$适合不等式$0 < |x - x_0| < \delta$(或$|x| > X$)，对应的函数值总满足不等式
    >
    > $|f(x)| > M$
    >
    > 那么称==函数==$f(x)$==为==当$x \to x_0$，或$x \to \infty$时的==无穷大==

    > 按照极限定义，无穷大的函数，极限是不存在的，但为了叙述方便，也可以称函数的极限是无穷大，$\displaystyle \lim_{x \to x_0}f(x) = \infty$，或，$\displaystyle \lim_{x \to \infty}f(x) = \infty$

    - **无穷大与无穷小**

        > 在*自变量*的*同一变化过程*中，如果$f(x)$为无穷大，那么$\frac 1 {f(x)}$为无穷小；如果$f(x)$为无穷小，且$f(x) \ne 0$，则$\frac 1 {f(x)}$为无穷大

# 5. 极限运算法则

- 使用极限运算法则，可以求解部分函数的极限

- 针对$x \to x_0$和$x \to \infty$都成立

> - 定理1
>     - 两个无穷小的==和==仍是无穷小
> - 推论
>     - 有限个无穷小的和仍是无穷小

> - 定理2
>     - 有界函数与无穷小的==乘积==是无穷小
> - 推论1
>     - 常数与无穷小的乘积是无穷小
> - 推论2
>     - 有限个无穷小的乘积是无穷小

> - 定理3
>     - 如果$\lim f(x) = A$、$\lim g(x) = B$，则有
>         - $\lim[f(x) \pm g(x)] = \lim f(x) \pm \lim g(x) = A \pm B$
>         - $\lim[f(x) \times g(x)] = \lim f(x) \times \lim g(x) = A \times B$
>         - $\text{若}B \ne 0, \;\;\lim\frac {f(x)} {g(x)} = \frac {\lim f(x)} {\lim g(x)} = \frac A B$
> - 推论1
>     - 如果$f(x)$的极限存在，而$c$为常数，那么$\lim [cf(x)] = c\lim f(x)$
> - 推论2
>     - 如果$f(x)$的极限存在，而$n$是正整数，那么$\lim[f(x)]^n = [\lim f(x)]^n$

> - 定理4
>     - 设有数列$\{x_n\}$， $\{y_n\}$，如果$\displaystyle \lim_{n \to \infty} x_n = A$、$\displaystyle \lim_{n \to \infty} y_n = B$，则有
>         - $\displaystyle \lim_{n \to \infty}(x_n + y_n) = \displaystyle \lim_{n \to \infty} x_n \pm \displaystyle \lim_{n \to \infty} y_n = A \pm B$
>         - $\displaystyle \lim_{n \to \infty}(x_n \times y_n) = \displaystyle \lim_{n \to \infty} x_n \times \displaystyle \lim_{n \to \infty} y_n = A \times B$
>         - $\text{若}B \ne 0, \;\;\displaystyle \lim_{n \to \infty}\frac {x_n} {y_n} = \frac {\displaystyle \lim_{n \to \infty} x_n} {\displaystyle \lim_{n \to \infty} y_n} = \frac A B$

> - 定理5
>     - 如果$\varphi(x) \ge \psi(x)$，且$\lim \varphi(x) = A$，$\lim \psi(x)=B$，那么$A \ge B$

> - 定理6
>
>     - 设函数$y = f[g(x)]$是由函数$u=g(x)$和$y=f(u)$复合而来，且$f[g(x)]$在$x_0$的某一去心邻域内有定义
>
>         若$\displaystyle \lim_{x \to x_0}u(x) = u_0$，$\displaystyle \lim_{u \to u_0}f(u) = A $
>
>         且存在$\delta_0 >0$，当$x \in \stackrel {\circ} {U}(x_0, \delta_0)$时，有$g(x) \ne u_0$，那么
>
>         $\displaystyle \lim_{x \to x_0}f[g(x)] = \displaystyle \lim_{u \to u_0}f(u) = A $

- 极限求解方法 之一

    > 涉及多项式，和有理分式的极限

    - 当$x \to x_0$时
        - 如果是多项式函数的极限，可以将$x_0$带入函数直接计算出极限
        - 如果是有理分式的极限，且分母带入$x_0$后不为$0$，可以将$x_0$带入函数直接计算出极限
            - 如果分母为$0$
                - 先考虑约分是否可以计算出极限
                - 再考虑如果分母为$0$，分子不为$0$，则其倒数的极限为$0$，也即无穷小，根据无穷小的性质，可推断原有理分式极限为$\infty$
                - 都不可以考虑其他方法
    - 当$x \to \infty$时
        - 如果是有理分式的极限，根据分子分母中，系数非零的最高次项的次数，进行判断
            - 分子次数 $<$ 分母次数，极限为$0$
            - 分子次数 $=$ 分母次数，极限为分子分母中最高次项的系数之比
            - 分子次数 $>$ 分母次数，极限为$\infty$

# 6. 极限存在准则 与 两个重要极限

1. 准则一        **夹逼定理**

    > 如果数列$\{x_n\}$，$\{y_n\}$，$\{z_n\}$满足以下条件
    >
    > - 从某项起，即$\exists n_0 \in \mathbb {N^+}$，当$n > n_0$时，有$\{y_n\} \le \{x_n\} \le \{z_n\}$
    > - $\displaystyle \lim_{n \to \infty}y_n = a, \;\;\lim_{n \to \infty}z_n = a$
    >
    > 那么数列$\{x_n\}$的极限存在，且也为$a$

    > 如果函数$f(x)$，$g(x)$，$h(x)$满足以下条件
    >
    > - 对$x \in \stackrel {\circ} {U}(x_0, r)$(或$|x| > X$)，有$g(x) \le f(x) \le h(x)$
    > - $\displaystyle \lim_{n \to \infty }g(x) = A, \;\;\lim_{n \to \infty}h(x) = A$ 或 $\displaystyle \lim_{n \to x_0 }g(x) = A, \;\;\lim_{n \to x_0}h(x) = A$
    >
    > 那么函数$f(x)$的极限存在，且也为$A$

2. 准则二        **==单调有界==数列必有极限**

    **<u>充分条件</u>**

    > 如果数列$\{x_n\}$单调且有界，那么数列$\{x_n\}$一定有极限，也即一定收敛
    >
    > *此处的单调是广义的，包含等号*

    > 设函数$f(x)$在点$x_0$的某个左邻域内单调且有界，则$f(x)$在$x_0$的左极限必定存在
    >
    > 设函数$f(x)$在点$x_0$的某个右邻域内单调且有界，则$f(x)$在$x_0$的右极限必定存在
    >
    > 设$X$是任意大的正数，函数$f(x)$在$x > X$的区间上单调且有界，则$f(x)$在$x \to +\infty$的极限必定存在
    >
    > 设$X$是任意大的正数，函数$f(x)$在$x < -X$的区间上单调且有界，则$f(x)$在$x \to -\infty$的极限必定存在

3. 柯西极限存在准则(柯西审敛原理)

    > 数列$\{x_n\}$收敛的==充分必要条件==是：
    > 对于任意给定的正数$\varepsilon$，存在正整数$N$，使得当$n > N, \;\; n > N$时，有
    > $|x_n - x_m| < \varepsilon$
    > 可以推广到函数极限存在的充要条件

- 两个重要极限
    - $\displaystyle \lim_{x \to 0}\frac {sin(x)} {x} = 1$
    - $\displaystyle \lim_{x \to \infty}(1 +  {\frac 1 x})^x = e$
        - 更一般的形式
            - $\displaystyle \lim_{n \to \infty} (1 + \frac x n)^{n} = e^x$
            - $\displaystyle \lim_{h \to 0}(1 + hx)^{\frac 1 h} = e^x$

# 7. 无穷小比较

- 两个无穷小的和/差/积都是无穷小，但对于商，会存在等于$0,\;\infty,\;c\; c \ne 0$的情形
  - 比值为$0$，说明分子趋于零的速度快于分母趋于零的速度
  - 比值为$\infty$，说明分母趋于零的速度快于分子趋于零的速度
  - 比值为$1$，说明分子分母趋于零的速度快慢相仿


- 无穷小比值相关定理
  
  
    - $\alpha$, $\beta$都是同一个自变量变化过程中的无穷小，且$\alpha \ne 0$，$\lim \frac {\beta} {\alpha}$也是同一自变量变化过程中的极限
    
    > 如果$\lim \frac {\beta} {\alpha} = 0$，那么就说$\beta$是比$\alpha$高阶的无穷小，记作$\beta = o(\alpha)$
    
    > 如果$\lim \frac {\beta} {\alpha} = \infty$，那么就说$\beta$是比$\alpha$低阶的无穷小
    
    > 如果$\lim \frac {\beta} {\alpha} = c \;\;c \ne 0$，那么就说$\beta$与$\alpha$同阶的无穷小
    
    > 如果$\lim \frac {\beta} {\alpha^k} = c \;\;c \ne 0,\;\; k > 0$，那么就说$\beta$是关于$\alpha$的$k$阶无穷小
    
    > 如果$\lim \frac {\beta} {\alpha} = 1$，那么就说$\beta$与$\alpha$是等价无穷小，记作$\beta \sim \alpha$
    >
    > > 等价无穷小具有如下性质 
    > >
    > > - 自反性，$\alpha \sim \alpha$
    > > - 对称性，若$\alpha \sim \beta$， 则$\beta \sim \alpha$
    > > - 传递性，若$\alpha \sim \beta$，$\beta \sim \gamma$，则$\alpha \sim \gamma$
    
- 定理一：

    > $\beta$和$\alpha$是等价无穷小的充要条件是，$\beta = \alpha + o(\alpha)$

- 定理二：

    > 设$\alpha \sim \stackrel {\sim} {\alpha}$，$\beta \sim \stackrel {\sim} {\beta}$， 且极限$\lim \frac {\stackrel {\sim} {\beta}} {\stackrel {\sim} {\alpha}}$存在，则
    >
    > $\lim \frac {\beta} {\alpha} = \lim \frac {\stackrel {\sim} {\beta}} {\stackrel {\sim} {\alpha}}$

- 常见等价无穷小

    > 当$x \to 0$时有如下等价无穷下
    
    - $sin(x) \sim x$
    - $tan(x) \sim x$
    - $arcsin(x) \sim x$
    - $arctan(x) \sim x$
    - $1-cos(x) \sim \frac 1 2 x^2$
    - $sec(x) - 1 \sim \frac 1 2 x^2$
    - $\sqrt[n]{1+x} - 1 \sim \frac 1 n x$
        - 证明过程
            - <img src="chap 1 函数与极限.assets/image-20241227150755966.png" alt="image-20241227150755966" style="zoom:67%;" />    

# 8. 函数的连续性和间断点

- 增量变量的描述
    - 变量从一个初值变到终值，终值与初值的差就叫做变量的增量，记作$\Delta x$，变量可任取
    - 设函数$f(x)$在$x_0$的某邻域内是有定义的，则，函数的增量，指的是自变量$x$在该邻域内，从$x_0$变到$x_0+\Delta x$时，函数值$f(x)$相应的从$f(x_0)$变到$f(x_0 + \Delta x)$，将此变化记为$\Delta y = f(x_0 + \Delta x) - f(x_0)$

- 在某点$x_0$处连续
    - 增量表示法
    
        > 设函数$f(x)$在点$x_0$的某一领域内有定义，如果$\displaystyle \lim_{\Delta x \to 0}f(x_0+\Delta x) - f(x_0)=0$，则称函数$y=f(x)$在点$x_0$连续
    - 函数表示法
    
        > 设函数$f(x)$在点$x_0$的某一领域内有定义，如果$\displaystyle \lim_{x \to x_0}f(x) = f(x_0)$，则称函数$𝑦=𝑓(𝑥)$在点$𝑥_0$连续
    
        - 变化过程：
            - 令$x = x_0 + \Delta x$，所以当$\Delta x \to 0$，意味着$x \to x_0$
            - $\Delta y = f(x) - f(x_0)$，所以有$f(x) = f(x_0) + \Delta y$，所以当$\Delta y \to 0$，意味着$f(x) \to f(x_0)$
    - $\varepsilon-\delta$表示法
    
        > $f(x)$在点$x_0$处连续$\Leftrightarrow$$\forall \varepsilon > 0 $，$\exists \delta >0$，使得当$|x - x_0| < \delta$时，有$|f(x) - f(x_0)| < \varepsilon$
    - 左右连续
    
        > 左连续
        >
        > 如果$\displaystyle \lim_{x \to x_0^-}f(x) = f(x_0^-)$存在，且等于$f(x_0)$，那么就说函数$f(x)$在点$x_0$处左连续
        
        > 右连续
        > 如果$\displaystyle \lim_{x \to x_0^+}f(x) = f(x_0^+)$存在，且等于$f(x_0)$，那么就说函数$f(x)$在点$x_0$处右连续
    - 连续的三个条件
    
        - 函数在$x_0$有定义
        - 函数当想$x \to x_0$的极限存在
        - 函数值与极限值相等
    - 连续的几何意义
    
        - 函数图像在$x_0$的某一邻域内，是连成一片的，没有跳跃，空洞或断裂
        - 可以从左到右画过$x_0$点，不需要抬笔

- 在区间上连续

    > 在区间上每个点都连续的函数，叫做在该区间上的连续函数
    >
    > 如果区间包括端点，则说，在左端点上连续，指的是右连续，在右端点上连续，指的是左连续

    - 几何意义
        - 区间上连续的函数的图像，是一条连续而不间断的曲线

- 函数的间断点

    > 设函数$f(x)$在点$x_0$的某一去心邻域内有定义，在此前提下，如果函数$f(x)$有下述情况之一，则函数$f(x)$在点$x_0$处不连续，点$x_0$称为函数$f(x)$的不连续点或间断点
    > - 在$x = x_0$处无定义
    > - 在$x = x_0$处虽有定义，但极限$\displaystyle \lim_{x \to x_0}f(x)$不存在
    > - 在$x = x_0$处虽有定义，且极限$\displaystyle \lim_{x \to x_0}f(x)$虽存在，但极限值不等于函数值，也即$\displaystyle \lim_{x \to x_0}f(x) \ne f(x_0)$
    
    - 间断点分类
        - 第一类间断点，左右极限存在，但不满足连续性条件
            - 可去间断点，指的是左右极限存在且相等，但函数值未定义或不等于极限，可通过重新定义函数在该点的值来消除不连续
                - $y = \frac {x^2 - 1} {x - 1}$，在点$x = 1$无定义，左右极限存在且相等，因此可以补充定义，消除不连续，所以点$x = 1$是$y = \frac {x^2 - 1} {x -1}$的可去间断点
            - 跳跃间断点，指的是左右极限存在，但不相等，函数值可以定义也可以未定义
                - $f(x) = \begin{cases} x - 1, & x < 0,\\0, & x = 0, \\ x +1 &x >0. \end{cases}$，在点$x=0$处左右极限存在但不相等，且产生了跳跃现象，因此$x = 0$是$f(x)$的跳跃间断点
        - 第二类间断点，除了第一类的间断点外都称为第二类间断点，也即左右极限至少一个不存在
            - 无穷间断点，左右极限中至少一个趋于无穷
                - $y=tan(x)$，点$x = \frac {\pi} 2 + k\pi \; k \in \mathbb Z$是$y=tan(x)$的无穷间断点
            - 震荡间断点，左右极限不存在，且函数无限震荡
                - $y=sin(\frac 1 x)$，点$x=0$是函数的震荡间断点，因为在$x=0$处无定义，且函数值在$[-1, 1]$之间无限震荡

# 9. 连续函数的运算 与 初等函数的连续性

- 连续函数的和/差/积/商的连续性

    > 设函数$f(x)$和$g(x)$在点$x_0$处连续，则他们的和差$f \pm g$，积$f \times g$，商$\frac f g$($g(x_0) \ne 0$)也都在点$x_0$处连续
- 反函数和复合函数的连续性

    - 反函数的连续性

        > 如果函数$f(x)$在区间$I$上单调递增或递减，且连续，那么其反函数$f^{-1}(x)$在对应的区间$I_y={y | y=f(x), \; x \in I_x}$上单调递增或递减，且连续
    - 连续的复合函数求极限
        > 设函数$y = f[g(x)]$是由函数$u=g(x)$和$y=f(u)$复合而来，$\stackrel {\circ} {U}(x_0) \subset I_{f \circ g}$，若$\displaystyle \lim_{x \to x_0}g(x)=u_0$，而函数$y=f(u)$在$u = u_0$处连续，则有
        > $\displaystyle \lim_{x \to x_0}f[g(x)] = \lim_{u \to u_0}f(u) = f(u_0)$
        >
        > > 说明对连续的符合函数求极限时，可以做代换$u = g(x)$，那么复合函数求极限就变换为了求$\displaystyle \lim_{u \to u_0}f(u)$，其中$u= u_0$
        >
        > 或
        > $\displaystyle \lim_{x \to x_0}f[g(x)] = f[\lim_{x \to x_0}g(x)]$
        >
        > > 说明对连续的符合函数求极限时，函数符号$f$可以与连续符号$\displaystyle \lim_{x \to x_0}做交换
        
    - 复合函数连续性传导
        > 设函数$y = f[g(x)]$是由函数$u=g(x)$和$y=f(u)$复合而来，$U(x_0) \subset I_{f \circ g}$，若函数$g(x)$在$x = x_0$处连续，且$u_0=g(u)$，而函数$y=f(u)$在$u = u_0$处连续，则有
        > 复合函数$y=f[g(x)]$在$x = x_0$处连续

- 初等函数的连续性

    > 基本初等函数，在其定义域内，都是连续的

    > 一切初等函数，在其定义区间内，都是连续的


















