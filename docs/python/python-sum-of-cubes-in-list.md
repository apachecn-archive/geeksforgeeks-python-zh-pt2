# Python–列表中立方体的总和

> 原文:[https://www.geeksforgeeks.org/python-sum-of-cubes-in-list/](https://www.geeksforgeeks.org/python-sum-of-cubes-in-list/)

Python 作为魔术师的语言，可以用来以简单明了的方式执行许多繁琐和重复的任务，拥有充分利用这一工具的知识总是有用的。一个这样的小应用程序可以在一行中找到列表立方体的总和。让我们讨论一下实现这一点的某些方法。

**方法#1:使用`reduce()`+lambda**
lambda 函数在一行中执行冗长任务的能力，允许它与用于累积子问题的 reduce 相结合来执行该任务。仅适用于 Python 2。

```py
# Python code to demonstrate 
# Cube Summation in List
# using reduce() + lambda

# initializing list
test_list = [3, 5, 7, 9, 11]

# printing original list 
print ("The original list is : " + str(test_list))

# using reduce() + lambda
# Cube Summation in List
res = reduce(lambda i, j: i + j * j*j, [test_list[:1][0]**3]+test_list[1:])

# printing result
print ("The sum of cubes of list is : " + str(res))
```

**Output :**

```py
The original list is : [3, 5, 7, 9, 11]
The sum of cubes of list is : 2555

```