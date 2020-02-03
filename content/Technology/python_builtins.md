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

One of the `key` aspects of `Python's` popularity today is it's `large Libraries` , both __[Standard](https://docs.python.org/3/library/index.html)__ and __[External](https://pypi.org)__.

And until recently, I haven't come across the `os.path.expanduser()` function from the `os` module, which had been super useful for the script that I was developing. And this was suggested by my _[mentor](https://sharats.me/)_.

Almost instantaneously I've decided that, one way to _at least_ learn about existence of a lot of such functions is to make sure to skim the amazing documentation every once in a while and hopefully periodically (intervals of _every day_ sounds _too ambitious_ and _every week_ sounds _too lethargic_, so, let's see) and implement the famous `Feynman Technique` with it.

## Idea

<!-- Starting right with the \_\_builtins__ The basic idea is to learn about a function including about each of it's arguments  -->

#TODO: Write a brief description

For the purpose of this article we'll only be covering the functions that are part of the `modules` of the `Standard Library` .

## Platform

This article is written with `Python 3.8` running on `Windows 10` . Here are the system details:

``` powershell
PS C:\> systeminfo
OS Name:    Microsoft Windows 10 Enterprise

PS C:\> python -V
Python 3.8.0
```

<!-- ## How to use this page effectively

> _Just in case your adrenaline is rushing you to scroll right to the bottom of this page, read the below_

Since, I expect to update this page regularly with more and more functions which would eventually lead to exhibiting increase in the length of the page to more than frustrating numbers of scrolls, I suggest you to either use `ctrl/cmd + f` key combination and find the word you're looking for or use the `PgDn` key to manually scroll but with a relatively better levels of frustration.-->

## Library : Standard

#TODO: Write a brief description

### Module : Builtins

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

