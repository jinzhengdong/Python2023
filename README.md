# Python 2023

## 开始

### 什么是Python

Python是一种高级编程语言，由Guido van Rossum于1991年创建。它是一种解释性语言，可以在各种操作系统上运行，包括Windows、Linux和MacOS等。Python的设计目标之一是使代码易于阅读和编写。因此，它的语法非常简洁，且有很好的可读性。

Python拥有丰富的标准库和第三方库，使其成为许多应用程序和系统开发的首选语言。Python可以用于Web开发、数据科学、机器学习、人工智能、自动化、游戏开发和科学计算等领域。Python还有一个活跃的社区，为Python用户提供了大量的文档和支持。

### 安装Python

安装Python通常可以通过以下几个步骤完成：

* 下载Python安装程序：首先，需要从 [Python官方网站](https://www.python.org/downloads/) 下载适用于您的操作系统的Python安装程序。在下载页面中，选择与您的操作系统版本和位数相应的安装程序。
* 运行安装程序：下载完成后，运行Python安装程序。在安装过程中，您可以选择安装Python的版本和选项。默认情况下，Python会被安装到您的计算机的默认位置。
* 配置环境变量：在Windows系统中，需要将Python添加到环境变量中，以便您可以在命令行中运行Python解释器。在Mac和Linux系统中，这通常是默认设置。
* 验证安装：安装完成后，您可以在命令行中输入“python”来验证Python是否已成功安装。如果安装成功，您将看到Python解释器的交互式提示符。

在安装Python后，您可以使用命令行或其他Python集成开发环境（IDE）来编写和运行Python代码。同时，需要注意Python版本的兼容性，以确保代码可以在您所使用的Python版本中运行。

（B站视频）

### Python解释器

要使用Python解释器，您可以按照以下步骤进行操作：

* 打开命令行或终端：在Windows系统中，您可以按下Win+R键，然后输入"cmd"打开命令提示符；在Mac和Linux系统中，您可以使用Terminal应用程序。
* 输入"python"：在命令行或终端中输入"python"，然后按下回车键，就可以启动Python解释器。
* 使用解释器：在Python解释器中，您可以输入Python代码并立即执行它们。例如，您可以尝试输入以下代码并按下回车键：

```python
print("Hello, World!")
```

如果一切正常，您将看到输出："Hello, World!"。

* 退出解释器：要退出Python解释器，请输入"exit()"或"quit()"命令，然后按下回车键即可。

Python解释器是一个强大的工具，可以帮助您快速测试和验证代码。同时，需要注意Python解释器的版本和兼容性，以确保您的代码可以在目标环境中正确运行。

请在Python解释器中运行以下代码示例：

* 变量赋值和使用：

```python
x = 10
y = 20
z = x + y
print(z)
```

* 条件语句：

```python
x = 10
if x > 5:
    print("x is greater than 5")
else:
    print("x is less than or equal to 5")
```

* 循环语句：

```python
for i in range(5):
    print(i)
```

* 列表操作：

```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
for fruit in fruits:
    print(fruit)
```

* 函数定义和调用：

```python
def add_numbers(x, y):
    return x + y

result = add_numbers(10, 20)
print(result)
```

这些示例代码只是Python语言的冰山一角。Python拥有非常丰富的库和框架，可以用于各种不同的应用场景，例如Web开发、数据科学、机器学习、人工智能等。需要根据具体的需求选择相应的库和框架进行学习和应用。

（B站视频）

### 代码编辑器

Python拥有许多开发工具，可以根据不同的需求和偏好进行选择。以下是Python常用的开发工具：

* PyCharm：是一款功能强大的Python集成开发环境（IDE），提供了代码编辑、调试、测试和版本控制等功能，适用于Web开发、数据科学和机器学习等领域。
* Jupyter Notebook：是一种交互式的Web应用程序，可以用于数据科学和机器学习等领域。它提供了一个笔记本界面，可以在其中编写和运行代码，并展示结果。
* Spyder：是一款Python科学计算环境，提供了类似于Matlab的界面和功能，适用于科学计算和数据分析等领域。
* Visual Studio Code：是一款轻量级的集成开发环境，提供了代码编辑、调试和版本控制等功能，可以使用各种插件扩展其功能。
* Sublime Text：是一款轻量级的文本编辑器，支持多种编程语言，可以通过插件扩展其功能。
* Atom：是一款自由和开源的文本编辑器，支持多种编程语言，可以通过插件扩展其功能。

以上开发工具只是Python开发工具中的一部分，还有很多其他的工具可以根据自己的需要选择使用。我们的课程主要使用Visual Studio Code和PyCharm。

### 你的第一个Python程序

以下的Python程序，它可以让用户输入一个整数，并判断该整数是奇数还是偶数：

```python
# 获取用户输入
num = int(input("请输入一个整数："))

# 判断整数是否为偶数
if num % 2 == 0:
    print("{0}是偶数".format(num))
else:
    print("{0}是奇数".format(num))
```

在这个程序中，首先使用input函数获取用户输入的整数，并使用int函数将其转换为整型。然后，使用模运算符%判断该整数是否为偶数，如果余数为0，则说明是偶数，否则为奇数。最后，使用print函数输出结果。

这个程序非常简单，适合初学者进行练习和学习。通过编写这个程序，初学者可以熟悉Python的输入输出、数据类型和条件语句等基本概念。同时，需要注意在输入整数时要确保输入的是一个整数，否则程序会抛出异常。

对于首次接触编程的同学请跟着我们的课程使用Visual Studio Code来完成我们的第一个Python程序。

（B站视频）

### VS Code Python扩展

以下是一些常用的Visual Studio Code扩展，可以提高Python开发效率：

* Python：官方提供的Python插件，提供了代码智能感知、调试、测试和代码格式化等功能。
* Pylance：基于Microsoft的语言理解技术提供代码智能感知功能，支持类型提示、代码跳转和代码重构等功能。
* Code Runner：提供快速运行Python代码的功能，可以在编辑器内运行Python代码。
* Bracket Pair Colorizer：提供括号配对颜色的功能，方便编写Python代码时阅读代码。
* Auto Docstring：提供生成函数文档的功能，可以帮助编写规范的函数文档。
* Python Test Explorer：提供在Visual Studio Code中运行和调试Python测试的功能，可以使用pytest、unittest和nose等测试框架。

以上扩展只是Python开发中的一部分，可以根据自己的需要选择和安装相应的扩展。同时，需要注意安装扩展时要从官方或可信的来源下载和安装，以免遇到安全问题。

（B站视频）

### Linting Python Code

在Python开发中，代码风格和代码质量的重要性不言而喻。Linting是一种自动化检查代码质量和风格的工具，可以帮助开发者找出代码中的潜在问题，从而提高代码的可读性、可维护性和可重用性。Python开发中常用的Linting工具有以下几种：

* Pylint：Pylint是一个Python Linting工具，可以检查代码质量、风格和错误等，同时也支持插件扩展。
* Flake8：Flake8是一个基于Pylint和pycodestyle的Python Linting工具，可以检查代码质量、风格和错误等，同时也支持插件扩展。
* Pyflakes：Pyflakes是一个轻量级的Python Linting工具，可以检查代码错误和未使用的变量等。
* Black：Black是一个Python代码格式化工具，可以自动化格式化Python代码，使其符合PEP 8代码规范。
* Mypy：Mypy是一个Python类型检查工具，可以在代码编写期间捕获类型错误，提高代码的类型安全性。

可以根据自己的需要选择和使用相应的Linting工具。值得注意的是，虽然Linting工具可以检查和纠正一些常见的代码问题，但并不能完全取代代码审查和测试等其他工具和方法。

（B站视频）

### Python代码的格式及格式化

Python代码格式化是一种将代码格式化为规范、易读和易于维护的样式的技术。在Python开发中，遵循PEP 8代码规范可以帮助提高代码的可读性、可维护性和可重用性。以下是几种常见的Python代码格式化方法：

* 使用自动化格式化工具：Black是一个自动化的Python代码格式化工具，它可以根据PEP 8规范格式化Python代码，并在维护和阅读代码时提供帮助。
* 使用编辑器和IDE的代码格式化功能：大多数文本编辑器和IDE都提供了代码格式化功能，可以通过快捷键或菜单命令对代码进行格式化。例如，在Visual Studio Code中可以使用Pylance插件的代码格式化功能，或使用快捷键“Shift + Alt + F”格式化代码。
* 手动格式化代码：如果没有自动化工具和编辑器的支持，可以手动根据PEP 8规范对代码进行格式化，例如对缩进、空格、换行等进行调整。这种方法比较耗时，但可以更好地理解PEP 8规范并提高代码质量。

无论使用哪种方法，都需要遵循PEP 8规范并保持代码的一致性和可读性。下面演示的这段代码很好的演示了PEP 8规范：

```python
# This is a comment
import os
import sys


def func(arg1, arg2='default'):
    """This is a function docstring"""
    if arg1 == 0:
        return arg2
    elif arg1 == 1:
        return arg1 + arg2
    else:
        return arg1 * arg2


class MyClass:
    """This is a class docstring"""
    def __init__(self, arg1, arg2):
        self.arg1 = arg1
        self.arg2 = arg2

    def get_arg1(self):
        return self.arg1

    def get_arg2(self):
        return self.arg2


if __name__ == '__main__':
    # This is an example of how to use the code
    my_obj = MyClass(1, 'test')
    result = func(1, 2)
    print(result)
```

这段代码保持了PEP 8规范，如下：

* 代码缩进使用四个空格。
* 模块和包名使用小写字母，单词间使用下划线分隔。
* 函数名和变量名使用小写字母，单词间使用下划线分隔。
* 类名使用驼峰命名法，首字母大写。
* 代码中使用双引号表示字符串。
* 行长度不超过79个字符。
* 函数和类的定义之间要有两个空行。
* 在类中定义方法时，方法名之前要有一个空行。
* 在if、for和while等语句中的条件表达式之后要加一个空格，例如"if x == 1:"。
* 在注释之前要有一个空格。

保持代码风格的一致性和规范可以提高代码的可读性和可维护性，有助于团队协作和代码重用。

### 简洁的运行Python代码

在VS Code中可以通过以下步骤简洁地运行Python代码：

* 安装Python扩展：在VS Code中安装Python扩展，可以使用VS Code的Python工具来编写、调试和运行Python代码。
* 打开Python文件：在VS Code中打开Python文件，可以使用快捷键“Ctrl + O”打开文件，或者从菜单栏中选择“文件”->“打开文件”。
* 运行代码：在VS Code中运行Python代码，可以使用以下方法：
  * 使用快捷键：选择要运行的代码，然后使用快捷键“Shift + Enter”或“Ctrl + Alt + N”运行选中的代码。
  * 使用命令面板：打开命令面板，输入“Python: Run Python File in Terminal”并选择该命令，即可在终端中运行Python文件。
  * 使用右键菜单：右键单击Python文件，选择“在终端中运行Python文件”选项，即可在终端中运行Python文件。
* 查看输出结果：在VS Code中查看Python代码的输出结果，可以在终端中查看运行结果。如果代码需要从终端获取输入，可以在终端中输入相应的数据并按回车键。

使用VS Code运行Python代码简洁方便，可以快速进行Python开发和调试。

### Python实现

Python实现是实现Python编程语言规范的不同软件应用程序。这些实现允许开发人员编写Python代码并在不同的平台上执行，包括桌面计算机、服务器、移动设备和嵌入式系统。有几种Python实现可用，每种实现都有自己的特点、优点和缺点。

一些流行的Python实现包括：

* CPython：这是最广泛使用的Python实现，用C语言编写。它是Python的参考实现，也是大多数操作系统默认的实现。CPython提供与其他Python实现的高度兼容性和广泛的第三方库。
* Jython：这是一个在Java虚拟机（JVM）上运行的Python实现。Jython允许开发人员无缝地使用Java库和Python代码，并且它提供了与基于Java的企业系统的卓越集成。
* IronPython：这是一个在.NET框架上运行的Python实现。IronPython与.NET框架完全集成，允许开发人员使用Python代码与.NET库和工具。
* PyPy：这是一个使用Python本身编写的Python实现。它提供了一个即时编译器（JIT），可以显著加速Python代码的执行。PyPy支持与CPython相同的语法和模块，并且与大多数Python代码兼容。

每个Python实现都有自己的优点和缺点，适用于不同的用例。开发人员应选择最适合他们项目要求和开发环境的实现。

### Python代码是如何运行的

Python代码通常需要经过以下步骤才能运行：

* 编写代码：使用文本编辑器编写Python代码，并将其保存为以.py结尾的文件。
* 解释代码：Python解释器读取Python文件中的代码，并逐行解释和执行它。
* 执行代码：Python解释器将代码转换为计算机可理解的机器语言指令，并执行代码。

以下是一个简单的Python程序的例子，该程序将打印“Hello, World!”到控制台：

```python
print("Hello, World!")
```

在运行此程序之前，您需要使用文本编辑器将其保存为以.py结尾的文件，例如“hello_world.py”。

要运行此程序，您可以使用Python解释器运行以下命令：

```python
python hello_world.py
```

这将在控制台上打印“Hello, World!”。解释器将读取Python文件中的代码，将其转换为机器语言指令并执行它，最终输出到控制台。

## Python的原生数据类型

### 变量

在Python中，变量是一个用于存储值的标识符。变量可以存储各种类型的数据，包括数字、字符串、列表、元组、字典等等。变量名是由字母、数字和下划线组成的标识符，它们必须以字母或下划线开头，不能以数字开头。Python中的变量是动态类型的，这意味着你可以随时更改变量的数据类型。

以下是几个Python变量的示例：

```python
# 定义一个整数变量x，并赋值为10
x = 10

# 定义一个字符串变量name，并赋值为"John"
name = "John"

# 定义一个列表变量my_list，并赋值为[1, 2, 3]
my_list = [1, 2, 3]

# 定义一个元组变量my_tuple，并赋值为(1, 2, 3)
my_tuple = (1, 2, 3)

# 定义一个字典变量my_dict，并赋值为{"name": "John", "age": 30}
my_dict = {"name": "John", "age": 30}
```

在这些示例中，我们定义了不同类型的变量，例如整数、字符串、列表、元组和字典。每个变量都有一个名称和一个值，并且可以随时更改其值或数据类型。例如，我们可以通过赋予不同的值来更改整数变量x的值，或者更改my_dict变量中的一个值。

总之，Python变量是用于存储值的标识符，它们可以存储不同类型的数据，并且可以随时更改它们的值和类型。

### 字符串

在Python中，字符串是一种序列类型，用于存储文本数据。字符串是由一系列字符组成的，可以是字母、数字、标点符号或其他任何字符。Python中的字符串使用单引号、双引号或三引号括起来，例如：

```python
# 使用单引号定义一个字符串
str1 = 'Hello, world!'

# 使用双引号定义一个字符串
str2 = "Python is awesome."

# 使用三引号定义一个多行字符串
str3 = """This is a
multi-line
string."""
```

Python字符串是不可变的，这意味着一旦创建了字符串，就不能更改它的内容。但是，我们可以通过字符串方法来操作字符串，例如切片、连接、替换等。

以下是一些Python字符串的常用操作：

* 字符串切片：使用索引或切片符号来获取字符串中的子字符串。

```python
str = "Hello, world!"
print(str[0])       # 输出第一个字符 "H"
print(str[2:5])     # 输出从第三个字符开始到第五个字符的子字符串 "llo"
```

* 字符串连接：使用加号运算符来连接两个字符串。

```python
str1 = "Hello"
str2 = "world"
print(str1 + " " + str2)     # 输出 "Hello world"
```

* 字符串替换：使用replace()方法来替换字符串中的子字符串。

```python
str = "Hello, world!"
new_str = str.replace("world", "Python")
print(new_str)      # 输出 "Hello, Python!"
```

* 字符串格式化：使用字符串格式化操作符或format()方法来创建格式化的字符串。

```python
name = "John"
age = 30
print("My name is %s and I am %d years old." % (name, age))
# 输出 "My name is John and I am 30 years old."
print(f"My name is {name} and I am {age}} years old.")
# 输出 "My name is John and I am 30 years old."
```

总之，Python字符串是一种序列类型，用于存储文本数据。字符串是不可变的，但我们可以使用字符串方法来操作字符串，例如切片、连接、替换和格式化。字符串在Python中是非常常用的数据类型，因为它们可以用于处理文本数据。

### 转义字符

在Python字符串中，转义字符用来表示一些特殊字符，如引号、换行符等。转义字符是以反斜杠开头的字符，后面跟着特殊字符的表示形式。以下是一些常用的Python转义字符：

| 转义字符 | 含义                                         |
| -------- | -------------------------------------------- |
| `\'`     | 单引号                                       |
| `\"`     | 双引号                                       |
| `\\`     | 反斜杠                                       |
| `\n`     | 换行符                                       |
| `\t`     | 制表符                                       |
| `\r`     | 回车符，将光标移到当前行的开头              |
| `\b`     | 退格符，将光标向左移动一格                  |
| `\f`     | 换页符，将光标移到下一页的开头              |
| `\v`     | 垂直制表符                                   |
| `\a`     | 响铃，发出警告声                             |
| `\uXXXX` | 16位Unicode字符，如`\u00A9`表示版权符号     |
| `\UXXXXXXXX` | 32位Unicode字符，如`\U0001F600`表示笑脸符号 |

以上是一些常见的Python转义字符及其含义，掌握这些转义字符的含义和用法，可以帮助我们更好地处理和操作Python中的字符串。

### 字符串方法

Python中字符串有很多常见的操作，下面列举一些常见的操作方法，并演示其用法：

* 字符串拼接

通过`+`符号可以将两个字符串拼接在一起，生成一个新的字符串。例如：

```python
str1 = "Hello"
str2 = "world"
str3 = str1 + " " + str2
print(str3)  # 输出：Hello world
```

* 字符串复制

通过`*`符号可以将一个字符串复制多次，生成一个新的字符串。例如：

```python
str1 = "Hello"
str2 = str1 * 3
print(str2)  # 输出：HelloHelloHello
```

* 字符串截取

可以使用`[]`操作符来获取字符串中的某个字符或一段子串。例如：

```python
str = "Hello, world!"
print(str[0])     # 输出：H
print(str[7:12])  # 输出：world
```

* 字符串长度

可以使用len()函数来获取一个字符串的长度。例如：

```python
str = "Hello, world!"
print(len(str))  # 输出：13
```

* 字符串查找

可以使用`index()`函数或`find()`函数来查找字符串中是否包含某个子串，如果存在则返回其在字符串中的索引位置，否则返回`-1`。例如：

```python
str = "Hello, world!"
print(str.find("world"))  # 输出：7
print(str.index("world"))  # 输出：7
print(str.find("python"))  # 输出：-1
```

* 字符串替换

可以使用replace()函数来将一个字符串中的子串替换为另一个字符串。例如：

```python
str = "Hello, world!"
new_str = str.replace("world", "Python")
print(new_str)  # 输出：Hello, Python!
```

* 字符串分割

可以使用split()函数将一个字符串按照某个分隔符进行分割，返回一个列表。例如：

```python
str = "Hello,world,Python"
list = str.split(",")
print(list)  # 输出：['Hello', 'world', 'Python']
```

* 字符串大小写转换

可以使用upper()函数将字符串中的所有字母转换为大写，使用lower()函数将字符串中的所有字母转换为小写。例如：

```python
str = "Hello, world!"
upper_str = str.upper()
lower_str = str.lower()
print(upper_str)  # 输出：HELLO, WORLD!
print(lower_str)  # 输出：hello, world!
```

以上是常见的Python字符串操作方法，掌握这些操作方法可以帮助我们更好地处理和操作Python中的字符串。

### 数值类型

Python中的数值类型包括整数（int）、浮点数（float）、复数（complex）。其中，整数类型用于存储整数值，浮点数类型用于存储浮点数值，复数类型用于存储复数值。请看下面的例子：

* 整数类型（int）:

```python
x = 10          # 定义一个整数变量x
y = 0b1010      # 定义一个二进制整数变量y，值为10
z = 0o12        # 定义一个八进制整数变量z，值为10
w = 0xa         # 定义一个十六进制整数变量w，值为10
```

* 浮点数类型（float）：

```python
x = 3.14        # 定义一个浮点数变量x
y = 2.0e-4      # 定义一个科学计数法表示的浮点数变量y，值为0.0002
z = float("3.14")  # 将字符串转换为浮点数类型，值为3.14
```

* 复数类型（complex）：

```python
x = 3 + 4j      # 定义一个复数变量x，值为3+4j
y = complex(3, 4)  # 用complex()函数定义一个复数变量y，值为3+4j
z = x + y       # 复数加法，值为6+8j
w = x * y       # 复数乘法，值为-9+24j
```

这些示例展示了Python数字类型的基本用法，包括整数、浮点数和复数类型。通过使用这些数字类型，我们可以进行数值计算、数据转换和复数运算等操作。

### 数值相关方法及math库

Python 中，可以对整数 (int)、浮点数 (float) 和复数 (complex) 进行各种数学运算，下面是一些常见的运算方法：

* 加法：使用 `+` 运算符进行加法运算。

```python
# 整数加法
a = 5
b = 3
c = a + b
print(c)  # 输出 8

# 浮点数加法
x = 2.5
y = 1.2
z = x + y
print(z)  # 输出 3.7

# 复数加法
m = 3 + 4j
n = 1 + 2j
p = m + n
print(p)  # 输出 (4+6j)
```

* 减法：使用 `-` 运算符进行减法运算。

```python
# 整数减法
a = 5
b = 3
c = a - b
print(c)  # 输出 2

# 浮点数减法
x = 2.5
y = 1.2
z = x - y
print(z)  # 输出 1.3

# 复数减法
m = 3 + 4j
n = 1 + 2j
p = m - n
print(p)  # 输出 (2+2j)
```

* 乘法：使用 `*` 运算符进行乘法运算。

```python
# 整数乘法
a = 5
b = 3
c = a * b
print(c)  # 输出 15

# 浮点数乘法
x = 2.5
y = 1.2
z = x * y
print(z)  # 输出 3.0

# 复数乘法
m = 3 + 4j
n = 1 + 2j
p = m * n
print(p)  # 输出 (-5+10j)
```

* 除法：使用 `/` 运算符进行除法运算。

```python
# 整数除法
a = 5
b = 3
c = a / b
print(c)  # 输出 1.6666666666666667

# 浮点数除法
x = 2.5
y = 1.2
z = x / y
print(z)  # 输出 2.0833333333333335

# 复数除法
m = 3 + 4j
n = 1 + 2j
p = m / n
print(p)  # 输出 (1.6-0.2j)
```

* 取模运算：使用 `%` 运算符进行取模运算。

```python
a = 5
b = 3
c = a % b
print(c)  # 输出 2
```

* 幂运算：使用 ** 运算符进行幂运算。

```python
# 整数幂运算
a = 2
b = 3
c = a ** b
print(c)  # 输出 8

# 浮点数幂运算
x = 2.5
y = 3
z = x ** y
print(z)  # 输出 15.625
```

* `//` 整除运算符：返回两个数相除的整数部分，即向下取整。

```python
>>> 15 // 2
7
>>> -15 // 2
-8
```

* `divmod()` 函数：返回两个数的商和余数，返回的结果是一个元组(tuple)，第一个元素是商，第二个元素是余数。

```python
>>> divmod(15, 2)
(7, 1)
>>> divmod(-15, 2)
(-8, 1)
```

* `abs()` 函数：返回数的绝对值。

```python
>>> abs(-10)
10
>>> abs(10)
10
```

* `round()` 函数：对数进行四舍五入取整。

```python
>>> round(3.14159, 2)
3.14
>>> round(3.14159)
3
```

除了上面介绍的这些针对数值类型的方法外，Python的`math`库提供了一些数学运算相关的函数，包括三角函数、对数、幂、根号等。下面是一些常用的方法：

* math.sqrt(x)：返回x的平方根。
* math.ceil(x)：返回不小于x的最小整数。
* math.floor(x)：返回不大于x的最大整数。
* math.pow(x, y)：返回x的y次幂。
* math.exp(x)：返回e的x次幂。
* math.log(x)：返回x的自然对数。
* math.log10(x)：返回x的以10为底的对数。
* math.sin(x)：返回x的正弦值。
* math.cos(x)：返回x的余弦值。
* math.tan(x)：返回x的正切值。
* math.degrees(x)：将弧度转换为角度。
* math.radians(x)：将角度转换为弧度。

下面是一些使用示例：

```python
import math

# 计算平方根
print(math.sqrt(16))  # 4.0

# 计算三角函数
print(math.sin(math.pi/2))  # 1.0
print(math.cos(math.pi/2))  # 6.123233995736766e-17
print(math.tan(math.pi/4))  # 0.9999999999999999

# 计算对数和幂
print(math.log(2.718))  # 0.999896315728952
print(math.log10(100))  # 2.0
print(math.pow(2, 3))  # 8.0

# 向上取整和向下取整
print(math.ceil(1.1))  # 2
print(math.floor(1.9))  # 1
```

需要注意的是，math库中的函数参数和返回值都是浮点数类型，如果需要计算整数，可以使用Python的内置函数进行转换。

### 类型转换

Python中的数据类型转换通常使用强制类型转换来实现。Python支持将一种数据类型转换为另一种数据类型，包括整数、浮点数、字符串、列表、元组和字典等数据类型。

以下是一些常用的类型转换方法及其示例：

* 将整数转换为浮点数类型

```python
x = 5
y = float(x)
print(y)  # 输出 5.0
```

* 将浮点数转换为整数类型

```python
x = 5.5
y = int(x)
print(y)  # 输出 5
```

* 将字符串转换为整数类型

```python
x = '5'
y = int(x)
print(y)  # 输出 5
```

* 将字符串转换为浮点数类型

```python
x = '5.5'
y = float(x)
print(y)  # 输出 5.5
```

* 将字符串转换为列表类型

```python
x = '1,2,3,4,5'
y = x.split(',')
print(y)  # 输出 ['1', '2', '3', '4', '5']
```

* 将列表转换为字符串类型

```python
x = ['1', '2', '3', '4', '5']
y = ','.join(x)
print(y)  # 输出 '1,2,3,4,5'
```

* 将元组转换为列表类型

```python
x = (1, 2, 3, 4, 5)
y = list(x)
print(y)  # 输出 [1, 2, 3, 4, 5]
```

* 将列表转换为元组类型

```python
x = [1, 2, 3, 4, 5]
y = tuple(x)
print(y)  # 输出 (1, 2, 3, 4, 5)
```

* 将字典的键或值转换为列表类型

```python
x = {'a': 1, 'b': 2, 'c': 3}
y = list(x.keys())
print(y)  # 输出 ['a', 'b', 'c']

y = list(x.values())
print(y)  # 输出 [1, 2, 3]
```

除上面列举的几种数据类型转换外，Python还提供了一些其他的数据转换方式：

* bin(x)：将整数 x 转换为二进制字符串。
* oct(x)：将整数 x 转换为八进制字符串。
* hex(x)：将整数 x 转换为十六进制字符串。
* ord(c)：返回字符 c 的 Unicode 码点。
* chr(i)：返回 Unicode 码点 i 对应的字符。
* bytes(x)：将 x 转换为字节类型。
* bytearray(x)：将 x 转换为可变字节数组类型。
* memoryview(x)：将 x 转换为内存视图类型。

这些转换方式的使用方法与上面列出的数据类型转换方式类似，都是通过将需要转换的数据作为参数传入相应的函数或方法中进行转换。

## 流程控制

### 比较操作符

Python 的比较操作符用于比较两个值之间的关系，结果返回布尔值 True 或 False。Python 中常见的比较操作符包括：

* `==`：等于。比较两个值是否相等，如果相等则返回 True，否则返回 False。

```python
x = 5
y = 10
print(x == y)  # False
print(x == 5)  # True
```

* `!=`：不等于。比较两个值是否不相等，如果不相等则返回 True，否则返回 False。

```python
x = 5
y = 10
print(x != y)  # True
print(x != 5)  # False
```

* `<`：小于。比较左侧值是否小于右侧值，如果是则返回 True，否则返回 False。

```python
x = 5
y = 10
print(x < y)  # True
print(x < 5)  # False
```

* `>`：大于。比较左侧值是否大于右侧值，如果是则返回 True，否则返回 False。

```python
x = 5
y = 10
print(x > y)  # False
print(y > x)  # True
```

* `<=`：小于等于。比较左侧值是否小于等于右侧值，如果是则返回 True，否则返回 False。

```python
x = 5
y = 10
z = 5
print(x <= y)  # True
print(x <= z)  # True
```

* `>=`：大于等于。比较左侧值是否大于等于右侧值，如果是则返回 True，否则返回 False。

```python
x = 5
y = 10
z = 5
print(y >= x)  # True
print(z >= x)  # True
```

这些比较操作符可以与数值、字符串、布尔值等类型的数据进行比较。比较操作符的使用方法非常简单，只需要将需要比较的两个值放在操作符两侧，运算结果会返回一个布尔值。

### 条件语句

在Python中，条件语句用于基于条件执行代码块。Python中有两个主要的条件语句：`if`语句和`if-else`语句。

#### if语句

`if`语句用于检查一个条件是否成立，如果成立则执行一段代码。if语句的语法结构如下：

```python
if condition:
    # code block to execute if condition is true
```

其中，`condition`是一个表达式，它的值为`True`或`False`。如果`condition`为`True`，则执行`if`语句下缩进的代码块。

例如，以下代码演示了如何使用`if`语句检查一个数是否为正数：

```python
x = 10

if x > 0:
    print("x is a positive number")
```

#### if-else语句

`if-else`语句用于检查一个条件是否成立，如果成立则执行一个代码块，否则执行另一个代码块。`if-else`语句的语法结构如下：

```python
if condition:
    # code block to execute if condition is true
else:
    # code block to execute if condition is false
```

例如，以下代码演示了如何使用if-else语句检查一个数是否为正数：

```python
x = -10

if x > 0:
    print("x is a positive number")
else:
    print("x is not a positive number")
```

#### if-elif-else语句

`if-elif-else`语句用于检查多个条件，如果第一个条件不成立，则检查第二个条件，以此类推。如果所有条件都不成立，则执行最后一个代码块。`if-elif-else`语句的语法结构如下：

```python
if condition1:
    # code block to execute if condition1 is true
elif condition2:
    # code block to execute if condition2 is true
elif condition3:
    # code block to execute if condition3 is true
else:
    # code block to execute if all conditions are false
```

例如，以下代码演示了如何使用if-elif-else语句检查一个数的正负性：

```python
x = 0

if x > 0:
    print("x is a positive number")
elif x < 0:
    print("x is a negative number")
else:
    print("x is zero")
```

以上代码将首先检查`x`是否大于`0`，如果是则打印`x is a positive number`。如果`x`不大于`0`，则检查`x`是否小于`0`，如果是则打印`x is a negative number`。如果`x`既不大于`0`也不小于`0`，则打印`x is zero`。

### 三元操作符

Python的三元操作符是一种简洁的条件语句，用于根据条件返回不同的值。三元操作符的语法如下：

```sql
value_if_true if condition else value_if_false
```

其中，condition 是一个布尔表达式，value_if_true 是在 condition 为 True 时返回的值，value_if_false 是在 condition 为 False 时返回的值。

以下是一个简单的示例，说明如何使用三元操作符：

```python
x = 10
y = 20

max_value = x if x > y else y

print(max_value)
```

在上面的代码中，如果 x 大于 y，则 max_value 被赋值为 x，否则 max_value 被赋值为 y。在本例中，由于 x 不大于 y，因此 max_value 被赋值为 y。

三元操作符在某些情况下可以用于简化代码，但它也可能使代码难以理解。在使用三元操作符时，请确保您的代码易于阅读和理解。

### 逻辑操作符

Python中的逻辑操作符是用于组合布尔表达式的运算符，包括`and`、`or`和`not`。这些操作符允许我们在条件语句中进行更复杂的逻辑判断。

下面我们分别介绍一下这些逻辑操作符，并举例说明它们的使用方法。

* and操作符

and操作符用于组合两个布尔表达式，并在两个表达式都为True时返回True，否则返回False。

示例：

```python
x = 10
y = 20
z = 30

if x < y and y < z:
    print("x is less than y, and y is less than z")
else:
    print("Either x is not less than y, or y is not less than z, or both.")
```

在上面的示例中，我们使用and操作符组合了两个比较表达式，用于检查变量x是否小于y，并且y是否小于z。因为这两个表达式都为真，所以整个表达式的值为True，并输出x is less than y, and y is less than z。

* or操作符

or操作符用于组合两个布尔表达式，并在两个表达式至少一个为True时返回True，否则返回False。

示例：

```python
x = 10
y = 20
z = 30

if x > y or y > z:
    print("Either x is greater than y, or y is greater than z, or both.")
else:
    print("x is not greater than y, and y is not greater than z")
```

在上面的示例中，我们使用or操作符组合了两个比较表达式，用于检查变量x是否大于y，或者y是否大于z。因为这两个表达式都为假，所以整个表达式的值为False，并输出x is not greater than y, and y is not greater than z。

* not操作符

not操作符用于取反一个布尔表达式的值。如果表达式的值为True，则返回False，如果表达式的值为False，则返回True。

示例：

```python
x = 10
y = 20

if not x > y:
    print("x is not greater than y")
else:
    print("x is greater than y")
```

在上面的示例中，我们使用not操作符取反了比较表达式x > y的值。因为x不大于y，所以not x > y的值为True，并输出x is not greater than y。

以上就是Python中的逻辑操作符的使用方法和示例。在编写条件语句时，逻辑操作符是非常重要的工具，可以让我们处理更加复杂的逻辑。

### 短路评估

在Python中，逻辑运算符的短路评估是指只要能确定整个表达式的值，就不再计算后续的表达式的过程。这样可以提高代码的效率并避免不必要的计算。

在Python中，当使用and运算符时，如果第一个操作数的值为False，则整个表达式的值为False，不再计算后续的操作数。同样地，当使用or运算符时，如果第一个操作数的值为True，则整个表达式的值为True，不再计算后续的操作数。

以下是一些示例，说明短路评估是如何工作的：

```python
x = 10
y = 0

if y != 0 and x/y > 2:
    print("x is more than twice of y")

# 在上面的代码中，由于y等于0，因此短路评估可以避免对第二个表达式进行计算，并且不会触发除以0的错误。

if x > 5 or y/x > 2:
    print("Either x is more than 5, or y is more than twice of x")

# 在上面的代码中，由于x大于5，因此短路评估可以避免对第二个表达式进行计算，并且不会触发除以0的错误。
```

总之，在编写Python代码时，短路评估是一种常用的技巧，可以帮助我们编写更高效的代码并避免不必要的错误。

### For循环

在Python中，for循环用于迭代序列（如列表、元组、字符串等）或其他可迭代对象（如字典、文件等）中的元素。for循环是一种常用的控制结构，可以方便地对序列中的每个元素执行相同的操作。

for循环的基本语法如下：

```python
for 变量 in 序列:
    # 循环体代码块
```

其中，变量表示当前迭代的元素，序列表示需要迭代的序列。在每次循环中，变量会依次取得序列中的每个元素，并执行循环体中的代码块。

以下是一些示例，演示了for循环的使用方法：

```python
# 使用for循环迭代列表
fruits = ['apple', 'banana', 'orange']
for fruit in fruits:
    print(fruit)

# 使用for循环迭代元组
colors = ('red', 'green', 'blue')
for color in colors:
    print(color)

# 使用for循环迭代字符串
name = 'Alice'
for char in name:
    print(char)

# 使用for循环迭代字典
scores = {'Alice': 80, 'Bob': 90, 'Charlie': 85}
for name, score in scores.items():
    print(name, score)
```

### For-Else循环

在Python中，for-else循环是一种常用的控制结构，它的语法与普通的for循环类似，但在循环结束后，如果没有执行break语句，那么else语句块中的代码就会被执行。for-else循环可以在需要在循环结束后执行一些额外的代码时非常有用。

for-else循环的基本语法如下：

```python
for 变量 in 序列:
    # 循环体代码块
else:
    # else代码块
```

以下是一个简单的例子，说明for-else循环的使用方法：

```python
fruits = ['apple', 'banana', 'orange']
for fruit in fruits:
    if fruit == 'banana':
        print("I don't like bananas, skipping")
        continue
    print("I like", fruit)
else:
    print("I've run out of fruits to like")
```

在上面的代码中，for循环迭代了一个水果列表。如果循环中遇到了"banana"，那么代码会跳过这个元素并继续循环。否则，代码会打印出"I like"和当前水果的名称。在循环结束后，else语句块中的代码会被执行，输出"I've run out of fruits to like"。

另一个例子：

```python
nums = [2, 3, 6, 9, 11]
for num in nums:
    if num % 2 == 0:
        print(num, "is even")
        break
else:
    print("No even number found")
```

在上面的代码中，for循环迭代了一个数字列表。如果循环中找到了一个偶数，那么代码会打印出这个数是偶数并终止循环。否则，代码会继续循环直到所有元素都被迭代完成。在循环结束后，else语句块中的代码会被执行，输出"No even number found"。

### For嵌套循环

在Python中，for循环可以嵌套，也就是在for循环内部再嵌套一个for循环。嵌套的for循环可以用于处理多维数据结构，例如列表中的列表，或者字典中的字典。

嵌套的for循环的语法如下：

```python
for 变量1 in 序列1:
    for 变量2 in 序列2:
        # 循环体代码块
```

其中，变量1表示外部循环中的元素，变量2表示内部循环中的元素，序列1表示外部循环需要迭代的序列，序列2表示内部循环需要迭代的序列。

以下是一个简单的例子，演示了如何使用嵌套的for循环来遍历一个二维列表：

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
for row in matrix:
    for num in row:
        print(num, end=' ')
    print()
```

在上面的代码中，我们定义了一个二维列表matrix，然后使用嵌套的for循环来遍历这个列表中的所有元素。外部循环遍历每一行，内部循环遍历每一行中的每个元素。在内部循环中，我们打印每个元素，并使用end参数来设置打印结束后的字符为空格。最后，我们在每一行结束后打印一个换行符，以便在控制台上输出一个矩阵形式的表格。

嵌套的for循环还可以用于处理嵌套的字典等数据结构，具体的使用方式取决于具体的数据结构和业务需求。需要注意的是，使用嵌套的for循环会增加代码的复杂度和运行时间，因此在使用时需要慎重考虑。

### 可迭代

在Python中，可迭代对象是指可以使用for循环遍历的对象。以下是Python中常见的可迭代对象类型及其示例：

* 列表（list）：由一系列元素组成的可变序列，可以使用for循环遍历每个元素。

```python
lst = [1, 2, 3, 4]
for num in lst:
    print(num)
```

输出：

```
1
2
3
4
```

* 元组（tuple）：由一系列元素组成的不可变序列，可以使用for循环遍历每个元素。

```python
tpl = (1, 2, 3, 4)
for num in tpl:
    print(num)
```

输出：

```
1
2
3
4
```

* 字符串（string）：由一系列字符组成的不可变序列，可以使用for循环遍历每个字符。

```python
s = "hello"
for ch in s:
    print(ch)
```

输出：

```
h
e
l
l
o
```

* 集合（set）：由一组唯一的元素组成的无序集合，可以使用for循环遍历每个元素。

```python
s = set([1, 2, 3, 4])
for num in s:
    print(num)
```

输出：

```
1
2
3
4
```

* 字典（dict）：由一组键值对组成的映射关系，可以使用for循环遍历每个键或值。

```python
d = {"name": "Alice", "age": 30, "gender": "female"}
for key in d:
    print(key, d[key])
```

输出：

```
name Alice
age 30
gender female
```

* 文件对象（file）：代表打开的文件，可以使用for循环遍历文件中的每一行。

```python
f = open("myfile.txt")
for line in f:
    print(line)
```

输出：

```
line 1
line 2
line 3
```

需要注意的是，Python中还有其他可迭代对象类型，例如生成器（generator）和迭代器（iterator）。这些类型的讲解超出了本节的范围，感兴趣的同学可以自行了解。

### While循环

Python中的while循环用于反复执行一段代码，直到指定的条件不再满足为止。以下是while循环的语法：

```python
while condition:
    # code to be executed repeatedly
```

其中，condition是一个布尔表达式，表示循环继续的条件。只要condition为True，就会一直执行循环内的代码。当condition变为False时，循环停止。

以下是一个简单的while循环的示例，用于计算1到10的和：

```python
total = 0
num = 1
while num <= 10:
    total += num
    num += 1
print("The sum of 1 to 10 is", total)
```

在上面的代码中，我们使用while循环计算了1到10的和。初始时，total被设置为0，num被设置为1。在每次循环中，我们将num加到total中，并将num加1。只要num小于或等于10，就会一直执行循环。当num变为11时，循环终止。最后，我们使用print语句打印总和。

输出结果为：

```python
The sum of 1 to 10 is 55
```

需要注意的是，如果循环条件始终为True，那么循环将永远不会停止，这将导致无限循环。因此，在编写while循环时，必须确保循环条件可以在某个时刻变为False，以避免无限循环。同时，在循环内部必须确保修改循环条件，否则可能会出现死循环，我们在下一节会专门介绍。

### 无限循环

需要注意的是，如果循环条件始终为True，那么循环将永远不会停止，这将导致无限循环。因此，在编写while循环时，必须确保循环条件可以在某个时刻变为False，以避免无限循环。同时，在循环内部必须确保修改循环条件，否则可能会出现死循环。

```python
while True:
    user_input = input("Enter a number (q to quit): ")
    if user_input == "q":
        break
    else:
        number = int(user_input)
        print("The square of", number, "is", number**2)
```

在上面的代码中，我们使用while True来创建一个无限循环，直到用户输入了字符"q"为止。在每次循环中，我们使用input函数等待用户输入一个数字，并将其存储在user_input变量中。如果用户输入了"q"，我们使用break语句来强制退出循环。否则，我们将user_input转换为整数，并计算其平方。最后，我们使用print语句将结果输出到屏幕上。

需要注意的是，如果在循环内部忘记使用break语句来退出循环，程序将一直运行下去，直到被强制终止。因此，在编写无限循环时，一定要确保程序可以在某个时刻被终止。例如，上面的示例中使用了一个特殊字符"q"来终止循环。如果用户输入了该字符，程序将立即退出循环。

