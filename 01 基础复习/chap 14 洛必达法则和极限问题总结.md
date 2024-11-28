# 1. 洛必达法则

## 1.1 洛必达法则应用场景

- 类型A
    - 如果极限是==分式==的形式，如$\displaystyle \lim_{x \to a} \frac {f(x)} {g(x)}$，带入$a$后，如果是不定式，也即$\frac 0 0$或$\frac {\pm \infty}{\pm \infty}$，可以使用洛必达法则
    - $\displaystyle \lim_{x \to a} \frac {f(x)} {g(x)} \stackrel{l'H}{=} \displaystyle \lim_{x \to a} \frac {f^{\prime}(x)} {g^{\prime}(x)}$
- 类型B1
    - 如果极限是==求差==的形式，如$\displaystyle \lim_{x \to a} f(x)-g(x)$，带入$a$后，如果是$\pm(\infty - \infty)$，可以采取==通分==，或者==乘以共轭表达式==的形式，转换为类型A，从而应用洛必达法则
    - 如果是加和的形式，也即$\infty + \infty$，其结果是确定的，也即$\infty$
    - 只有求差的时候，因为是无穷大减掉无穷大，其结果是不确定的
- 类型B2
    - 如果极限是乘积的形式，如$\displaystyle \lim_{x \to a} f(x)g(x)$，带入$a$后，如果是$0 \times \pm \infty$，选择两个因式中较为简单的==取倒数放到分母==，转换为类型A，从而应用洛必达法则
    - $\displaystyle \lim_{x \to a} f(x)g(x) \stackrel {l'H} {=} \displaystyle \lim_{x \to a} \frac {g(x)} {\frac 1 {f(x)}}$
- 类型C
    - 如果极限是指数形式，且底和指数都包含变量，如$\displaystyle \lim_{x \to a} f(x)^{g(x)}$，带入$a$后如果是不定式形式，也即$1^{\pm \infty}$或$\infty^0$或$0^0$，则==先取对数==转换为类型A或类型B2，计算出极限后==再取指数==恢复为原函数的极限

## 1.2 类型A $\frac 0 0$

![image-20241128093157861](<chap 14 洛必达法则和极限问题总结.assets/image-20241128093157861.png>)

## 1.3 类型A $\frac {\pm \infty}{\pm \infty}$

![image-20241128093217627](<chap 14 洛必达法则和极限问题总结.assets/image-20241128093217627.png>)

## 1.4 类型B1 $\pm(\infty - \infty)$

<img src="chap 14 洛必达法则和极限问题总结.assets/image-20241128093233597.png" alt="image-20241128093233597" style="zoom:80%;" />

## 1.5 类型B2 $0 \times \pm \infty$

<img src="chap 14 洛必达法则和极限问题总结.assets/image-20241128100227737.png" alt="image-20241128100227737" style="zoom:80%;" />

## 1.6 类型C  $1^{\pm \infty}$或$\infty^0$或$0^0$

![image-20241128100305068](<chap 14 洛必达法则和极限问题总结.assets/image-20241128100305068.png>)

![image-20241128100323562](<chap 14 洛必达法则和极限问题总结.assets/image-20241128100323562.png>)

![image-20241128100338503](<chap 14 洛必达法则和极限问题总结.assets/image-20241128100338503.png>)

