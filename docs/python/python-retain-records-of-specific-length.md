# Python |保留特定长度的记录

> 原文:[https://www . geeksforgeeks . org/python-保留特定长度的记录/](https://www.geeksforgeeks.org/python-retain-records-of-specific-length/)

有时，在处理记录时，我们可能希望以这样一种方式过滤记录，即我们需要丢弃不包含构成记录所需的确切元素数的记录。让我们讨论执行这项任务的某些方法。

**方法#1:使用列表理解+ `len()`**
在该方法中，我们只需遍历列表，丢弃与构成记录所需的匹配长度不匹配的元组。长度的计算由`len()`完成。

```
# Python3 code to demonstrate working of
# Retain records of specific length
# Using list comprehension + len()

# Initializing list
test_list = [(4, 5, 6), (5, 6), (2, 3, 5), (5, 6, 8), (5, 9)]

# printing original list
print("The original list is : " + str(test_list))

# Initializing desired length 
N = 3

# Retain records of specific length
# Using list comprehension + len()
res =  [sub for sub in test_list if len(sub) == 3]

# printing result
print("The tuple list after removing uneven records: " + str(res))
```

**Output :**

```
The original list is : [(4, 5, 6), (5, 6), (2, 3, 5), (5, 6, 8), (5, 9)]
The tuple list after removing uneven records: [(4, 5, 6), (2, 3, 5), (5, 6, 8)]

```