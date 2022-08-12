---
layout: post
title: "Transformations"
author: Cetus Li
date: 2022-08-12
---
#### **转换（Transformations）**
- 数据准备的时间超过整个数据分析时间的 90% 以上。
- 变量测量尺度的选择是数据准备工作的一部分。
- 变量的线性变换（尺度选择）不会影响相关系数，相关系数不要求变量具有正态分布。
- 有时候变量换一种表达形式，变量之间的关系会更加清晰，比如用对数形式可以得到线性关系（关系清晰）。
- 数据转换可以解决正态分布的偏移（skew）问题，避免假设数据正态分布的假设扰动。
- 对数转换是图基幂阶（Tukey’s ladder of powers）变换的一个特列。 λ=0 时，指定为求对数 log(x)，而不是 $x^0=1$ （这样做的原因涉及高等数学洛必达法则 L'Hpital's rule）。
- 还有一些更高级的转换，比如 the Box-Cox transformation 。


#### **图基幂阶（Tukey Ladder of Powers）**
Tukey（1977）描述了使用幂变换有序地重新表达变量，并以此找到一个显示线性关系的变换。图基变换的定义：

$$\tilde{x}_{\lambda} =\begin{cases}
 x^{\lambda }  & \text{ if } \lambda >0 \\
 \log_{}{x}  & \text{ if } \lambda =0 \\
 -(x^{\lambda }) & \text{ if } \lambda <0
\end{cases}$$

1. 对于二元数据 （x, y），其中一个变量做了某个 λ 的图基变化后变成 $\tilde{x}$ 或者 $\tilde{y}$ ，我们的目的是找到使（ $\tilde{x}$ ,y）或者（x, $\tilde{y}$ ） 的相关系数 r 最大的 λ 。 作 r 与 λ 的关系图，图中 r 最大值对应的 λ 值就是我们要找的 λ 。（0 $\le$ |r| $\le$ 1 ，|r|=1 时，新数据的散点图是一条直线。）
2. 对于分布有偏移（skewness）的变量 X ，通过简单变换后可以消除偏移变成近正态分布，我们的目的是找到使  $\tilde{X}$ 的正态分布 Q-Q 图最接近直线的 λ 。正态分布 Q-Q 图中数据对应的相关系数为 r ，作 r 与 λ 的关系图，图中 r 最大值对应的 λ 值就是我们要找的 λ 。


#### **Box-Cox变换（Box-Cox Transformations）**

$$\tilde{x}_{\lambda}=\frac{x^\lambda -1}{\lambda} $$

图基变换的所有 λ 对应的图线都经过点 （0， 0），Box-Cox变换的所有 λ 对应的图线都经过点 （1， 0）。


**举例：**
多项式方程作为多元方程的一种，在回归到这种形式时，有没有一种如下的更简洁形式呢？

$$y=b_{0}+b_{1}x+b_{2}x^2+...+b_{n}x^n \Rightarrow y=b_{0}+b_{1}x^\lambda \parallel y^\lambda =b_{0}+b_{1}x$$

其中 λ 是一个参数，选择一个可使 x 与 y 关系尽可能接近直线的 λ 。找到了符合的表达式，可以把 x 转换后再做数据分析，因为线性关系在分析数据和回答问题中是很特殊的。

