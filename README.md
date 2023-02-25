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