---
layout: post
title: "sql 函数"
author: Cetus Li
date: 2022-09-26
---
### 排名
前两个数相同的 5 个数排名：
- DENSE_RANK()。如果使用 DENSE_RANK() 进行排名会得到：1，1，2，3，4。
- RANK()。如果使用 RANK() 进行排名会得到：1，1，3，4，5。
- ROW_NUMBER()。如果使用 ROW_NUMBER() 进行排名会得到：1，2，3，4，5。
