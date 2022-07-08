---
layout: post
title: "Statistics Introduction"
author: Cetus Li
date: 2022-06-07
---
####  <b>统计学介绍</b>
- <b>WHAT:</b> “Statistics” refers to a range of techniques and procedures for analyzing, interpreting, displaying, and making decisions based on data.
- <b>WHY:</b> Take control of your life, it means being able to properly evaluate the data and claims that bombard you every day. If you cannot distinguish good from faulty reasoning, then you are vulnerable to manipulation and to decisions that are not in your best interest. Statistics provides tools that you need in order to react intelligently to information you hear or read.

####  <b>统计学内容</b>
- <b>描述性统计：</b> descriptive statistics, 使用数字来总结和描述数据，不涉及通过现有数据去推广结论。
- <b>推断统计：</b> inferential statistics, 取总体数据的子集作为样本，分析得出结论，推广到总体，且推广必须具有合理性。保证这个合理性是统计学很重要的一部分。

####  <b>关于从样本到总体的合理性</b>
1. 简单随机取样，需要关心样本量大小和该样本代表总体和偏离总体的概率。（对总体进行无限数次采样，样本分布呈正态分布，一个样本作为最具代表性的峰值分布还是偶然事件的极值分布的概率分别是多少）
2. 复杂取样，如一种是从简单随机取样中再次进行随机分配，一种是按比例进行分层随机取样，还有其他复杂取样。
3. 明确正确的总体范围。
4. 明确推断的可信度，即推断的结论适用于总体的概率。

#### <b>百分位数</b>
百分位数（percentile）是全部数据由小到大排列后，每个数都有自己的秩（从1到N，N是数据总量），取 N 的百分之 M 为秩，所对应的数就是第 M 百分位数。
<br/><br/><b>`举例：`</b> 100名学生的数学成绩的第85百分位数（85th percentile）就是分数由低到高第85名同学的数学成绩。
<br/><br/>
<b>最常用的计算公式</b>
- 取 N+1 的百分之 M 为秩:  R = $(N+1)\times \frac{M}{100}$ , R 的整数部分叫 IR，小数部分叫 FR. （例如 R=2.25，则 IR=2，FR=0.25）
- 若 FR 为0，秩为 IR 的数就是第 M 百分位数。
- 若 FR 不为0，`第 M 百分位数 = 秩为 IR 的数 + [秩为 (IR+1) 的数 - 秩为 IR 的数]*FR`.

#### <b>统计量的刻度类型</b>
1. 名称型，Nominal scales，各个刻度之间无大小关系，如喜欢的颜色。
2. 顺序型，Ordinal scales，各个刻度之间有大小关系，但是各项之间的差无法量化，如对多个电视剧喜欢的程度。
3. 间隔型，Interval scales，各个刻度之间有大小关系，相邻刻度有相同的间隔，但是没有绝对0项，各项之间不能根据大小算比例关系，如不知道起点的田径比赛中多个运动员之间的相对距离。
4. 比率型，Ratio scales，各个刻度之间有大小关系，相邻刻度有相同的间隔，有绝对0项，各项之间有比率关系，如知道起点的田径比赛中多个运动员的绝对距离。

#### <b>分布</b>
1. 离散变量的频数分布和比例（概率）分布都是柱形图。
2. 连续变量的频数分布是直方图，连续变量的概率分布是曲线图（典型的就是正态分布，normal distribution），又叫概率密度图。
3. 分布图右侧尾巴过长峰值偏左叫做向右倾斜、正倾斜（skewed to the right），左边尾巴过长峰值偏右叫做向左倾斜、负倾斜（skewed to the left）。
4. 有两个峰值的分布叫做双峰分布（bimodal distribution）。
5. 关于分布的峰度（kurtosis）:与正太分布相比，中间高，两侧尾巴小的叫做尖峰分布（leptokurtic）；中间平缓，两侧尾巴大的叫做扁峰分布（platykurtic）。


------
#### <b>题外话</b>
虽然不被所有统计学者接受，但是，几乎在所有实际情况下，顺序型（Ordinal scale） 刻度的均值是有意义的统计数据。但某些情况下，如此计算具有误导性，因为顺序型刻度各项之间的差无法量化。

数据在可数时，data 是复数，单数是 datum.

参考：莱斯大学的 David Lane 助理教授开发的[在线统计学课程][website]



[website]: https://onlinestatbook.com/
[ebook]: https://onlinestatbook.com/Online_Statistics_Education.pdf
