---
title: "1. Understanding Recursion"
categories: ["Python", "Recursion", "Functional Programming"]
date: 2019-12-21T16:00:00+05:30
publishdate: 2019-12-21T17:00:40+05:30
draft: false
---

<center>
<i>To Understand <b>Recursion</b>, one must first understand <b>Recursion</b></i>
<p style="text-align:right"><i> &nbsp; - &nbsp; <b>Stephen Hawking</b></i></p>
</center>

Recursion in that type of programming construct that first bewilders those who take their first glance at it, frightens those who tries to approach it but once you step forward fearlessly and compassionately (slowly and steadily with understanding, in this context), you'll get to tame it and that is when you'd realise that it isn't just any other pet that one could have but the strongest and omnipotent (sort of, exaggeration) Dragon that you could have by your side.

So, without any further ado, let's just barge in.

Today, I have come across a video on [Youtube](https://www.youtube.com) by **interviewing.io** called [Python interview with a Google Engineer: Coin Change](https://youtu.be/HWW-jA6YjHk)

While going through the video I felt like I should try solving this problem but using recursion.

Before getting into solving the problem, let's first try and understand the Problem.

## Problem Statement

Suppose, You are at a grocery store and about to buy some groceries worth INR 99.15/-. You give the shopkeeper at the counter a INR 100/- bill and now the shopkeeper must return the exact change back to you and not some *mints* or *chocolates*.

We know that, he has to return .85 paise (100 - 99.15) but (assume) we have only the following denominations of coins available.

* 0.50 paise
* 0.25 paise
* 0.05 paise
* 0.01 paise

We have to calculate the number of coins that we've to return to return the exact change to you.

As in the case above:

The shopkeeper has to return:

* 1 of 0.50 paise coin
* 1 of 0.25 paise coin
* 2 of 0.05 paise coin

=> a total of **3 coins**.

Now, what we have to do is, write a program for the same.

Hoping that you've understood the problem, let's now get into solving it.

### Algorithmic Approach Towards Solution

#### Step 1

We've to write a function that takes in the change that has to be given back to the customer and returns the **number of coins** to return.

```python
def coins_change(amount):
    # Calculation comes here
    return no_of_coins
```

Before calculating the exact number of coins to return, we must somehow store the denominations of the coins available with us. Isn't it?

For this, I felt like having a dictionary with the denominations of the coins as **keys** and the number of coins of that denomination that are available as **values**.(trying to emulate the real-time POS machine's cash drawer)

This data structure can be created within or outside the function as it doesn't matter much for our current scenario and I have just assumed some numbers for coins available for each denomination

```python
def coins_change(amount):
    denominations = {50:5, 25:5, 5:10, 1:20}
    # Calculation comes here
    return no_of_coins
```

Now the key part starts. From the number of coins available of each denomination, I somehow have to start from the highest denomination available and possible.

=> if I have to return 35 paise, then I have to start pulling the coins from 25 paise denomination slot and then from the 5 paise coins slot.

=> If I have to return 9 paise, then I have to pull 1 of the 5 paise coins and 4 of 1 paise coins.

=> We've to read the keys of the dictionary in a descending order format.

```python
def coins_change(amount):
    denominations = {50:5, 25:5, 5:10, 1:20}
    for denomination in sorted(denominations, reverse = True):
    # Calculation comes here
    return no_of_coins
```

Now, at each iteration of the `for` loop, we get each denomination availabe, in a descending order format.

Therefore, we've to first check if that `amount` (the change we've to return) is bigger than the `denomination` at hand.

If `false` , go to the next denomination, else

```python
def coins_change(amount):
    coins_draw = {50:5, 25:5, 5:10, 1:20}
    for denomination in sorted(denominations, reverse = True):
        if amount >= denomination:
    # Calculation comes here
    return no_of_coins
```

and, now, we've to calculate.

As per the scenario above, the shopkeeper has to return 85 paise to you.

The first available denomination is, **50 paise** but we want to know the number of coins of 50 paise to return and this will be given by the **Floor Division** ( `//` ) operator.

```python
>>>85 // 50
1
```

and the remaining change to be given is determined by the **Modulo** ( `%` ) operator.

```python
>>>85 % 50
35
```

and *Here comes __Recursion__*

Recursion is a method where, if in a `function` definition, say, `func()` , if you're also calling the function `func()` , then it is called as recursion.

Don't worry about the definition above but just try to look into the example below and try to fathom.

```python
def coins_change(amount):
    coins_draw = {50:5, 25:5, 5:10, 1:20}
    for denomination in sorted(denominations, reverse = True):
        if amount >= denomination:
            if amount % denomination:
                return (amount // denomination) + change_coins(amount - ((amount // denomination) * denomination))
    # Calculation comes here
    return no_of_coins
```

=> after checking the condition below:

```python
if amount >= denomination:
```

We're checking if enough coins of `denomination` at hand would clear the amount to be returned. For example, 

If the the change to be returned is 50 paise then 1 of the 50 paise coins should be enough to be returned right? So, to check this, we use the **Modulo** `(%)` operator.

```python
if amount % denomination:
```

we are just calculating the number of coins of the current `denomination` that we have at hand, should be returned and the remaining amount for which the no of coins are yet to be calculated are being given back to the `coins_change()` function.

Ex: As with the case that we've been looking into, since we've to get 85 paise back, 

```python
(amount // denomination) # This will determine that 1 of 50 paise coins have to be given and

amount - ((amount // denomination) * denomination)
```

=> which is nothing but, amount  = 85

=> amount // 50 = 85 // 50 = 1

=> ((amount // denomination) * 50) = ((85 // 50) * 50) = 50

=> amount - ((amount // denomination) * denomination) = 85 - 50 = 35 is given back to the `coins_change()` function to calculate the number of coins the remaining 35 paise take.

Now, when `coins_change()` function now gets **35** as the input, 

it would again repeat the process that was done for the initial 85 paise, 

=> if 35 >= 50

`False` 

=> the iterator goes to the `next` value, which is 25.

=> if 35 >= 25

`True` 

=> calculate 35 // 25 and the remaining `amount` for which the number of coins is yet to be determined, which is (35 - (35 // 25) * 25) = (35 - (1) * 25) = 35 - 25 = 10

and now, the value **10** is passed to our function and again it checks

=> if 10 >= 50

`False` 

=> if 10 >= 25

`False` 

=> if 10 >= 5

`True` 

but only this time, `amount % denomination` will be `0` , as `10 % 10` gives no remainde and therefore, the recursion stops as we've included the conditon that says

```python
if amount % denomination: # this condition will return `False` 
    return amount // denomination # and therefore, this statement gets executed
```

which finally results in, 1 (of 50 paise coin) + 1 (of 25 paise coin) + 2 of (of 5 paise coins) which amounts to **4 coins**.

And this is how **Recursion** is implemented.

and here is the complete working code:

```python
def change_coins(amount=None):
    denominations = {50: 5, 25: 5, 5: 10, 1: 20}
    if amount:
        for denomination in sorted(denominations, reverse=True):
            if amount >= denomination:
                if amount % denomination:
                    return (amount // denomination) + change_coins(amount - ((amount // denomination) * denomination))
                else:
                    return amount // denomination
```

Please comment below if you have any doubts or reach me [here](https://gauthamsk.me/contact-me/)