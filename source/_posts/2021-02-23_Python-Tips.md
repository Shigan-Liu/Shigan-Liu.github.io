---
title: Python Tips
tags:
  - Python
mathjax: true
abbrlink: dcbfa745
date: 2021-02-23 09:35:44
---

Scientific computing, plotting, and data IO highly rely on packages in python. However,  there are much many specific and trivial methods and functions and they sometimes designed in quite different form in different packages, which are hard to memory. Therefore, I wrote this post to aid the usage of some important packages. It is assumed that readers have basic knowledge of python and those packages.

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
dates = [str(i).split(' ')[0].replace('-', '') for i in dates]
"""
['20170101', '20170102', '20170103', '20170104', '20170105', '20170106', '20170107', '20170108', '20170109', '20170110']
"""
```

**References:**       

## 3. Tips for Xarray
```python
import Xarray as xr

# NetCDF File IO

```

**References:**       

## 4. Tips for Cartopy
```python
import cartopy.crs as ccrs
```

**References:**       
1. [cartopy 绘制中国地图，南海诸岛和十段线](https://blog.csdn.net/weixin_42355670/article/details/106007204)           
2. [Cartopy绘图 | 中国地图最正确的使用方式](https://www.kesci.com/mw/project/5f3c95a3af3980002cbf560b)            
3. [小白学习cartopy画地图的第一天](https://blog.csdn.net/weixin_42372313/article/details/113572786)              
4. [Python兰伯特投影中国区域等值线图](https://my.oschina.net/u/4579695/blog/4879010)           
5. [How to remove latitude labels in x axis in cartopy 0.18](https://github.com/SciTools/cartopy/issues/1530)         
 
## 5. Tips for Basemap
```python
from mpl_toolkits.base import Basemap
import matplotlib.pyplot as plt
```

**References:**       

## 6. Tips for Numpy
```python
import numpy as np
```

**References:**       

## 7. Tips for SciPy
```python
import scipy

# Regression
```

**References:**       

## 8. Tips for PyTorch
```python
import torch
```

**References:**       

## 9. Tips for Calendar, Datetime, and Time
```python
import calendar
import datetime as dt
import time

# Datetime <=> String
```

**References:**       

## 10. Tips for MatPlotLib and Seaborn
```python
import matplotlib.pyplot as plt
import seaborn as sbn

plt.rcParams['font.sans-serif']=['SimHei'] # To support Chinese character
plt.rcParams['axes.unicode_minus']=False # To display minus 

# Bar Chart

# Pie Chart

# Line Plot

# Scatter Plot

# Color Bar Settings

# Legend Settings

# Design Axes
```

**References:**       