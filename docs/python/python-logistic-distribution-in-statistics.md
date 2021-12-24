# Python–统计中的逻辑分布

> 原文:[https://www . geesforgeks . org/python-logistics-distribution-in-statistics/](https://www.geeksforgeeks.org/python-logistic-distribution-in-statistics/)

**scipy.stats.logistic()** 是一个 logistic(或 Sech 平方)连续随机变量。它继承自泛型方法的，作为 **rv_continuous 类**的实例。它用特定于这个特定分布的细节来完成这些方法。

**参数:**

> **q :** 上下尾概率
> T3】x:分位数
> **loc :** 【可选】位置参数。默认= 0
> **比例:**【可选】比例参数。默认值= 1
> **大小:**【整数元组，可选】形状或随机变量。
> **时刻:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**逻辑斯蒂(或平方)连续随机变量

**代码#1:创建逻辑(或秒平方)连续随机变量**

```
# importing library

from scipy.stats import logistic  

numargs = logistic.numargs 
a, b = 4.32, 3.18
rv = logistic(a, b) 

print ("RV : \n", rv)  
```

**输出:**

```
RV : 
 scipy.stats._distn_infrastructure.rv_frozen object at 0x000002A9D691AF48

```

 **代码#2:逻辑(或平方)连续变量和概率分布**

```
import numpy as np 
quantile = np.arange (0.03, 2, 0.21) 

# Random Variates 
R = logistic.rvs(a, b) 
print ("Random Variates : \n", R) 

# PDF 
R = logistic.pdf(a, b, quantile) 
print ("\nProbability Distribution : \n", R) 
```

**输出:**

```
Random Variates : 
 2.655712569915262

Probability Distribution : 
 [3.09335001e-48 2.86886306e-04 2.07194337e-02 7.76003172e-02
 1.34094156e-01 1.71154982e-01 1.89845362e-01 1.96114490e-01
 1.95030508e-01 1.89935182e-01]

```

**代码#3:图形表示。**

```
import numpy as np 
import matplotlib.pyplot as plt 

distribution = np.linspace(0, np.minimum(rv.dist.b, 3)) 
print("Distribution : \n", distribution) 

plot = plt.plot(distribution, rv.pdf(distribution)) 
```

**输出:**

```
Distribution : 
 [0\.         0.06122449 0.12244898 0.18367347 0.24489796 0.30612245
 0.36734694 0.42857143 0.48979592 0.55102041 0.6122449  0.67346939
 0.73469388 0.79591837 0.85714286 0.91836735 0.97959184 1.04081633
 1.10204082 1.16326531 1.2244898  1.28571429 1.34693878 1.40816327
 1.46938776 1.53061224 1.59183673 1.65306122 1.71428571 1.7755102
 1.83673469 1.89795918 1.95918367 2.02040816 2.08163265 2.14285714
 2.20408163 2.26530612 2.32653061 2.3877551  2.44897959 2.51020408
 2.57142857 2.63265306 2.69387755 2.75510204 2.81632653 2.87755102
 2.93877551 3\.        ]

```

![](img/5c5653319af994d3b79485b47a1fc85d.png)

**代码#4:变化的位置参数**

```
import matplotlib.pyplot as plt 
import numpy as np 

x = np.linspace(0, 5, 100) 

# Varying positional arguments 
y1 = logistic .pdf(x, 1, 3) 
y2 = logistic .pdf(x, 1, 4) 
plt.plot(x, y1, "*", x, y2, "r--") 
```

**输出:**

![](img/a57a2227dd039bd76638fe870912f38c.png)