# Python |元组列表中的最大元素

> 原文:[https://www . geesforgeks . org/python-元组列表中的最大元素/](https://www.geeksforgeeks.org/python-maximum-element-in-tuple-list/)

有时，在处理记录形式的数据时，我们可能会遇到一个问题，即我们需要找到收到的所有记录的最大元素。这是数据科学领域中非常常见的应用。让我们讨论执行这项任务的某些方法。

**方法#1:使用`max()` +生成器表达式**
这是实现解决这个任务最基本的方法。在本文中，我们使用生成器表达式迭代整个嵌套列表，并使用 max()获得最大元素。

```py
# Python3 code to demonstrate working of
# Maximum element in tuple list
# using max() + generator expression

# initialize list 
test_list = [(2, 4), (6, 7), (5, 1), (6, 10), (8, 7)]

# printing original list 
print("The original list : " + str(test_list))

# Maximum element in tuple list
# using max() + generator expression
res = max(int(j) for i in test_list for j in i)

# printing result
print("The Maximum element of list is : " + str(res))
```

**Output :**

```py
The original list : [(2, 4), (6, 7), (5, 1), (6, 10), (8, 7)]
The Maximum element of list is : 10

```