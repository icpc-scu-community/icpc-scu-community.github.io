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

This was the **easiest** problem of the contest. You are asked to round the division result to be even.

**Note**:

- `ceil` will always rounds the results to the upper bound `ceil(2.3) = 3`.
- `floor` will always rounds the results to the lower bound `floor(3.9) = 3`.
- `round` will rounds the results towards the nearest integer `round(2.6) = 3`, `round(3.2) = 3`.

We don't need to use any of them, We can simply calculate the integer division and check whether it is odd or not, if it is odd then add one to the result, otherwise print the result.

{% gist 60f8207d63e17d5dd51614ecbabf4d33 amr-and-even-integers.cpp %}

---

You can [view](https://gist.github.com/amrsalama/60f8207d63e17d5dd51614ecbabf4d33) or [download](https://gist.github.com/amrsalama/60f8207d63e17d5dd51614ecbabf4d33/archive/master.zip) all the solutions.
