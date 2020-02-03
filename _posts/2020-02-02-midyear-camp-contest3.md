---
title: Midyear Online Camp - Contest 03
tags: [Editorial]
style: fill
color: dark
description: Editorial of the third contest, Midyear Online Camp.
---

Contest link: [https://codeforces.com/contests/267777](https://codeforces.com/contests/267777)

{% capture list_items %}
A. Amr and Even Integers
B. Omar and Bike
C. Ismail's Exams
D. Amr's Revenge
E. Defeating Attack
F. Khaled's Birthday
{% endcapture %}
{% include elements/list.html title="Solutions" type="toc" %}

## A. Amr and Even Integers

> Credits: Amr Salama

This was the **easiest** problem in the contest. You are asked to round the division result to be even.

**Note**:

- `ceil` will always rounds the result to the upper bound `ceil(2.3) = 3`.
- `floor` will always rounds the result to the lower bound `floor(3.9) = 3`.
- `round` will rounds the result towards the nearest integer `round(2.6) = 3`, `round(3.2) = 3`.

We don't need to use any of them, We can simply calculate the integer division and check whether it is odd or not, if it is odd then add one to the result, otherwise print the result.

{% gist 60f8207d63e17d5dd51614ecbabf4d33 amr-and-even-integers.cpp %}

## B. Omar and Bike

> Credits: Ismail Akram

To solve this problem you need to note input constraint (`m <= n`), So there is a possibility that `m` could be equal to `n`, and so Omar may not save any money at all in this case (`n - m = 0`), and you should print `-1` in this case.

Otherwise, the result is the `ceil` of `k / (n-m)`. If you didn't check for `-1` case first, you may have `run time error` due to division by zero.

{% gist 60f8207d63e17d5dd51614ecbabf4d33 omar-and-bike.cpp %}

---

You can [view](https://gist.github.com/amrsalama/60f8207d63e17d5dd51614ecbabf4d33) or [download](https://gist.github.com/amrsalama/60f8207d63e17d5dd51614ecbabf4d33/archive/master.zip) all the solutions.
