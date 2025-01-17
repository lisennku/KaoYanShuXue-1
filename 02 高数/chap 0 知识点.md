# 1. 概念

# 2. 基本初等函数

## 2.1 幂函数

### 2.1.1 函数性质

- $y=x^{\mu}$，其中$x$是自变量，$\mu$是常数

- 幂函数的定义域、值域和函数图像与$\mu$有关

    - $\mu$为正整数

        - 定义域为$\mathbb R$

        - 值域和图像和其他特性

            - 经过原点

            - 当$\mu$是偶数时，值域为$y \in \textcolor{red}{[}0, +\infty]$，函数为偶函数，关于$y$轴对称，图像先递减到原点，然后再递增

            - 当$\mu$为奇数时，值域为$\mathbb R$，函数为奇函数，关于原点对称，图像递增

                <img src="chap 0 知识点.assets/image-20250106160728114.png" alt="image-20250106160728114" style="zoom:50%;" />

    - $\mu$为负整数

        - 定义域为$\mathbb R \setminus  \{0\}$

        - 值域和图像和其他特性

            - ==不==经过原点

            - 当$\mu$是偶数时，值域为$y \in \textcolor{red}{(}0, +\infty)$，函数为偶函数，关于$y$轴对称，左侧图像递增，右侧图像递减

            - 当$\mu$是奇数时，值域为$\mathbb R \setminus  \{0\}$，函数为奇函数，关于原点对称，图像在第一、第三象限均递减

                <img src="chap 0 知识点.assets/image-20250106161310254.png" alt="image-20250106161310254" style="zoom:50%;" />

    - $\mu$为正分数

        - 定义域

            - $\mu$为偶数时，定义域为$x \in [0, +\infty]$
            - $\mu$为奇数时，定义域为$\mathbb R$

        - 值域和图像和其他特性

            - $\mu$为偶数时，值域为$x \in [0, +\infty]$，图像只在第一象限，递增

            - $\mu$为奇数时，值域为$\mathbb R$，图像关于原点对称，递增

                <img src="chap 0 知识点.assets/image-20250106161807461.png" alt="image-20250106161807461" style="zoom:50%;" />

    - $\mu$为负分数

        - 定义域

            - $\mu$为偶数时，定义域为$x \in \textcolor{red}{(}0, +\infty)$
            - $\mu$为奇数时，定义域为$\mathbb R \setminus \{0\}$

        - 值域和图像和其他特性

            - $\mu$为偶数时，值域为$y \in \textcolor{red}{(}0, +\infty)$，图像只在第一象限，递减

            - $\mu$为奇数时，值域为$\mathbb R \setminus  \{0\}$，图像关于原点对称，图像在第一、第三象限均递减

                <img src="chap 0 知识点.assets/image-20250106162521464.png" alt="image-20250106162521464" style="zoom:50%;" />

- 幂函数比较

    - $\mu$大于$0$，$\mu_1$是小于$1$的数，$\mu_2$等于$1$，$\mu_3$是大于$1$的数，则有

        - 在$x \in (0, 1)$，$x^{\mu_1} > x^{\mu_2} > x^{\mu_3}$

        - 在$x \in (1, +\infty)$，$x^{\mu_1} < x^{\mu_2} < x^{\mu_3}$

            <img src="chap 0 知识点.assets/image-20250106163019120.png" alt="image-20250106163019120" style="zoom:50%;" />

    - $\mu$小于$0$，$\mu_1$是大于$-1$的数，$\mu_2$等于$-1$，$\mu_3$是小于$-1$的数，则有

        - 在$x \in (0,1)$，$x^{\mu_1} < x^{\mu_2} < x^{\mu_3}$

        - 在$x \in (1, +\infty)$$x \in (0, 1)$，$x^{\mu_1} > x^{\mu_2} > x^{\mu_3}$

            <img src="chap 0 知识点.assets/image-20250106163220862.png" alt="image-20250106163220862" style="zoom:50%;" />

