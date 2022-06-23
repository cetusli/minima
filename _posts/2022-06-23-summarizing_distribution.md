---
layout: post
title: "Summarizing Distributions"
author: Cetus Li
date: 2022-06-23
---
#### <b>分布的中心趋势</b>
找到一个分布对应的变量的中心有三种思路：1、把数据顺序排列，找到平衡点；2、找到使绝对偏差和最小的数；3、找到使方差和最小的数。
<br/>常用的表征数据中心的度量：
- 均值（mean），也叫算术平均值。
- 中位数（median），数字按从小到大顺序排列，中间的数或者中间两数的均值。
- 三均值（trimean），`（第25百分位数+第50百分位数*2+第75百分位数）/4`.
- 截尾均值（trimmed mean），A mean trimmed 20% is trimming 10% off the data from each tail.
- 众数（mode），出现次数最多的数。
- 几何均值（geometric mean），所有数相乘后再取1/N次幂。

#### <b>分布的离散程度</b>
- 全距（range），等于分布中最大数减去最小数。
- 四分位间距（interquartile range, IQR），`IQR = 75th percentile - 25th percentile`，即第75百分位数减去第25百分位数。
- 绝对偏差（absolute deviation），每个数与中心数的距离的平均值。
- 方差（variance），每个数与中心数的距离的平方的平均值。
- 标准偏差（standard deviation）,也叫标准差，是方差的平方根。
- 绝对偏差和（the sum of the absolute deviations），每个数与中心数的距离的加和。
- 方差和（the sum of the squared deviations），每个数与中心数的距离的平方的加和。

#### <b>分布的偏移度和峰度</b>
- 偏移度（skew），计算方法1之Pearson法：`3（mean-median）/标准差` ;计算方法2之最常用法：`((X-均值)^3/标准差^3)的连续加和`。
- 峰度（kurtosis），计算方法：`((X-均值)^4/标准差^4)的连续加和-3` （3是正态分布的峰度，减去3代表默认正态分布无峰度）。

#### <b>方差和定律</b>
两个独立变量相加或者相减得到的新变量的方差，都等于这两个独立变量各自的方差之和。`variance(X+or-Y)=variance(X)+variance(Y)`

#### <b>其他定律</b>
1. 所有数全部加上同一个数，均值也会加上这个数，方差不会变，标准差不会变。
2. 所有数全部乘以同一个数，均值也会乘以这个数，方差会乘以这个数的平方，标准差只会乘以这个数。
3. 使绝对偏差和最小的数是中位数 median。
4. 使数据平衡以及方差和最小的数是算术平均值 mean。
5. 只在对称分布中 mean 等于 median，正偏移分布中 mean 大于 median.

------
#### <b>题外话</b>
假定样本的方差总是小于总体方差的。那么，在使用样本方差来推断/估计/表征总体方差时，会低估总体的方差，所有在计算（每个数与中心数的距离的平方的平均值）时，把求平均步骤中的 `N` 改为 `N-1`来达到增大样本方差的效果，使之更能代表总体方差。
