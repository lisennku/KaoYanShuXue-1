# 1. 基础知识

## 1.1 弧度与度

- 弧度和度，都是用来衡量角大小的单位
  - 度，是将完整的圆平均分为360， 每一份都是1度，记为$1^\circ$
  - 弧度，是指在一个半径为$r$的圆中，弧长$s$对应的角的大小，记为$\theta$，单位为$rad$
    - 一个圆的$360^{\circ}$等于$2\pi$弧度
    - 常用弧度

      - $\frac {\pi} 6 = 30^{\circ}$
      - $\frac {\pi} 4 = 45^{\circ}$
      - $\frac {\pi} 3 = 60^{\circ}$
      - $\frac {\pi} 2 = 90^{\circ}$
- 弧度与度换算
  - 记弧度为$\theta$，度为$d$，则有
    - $\theta = d \times  {\frac {\pi} {180}}$
    - $d = \theta \times \frac {180} {\pi}$
    - ![image-20241111145125301](<chap 2 三角学回顾.assets/image-20241111145125301.png>)

## 1.2 基本三角函数 $[0, \frac {\pi} 2]$

在直角三角形中，除直角外的一角，记为$\theta$，则有

- 正弦 $sin(\theta) = \frac {对边} {斜边}$
- 余弦 $cos(\theta) = \frac {邻边} {斜边}$
- 正切 $tan(\theta) = \frac {对边} {邻边}$
- 正割 $csc(\theta) = \frac 1 {sin(\theta)}$
- 余割 $sec(\theta) = \frac 1 {cos(\theta)}$
- 余切 $cot(\theta) = \frac 1 {tan(\theta)}$

## 1.3 扩展到$[0, 2\pi]$的三角函数

- 参考角
    - 一般来说，$\theta$的参考角，是在表示$\theta$的射线和$x$轴之间最小的角
- ASTC方法
    - 指的是将坐标轴从右上逆时针开始，每个象限内为正数的三角函数(正弦、余弦、正切)
        - A 表示第一象限内，三个都是正数
        - S 表示第二象限内，$sin$为正数
        - T 表示第三象限内，$tan$为正数
        - C 表示第四象限内，$cos$为正数

## 1.4 $[0, 2\pi]$以外的三角函数

- 减去$2\pi$的倍数即可，或者求补角

## 1.5 函数图像

- 三角函数的函数图像是周期性的，其中$sin$、$cos$、$csc$、$sec$是以$2\pi$为周期的函数，$tan$、$cot$是以$\pi$为周期的函数
- $sin$、$csc$、$tan$、$cot$是奇函数
- $cos$、$sec$是偶函数
    - ![alt text](<chap 2 三角学回顾.assets/image-20241111151433635.png>)
    - ![alt text](<chap 2 三角学回顾.assets/image-20241111151446651.png>)
    - <img src="chap 2 三角学回顾.assets/image-20241111151516484.png" alt="image-20241111151516484" style="zoom: 80%;" />
    - ![image-20241111151744395](<chap 2 三角学回顾.assets/image-20241111151744395.png>)
    - ![image-20241111151752508](<chap 2 三角学回顾.assets/image-20241111151752508.png>)
    - ![image-20241111151759155](<chap 2 三角学回顾.assets/image-20241111151759155.png>)

## 1.6 三角恒等式

### 1.6.1 用正弦余弦表示正切余切

- $tan(x) = \frac {\sin(x)} {cos(x)}$
- $cot(x) = \frac {\cos(x)} {sin(x)}$

### 1.6.2 毕达哥拉斯定理

- $sin^2(x) + cos^2(x) = 1$

- 两边同时除以$cos^2(x)$，可得
    - $1 + tan^2(x) = \frac 1 {cos^2(x)} = sec^2(x)$
- 两边同时除以$sin^2(x)$，可得
    - $1 + cot^2(x) = \frac 1 {sin^2(x)} = csc^2(x)$

### 1.6.3 互余

不带有`co`的三角函数，$sin$、$tan$、$sec$，和带有`co`的三角函数是互余的关系，当两个自变量相加等于$\frac {\pi} 2$时，他们的值相等

也即：

- $sin(x) = cos(\frac {\pi} 2 - x)$
- $tan(x) = cot(\frac {\pi} 2 - x)$
- $sec(x) = csc(\frac {\pi} 2 - x)$

反之也成立：

- $cos(x) = sin(\frac {\pi} 2 - x)$
- $cot(x) = tan(\frac {\pi} 2 - x)$
- $csc(x) = sec(\frac {\pi} 2 - x)$

### 1.6.4 和差公式

- 和公式

    - $sin(\alpha + \beta) = sin(\alpha)cos(\beta) + cos(\alpha)sin(\beta)$

    - $cos(\alpha + \beta) = cos(\alpha)cos(\beta) - sin(\alpha)sin(\beta)$
    - 推导过程
        - <img src="chap 2 三角学回顾.assets/baeb959cd696afe9c888f38b4866829.jpg" alt="baeb959cd696afe9c888f38b4866829" style="zoom:33%;" />

- 差公式

    - $sin(\alpha - \beta) = sin(\alpha)cos(\beta) + cos(\alpha)sin(\beta)$

    - $cos(\alpha - \beta) = cos(\alpha)cos(\beta) + sin(\alpha)sin(\beta)$
    - 通过$sin(\alpha - \beta) = sin(\alpha + (- \beta))$和$cos(\alpha - \beta) = cos(\alpha + (- \beta))$并结合$sin/cos$奇偶性即可推导出

### 1.6.5 倍角公式

- 将和公式中的$\alpha,\beta$替换为一样的角即可得出倍角公式
- $sin(2\alpha) = 2sin(\alpha)cos(\alpha)$
- $cos(2\alpha) = cos^2(\alpha) - sin^2(\alpha)$
    - 结合毕达哥拉斯公式，可知
        - $cos(2\alpha) = 2cos^2(\alpha) - 1$
        - 或
        - $cos(2\alpha) = 1 - 2sin^2(\alpha)$

### 1.6.6 半角公式

- 正弦：$ \sin\left(\frac{\theta}{2}\right) = \pm \sqrt{\frac{1 - \cos(\theta)}{2}} $
- 余弦： $\cos\left(\frac{\theta}{2}\right) = \pm \sqrt{\frac{1 + \cos(\theta)}{2}} $
- 正切： $\tan\left(\frac{\theta}{2}\right) = \frac{1 - \cos(\theta)}{\sin(\theta)} = \frac{\sin(\theta)}{1 + \cos(\theta)}$

- 证明过程
    - <img src="chap 2 三角学回顾.assets/12aa1aec4f87cf02ca9fc14e68476bf.jpg" alt="12aa1aec4f87cf02ca9fc14e68476bf" style="zoom:33%;" />





















​		