### 2.1.2 幂函数导数

> 设$y = x^{\mu}$，则$\frac {dy} {dx} = \mu x^{\mu -1}$

## 2.2 指数函数

### 2.2.1 函数性质

- $y = a^x\;a >0,\; a\ne 1$，其中$a$为常数

- 定义域，$\mathbb R$

- 值域，$y \in (0, +\infty)$

- 当$0< a < 1$时，函数图像严格递减，指数衰减趋势

- 当$a > 1$时，函数图像严格递增，指数增长趋势

    <img src="chap 0 知识点.assets/image-20250106165557374.png" alt="image-20250106165557374" style="zoom:50%;" />

### 2.2.2 导数

> 设$y=a^x,\; a > 0, \; a\ne1$，则$\frac {dy} {dx} =  a^xlna$

## 2.3 对数函数

### 2.3.1 函数性质

- $y=log_a(x),\; a >0, \; a \ne 1$，其中$a$为常数

- 定义域，$x \in (0, +\infty)$

- 值域， $\mathbb R$

- 当$0< a < 1$时，函数图像严格递减

- 当$a > 1$时，函数图像严格递增

    <img src="chap 0 知识点.assets/image-20250106165631596.png" alt="image-20250106165631596" style="zoom:50%;" />

### 2.3.2 导数

> 设$y=log_a(x)\; a >0,\;a \ne 1$，则$\frac {dy} {dx} = \frac {1} {xlna}$

## 2.4 三角函数

- 正弦
    - 函数性质
    - 函数图像
    - 导数

- 余弦
    - 函数性质
    - 函数图像
    - 导数

- 正切
    - 函数性质
    - 函数图像
    - 导数
    
- 余切
    - 函数性质
    - 函数图像
    - 导数

- 正割 $sec(x) = \frac {1} {cos(x)}$
    - 函数性质
    
        - 定义域，$x \in \mathbb R, \; x \ne \frac {\pi} {2} +k\pi,\; k \in \mathbb Z$
        - 值域，$y \in (-\infty, -1] \cup [1, +\infty)$，为偶函数，周期为$2\pi$
        - 因其是$cos(x)$的倒数，所以在$cos(x)$每个为$0$的位置都有一个垂直渐近线
    - 函数图像
    
        <img src="chap 0 知识点.assets/image-20250107233120322.png" alt="image-20250107233120322" style="zoom:50%;" />
    - 导数
        - $[sec(x)]^{\prime} = sec(x)tan(x)$
    
- 余割 $csc(x) = \frac {1} {sin(x)}$
    - 函数性质
    
        - 定义域，$x \in \mathbb R,\; x \ne k\pi, \; k \in \mathbb Z$
        - 值域，$y \in (-\infty, -1] \cup [1, +\infty)$，非奇非偶函数，周期为$2\pi$
        - 因其是$sin(x)$的倒数，所以在$sin(x)$每个为$0$的位置都有一个垂直渐近线
    
    - 函数图像
    
        <img src="chap 0 知识点.assets/image-20250107233807943.png" alt="image-20250107233807943" style="zoom:50%;" />
    
    - 导数
        - $[csc(x)]^{\prime} = csc(x)cot(x)$


## 2.5 反三角函数

- 反正弦 $arcsin(x)$
  
    - $arcsin(x)$函数是$sin(x)$的反函数，但因在整个定义域上，$sin(x)$不满足水平线检验，因此只挑选$sin(x),\; x\in [-\frac {\pi} {2}, \frac {\pi} {2}]$进行反函数	
    - 函数性质

        - 定义域，$x \in [-1, +1]$
        - 值域，$y \in [-\frac {\pi} {2}, \frac {\pi} {2}]$，为奇函数，经过原点，定义域上严格单调递增
    - 函数图像
    
        <img src="chap 0 知识点.assets/image-20250107122628225.png" alt="image-20250107122628225" style="zoom: 67%;" />
    - 导数
    
        - $[arcsin(x)]^{\prime} = \frac {1} {\sqrt{1-x^2}}$
    
