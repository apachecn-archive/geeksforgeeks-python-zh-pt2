# Python |使用 Tkinter 的随机密码生成器

> 原文:[https://www . geesforgeks . org/python-random-password-generator-using-tkinter/](https://www.geeksforgeeks.org/python-random-password-generator-using-tkinter/)

随着技术的发展，一切都依赖于数据，而保护这些数据是主要的关注点。密码是为了保护我们上传到网上的数据安全。
一个简单的密码很容易被黑，所有的个人信息都可能被滥用。为了防止这样的事情发生，保证数据的安全，我们的密码保持非常强是非常必要的。
让我们创建一个简单的应用程序，它可以使用 Python [**Tkinter**](https://www.geeksforgeeks.org/python-gui-tkinter/) 模块随机生成强密码。
该应用程序可以生成随机密码，由字母、数字和特殊字符组合而成。可以根据需要提及密码的长度，也可以选择密码的强度。
**所需模块:**

```
import random
import pyperclip
from tkinter import * from tkinter.ttk import *
```

下面是实现:

## 蟒蛇 3

```
# Python program to generate random
# password using Tkinter module
import random
import pyperclip
from tkinter import *
from tkinter.ttk import *

# Function for calculation of password
def low():
    entry.delete(0, END)

    # Get the length of password
    length = var1.get()

    lower = "abcdefghijklmnopqrstuvwxyz"
    upper = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz"
    digits = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789 !@#$%^&*()"
    password = ""

    # if strength selected is low
    if var.get() == 1:
        for i in range(0, length):
            password = password + random.choice(lower)
        return password

    # if strength selected is medium
    elif var.get() == 0:
        for i in range(0, length):
            password = password + random.choice(upper)
        return password

    # if strength selected is strong
    elif var.get() == 3:
        for i in range(0, length):
            password = password + random.choice(digits)
        return password
    else:
        print("Please choose an option")

# Function for generation of password
def generate():
    password1 = low()
    entry.insert(10, password1)

# Function for copying password to clipboard
def copy1():
    random_password = entry.get()
    pyperclip.copy(random_password)

# Main Function

# create GUI window
root = Tk()
var = IntVar()
var1 = IntVar()

# Title of your GUI window
root.title("Random Password Generator")

# create label and entry to show
# password generated
Random_password = Label(root, text="Password")
Random_password.grid(row=0)
entry = Entry(root)
entry.grid(row=0, column=1)

# create label for length of password
c_label = Label(root, text="Length")
c_label.grid(row=1)

# create Buttons Copy which will copy
# password to clipboard and Generate
# which will generate the password
copy_button = Button(root, text="Copy", command=copy1)
copy_button.grid(row=0, column=2)
generate_button = Button(root, text="Generate", command=generate)
generate_button.grid(row=0, column=3)

# Radio Buttons for deciding the
# strength of password
# Default strength is Medium
radio_low = Radiobutton(root, text="Low", variable=var, value=1)
radio_low.grid(row=1, column=2, sticky='E')
radio_middle = Radiobutton(root, text="Medium", variable=var, value=0)
radio_middle.grid(row=1, column=3, sticky='E')
radio_strong = Radiobutton(root, text="Strong", variable=var, value=3)
radio_strong.grid(row=1, column=4, sticky='E')
combo = Combobox(root, textvariable=var1)

# Combo Box for length of your password
combo['values'] = (8, 9, 10, 11, 12, 13, 14, 15, 16,
                   17, 18, 19, 20, 21, 22, 23, 24, 25,
                   26, 27, 28, 29, 30, 31, 32, "Length")
combo.current(0)
combo.bind('<<ComboboxSelected>>')
combo.grid(column=1, row=1)

# start the GUI
root.mainloop()
```