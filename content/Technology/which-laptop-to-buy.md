---
title: "Which Laptop to buy next?"
categories: ["Linux","Python"]
date: 2019-07-29T06:41:00+05:30
publishdate: 2019-07-29T10:51:36+05:30
# draft: true
---

## My Laptop already got slow, which one should I buy next?

A while ago, my friend while talking to one of his students' asked "What happens if a carpenter does not have the proper tools or tools that are not in proper condition?", rhetorically. I'm not sure whether the student asked about something or said something prior but that actually doesn't matter, because, both the analogy and that question of my friend seemed more important.

- How can one claim that a tool is proper or not in case that tool is a "Computer"?

- How is "proper" defined in this context?

Well, I've been pursuing the quest of finding the "proper" machine for my work since then. I was not fully satisfied with my computer then and I don't think I'm even now but for different reasons. 

So, here is what I've learnt by far:

1. I was having a Dell Latitude Laptop with the configuration :
    | Item | Description |
    | --- | --- |
    | Processor | Intel Core i5 - 4210 |
    | RAM | 4GB DDR3 SD |
    | OS | Windows 10 (Activated) |

    which was about an year old for then. 

<!-- As one of my most recent guru says, "Computers are good at repetitions". For example, Humans might require all the time in the world to add a billion integers together and give the sum and that's where computers came into picture, originally. But, those repetitions themselves paved way for the implementation of the concepts like Servers, Automation and AI (the most recent repetition utilization technology).

But, to be able to implement those technologies I need a computer that has the capacity / configuration of a latest server if not a super computer, as it has already got about half a decade old and runs at the speed of a computer from the previous century. I think I have to buy a new one. (assuming) I have a budget for a MacBook Pro, I'm not sure of how long would that support me? Cuz, me experiencing the sluggishness of my laptop started with my 2012 edition MacBook Pro itself. I started experiencing the lags in system bootups and application startups from 2017. I genuinely thought, it served me well for 5 years, maybe its time for it's retirement. Then, I had a relatively new Dell laptop with 4th generation Intel Core i5 processor and OS upgraded to Windows 10 (when Microsoft rolled out free upgrade for all users of Windows 7 or newer). I felt it to be comparatively faster to my relatively older MacBook Pro, but still I wasn't happy with the boot-up times or the application startup times but I thought I had no choice, at least for then, until, I buy a beast of a machine.

It was around then that I met my new manager and his age old laptop (could be from the 18th century... a couple of years more and it could find a place for itself in the nearest museum) at work and I wondered and asked him "how are you still managing with your laptop, how old is it? what are the boot up times with Windows 10 on it? what is it's configuration?". Trust me, the answers to all those questions were utterly depressing but looking at my pityful expression for him, he said this finally, "I manage my windows services on it!". Now, that hit my mind hard and got stuck in it, even to date.

I did a bit of research implemented a couple of suggesstions that I found online and the machine picked up with a significant improvement in the bootup and application start times and my Disk too is no more engaged at 100% utilization even when no application was running (other than the ones that the OS runs).

Later in the year, I met my friend (whose's name was mentioned in the bottom of my [homepage](http://gauthamsk.me)) and learnt about Linux. He was using a laptop which was older to mine then and to my shock it had some exciting bootup and application startup times. Then I did my tiny research on Linux operating systems and the various distros available and finally zeroed on to [Linuxmint](https://linuxmint.com/) which my friend suggested.

All this was in 2017 and I'm still using the same Dell laptop, in the 2nd half of 2019. It now has a bootup time of about 25 seconds and shutdown time of 7 seconds. Which means, If I have a task that takes about half a minute, I could turn my laptop on, get the task done and shut it down in under a minute, literally. Lately, I realised that I did the right thing with my computer once again when I tried to setup a rasa project in my laptop and work on it as doing the same in my work computer feels like a nightmare though it is a relatively newer machine. -->

### What I did to improve the performance of my computer with Windows 10

I opened the "Task Manager" (Ctrl + Shift + Esc) and learnt to my shock that my CPU utilization is not going beyond 30%. It is only Ram and Disk that are maxing out. Ram generally at 86% of utilization but Disk (HDD) is stuck at 100%. This simply meant that, the Ram and Disk are becomming the bottlenecks for my CPU's performance. Then searched for tips and tricks to improve the performance of my machine and implemented the following:

1. Disabled as many applications as I could from the Startup ("Startup" tab in the "Task Manager"). This helped me reduce my bootup time. 

2. Disabled the following services from the services window (windows + 'r' -> type "services.msc" -> click 'ok') and restarted machine:
    - Superfetch
    - Windows Search
    - Fax
    - Print Spooler
    - Windows Tips and Tricks

3. Some articles (online) also suggested to disable "Shadows and Visual effects" but I wasn't interested in it and let it be.

4. (Uninstall if you have any anti-virus installed in your computer) Since I studied about the Windows Defender and found it to be pretty effective I haven't installed any 3rd party anti-virus solution on my pc.

5. Uninstalled Bloatware - All applications that I deemed unnecessary. (Please be careful to not to uninstall any OS required application. Learn about the applications thoroughly online using articles or forums)

6. Disk Cleanup - which cleaned about 8gb of unnecessary files.

### What I did to improve the performance of my computer with Linux

- I Installed It!

I ain't exggerating but I actually done nothing else apart from installing Linuxmint in my computer. Now, it boots up and opens appliccations at a better pace.

### Coming back to the D-Question



However, I want to buy a new laptop even as of now as I want to have a lighter machine, one that makes me feel like carrying it to everywhere I go and all the time and does not make my mind pop-up the question, "Will I be really using it there?" and I have other plans for my existing laptop which we'll keep for another article.
