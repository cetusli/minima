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
- 到目前为止，最常用的最佳拟合线（回归函数线）标准是使预测误差平方和最小的线。

#### **简单线性回归的计算**
在统计学软件中计算简单线性回归函数的方法（预测误差平方和最小的直线）：
1. 计算五个统计量：X、Y 各自的均值与标准差（Mean and Standard Deviation）和 X 与 Y 的相关系数 r ，即 $M_{X} ,M_{Y} ,S_{X} ,S_{Y} ,r$ 。
2. 斜率 $b=r\frac{S_{Y}}{S_{X}}$ 。
3. 截距 $A=M_{Y}-bM_{X}$ 。
4. 变量标准化后函数简化为 b = r and A = 0 。



