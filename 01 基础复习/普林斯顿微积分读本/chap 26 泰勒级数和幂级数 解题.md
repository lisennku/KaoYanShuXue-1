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

> 常见麦克劳林级数

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
  >

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
  >

  - 求解$ln(x)$在$x=1$处的泰勒级数

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

> 若一个幂级数收敛于开区间$(a, b)$上的可导函数$f$，则可以通过对幂级数==逐项求导==，得到一个在相同区间上==收敛==于$f^{\prime}$的==新幂级数==
>
> > 新幂级数在区间端点$a,b$的收敛性要特殊判断
>
> 如果是求泰勒多项式，需要注意，求导后的泰勒多项式的阶数，比原阶数==少1==

- 求$sin(x)$的麦克劳林级数

  $$
  \begin{align*}
  & 考虑(cos(x))^{\prime} = -sin(x)\\
  & 则根据cos(x) = \displaystyle \sum_{n=0}^{\infty}\frac {(-1)^n} {(2n)!}x^{2n}=1 - \frac 1 {2!}x^2  + \frac 1 {4!}x^4 - \frac 1 {6!}x^6 + \dots\\
  & 则两边求导，可得到\\
  & -sin(x) = -x + \frac 1 {3!}x^3 - \frac 1 {5!}x^5+\dots\\
  & sin(x) = x - \frac 1 {3!}x^3 + \frac 1 {5!}x^5+\dots = \displaystyle \sum_{n=0}^{\infty}\frac {(-1)^n} {(2n+1)!}x^{2n+1}\\
  \end{align*}
  $$
- 求$f(x)=\frac 1 {(1+x)^2}$的麦克劳林级数

  $$
  \begin{align*}
  & 考虑到函数\frac 1 {(1+x)^2}是函数-\frac 1 {(1+x)}的导数，那么先看\frac 1 {(1+x)}的麦克劳林级数\\
  & \frac 1 {(1+x)}的麦克劳林级数是将\frac 1 {(1-x)}的麦克劳林级数中的x换为-x\\
  & \frac 1 {(1-x)}=1 + x + x^2 + x^3 + \dots\\
  & 则有\frac 1 {(1+x)} = 1 -x + x^2 -x^3 +\dots\\
  & 再求导，则有\\
  & -\frac 1 {(1+x)^2} = -1 + 2x - 3x^2 + 4x^3 + \dots\\
  & 所以有\frac 1 {(1+x)^2} = 1-2x + 3x^2 - 4x^3 + \dots = \displaystyle \sum_{n=0}^{\infty}(-1)^n(n+1)x^n\\
  \end{align*}
  $$

## 2.3 泰勒级数求积分

> 若一个幂级数收敛于开区间$(a, b)$上的可积函数$f$，则可以通过对幂级数==逐项求积分==，得到一个在相同区间上==收敛==于$\int f(x)dx$的==新幂级数==
>
> > 如果是不定积分，需要考虑常数$C$，并根据特殊的$x$值求出$C$
>
> 如果是求泰勒多项式，需要注意，积分后的泰勒多项式的阶数，比原阶数==多1==

- 求$f(x)=ln(1-x)$的麦克劳林级数

  $$
  \begin{align*}
  & 考虑到ln(1-x)是-\frac 1 {1-x}的积分(没有常数项)，所以可以使用积分法求原函数的麦克劳林级数\\
  & -\int \frac 1 {1-x}dx =- \int \sum_{n=0}^{\infty}x^ndx=-\sum_{n=0}^{\infty}\frac 1 {n+1}x^{n+1} + \textcolor{red}{C}=\sum_{n=\textcolor{red}{1}}^{\infty}-\frac {1}{n}x^{n}+ \textcolor{red}{C}\\
  & 则有ln(1-x) = \sum_{n=\textcolor{red}{1}}^{\infty}-\frac {1}{n}x^{n}+ \textcolor{red}{C}\\
  & 当x=0时，左侧为0，右侧为0+C，所以C等于0\\
  & \therefore ln(1-x) = \sum_{n=\textcolor{red}{1}}^{\infty}-\frac {1}{n}x^{n}
  \end{align*}
  $$
