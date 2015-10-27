# modules

If you quit from the Python interpreter and enter it again, the definitions you have made (functions and variables) are lost. Therefore, if you want to write a somewhat longer program, you are better off using a text editor to prepare the input for the interpreter and running it with that file as input instead. This is known as creating a script. As your program gets longer, you may want to split it into several files for easier maintenance. You may also want to use a handy function that you’ve written in several programs without copying its definition into each program.

如果你从python退出又重新进入的话，你创建过的定义（函数和变量）会丢失。因此，如果你想写一些长的程序，为了给输入python做准备工作你最好使用文本编辑器，and running it with that file as input instead(不知道怎么翻比较好)。这就是所谓的创建script。随着你程序的变长，为了更好的维护，你可能会想把程序分成几个文件。你可能也会想使用你已经在一些文件里写过的hardy函数，而不是复制函数到每个文件。



To support this, Python has a way to put definitions in a file and use them in a script or in an interactive instance of the interpreter. Such a file is called a module; definitions from a module can be imported into other modules or into the main module (the collection of variables that you have access to in a script executed at the top level and in calculator mode).

为了支持这种做法，python有种方法用来把定义放进一个文件，并且在script或an interactive instance of the interpreter中来使用这些定义。这种文件就叫module。一个module中的定义可以导入到其他的modules中或是主module中（你可以进入的script中的变量集合，在计算模式中会被优先执行）



A module is a file containing Python definitions and statements. The file name is the module name with the suffix .py appended. Within a module, the module’s name (as a string) is available as the value of the global variable __name__. For instance, use your favorite text editor to create a file called fibo.py in the current directory with the following contents:

Module是一种包括了python的定义和statements的文件。文件名是module名并加上.py的后缀。在一个module中，module的名字（作为字符串string）作为the value of the global variable_name_是可用的。举例来说，用你最爱的编辑器在现有directory建了个名叫fibo.py的文件，如下所示：

# Fibonacci numbers module

def fib(n):    # write Fibonacci series up to n
    a, b = 0, 1
    while b < n:
        print b,
        a, b = b, a+b

def fib2(n): # return Fibonacci series up to n
    result = []
    a, b = 0, 1
    while b < n:
        result.append(b)
        a, b = b, a+b
return result


Now enter the Python interpreter and import this module with the following command:

太简单不翻了



>>> import fibo



This does not enter the names of the functions defined in fibo directly in the current symbol table; it only enters the module name fibo there. Using the module name you can access the functions:

在现symbol table中，这步没有直接输入在fibo里定义的函数名称；仅仅只是输入了module的名字fibo。通过调用Module的名称，你可以直接进入这些函数：



>>> fibo.fib(1000)
1 1 2 3 5 8 13 21 34 55 89 144 233 377 610 987
>>> fibo.fib2(100)
[1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]
>>> fibo.__name__
'fibo'



If you intend to use a function often you can assign it to a local name:

如果你打算经常使用一个函数，你可以把它指定到本地名

>>>
>>> fib = fibo.fib
>>> fib(500)
1 1 2 3 5 8 13 21 34 55 89 144 233 377




Module可以像函数的说明一样，可以包括执行它时的说明。这些说明是为了初始化module。因此，module的作者可以在module里使用global变量，而不用担心
