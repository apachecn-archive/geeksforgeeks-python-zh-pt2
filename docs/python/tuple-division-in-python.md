# Python 中的元组划分

> 原文:[https://www.geeksforgeeks.org/tuple-division-in-python/](https://www.geeksforgeeks.org/tuple-division-in-python/)

有时，在处理记录时，我们可能会遇到一个问题，即我们可能需要跨元组执行数学除法运算。这个问题可能发生在日常编程中。让我们讨论执行这项任务的某些方法。

**方法#1:使用`zip()` +生成器表达式**
以上功能的组合可用于执行该任务。在这种情况下，我们使用生成器表达式执行划分任务，每个元组的映射索引由 zip()完成。

```
# Python3 code to demonstrate working of 
# Tuple division
# using zip() + generator expression 

# initialize tuples 
test_tup1 = (10, 4, 6, 9) 
test_tup2 = (5, 2, 3, 3) 

# printing original tuples 
print("The original tuple 1 : " + str(test_tup1)) 
print("The original tuple 2 : " + str(test_tup2)) 

# Tuple division 
# using zip() + generator expression 
res = tuple(ele1 // ele2 for ele1, ele2 in zip(test_tup1, test_tup2)) 

# printing result 
print("The divided tuple : " + str(res)) 
```

**Output :**

```
The original tuple 1 : (10, 4, 6, 9)
The original tuple 2 : (5, 2, 3, 3)
The divided tuple : (2, 2, 2, 3)

```