- 求$tan^{-1}(x)$的麦克劳林级数
    $$
    \begin{align*}
    & tan^{-1}(x)是\frac 1 {1 + x^2}的反导数\\
    & 根据\frac 1 {1-x}的泰勒级数，并将x换为-x^2，则有\\
    & \frac 1 {1 + x^2} = \sum_{n=0}^{\infty} (-1)^nx^{2n} \\
    & 对\frac 1 {1 + x^2} 计算不定积分，则有\\
    & tan^{-1}(x) = \int \frac 1 {1 + x^2}dx = \int \sum_{n=0}^{\infty} (-1)^nx^{2n}dx = C + x - \frac 1 3 x^3 + \frac 1 5 x^5 - \dots\\
    & 当x = 0时，左侧为0，右侧为C，所以C=0  \\
    & 所以tan^{-1}(x) = x - \frac 1 3 x^3 + \frac 1 5 x^5 - \dots = \sum_{n=0}^{\infty}\frac {(-1)^n} { 2n+1} x^{2n+1}\\
    \end{align*} 
    $$
    
- 求$f(x)=\displaystyle \int_0^{x}sin(t^3)dt$的麦克劳林级数
    $$
    \begin{align*}
    & 根据sin(x)的泰勒级数和x换为t^3，计算sin(t^3)的泰勒级数\\
    & sin(t^3) = \sum_{n=0}^{\infty}\frac {(-1)^n} {(2n+1)!} t^{6n+3}\\
    & f(x) = \int_0^{x}sin(t^3)dt = \int_0^{x}\sum_{n=0}^{\infty}\frac {(-1)^n} {(2n+1)!} t^{6n+3}dt\\
    & f(x) = \sum_{n=0}^{\infty}\frac {(-1)^n} {(6n+4)(2n+1)!} x^{6n+4}
    \end{align*}
    $$


## 2.4 泰勒级数加减乘除

> 已知两个函数$f(x)$和$g(x)$关于$x=a$的泰勒级数，则$f(x)\pm g(x)$的泰勒级数，是两个泰勒级数的和或差
>
> 收敛区间，是两个泰勒级数的收敛区间的==交集==
>
> 如果是求泰勒多项式，则阶数为两个多项式中小那个

> 已知两个函数$f(x)$和$g(x)$关于$x=a$的泰勒级数，则$f(x)g(x)$的泰勒级数，是两个泰勒级数的积
>
> 收敛区间，是两个泰勒级数的收敛区间的==交集==
>
> 如果是求泰勒多项式，应该略去乘积中次数大于阶数的项

> 已知两个函数$f(x)$和$g(x)$关于$x=a$的泰勒级数，则$\frac {f(x)} {g(x)}$的泰勒级数，是两个泰勒级数的商
>
> 求级数的商，可以和前述的多项式除法类似，使用长除法，唯一区别是除数要按照次数递增的顺序，而不是前述递减的顺序

- 求$e^xsin(x)$的三阶麦克劳林级数
    $$
    \begin{align*}
    & e^x = 1 + x + \frac 1 2 x^2 + \frac 1 {3!} x^3 + \dots\\
    & sin(x) = x - \frac 1 {3!}x^3 + \dots\\
    & e^xsin(x) = (1 + x + \frac 1 2 x^2 + \frac 1 {3!} x^3 + \dots)(x - \frac 1 {3!}x^3 + \dots)=x - \frac 1 {3!}x^3+x^2+\frac 1 2 x^3 \\
    & = x + x^2 + \frac 1 3 x^3 + \dots
    \end{align*}
    $$
- 求$tan(x)$的四阶麦克劳林级数
    $$
    \begin{align*}
    & tan(x) = \frac {sin(x)} {cos(x)}\\
    & sin(x) = x - \frac 1 3 x^3 + \dots \\
    & cos(x) = 1 - \frac 1 2 x^2 + \frac 1 {4!}x^4 - \dots \\
    \end{align*}
    $$
    <img src="chap 26 泰勒级数和幂级数 解题.assets/image-20241219143919311.png" alt="image-20241219143919311" style="zoom:80%;" />

