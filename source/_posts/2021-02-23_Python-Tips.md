---
title: Python Tips
tags:
  - Python
mathjax: true
abbrlink: dcbfa745
date: 2021-02-23 09:35:44
---

**Abstract:**

<!-- more -->

## 1. Introduction

## 2. Tips for Pandas
```python
import pandas as pd

# On DataFrame
## Create DF

# Date series
dates = pd.date_range(start='2020-01-01', end='2020-01-10', freq='5D')
"""
DatetimeIndex(['2020-01-01', '2020-01-06'], dtype='datetime64[ns]', freq='5D')
"""
dates = pd.date_range(start='2020-01-01', periods=10, freq='D')
"""
DatetimeIndex(['2020-01-01', '2020-01-02', '2020-01-03', '2020-01-04',
               '2020-01-05', '2020-01-06', '2020-01-07', '2020-01-08',
               '2020-01-09', '2020-01-10'],
              dtype='datetime64[ns]', freq='D')
"""
```

## 3. Tips for Xarray
```python

```

## 4. Tips for Cartopy
```python

```

**References:**       
1. [cartopy 绘制中国地图，南海诸岛和十段线](https://blog.csdn.net/weixin_42355670/article/details/106007204)           
2. [Cartopy绘图 | 中国地图最正确的使用方式](https://www.kesci.com/mw/project/5f3c95a3af3980002cbf560b)            
3. [小白学习cartopy画地图的第一天](https://blog.csdn.net/weixin_42372313/article/details/113572786)              
4. [Python兰伯特投影中国区域等值线图](https://my.oschina.net/u/4579695/blog/4879010)           
5. [How to remove latitude labels in x axis in cartopy 0.18](https://github.com/SciTools/cartopy/issues/1530)         
 
## 5. Tips for Basemap
```python

```

## 6. Tips for Numpy
```python

```