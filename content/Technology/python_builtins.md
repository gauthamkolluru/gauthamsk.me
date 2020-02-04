---
title: "Python Builtins"
categories: ["Python"]
tags: ["Python"]
date: 2020-02-03T17:13:00+05:30
publishdate: 2020-02-03T20:00:36+05:30
draft: true
---

* Background 
* Idea
* how to go through
* function
* conclusion

## Background

One of the `key` aspects of `Python's` popularity is it's extensive `Libraries`. With the inception of Machine Learning, Data Science and Artificial Intelligence in general, people have sure become familiar with the packages like `scikit learn`, `numpy`, `pandas` and more but most of the functions that reside in those packages are still staying out of sight of the human eye.

Likewise, not until recently, I have come across the `os.path.expanduser()` function from the `os` module, which had been super useful for the script that I was developing. And this was suggested by my _[mentor](https://sharats.me/)_.

And almost instantaneously I've decided that, one way to _at least_ learn about existence of a lot of such functions is to make sure to skim the _amazing_ documentation every once in a while and hopefully periodically (intervals of _every day_ sounds _too ambitious_ and _every week_ sounds _too lethargic_, so, let's see) and implement the famous `Feynman Technique` with it.

## Idea

<!-- Starting right with the \_\_builtins__ The basic idea is to learn about a function including about each of it's arguments  -->

<!-- #TODO: Write a brief description -->

The idea is to _literally_ look into each function available in each module of the Python Standard Library with `syntax` and examples along with some useful usecases.

For the purpose of this article we'll only be covering the functions that are part of the `modules` of the [`Python Standard Library`](https://docs.python.org/3/library/index.html).

## Platform

This article is written with `Python 3.8` running on `Microsoft Windows 10`, as shown below :

``` powershell
PS C:\> systeminfo
OS Name:    Microsoft Windows 10 Enterprise

PS C:\> python -V
Python 3.8.0
```

<!-- ## How to use this page effectively

> _Just in case your adrenaline is rushing you to scroll right to the bottom of this page, read the below_

Since, I expect to update this page regularly with more and more functions which would eventually lead to exhibiting increase in the length of the page to more than frustrating numbers of scrolls, I suggest you to either use `ctrl/cmd + f` key combination and find the word you're looking for or use the `PgDn` key to manually scroll but with a relatively better levels of frustration.-->

Note: 

1. This article is not a subtitute for the official documentation. The official documentation is the base upon which some examples and certain practical nuances are being added. This document is intended as a supplement that covers the topics with additional detail.

2. We'll not be convering any of the standard or builtin `Exception` classes or type as part of this article. However, I might do separate article specific to them in future.

## Library : Standard

The Python _Modules_ and _Functions_ that shipped along with the Python interpreter are called as the `Python Standard Library`. Some of the components (modules / functions) are optional yet are commonly shipped through Python distributions. 

The library contains modules written in C for system level access, as well as the ones written in Python to provide some standardised solutions like `.sort()`

Though most of the modules and functions are common among the different distributions, there can be some _platform_ (Windows,Unix (based)) specific or _distribution_ (CPython, IronPython, Anaconda) specific modules or functions that can be found only in their respective distributions.

#TODO: Write a brief description

### Module : Builtins

As the title suggests, this module will be hosting the functions that reside in the `__builtins__ ` module that are packaged with the Python distribution and are loaded as soon as the interpreter is invoked.

To check the functions available in the `__builtins__`  module of the _Python_ distribution residing in your machine,

```powershell
PS C:\> python

Python 3.8.0 (tags/v3.8.0:fa919fd, Oct 14 2019, 19:37:50) [MSC v.1916 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.

>>> dir(__builtins__)

['ArithmeticError', 'AssertionError', 'AttributeError', 'BaseException', 'BlockingIOError', 'BrokenPipeError', 'BufferError', 'BytesWarning', 'ChildProcessError', 'ConnectionAbortedError', 'ConnectionError', 'ConnectionRefusedError', 'ConnectionResetError', 'DeprecationWarning', 'EOFError', 'Ellipsis', 'EnvironmentError', 'Exception', 'False', 'FileExistsError', 'FileNotFoundError', 'FloatingPointError', 'FutureWarning', 'GeneratorExit', 'IOError', 'ImportError', 'ImportWarning', 'IndentationError', 'IndexError', 'InterruptedError', 'IsADirectoryError', 'KeyError', 'KeyboardInterrupt', 'LookupError', 'MemoryError', 'ModuleNotFoundError', 'NameError', 'None', 'NotADirectoryError', 'NotImplemented', 'NotImplementedError', 'OSError', 'OverflowError', 'PendingDeprecationWarning', 'PermissionError', 'ProcessLookupError', 'RecursionError', 'ReferenceError', 'ResourceWarning', 'RuntimeError', 'RuntimeWarning', 'StopAsyncIteration', 'StopIteration', 'SyntaxError', 'SyntaxWarning', 'SystemError', 'SystemExit', 'TabError', 'TimeoutError', 'True', 'TypeError', 'UnboundLocalError', 'UnicodeDecodeError', 'UnicodeEncodeError', 'UnicodeError', 'UnicodeTranslateError', 'UnicodeWarning', 'UserWarning', 'ValueError', 'Warning', 'WindowsError', 'ZeroDivisionError', '_', '__build_class__', '__debug__', '__doc__', '__import__', '__loader__', '__name__', '__package__', '__spec__', 'abs', 'all', 'any', 'ascii', 'bin', 'bool', 'breakpoint', 'bytearray', 'bytes', 'callable', 'chr', 'classmethod', 'compile', 'complex', 'copyright', 'credits', 'delattr', 'dict', 'dir', 'divmod', 'enumerate', 'eval', 'exec', 'exit', 'filter', 'float', 'format', 'frozenset', 'getattr', 'globals', 'hasattr', 'hash', 'help', 'hex', 'id', 'input', 'int', 'isinstance', 'issubclass', 'iter', 'len', 'license', 'list', 'locals', 'map', 'max', 'memoryview', 'min', 'next', 'object', 'oct', 'open', 'ord', 'pow', 'print', 'property', 'quit', 'range', 'repr', 'reversed', 'round', 'set', 'setattr', 'slice', 'sorted', 'staticmethod', 'str', 'sum', 'super', 'tuple', 'type', 'vars', 'zip']
```

#TODO: Write a brief description

* abs() : `abs` is an abbreviation for `absolute` , the function that belongs to field of Mathematics. It takes the _input_ of `one`  `real` or `complex` number and returns:

    - in case of `real` :
        - the `unsigned` value of the input
        - Ex:
            ``` python
            >>> abs(-5) #int
            5
            >>> abs(-5.5) #float
            5.5
            >>> abs(5.5)
            5.5
            ```

        


    - in case of `complex` :
        - the `magnitude` of the input => abs(a+bj) == <span>&radic; (a)<sup>2</sup>+(b)<sup>2</sup></span>
        - Ex:
            ``` python
            >>> abs(3+4j)
            5.0
            >>> abs(-1+3j)
            3.1622776601683795
            ```