- 反余弦 $arccos(x)$

    - $arccos(x)$函数是$cos(x)$的反函数，但因在整个定义域上，$cos(x)$不满足水平线检验，因此只挑选$cos(x),\; x \in [0, \pi]$这个区间上进行反函数

    - 函数性质

        - 定义域，$x \in [-1, 1]$
        - 值域，$y \in [0, \pi]$，非奇非偶函数，经过点$(0, \frac {\pi} {2})$，定义域上严格单调递减

    - 函数图像

        <img src="chap 0 知识点.assets/image-20250107122831144.png" alt="image-20250107122831144" style="zoom:67%;" />

    - 导数

        - $[arccos(x)]^{\prime} = -\frac {1} {\sqrt{1-x^2}}$

- 反正切 $arctan(x)$
  
    - $arctan(x)$是$tan(x)$的反函数，但因在整个定义域上，$tan(x)$​不满足水平线检验，因此只挑选$tan(x),\; x\in [-\frac {\pi} {2}, \frac {\pi} {2}]$进行反函数
    
    - 函数性质

        - 定义域，$x \in \mathbb R$
        - 值域，$y \in \textcolor{red}{(}-\frac {\pi} {2}, \frac {\pi} {2}\textcolor{red}{)}$，为奇函数，经过原点，定义域上严格单调递增
    
    - 函数图像
    
        <img src="chap 0 知识点.assets/image-20250107234814527.png" alt="image-20250107234814527" style="zoom:50%;" />
    
    - 导数
        - $[arctan(x)]^{\prime} = \frac {1} {1 + x^2}$
    
- 反余切 $arccot(x)$

    - $arccot(x)$是$cot(x)$的反函数，但因在整个定义域上，$cot(x)$不满足水平线检验，因此只挑选$cot(x),\; x\in [0, \pi]$进行反函数
    - 函数性质

        - 定义域，$x \in \mathbb R$
        - 值域，$y \in \textcolor{red}{(}0, \pi\textcolor{red}{)}$，非奇非偶函数，经过点$(0, \frac {\pi} {2})$，定义域上严格单调递减
    - 函数图像 

        <img src="chap 0 知识点.assets/image-20250107234846876.png" alt="image-20250107234846876" style="zoom:50%;" />

    - 导数
        - $[arctan(x)]^{\prime} = -\frac {1} {1 + x^2}$

- 反正割 $arcsec(x)$
    - 函数性质
    - 函数图像
    - 导数
        - $[arcsec(x)]^{\prime} = \frac {1} {|x|\sqrt{x^2-1}}$

- 反余割 $arccsc(x)$
    - 函数性质
    - 函数图像
    - 导数
        - $[arccsc(x)]^{\prime} = -\frac {1} {|x|\sqrt{x^2-1}}$


## 2.6三角函数公式

## 2.7 双曲函数

- 双曲正弦 $sinh(x) =\frac {e^x - e^{-x}} {2}$
    - 函数性质
    
        - 定义域， $\mathbb R$
        - 值域，$\mathbb R$，函数为奇函数，经过原点，定义域上严格单调递增
    
    - 函数图像
    
        <img src="chap 0 知识点.assets/image-20250106231802695.png" alt="image-20250106231802695" style="zoom:50%;" />
    
    - 导数
    
        $[sinh(x)]^{\prime} = cosh(x) =\frac {e^x + e^{-x}} {2}$
    
- 双曲余弦 $cosh(x) =\frac {e^x + e^{-x}} {2}$
    - 函数性质
    
        - 定义域， $\mathbb R$
        - 值域，$y \in [1, +\infty)$，函数为偶函数，关于$y$轴对称，从左到零，严格单调递减，再到正无穷，严格单调递增
    - 函数图像
    
        - <img src="chap 0 知识点.assets/image-20250106233439591.png" alt="image-20250106233439591" style="zoom:50%;" />
    - 导数
    
        $[cosh(x)]^{\prime}=sinh(x) = \frac {e^x - e^{-x}} {2}$
    
