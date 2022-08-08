---
layout: post
title: "Regression"
author: Cetus Li
date: 2022-08-04
---
#### **回归（Regression）**
- Predictor Variable，预测因子，用 X 指代。
- Criterion Variable，准则变量，用 Y 指代。
- 从 X 预测 Y 的方法叫做回归。
- 只有一个 X 的回归叫做简单回归（Simple Regression）。
- Y 作为 X 的函数，函数图像是一条直线的叫做线性回归。
- 真实数据（X,Y），真实的 Y 与通过回归方程用 X 得到的预测 Y' 的差值 （Y-Y'）叫做预测误差（error of prediction）。
- 到目前为止，最常用的最佳拟合线（回归函数线）标准是使预测误差平方和 SSE 最小的线。

#### **简单线性回归的计算**
在统计学软件中计算简单线性回归函数的方法（预测误差平方和最小的直线）：
1. 计算五个统计量：X、Y 各自的均值与标准差（Mean and Standard Deviation）和 X 与 Y 的相关系数 r ，即 $M_{X} ,M_{Y} ,S_{X} ,S_{Y} ,r$ 。
2. 斜率 $b=r\frac{S_{Y}}{S_{X}}$ 。
3. 截距 $A=M_{Y}-bM_{X}$ 。
4. 变量标准化后函数简化为 b = r and A = 0 。
5. 简单线性回归不需要条件假设。

**在推断统计中，通过样本推断总体参数的 b 和 A ，需要假设，假设如下：**

- 两个变量之间是线性关系。
- 具有方差齐性（Homoscedasticity），即数据的各处方差相同，理解为数据波动幅度稳定。
- 预测误差（error of prediction）呈正态分布。

在推断统计过程中，对样本 b 值做 t 检验，零假设是：X 与 Y 无相关性，b=0。 $t=\frac{b-0}{S_{b}}$ ， 自由度 df=N-2， b 值的标准差 $S_{b}$ 计算公式是:

$$S_{b}=\frac{S_{e}}{\sqrt{SSX}}=\frac{\sqrt{\frac{SSE}{df}}}{\sqrt{SSX}} ,df=N-2,SSX=\Sigma (X-M_{X})^2$$

对 Pearson 相关系数 r 做 t 检验，零假设是：r=0。 $t=\frac{r\sqrt{N-2}}{\sqrt{1-r^2}}$， 自由度 df=N-2 。


#### **平方和划分**
SSY 是 Y 的离均差平方和(每个值减去均值后平方的加和)。SSY' 是通过回归函数用 X 得到的预测值 Y' 的离均差平方和。SSE 是误差平方和 $\Sigma(Y-Y')^{2}$ 。他们之间具有关系：

$$SSY=SSY'+SSE$$

SSY、SSY' 和 SSE 分别是变量 Y,Y' 和 Y-Y' 的离均差平方和。他们除以各自的自由度就得到各自的方差 $\sigma^{2}$ ，关系仍为： 

$$\sigma ^{2} _{total}= \sigma ^{2} _{Y}=\sigma ^{2} _{Y'}+\sigma ^{2} _{e}$$

SSY' 是 SSY 被解释的部分，SSE 是 SSY 未解释的部分。X 与 Y 的 Pearson 相关系数 r 和SSY 被解释比例具有关系：

$$r^{2} =\frac{SSY'}{SSY} =\frac{\sigma _{Y'}^{2}}{\sigma _{total}^{2}} $$



