# python 中的 zlib . compress

> 原文:[https://www.geeksforgeeks.org/zlib-compresss-in-python/](https://www.geeksforgeeks.org/zlib-compresss-in-python/)

借助`**zlib.compress(s)**`方法，我们可以通过`zlib.compress(s)`方法得到压缩的字符串字节。

> **语法:** `zlib.compress(string)`
> **返回:**返回压缩字符串。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`zlib.compress(s)`方法，我们能够使用该方法将字符串压缩为字节格式。

```py
# import zlib and compress
import zlib
s = b'This is GFG author, and final year student.'
print(len(s))

# using zlib.compress(s) method
t = zlib.compress(s)
print(len(t))
```

**输出:**

> 43
> 49

**例 2 :**

```py
# import zlib and compress
import zlib
s = b'GeeksForGeeks@12345678'
print(len(s))

# using zlib.compress(s) method
t = zlib.compress(s)
print(len(t))
```

**输出:**

> 22
> 27