- 双曲正切
    - 函数性质
    - 函数图像
    - 导数
    
- 双曲余切
    - 函数性质
    - 函数图像
    - 导数
    
- 双曲正割
    - 函数性质
    - 函数图像
    - 导数
    
- 双曲余割
    - 函数性质
    - 函数图像
    - 导数

## 2.9 反双曲函数

- 反双曲正弦 $arcsinh(x) = ln(x + \sqrt{x^2+1})$
    - 函数性质
    
        - 定义域， $\mathbb R$
        - 值域，$\mathbb R$，函数为奇函数，经过原点，定义域上严格单调递增
    - 函数图像
    
        <img src="chap 0 知识点.assets/image-20250106232828603.png" alt="image-20250106232828603" style="zoom:50%;" />
    - 导数
    
        - $[arcsinh(x)]^{\prime} = \frac {1} {\sqrt{x^2+1}}$
- 反双曲余弦  $arccosh(x) = ln(x + \sqrt{x^2-1})$
    - 函数性质
    
        - 需要注意的是，经过反函数计算后，应该也会有另一个函数$ln(x - \sqrt{x^2-1})$也符合反函数定义，但是选择加的
        - 定义域，$x \in [1, +\infty)$
        - 值域，$y \in [0, +\infty)$，经过点$(1, 0)$，定义域上严格单调递增
    - 函数图像
    
        <img src="chap 0 知识点.assets/image-20250107092355649.png" alt="image-20250107092355649" style="zoom:50%;" />
    - 导数
    
        - $[arccosh(x)]^{\prime} = \frac {1} {\sqrt{x^2-1}}$
- 反双曲正切
    - 函数性质
    - 函数图像
    - 导数
- 反双曲余切
    - 函数性质
    - 函数图像
    - 导数
- 反双曲正割
    - 函数性质
    - 函数图像
    - 导数
- 反双曲余割
    - 函数性质
    - 函数图像
    - 导数

# 3. 常见口诀

1. 函数在==某点==：

    > 可导必连续，连续不一定可导，但是不连续则一定不可导
    
2. 有界数列不一定收敛，单调有界数列必收敛

# 4. 常见公式

## 4.1 绝对值不等式

> - $|a + b| \le |a| + |b|$
> - $|a-b| \ge ||a| - |b||$

## 4.2 二项式公式

$\displaystyle (a + b)^n = \sum_{k = 0}^nC_n^ka^{n-k}b^k \quad n \in \mathbb N^+$

## 4.3 幂差公式

$a^n - b^n = (a - b)(a^{n-1} + a^{n-2}b + a^{n-3}b^2 + \dots + ab^{n-2} + b^{n-1})$

## 4.4 幂和公式

- $n$为奇数时

    $a^n + b^n = (a + b)(a^{n-1} - a^{n-2}b + a^{n-3}b^2 + \dots - ab^{n-2} + b^{n-1})$

    - 右侧第二个括号内符号正负交替，可以理解根据$b$的幂数进行变更，$(-1)^s$，其中$s$是某项中$b$的幂数
    - 最后一项定位$+b^{n-1}$，因为$n$为奇数

- $n$为偶数时，涉及到复数

## 4.5 最大最小值和绝对值

- $max\{a, b\} = \frac 1 2 (a + b + |a - b|)$
- $min\{a, b\} = \frac 1 2 (a + b - |a - b|)$

## 4.6 AM-GM不等式

> 算数平均数大于等于几何平均数

若$a$、$b$ 非负实数，则有$\frac {a+b} {2} \ge 2\sqrt{ab}$

推广到任意个数，则有，对任意正数$a_1, a_2,\dots,a_n$，有$\frac {a_1 + a_2 + \cdots + a_n} {n} \ge \sqrt[n]{a_1a_2\cdots a_n}$

