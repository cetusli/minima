---
layout: post
title: "Sampling Distributions"
author: Cetus Li
date: 2022-07-14
---

#### **抽样分布（Sampling Distributions）**
假设我们关注总体的某个特征，或者两个总体之间的关系，首先找到有效度的统计量，然后通过抽样计算出该统计量。多次抽样得到该统计量的多个值构成该统计量的抽样分布。
1. 均值的抽样分布（Sampling Distribution of the Mean）是均值为 $\mu_{m}$ ，方差为 $\sigma_{m}^2$ 的近似正态分布。$\mu_{m}=\mu$，$\sigma_{m}^2=\frac{\sigma^2}{N}$。即使总体不是正态分布，抽样分布也会是近似正态分布，而且样本量 N 越大，抽样分布越接近正态分布。
2. 均值差的抽样分布（Sampling Distribution of Difference Between Means）是均值为 $\mu_{m_{1}-m_{2}}=\mu_{1}-\mu_{2}$ ，方差为 $\sigma_{m_{1}-m_{2}}^2=\sigma_{m_{1}}^2+\sigma_{m_{2}}^2=\frac{\sigma_{1}^2}{N_{1}}+\frac{\sigma_{2}^2}{N_{2}}$ 的近似正态分布。
3. 相关系数的抽样分布（Sampling Distribution of Pearson's r）是以真实系数 r 为均值，0-1 为界限的偏移分布。统计学家 Fisher 发明了把 r 转换成正态分布变量的方法，新变量 z 的正态分布的标准差是 $\frac{1}{\sqrt{N-3}}$，N 是抽样次数，也是计算相关系数的数据对个数。

$$ z=\frac{1}{2} ln[\frac{1+r}{1-r} ] $$

 4. 比例的抽样分布（Sampling Distribution of p），可以理解成二项分布的延伸。二项分布的变量是 `N 次事件中结果为 A 的次数`，比例的抽样分布的变量是 `N 次事件中结果为 A 的比例（A 的次数/总次数 N）`。所以比例的抽样分布的均值和标准差就是二项分布的均值和标准差除以 N。均值为 $\mu_{p}=N\pi/N=\pi$ ，标准差为 $\sigma_{p}=\frac{\sqrt{N\pi(1-\pi)}}{N} =\sqrt{\frac{\pi(1-\pi)}{N}}$



