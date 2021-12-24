# PyQt5 QDial–获取滑块的值

> 原文:[https://www . geeksforgeeks . org/pyqt 5-qdial-get-sliders-value/](https://www.geeksforgeeks.org/pyqt5-qdial-getting-sliders-value/)

在本文中，我们将看到如何获得 QDial 的滑块值。虽然我们可以通过`setValue`方法编程更改，但是用户可以通过鼠标来更改该值。滑块强制该值在合法范围内，即该值应大于或等于最小值，并且应小于或等于最大值。更改该值也会更改滑块位置。

为此，我们对 QDial 对象使用`value`方法

> **语法:** dial.value()
> 
> **论证:**不需要论证
> 
> **返回:**返回整数

下面是实现

```py
# importing libraries
from PyQt5.QtWidgets import * 
from PyQt5 import QtCore, QtGui
from PyQt5.QtGui import * 
from PyQt5.QtCore import * 
import sys

class Window(QMainWindow):

    def __init__(self):
        super().__init__()

        # setting title
        self.setWindowTitle("Python ")

        # setting geometry
        self.setGeometry(100, 100, 500, 400)

        # calling method
        self.UiComponents()

        # showing all the widgets
        self.show()

    # method for components
    def UiComponents(self):

        # creating QDial object
        dial = QDial(self)

        # setting geometry to the dial
        dial.setGeometry(100, 100, 100, 100)

        # making notch visible
        dial.setNotchesVisible(True)

        # value
        value = 50

        # setting value to the dial slider
        dial.setValue(value)

        # creating a label
        label = QLabel("GeeksforGeeks", self)

        # setting geometry to the label
        label.setGeometry(220, 125, 200, 60)

        # making label multiline
        label.setWordWrap(True)

        # getting slider value
        value = dial.value()

        # setting text to the label
        label.setText("Value : " + str(value))

# create pyqt5 app
App = QApplication(sys.argv)

# create the instance of our Window
window = Window()

# start the app
sys.exit(App.exec())
```

**输出:**
![](img/dbfaf525a7774b4398697ec8b08b4fae.png)