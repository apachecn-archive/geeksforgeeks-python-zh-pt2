# python–列表中的 i^k 产品

> 原文:[https://www.geeksforgeeks.org/python-product-of-ik-in-list/](https://www.geeksforgeeks.org/python-product-of-ik-in-list/)

Python 作为魔术师的语言，可以用来以简单明了的方式执行许多繁琐和重复的任务，拥有充分利用这一工具的知识总是有用的。一个这样的小应用程序可以在一行中找到 i^k 的产品。让我们讨论一下实现这一点的某些方法。

**方法#1:使用`reduce() + lambda + pow()`**
lambda 函数的力量在一行中执行冗长的任务，允许它与用于累积子问题的 reduce 相结合，也执行这个任务。power()用于执行计算能力任务。仅适用于 Python 2。

```
# Python code to demonstrate 
# Product of i ^ k in List
# using reduce() + lambda + pow() 

# initializing list 
test_list = [1, 3, 5, 7, 9, 11] 

# printing original list 
print ("The original list is : " + str(test_list)) 

# initializing K 
K = 4

# using reduce() + lambda + pow() 
# Product of i ^ k in List 
res = reduce(lambda i, j: i * pow(j, K), [pow(test_list[:1][0], K)] + test_list[1:]) 

# printing result 
print ("The product of i ^ k of list is : " + str(res)) 
```

**Output :**

```
The original list is : [1, 3, 5, 7, 9, 11]
The product of i ^ k of list is : 11676104538800625

```