# 3. 利用幂级数和泰勒级数求导

> 泰勒级数的通项公式中，第$n$项的系数$a_n$的计算公式是$a_n\frac {f^{(n)}(a)} {n!}$，所以，根据第$n$项的系数可以计算出$f$的$n$次导数在$x=a$的值，也即
>
> $f^{(n)}(a) = n! \times a_n$
>
> > 需要注意的是：公式中其实存在==两个不同==的$n$
> >
> > - 第一个$n$，是函数$f$待解的$n$次导数，同时，该$n$也决定了泰勒级数中$x$的次数的具体值，也即下方的$x^n$
> > - 第二个$n$，是泰勒级数中，$x^n$项对应的系数$a_n$，通常$a_n$表示为一个通项公式，需要根据具体的公式解出此时系数$a_n$的值
>
> > 如果待解的$n$次导数，在泰勒级数中没有对应项，说明此时系数为$0$，所以有$f^{(n)}=n! \times 0 = 0$

- 设$f(x) = e^{x^2}$，求$f^{100}(0)$和$f^{101}(0)$
    $$
    \begin{align*}
    & e^{x^2} = \sum_{n=0}^{\infty}\frac 1 {n!}x^{2n}\\
    & 求100次导数，则找到x^{100}的系数a_{100}，根据2n = 100解得n=50\\
    & 所以a_{100}=\frac 1 {50!}\\
    & 则f^{100}(0) = \frac {100!} {50!}\\
    & 求101次导数，则找到x^{101}项，但级数中并不存在，说明系数a_{101}等于0\\
    & 则f^{100}(0) = 0
    \end{align*}
    $$

- 设$f(x)=\displaystyle \int_0^xsin(t^3)dt$，求$f^{50}(0)$和$f^{52}(0)$
    $$
    \begin{align*}
    & f(x)=\displaystyle \int_0^xsin(t^3)dt = \sum_{n=0}^{\infty}\frac {(-1)^n} {(6n+4)(2n+1)!} x^{6n+4}\\
    & f^{50}对应x^{50}，也即6n+4=50，所以n=\frac {23} 2，不是整数，所以系数为0，则有f^{50}(0)=0\\
    & f^{52}对应x^{52}，也即6n+4=52，所以n=8，所以系数为\frac 1 {52(17!)}，则f^{52}(0)= 52!\frac 1 {52(17!)}=\frac {51!}{17!}
    \end{align*}
    $$


# 4. 利用麦克劳林级数求极限

> 可以用泰勒级数/麦克劳林级数求特定极限

> 若一个函数有在 $0$ 附近收敛于该函数的麦克劳林级数, 则函数在==$x \to 0$==时渐近等价于级数的最低次项, 即  
>
> $f(x) = a_nx^n + a_{n+1}x^{n+1} + \dots, \text{当}x \to 0 \text{时}，有f(x) ～　a_nx^n$

- $\displaystyle \lim_{x \to 0} \bigg(\frac 1 {sin(x)} - \frac 1 {e^x-1}\bigg)$
    $$
    \begin{align*}
    & 先通分，得到\lim_{x \to 0}\frac {e^x-1-sin(x)} {sin(x)(e^x-1)}\\
    & e^x = 1 + x + \frac 1 2 x^2 + \frac 1 {3!} x^3 + \dots\\
    & sin(x) = x - \frac 1 {3!}x^3 + \frac 1 {5!}x^5+\dots\\
    & \therefore e^x-1-sin(x) = x + \frac 1 2 x^2 + \frac 1 {3!} x^3 \dots - (x - \frac 1 {3!}x^3 + \frac 1 {5!}x^5+\dots)～\frac {x^2} 2\\
    & sin(x)(e^x-1)
    \end{align*}
    $$
    

