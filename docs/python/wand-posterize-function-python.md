# 魔杖后置()功能–Python

> 原文:[https://www . geesforgeks . org/wand-posterize-function-python/](https://www.geeksforgeeks.org/wand-posterize-function-python/)

**posterize()** 函数是 Python Wand ImageMagick 库中的一个内置函数，用于降低每个通道的颜色级别。

> **语法:**
> 
> ```
> posterize(level, dither)
> ```
> 
> **参数:**该功能接受三个参数，如上所述，定义如下:
> 
> *   **级别:**该参数存储每个通道的级别数。
> *   **抖动:**该参数存储要应用的抖动方法。一些可用的方法是' undefined '，' no '，' riemersma '，' floyd_steinberg '。
> 
> **返回值:**该函数返回魔杖图像图像对象。

**原图:**

![](img/2d3a0fdbc25c0bbb46c47454d1b0acc7.png)

**例 1:**

## 蟒蛇 3

```
# Import library from Image
from wand.image import Image

# Import the image
with Image(filename ='../geeksforgeeks.png') as image:
    # Clone the image in order to process
    with image.clone() as posterize:
        # Invoke posterize function
        posterize.posterize(2, 'no')
        # Save the image
        posterize.save(filename ='posterize1.jpg')
```

**输出:**

![](img/e7e9fcd4d279704c33dd2d1910391adf.png)

**例 2:**

## 蟒蛇 3

```
# Import libraries from the wand 
from wand.image import Image
from wand.drawing import Drawing
from wand.color import Color

with Drawing() as draw:
    # Set Stroke color the circle to black
    draw.stroke_color = Color('black')
    # Set Width of the circle to 2
    draw.stroke_width = 1
    # Set the fill color to 'White (# FFFFFF)'
    draw.fill_color = Color('white')

    # Invoke Circle function with center at 50, 50 and radius 25
    draw.circle((200, 200), # Center point
                (100, 100)) # Perimeter point
    # Set the font style
    draw.font = '../Helvetica.ttf'
    # Set the font size
    draw.font_size = 30

    with Image(width = 400, height = 400, background = Color('# 45ff33')) as pic:
        # Set the text and its location
        draw.text(int(pic.width / 3), int(pic.height / 2), 'GeeksForGeeks !')
        # Draw the picture
        draw(pic)
        # Invoke posterize function method
        pic.posterize(3, 'floyd_steinberg')
        # Save the image
        pic.save(filename ='posterize2.jpg')
```

**输出:**

![](img/d8400b570ce7a32d5891c05abe34351f.png)