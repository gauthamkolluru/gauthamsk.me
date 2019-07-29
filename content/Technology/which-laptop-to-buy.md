---
title: "Which Laptop to buy next?"
categories: ["Linux","Python"]
date: 2019-07-29T06:41:00+05:30
publishdate: 2019-07-29T10:51:36+05:30
# draft: true
---

## My Laptop already got slow, which one should I buy next?

As one of my most recent guru says, "Computers are good at repetitions". Humans might require all the time in the world to add a billion integers together and give the sum and that's where computers came into picture, originally. But, those repetitions themselves paved way for the implementation of the concepts like Servers, Automation and AI (the most recent repetition utilization technology).

But, to be able to implement those technologies I need a computer that has the capacity / configuration of a server if not a super computer, because, my computer has already got about half a decade old and runs at the speed of a computer of the previous century. I think I have to buy a new one, though (assuming) I have a budget for a MacBook Pro, I'm not sure of how long would that support me? Cuz, me experiencing the sluggishness of my laptop started with my 2012 edition MacBook Pro itself. I started experiencing the lags in system bootups and application startups since 2017 itself. I genuinely thought, it served me well for 5 years, maybe its time for it's retirement. I had a relatively new Dell laptop with OS upgraded to Windows 10 (when Microsoft rolled out free upgrade for all users of Windows 7 or newer). I felt it to be comparatively faster to my relatively older MacBook Pro, but still I wasn't happy with the boot-up times or the application startup times but I thought I had no choice, at least then, until, I buy a beast of a machine.

It was around then that I met my new manager and his age old laptop (could be from the 18th century... a couple of years more and it could find a place for itself in the nearest museum) at work and I wondered and asked him "how are you still managing with your laptop, how old is it? what are the boot up times with Windows 10 on it? what is it's configuration?". Trust me, the answers to all those questions were utterly depressing but looking at my pityful expression for him, he said this finally, "I manage my windows services on it!". Now, that hit my mind hard and got stuck in it, even to date.

### What I did to improve the performance of my computer with Windows 10

I opened the "Task Manager" (Ctrl + Shift + Esc) and learnt to my shock that my CPU utilization is not going beyond 30%. It is only Ram and Disk that are maxing out. Ram generally at 86% of utilization but Disk (HDD) is stuck at 100%. This simply meant that, the Ram and Disk are becomming the bottlenecks for my CPU's performance. Then searched for tips and tricks to improve the performance of my machine and implemented the following:

1. Disabled as many applications as I could from the Startup ("Startup" tab in the "Task Manager"). This helped me reduce my bootup time. 

2. Disabled the following services from the services window (windows + 'r' -> type "services.msc" -> click 'ok') and restarted machine:
    - Superfetch
    - Windows Search
    - Fax
    - Print Spooler

And my computer got ready with an improved bootup time and application start time as my Disk utilization has then got down and the efficiency of my machine increased.

Later in the year, I met my friend (whose's name was mentioned in the bottom of my [homepage](http://gauthamsk.me)) and learnt about Linux. Then I did my small research on Linux operating systems and the various distros available and finally zeroed on to [Linuxmint](https://linuxmint.com/) which my friend suggested.

All this was in 2017 and I'm still using the same Dell laptop, in the 2nd half of 2019. It now has a bootup time of about 25 seconds and shutdown time of 7 seconds. Which means, If I have a task that takes about half a minute, I could turn my laptop on, get the task done and shut it down in under a minute, literally. Lately, I realised that I did the right thing with my computer once again when I tried to setup a rasa project in my laptop and work on it as doing the same in my work computer, feels like a nightmare though it is a relatively newer machine.

I think, most of the time, we are undermining the capabilities of the hardware we have at hand but not learning the Operating System that we have at hand. Doing the latter doesn't let the prior happen. I'm still learning Linux and yet very happy with the performance of my machine. 

However, I want to buy a new laptop even as of now as I want to have a lighter machine, one that I makes me feel like carrying it to everywhere and all the time and does not make my mind pop-up the question, "Will I be really using it there?" that in-turn pops-up the question "I should really buy a Laptop but **Which one to buy?**" and that is where all this started, ain't it?
