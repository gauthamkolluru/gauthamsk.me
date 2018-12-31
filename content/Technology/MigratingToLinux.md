---
title: "Migrating to the Linux World from Windows"
categories: ["Linux","Python"]
date: 2019-01-01T00:21:00+05:30
publishdate: 2019-01-01T02:17:36+05:30
# draft: true
---

Ever since I have bought my first desktop computer (an assembled one) back in 2005, just like most others even I got *Microsoft's* **Windows** operating system installed in it and the version was **XP**. Be it any OS that I have used till date, I have hardly felt the operating system to be really convenient to use as I haven't explored much on how to gain convenience and was just using the system through the GUI provided. Despite hailing from a Computer Science and Engineering background, I have recently decided not to use mouse/touchpad and to try doing most of my activities such as creating/renaming/moving/deleting files and folders, switching between applications or between tabs in the same application, executing my scripts, installing/opening a program and so on through the command prompt itself. Soon, I have started playing with my system path and creating aliases for the programs (ex: for py2 for Python2 and py for Python3) and even creating my own key combinations using [Auto Hot Key](https://www.autohotkey.com/). I have started liking the Windows 10 Operating System lately for its stability upto some extent but because my increased comfort of using it to the most. 

Irrespective of my comfort and it's stability, I always wanted to have my pc respond quickly for whatever task I give it and to achieve the same, I have disabled some of the services like the *Windows Search, Print Spooler, Indexing, etc...*. Despite all the measures taken, my pc used consume hours together to open Pycharm or SSMS and started freezing when I installed Eclipse IDE in it. 

For this frustrating reason, my plans of experiencing the **Linux** Operating System have come forward and on 25th December 2018, I have completely wiped my pc (with licensed Windows 10) clean and installed linux ([Click Here to know what happened when I tried sideloading linux on Windows 10](https://gauthamsk.me/technology/underconst/)) the latest 19.1 *Tessa* version of **Linuxmint Cinnamon** edition. Let's leave why Linuxmint Cinnamon and not something else for another article, as I want to share some tips for the prospective Linux migrants from other platforms for setting up their environments for Python Development.

For installing Linuxmint, all that one has to do is to download the .iso (image file) into your pc and burn it to an empty dvd or make a bootable flashdrive.

* Link to download the latest version of Linuxmint: https://www.linuxmint.com/download.php
* Click on <u>32-bit</u> to download 32 bit version of the OS or <u>64-bit</u> to download the 64 bit version of the edition (Cinnamon/Mate/Xfce) you want to  install. I have downloaded and installed the 64-bit version of Cinnamon, I shall be proceeding with the instructions for the same.
* [Learn how to create a bootable media](https://linuxmint-installation-guide.readthedocs.io/en/latest/burn.html)
* Soon after creating your bootable media, insert your media into your pc and restart your pc into 'One-time boot menu'. [This can be done in multiple ways](https://rivernetcomputers.com/5-ways-windows-10-boot-options-menu/)
* Follow the instructions on the screen and you'll be good to go with a fresh new installation of Linuxmint Cinnamon.

Basic and useful information:

* All your application that you install using *Software Manager* will fall into '/usr/bin' or '/usr/local/bin' folders
* To check the folders that are currently present in your system path, type ```echo $PATH```
* A better way to have more control and manage your application is to create a folder in your HOME folder and installing your applications there. This way, the folder gets automatically added to your $PATH enabling you to open your application from the CLI and even remove them easily when  required

Now, for a Python developer, he will be content only after successfully setting-up his python development environment which could be a bit of a complex task if you are one like me as I wouldn't want to install multiple instances of any program in a machine. But, we have to compromise here a bit with linux. Though almost every version of linux comes with python2.7 and python3.6 built-in, It is ***highly recommended to not to use those instances for your development environment as that might cause discrepencies with Operating System itself*** as the linux operating system uses those instances for its own scripts and therefore it is ***always recommended to install a separate version of python***

I have downloaded the latest version of Anaconda3 and have used the instance of python that has come with anaconda as my project interpreter for my python projects and am therefore being able to use the package installer and install all my packages such as pyodbc, scrapy, etc.. without any hassles.

I wish you'll a very happy transition to Linux. 

P.S.: This is my first tech article in my blog being published on 1st Jan 2019. Please give comments or suggestions on it as I'm looking forward to improve.

## Wish you all a Very Happy 2019!