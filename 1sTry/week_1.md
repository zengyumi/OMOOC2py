# Week 1  交互 101

## 任务内容

整体任务概述:

完成一个极简交互式日记系统,需求如下:
一次接收输入一行日记
保存为本地文件
再次运行系统时,能打印出过往的所有日记
时限: 0wd4~1wd3
发布: 发布到各自仓库的 _src/om2py0w/0wex1/ 目录中
指标:
包含软件使用说明书: README.md
能令其它学员根据说明书,运行系统,完成所有功能

### 交互 101-脚本调用
首先,得有一个稳定的代码记录容器: 脚本

以之前上传的 _src/om2py0w/0wex1/main.py 为例
如何调用之?
并确保每次调用返回相同的结果?

参考:

BeginnersGuideChinese - Python Wiki
6. Modules — Python 2.7.10 documentation
Code Style — The Hitchhiker's Guide to Python

### 交互 101-调用参数

然后, 脚本得能接收外部数据的输入

还是以 _src/om2py0w/0wex1/main.py 来操作吧
如何做到调用main.py获得外部的数据的同时,不需要每次都修改代码?
参考:

10. Brief Tour of the Standard Library — Python 2.7.10 documentation

### 交互 101-输入中文


接着最常见的要求,脚本如何获得外部中文文本?

还是以 _src/om2py0w/0wex1/main.py 为例吧
如果给的参数是中文字符, 运行脚本会发生什么事儿?
解决之!

参考:

2. Using the Python Interpreter — Python 2.7.10 documentation
docopt—language for description of command-line interfaces

### 交互 101-持续交互

每次记录一行日志,都要调用一次脚本嘛!?(嫌麻烦不?)

如何令 _src/om2py0w/0wex1/main.py 可以一直运行,等待我们的输入?
或是接受其它命令?
怎么退出脚本?

参考:

2. Built-in Functions — Python 2.7.10 documentation

### 交互 101-输出为文件
每次记录的日志如何变成一个本地文件,永久保存?

先不管数据结构, 就原样保存到文件(比如txt格式的)中吧!
文本怎么实现换行?
是否要加日期?
中文用什么编码?

参考:

open() 2. Built-in Functions — Python 2.7.10 documentation
5. Built-in Types — Python 2.7.10 documentation
6. 

### 交互 101-回读文本数据

那么,最后一个功能就能串联起来成为一个 mini 软件了!

每次运行 _src/om2py0w/0wex1/main.py 时
怎么自动将过往的日志都打印出来?
细节:
如何找到日志文件?
如何打开日志文件?
如何读取文件内容?
如何输出日志?
...
中文输出 OK 嘛?

参考:

open() 2. Built-in Functions — Python 2.7.10 documentation
5. Built-in Types — Python 2.7.10 documentation
