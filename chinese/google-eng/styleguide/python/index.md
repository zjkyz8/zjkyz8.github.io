## 谷歌Python风格指南
- [谷歌Python风格指南](#谷歌python风格指南)
  - [1 背景](#1-背景)
  - [2 Python语言规则](#2-python语言规则)
    - [2.1 Lint](#21-lint)
      - [2.1.1 定义](#211-定义)
      - [2.1.2 优势](#212-优势)
      - [2.1.3 劣势](#213-劣势)
      - [2.1.4 决议](#214-决议)
    - [2.2 导入(Imports)](#22-导入imports)
      - [2.2.1 定义](#221-定义)
      - [2.2.2 优势](#222-优势)
      - [2.2.3 劣势](#223-劣势)
      - [2.2.4 决议](#224-决议)
    - [2.3 包(Packages)](#23-包packages)
      - [2.3.1 优势](#231-优势)
      - [2.3.2 劣势](#232-劣势)
      - [2.3.3 决议](#233-决议)
    - [2.4 异常(Exceptions)](#24-异常exceptions)
      - [2.4.1 定义](#241-定义)
      - [2.4.2 优势](#242-优势)
      - [2.4.3 劣势](#243-劣势)
      - [2.4.4 决议](#244-决议)
    - [2.5 全局变量](#25-全局变量)
      - [2.5.1 定义](#251-定义)
      - [2.5.2 优势](#252-优势)
      - [2.5.3 劣势](#253-劣势)
      - [2.5.4 决议](#254-决议)
    - [2.6 嵌套/局部/内部类与方法](#26-嵌套局部内部类与方法)
      - [2.6.1 定义](#261-定义)
      - [2.6.2 优势](#262-优势)
      - [2.6.3 劣势](#263-劣势)
      - [2.6.4 决议](#264-决议)
    - [2.7 推导式与生成器表达式](#27-推导式与生成器表达式)
      - [2.7.1 定义](#271-定义)
      - [2.7.2 优势](#272-优势)
      - [2.7.3 劣势](#273-劣势)
      - [2.7.4 决议](#274-决议)
    - [2.8 默认迭代器与运算符](#28-默认迭代器与运算符)
      - [2.8.1 定义](#281-定义)
      - [2.8.2 优势](#282-优势)
      - [2.8.3 劣势](#283-劣势)
      - [2.8.4 决议](#284-决议)
    - [2.9 生成器](#29-生成器)
      - [2.9.1 定义](#291-定义)
      - [2.9.2 优势](#292-优势)
      - [2.9.3 劣势](#293-劣势)
      - [2.9.4 决议](#294-决议)
    - [2.10 Lambda函数](#210-lambda函数)
      - [2.10.1 定义](#2101-定义)
      - [2.10.2 优势](#2102-优势)
      - [2.10.3 劣势](#2103-劣势)
      - [2.10.4 决议](#2104-决议)
    - [2.11 条件表达式](#211-条件表达式)
      - [2.11.1 定义](#2111-定义)
      - [2.11.2 优势](#2112-优势)
      - [2.11.3 劣势](#2113-劣势)
      - [2.11.4 决议](#2114-决议)
    - [2.12 默认参数值](#212-默认参数值)
      - [2.12.1 定义](#2121-定义)
      - [2.12.2 优势](#2122-优势)
      - [2.12.3 劣势](#2123-劣势)
      - [2.12.4 决议](#2124-决议)
    - [2.13 属性(Properties)](#213-属性properties)
      - [2.13.1 定义](#2131-定义)
      - [2.13.2 优势](#2132-优势)
      - [2.13.3 劣势](#2133-劣势)
      - [2.13.4 决议](#2134-决议)
    - [2.14 True/False等价形式](#214-truefalse等价形式)
      - [2.14.1 定义](#2141-定义)
      - [2.14.2 优势](#2142-优势)
      - [2.14.3 劣势](#2143-劣势)
      - [2.14.4 决议](#2144-决议)
    - [2.15 词法域](#215-词法域)
      - [2.15.1 定义](#2151-定义)
      - [2.15.2 优势](#2152-优势)
      - [2.15.3 劣势](#2153-劣势)
      - [2.15.4 决议](#2154-决议)
    - [2.16 函数方法装饰器](#216-函数方法装饰器)
      - [2.16.1 定义](#2161-定义)
      - [2.16.2 优势](#2162-优势)
      - [2.16.3 劣势](#2163-劣势)
      - [2.16.4 决议](#2164-决议)
    - [2.17 线程](#217-线程)
      - [2.17.1 定义](#2171-定义)
      - [2.17.2 优势](#2172-优势)
      - [2.17.3 劣势](#2173-劣势)
      - [2.17.4 决议](#2174-决议)
    - [2.17 线程](#217-线程-1)
      - [2.17.1 定义](#2171-定义-1)
      - [2.17.2 优势](#2172-优势-1)
      - [2.17.3 劣势](#2173-劣势-1)
      - [2.17.4 决议](#2174-决议-1)
    - [2.18 超级功能](#218-超级功能)
      - [2.18.1 定义](#2181-定义)
      - [2.18.2 优势](#2182-优势)
      - [2.18.3 劣势](#2183-劣势)
      - [2.18.4 决议](#2184-决议)
    - [2.19 现代Python: Python3与from \_\_future\_\_ imports](#219-现代python-python3与from-__future__-imports)
      - [2.19.1 定义](#2191-定义)
      - [2.19.2 优势](#2192-优势)
      - [2.19.3 劣势](#2193-劣势)
      - [2.19.4 决议](#2194-决议)
    - [2.20 类型注解](#220-类型注解)
      - [2.20.1 定义](#2201-定义)
      - [2.20.2 优势](#2202-优势)
      - [2.20.3 劣势](#2203-劣势)
      - [2.20.4 决议](#2204-决议)
  - [Python风格规则](#python风格规则)
    - [3.1 分号](#31-分号)
    - [3.2 代码行长度](#32-代码行长度)
    - [3.3 括号](#33-括号)
    - [3.4 缩进](#34-缩进)
      - [3.4.1](#341)
    - [3.5 空行](#35-空行)
    - [3.6 空格](#36-空格)
    - [3.7 Shebang行](#37-shebang行)
    - [3.8 注释与Docstring](#38-注释与docstring)
      - [3.8.1 Docstrings](#381-docstrings)
      - [3.8.2 模块(Modules)](#382-模块modules)
      - [3.8.3 函数与方法](#383-函数与方法)
      - [3.8.4 类](#384-类)
      - [3.8.5 代码块与行内注释](#385-代码块与行内注释)
      - [3.8.6 标点、拼写与语法](#386-标点拼写与语法)
    - [3.9 字符串](#39-字符串)
      - [3.9.1 日志](#391-日志)
      - [3.9.2 错误信息](#392-错误信息)
    - [3.10 文件与套接字](#310-文件与套接字)
    - [3.11 TODO注释](#311-todo注释)
    - [3.12 导入格式](#312-导入格式)
    - [3.13 语句](#313-语句)
    - [3.14 Accessors](#314-accessors)
    - [3.15 命名](#315-命名)
      - [3.15.1 避免使用的名称](#3151-避免使用的名称)
      - [3.15.2 命名约定](#3152-命名约定)
      - [3.15.3 代码文件命名](#3153-代码文件命名)
      - [3.15.4](#3154)
    - [3.16 Main函数](#316-main函数)
    - [3.17 函数长度](#317-函数长度)
    - [3.18 类型注解](#318-类型注解)
      - [3.18.1 一般规则](#3181-一般规则)
      - [3.18.2 换行](#3182-换行)
      - [3.18.3 前向声明](#3183-前向声明)
      - [3.18.4 默认值](#3184-默认值)
      - [3.18.5 None类型](#3185-none类型)
      - [3.18.6 类型别名](#3186-类型别名)
      - [3.18.7 忽略类型](#3187-忽略类型)
      - [3.18.8 类型变量](#3188-类型变量)
      - [3.18.9 元组、列表比较](#3189-元组列表比较)
      - [3.18.10 TypeVar](#31810-typevar)
      - [3.18.11 字符串类型](#31811-字符串类型)
      - [3.18.12 导入类型](#31812-导入类型)
      - [3.18.13 条件导入](#31813-条件导入)
      - [3.18.14 循环依赖](#31814-循环依赖)
      - [3.18.15 泛型](#31815-泛型)
  - [4 结语](#4-结语)

### 1 背景
在谷歌中，主要使用的动态语言是Python。本风格指南列举了在Python编程中推荐使用的和避免使用的规则。

为了能够正确格式化代码，我们创建了[Vim配置文件](https://google.github.io/styleguide/google_python_style.vim)，对于Emacs用户，可以使用默认配置文件。

很多团队使用[yapf](https://github.com/google/yapf/)自动格式化工具以避免关于格式的争论。
### 2 Python语言规则
#### 2.1 Lint
基于[pylintrc](https://google.github.io/styleguide/pylintrc)在你的代码上运行```pylint```
##### 2.1.1 定义
```pylint```是一个可以用来发现Python代码中存在的缺陷与风格问题的工具。它可以发现那些通常在静态语言例如C和C++中本应由编译器发现的问题。由于Python的动态本性，可能一些警告是错误的；但是这些不正确的警告是罕见的。
##### 2.1.2 优势
能够捕获诸如拼写错误、使用未赋值的变量等容易忽略的错误。
##### 2.1.3 劣势
```pylint```不是完美的。为了能够利用这个工具，有时候我们需要使用一些变通方式，以禁止或修复警告。
##### 2.1.4 决议
确保使用```pylint```检查你的代码。
禁止那些不适当的警告，确保其他的问题可以被发现。可以通过行级注释禁止警告。
```python
dict = 'something awful' # Bad Idea... pylint: disable=redefined-buildin
```
```pylint```警告通过符号名称(```empty-docstring```) 标识，谷歌特定警告以```g-```开头。

如果禁止警告的原因无法通过符号名称清晰表达，可以添加一个解释。

通过此方式禁止的告警有一个好处是可以很容易的找到它。

可以通过以下命令查看所有```pylint```的警告：
```bash
pylint --list-msgs
```
使用如下命令获取某个警告的详细信息：
```bash
pylint --help-msg=C6409
```
推荐使用```pylint: disable```代替已被废弃的过时形式```pylint: disable-msg```
未使用的参数警告可以通过在函数的起始部分添加删除变量语句来修复警告。同时添加注释以解释删除的原因。"Unused"就足够了。例如：
```python
def viking_cafe_order(spam, beans, eggs=None):
    del beans, eggs  # Unused by vikings.
    return spam + spam + spam
```
其他常规修复这一警告的形式包括使用'\_'作为未使用的参数的标识，或在未使用的变量名前添加'unused\_'，或者为未使用的变量赋值'\_'。这些方式都是允许使用的，但不鼓励使用这种方式。因为这些方式会阻止函数的调用方通过变量名传值，并且不会强制这些未使用的参数未来也不会被使用。
#### 2.2 导入(Imports)
只能在包和模块上使用```import```语句，不要在独立的类与函数上使用。需要注意的是对于[导入类型](#31812-导入类型)此规则无效。
##### 2.2.1 定义
一种模块之间复用代码的机制
##### 2.2.2 优势
命名空间管理约定是简单的。每个标识符的来源通过统一的方式表示；```x.Obj```表示对象```Obj```定义在模块```x```中。
##### 2.2.3 劣势
模块名称仍然可能冲突。一些模块的名称会较长，从而带来使用的不便。
##### 2.2.4 决议
* 使用```import x```，导入包与模块
* 使用```from x import y```，其中x表示包前缀，y表示不含前缀的模块名。
* 使用```from x import y as z```，当需要导入两个名称均为```y```的模块或```y```较长时。
* 使用```import y as z```，仅当```z```为标准缩写（例如：np为numpy的缩写）

例如模块```sound.effects.echo```可通过如下方式导入：
```python
from sound.effects import echo
...
echo.EchoFilter(input, output, delay=0.7, atten=4)
```
在导入时不要使用相对名称。即使模块在相同包下，也要使用完整的包名。此要求可以阻止潜在的包被导入两次的问题发生。
从[导入类型](#31812-导入类型)与[six.moves模块](https://six.readthedocs.io/#module-six.moves)中导入不在此规范约束范围内。
#### 2.3 包(Packages)
使用模块全路径形式导入模块。
##### 2.3.1 优势
避免模块名称冲突，避免导入开发人员不期望的路径下的模块。使模块的查找变得简单。
##### 2.3.2 劣势
由于需要保持包的层级，代码部署难度增加。不过在现代部署机制下，这不是一个问题。
##### 2.3.3 决议
所有代码在导入模块时都要使用模块名加包名的形式。
导入应当如下所示：

推荐方式：
```python
# Reference absl.flags in code with the complete name (verbose).
import absl.flags
from doctor.who import jodie

FLAGS = absl.flags.FLAGS
```
```python
# Reference flags in code with just the module name (common).
from absl import flags
from doctor.who import jodie

FLAGS = flags.FLAGS
```
禁止方式：（假设文件位于```doctor/who/```，```jodie.py```也位于相同位置）
```python
# Unclear what module the author wanted and what will be imported.  The actual
# import behavior depends on external factors controlling sys.path.
# Which possible jodie module did the author intend to import?
import jodie
```
尽管在一些环境中主程序位于```sys.path```下，我们仍然不能假设所有主程序都位于```sys.path```下。这种情况下，代码应当假设```import jodie```导入的是第三方的或指向位于顶层的名为```jodie```的包，而非相同路径下的```jodie.py```。
#### 2.4 异常(Exceptions)
异常允许使用，但必须小心使用。
##### 2.4.1 定义
异常意味着中断正常的执行流程，转入处理错误或其他异常情况。
##### 2.4.2 优势
错误处理代码不会引起正常执行流代码混杂。当某个特定的情况发生时，异常允许执行流程忽略多层结构直接返回。例如
在N层嵌套函数中一步返回错误。
##### 2.4.3 劣势
可能会导致执行流程混乱。在调用第三方库时可能会忽略错误。
##### 2.4.4 决议
异常的使用必须遵循特定的情形：
* 在表意充分的情况下，使用内建的异常类。例如，抛出```ValueError```表示诸如违反先决条件的编程错误（例如在需要一个正数的地方传入一个负数的错误）。不要在公有API中使用```assert```语句验证参数的值。```assert```是用来保证内部正确性的，不能用于强制正确使用，也不能用于表示未知事件的发生。如果，使用抛出异常语句。例如：

  推荐方式
  ```python
  def connect_to_next_port(self, minimum):
    """Connects to the next available port.

    Args:
      minimum: A port value greater or equal to 1024.

    Returns:
      The new minimum port.

    Raises:
      ConnectionError: If no available port is found.
    """
    if minimum < 1024:
      # Note that this raising of ValueError is not mentioned in the doc
      # string's "Raises:" section because it is not appropriate to
      # guarantee this specific behavioral reaction to API misuse.
      raise ValueError(f'Min. port must be at least 1024, not {minimum}.')
    port = self._find_next_open_port(minimum)
    if not port:
      raise ConnectionError(
          f'Could not connect to service on port {minimum} or higher.')
    assert port >= minimum, (
        f'Unexpected port {port} when minimum was {minimum}.')
    return port
  ```
  禁止方式
  ```python
  def connect_to_next_port(self, minimum):
    """Connects to the next available port.

    Args:
      minimum: A port value greater or equal to 1024.

    Returns:
      The new minimum port.
    """
    assert minimum >= 1024, 'Minimum port must be at least 1024.'
    port = self._find_next_open_port(minimum)
    assert port is not None
    return port
  ```
* 依赖库内或包内可能会定义自己的异常。如此则必须继承自已有的异常类。新定义的异常名称应当以```Error```结尾，并且不应引入混乱（```foo.FooError```）。
* 禁止使用捕获所有异常的语句```except:```，禁止捕获异常```Exception```或```StandardError```，除非如下情形：
  * 将捕获的异常重新抛出
  * 当发生的异常无需外部知晓仅需进行记录而需要在程序中创建一个隔离点时。例如为防止一个线程崩溃而在最外层代码库创建的保护。
  Python在异常方面非常宽容，```except```会捕获所有的错误，包括名称拼写错误，sys.exit()调用，Ctrl+C中断，单元测试失败以及那些你不想捕获的其他种类异常。
* 最小化在```try```/```except```中的代码数量。```try```中代码越多，越有可能抛出你期望之外的代码。在这种情况下，```try```/```except```会隐藏真正的错误。
* 使用```finally```运行那些无论```try```中是否抛出异常都需要执行的代码。这往往在做清理时比较有用，例如关闭文件。

#### 2.5 全局变量
避免使用全局变量
##### 2.5.1 定义
定义于模块级别或类特性的变量。
##### 2.5.2 优势
偶尔会有用。
##### 2.5.3 劣势
会存在潜在的在导入时更改模块行为的风险，原因是全局变量的赋值在第一次模块导入时已经完成
##### 2.5.4 决议
避免使用全局变量

作为技术级别的变量，模块级别的常量是允许并鼓励使用的。例如：```MAX_HOLY_HANDGRENADE_COUNT = 3```。常量命名必须使用全部大写加下划线。参见[命名](#315-命名)。
如果需要，全局变量应当声明在模块类型，并通过在命名前加```\_```的方式保证仅内部可见。外部访问必须通过公有的模块级别函数。参见[命名](#315-命名)。
#### 2.6 嵌套/局部/内部类与方法
嵌套的局部函数和类。允许使用内部类。
##### 2.6.1 定义
类可以被定义在方法、函数或类的内部。函数可被定义在方法或函数的内部。嵌套函数对于闭包内定义变量有只读权限。
##### 2.6.2 优势
允许在一个非常有限的使用范围内定义一个工具类或工具函数。通常被用于实现装饰器。
##### 2.6.3 劣势
嵌套函数与嵌套类无法直接测试。嵌套结构会导致外部函数体过长，可读性降低。
##### 2.6.4 决议

#### 2.7 推导式与生成器表达式
简单场景下允许使用。
##### 2.7.1 定义
##### 2.7.2 优势
##### 2.7.3 劣势
##### 2.7.4 决议
#### 2.8 默认迭代器与运算符
##### 2.8.1 定义
##### 2.8.2 优势
##### 2.8.3 劣势
##### 2.8.4 决议
#### 2.9 生成器
##### 2.9.1 定义
##### 2.9.2 优势
##### 2.9.3 劣势
##### 2.9.4 决议
#### 2.10 Lambda函数
##### 2.10.1 定义
##### 2.10.2 优势
##### 2.10.3 劣势
##### 2.10.4 决议
#### 2.11 条件表达式
##### 2.11.1 定义
##### 2.11.2 优势
##### 2.11.3 劣势
##### 2.11.4 决议
#### 2.12 默认参数值
##### 2.12.1 定义
##### 2.12.2 优势
##### 2.12.3 劣势
##### 2.12.4 决议
#### 2.13 属性(Properties)
##### 2.13.1 定义
##### 2.13.2 优势
##### 2.13.3 劣势
##### 2.13.4 决议
#### 2.14 True/False等价形式
##### 2.14.1 定义
##### 2.14.2 优势
##### 2.14.3 劣势
##### 2.14.4 决议
#### 2.15 词法域
##### 2.15.1 定义
##### 2.15.2 优势
##### 2.15.3 劣势
##### 2.15.4 决议
#### 2.16 函数方法装饰器
##### 2.16.1 定义
##### 2.16.2 优势
##### 2.16.3 劣势
##### 2.16.4 决议
#### 2.17 线程
##### 2.17.1 定义
##### 2.17.2 优势
##### 2.17.3 劣势
##### 2.17.4 决议
#### 2.17 线程
##### 2.17.1 定义
##### 2.17.2 优势
##### 2.17.3 劣势
##### 2.17.4 决议
#### 2.18 超级功能
##### 2.18.1 定义
##### 2.18.2 优势
##### 2.18.3 劣势
##### 2.18.4 决议
#### 2.19 现代Python: Python3与from \_\_future\_\_ imports
##### 2.19.1 定义
##### 2.19.2 优势
##### 2.19.3 劣势
##### 2.19.4 决议
#### 2.20 类型注解
##### 2.20.1 定义
##### 2.20.2 优势
##### 2.20.3 劣势
##### 2.20.4 决议
### Python风格规则
#### 3.1 分号
不要在代码行的结尾使用分号，也不要使用分号将两条语句放到一行中。
#### 3.2 代码行长度
代码行最长为80个字符。
80个字符限制的例外：
* 更长的导入语句
* URL、路径或注释中包含的较长标志
* 定义在模块级别的不包含空格的字符串常量，这种常量较难分为两行，例如URL与路径。
  * Pylint禁用注释。（例如：```# pylint: disable=invalid-name```）

除```with```语句需要三个或更多上下文管理的情况外，不要使用反斜杠进行代码换行。

使用Python中的[小括号、中括号与大括号中的隐式代码行拼接](http://docs.python.org/reference/lexical_analysis.html#implicit-line-joining)。如果需要，可以在表达式前后添加额外的小括号。

推荐形式：
```python
foo_bar(self, width, height, color='black', design=None, x='foo',
             emphasis=None, highlight=0)

     if (width == 0 and height == 0 and
         color == 'red' and emphasis == 'strong'):
```
当一个字符串无法放在一行中时，使用小括号的隐式代码行拼接。
```python
x = ('This will build a very long long '
     'long long long long long long string')
```
在注释中，必要时可将长的URL放入单独的一行。

推荐形式：
```python
# See details at
# http://www.example.com/us/developer/documentation/api/content/v2.0/csv_file_name_extension_full_specification.html
```
禁止形式：
```python
# See details at
# http://www.example.com/us/developer/documentation/api/content/\
# v2.0/csv_file_name_extension_full_specification.html
```
当定义的```with```语句的表达式有三行或更多行，允许使用反斜杠连接代码行。对于两行表达式的情形，可以使用嵌套```with```语句：

推荐形式：
```python
with very_long_first_expression_function() as spam, \
    very_long_second_expression_function() as beans, \
    third_thing() as eggs:
    place_order(eggs, beans, spam, beans)
```
禁止形式：
```python
with VeryLongFirstExpressionFunction() as spam, \
    VeryLongSecondExpressionFunction() as beans:
    PlaceOrder(eggs, beans, spam, beans)
```
推荐形式：
```python
with very_long_first_expression_function() as spam:
    with very_long_second_expression_function() as beans:
        place_order(beans, spam)
```
请注意以上关于行拼接的例子中包含的缩进；具体解释请参阅[缩进](https://google.github.io/styleguide/pyguide.html#s3.4-indentation)

对于其他行达到80个字符限制，且yapf无法自动，允许行长度超过这一限制。
#### 3.3 括号
谨慎使用括号

在元组上使用括号是可以的，但并不是必须的。不要在返回语句或条件语句中使用括号，除非是为了行拼接的目的或是为了表示元组。

推荐方式：
```python
if foo:
    bar()
while x:
    x = bar()
if x and y:
    bar()
if not x:
    bar()
# For a 1 item tuple the ()s are more visually obvious than the comma.
onesie = (foo,)
return foo
return spam, beans
return (spam, beans)
for (x, y) in dict.items(): ...
```
禁止形式：
```python 
if (x):
    bar()
if not(x):
    bar()
return (foo)
```
#### 3.4 缩进
使用*4个空格*缩进代码

不要使用制表符或者制表符空格混合的方式。对于隐式行合并（[代码行长度](#32-代码行长度)一节中描述的情况）的情况，要么保证括号包含的元素垂直对齐，要么使用4个空格的[悬挂缩进](https://www.google.com.hk/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjpneOuuPzuAhXLGaYKHShaCUkQFjABegQIBBAD&url=https%3A%2F%2Fbaike.baidu.com%2Fitem%2F%25E6%2582%25AC%25E6%258C%2582%25E7%25BC%25A9%25E8%25BF%259B&usg=AOvVaw2__x8ye-clizvRX5Y95xXv)，同时保证左括号后换行。

推荐方式：
```python
# Aligned with opening delimiter
foo = long_function_name(var_one, var_two,
                        var_three, var_four)
meal = (spam,
        beans)

# Aligned with opening delimiter in a dictionary
foo = {
    long_dictionary_key: value1 +
                        value2,
    ...
}

# 4-space hanging indent; nothing on first line
foo = long_function_name(
    var_one, var_two, var_three,
    var_four)
meal = (
    spam,
    beans)

# 4-space hanging indent in a dictionary
foo = {
    long_dictionary_key:
        long_dictionary_value,
    ...
}
```
禁止形式：
```python
# Stuff on first line forbidden
foo = long_function_name(var_one, var_two,
    var_three, var_four)
meal = (spam,
    beans)

# 2-space hanging indent forbidden
foo = long_function_name(
    var_one, var_two, var_three,
    var_four)

# No hanging indent in a dictionary
foo = {
    long_dictionary_key:
    long_dictionary_value,
    ...
}
```
##### 3.4.1 

#### 3.5 空行
在顶级定义之间使用两个空行，例如函数定义和类定义。在方法之间使用一行定义，在类定义行与类第一个方法之间使用一个空行。在方法定义行后面不能再加空行。在函数和方法体内部可以按照判断自行添加空行。
#### 3.6 空格
遵循标准印刷规则在标点符号前后使用空格。

在小括号、中括号、大括号内部不要添加空格。

推荐方式：
```python
spam(ham[1], {eggs: 2}, [])
```

禁止方式：
```python
spam( ham[ 1 ], { eggs: 2 }, [ ] )
```
在逗号分号冒号前不要添加空格。除行尾外，在逗号分号冒号后添加空格。

推荐方式：
```python
if x == 4:
    print(x, y)
x, y = y, x
```

禁止方式：
```python
if x == 4 :
    print(x , y)
x , y = y , x
```
在参数列表、索引或数组前的左括号之前不要添加空格

推荐方式：
spam(1)
```
禁止方式：
```python
spam (1)
```
推荐方式：
```python
dict['key'] = list[index]
```
禁止方式：
```python
dict ['key'] = list [index]
```
在赋值运算符（```=```）、比较运算符（```==，<，>，!=，<>，<=，>=，in，not in，is，is not```）与布尔运算符（```and，or，not```）前后各添加一个空格。是否在数学运算符（```+```，```-```，```*```，```/```，```//```，```%```，```**```，```@```）前后添加空格可由个人自行决断。

推荐方式：
```python
x == 1
```
禁止方式：
```python
x<1
```
当使用了[类型注解](#220-类型注解)时，需要在默认值的```=```前后添加空格外，其他情况的默认值定义均无需使用空格。

推荐方式：
```python
def complex(real, imag=0.0): return Magic(r=real, i=imag)
def complex(real, imag: float = 0.0): return Magic(r=real, i=imag)
```
禁止方式：
```python
def complex(real, imag = 0.0): return Magic(r = real, i = imag)
def complex(real, imag: float=0.0): return Magic(r = real, i = imag)
```
不要使用空格来保持多行中符号的垂直对齐，这会增加维护负担。

推荐方式：
```python
foo = 1000  # comment
long_name = 2  # comment that should not be aligned

dictionary = {
    'foo': 1,
    'long_name': 2,
}
```
禁止方式：
```python
foo       = 1000  # comment
long_name = 2     # comment that should not be aligned

dictionary = {
    'foo'      : 1,
    'long_name': 2,
}
```
#### 3.7 [Shebang](https://zh.wikipedia.org/wiki/Shebang)行
大多数的python文件无需以```#!```作为起始行。在程序的主文件中使用```#!/usr/bin/env python3```（以支持虚拟环境）或者依[PEP-394](https://www.python.org/dev/peps/pep-0394/)使用```#!/usr/bin/python3```。
#### 3.8 注释与Docstring
确保正确使用模块、函数、方法的docstring以及行内注释
##### 3.8.1 Docstrings
Python使用docstrings文档化代码。docstring是包、模块、类或者函数内的第一条语句。```pydoc```通过对象的```__doc__```拉取这些字符串（在模块上运行```pydoc```并观察结果）。按照[PEP 257](https://www.google.com/url?sa=D&q=http://www.python.org/dev/peps/pep-0257/)，使用三个双引号```"""```作为docstrings的格式。
##### 3.8.2 模块(Modules)
##### 3.8.3 函数与方法
##### 3.8.4 类
##### 3.8.5 代码块与行内注释
##### 3.8.6 标点、拼写与语法
#### 3.9 字符串
##### 3.9.1 日志
##### 3.9.2 错误信息
#### 3.10 文件与套接字
#### 3.11 TODO注释
#### 3.12 导入格式
#### 3.13 语句
#### 3.14 Accessors
#### 3.15 命名
##### 3.15.1 避免使用的名称
##### 3.15.2 命名约定
##### 3.15.3 代码文件命名
##### 3.15.4
#### 3.16 Main函数
#### 3.17 函数长度
#### 3.18 类型注解
##### 3.18.1 一般规则
##### 3.18.2 换行
##### 3.18.3 前向声明
##### 3.18.4 默认值
##### 3.18.5 None类型
##### 3.18.6 类型别名
##### 3.18.7 忽略类型
##### 3.18.8 类型变量
##### 3.18.9 元组、列表比较
##### 3.18.10 TypeVar
##### 3.18.11 字符串类型
##### 3.18.12 导入类型
##### 3.18.13 条件导入

##### 3.18.14 循环依赖
循环依赖是由类型的坏味道引起的。这种代码是练习重构的好实例。尽管技术上可以保留循环依赖，但是各种构建系统会阻止模块彼此依赖。

使用```Any```替换引起循环依赖的模块。设置一个有意义的[别名](#3186-类型别名)，在本模块内使用新的类型名称（Any的任何特性均为Any）。在别名的定义与最后一条导入语句之间添加空行。
```python
from typing import Any

some_mod = Any  # some_mod.py imports this module.
...

def my_method(self, var: "some_mod.SomeType") -> None:
  ...
```
##### 3.18.15 泛型
当添加注解时，推荐指定参数类型为泛型，否则，[参数类型将被推导为```Any```](https://www.python.org/dev/peps/pep-0484/#the-any-type)
```python
def get_names(employee_ids: List[int]) -> Dict[int, Any]:
  ...
```
```python
# These are both interpreted as get_names(employee_ids: List[Any]) -> Dict[Any, Any]
def get_names(employee_ids: list) -> Dict:
  ...

def get_names(employee_ids: List) -> Dict:
  ...
```
如果最适合泛型的类型是```Any```，那么进行显式声名，但在很多场景下```TypeVar```更合适：
```python
def get_names(employee_ids: List[Any]) -> Dict[Any, Text]:
  """Returns a mapping from employee ID to employee name for given IDs."""
```
```python
T = TypeVar('T')
def get_names(employee_ids: List[T]) -> Dict[T, Text]:
  """Returns a mapping from employee ID to employee name for given IDs."""
```
### 4 结语
当编写代码时，花几分钟的时间阅读一下周围的代码并确认代码的风格。如果算术运算符前后使用了空格，那么你也使用。如果注释前后使用了#符号，那么你也如此。

本风格指南的意义是使用常规的词汇进行编程，以使开发人员重点关注内容而非实现方式。我们提供了大家普遍熟悉的词汇作为全局风格规范，但小范围的风格规范也同等重要。如果你在某个文件中增加的代码与已经存在的代码有很大不同，将导致代码阅读人员读到该代码时失去顺滑感。应避免这种情况。