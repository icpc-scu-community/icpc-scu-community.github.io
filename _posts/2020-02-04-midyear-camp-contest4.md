---
title: Midyear Online Camp - Contest 04
tags: [Editorial]
style: fill
color: primary
description: Editorial of the fourth contest, Midyear Online Camp.
---

Contest link: [https://codeforces.com/contests/268094](https://codeforces.com/contests/268094)

{% capture list_items %}
A. Hardest Problem
B. Count Digits
C. Cashier
D. Sum Them All
E. Sort my marks
{% endcapture %}
{% include elements/list.html title="Solutions" type="toc" %}

<script
>
MathJax = {
  tex: {
    inlineMath: [['$', '$'], ['\\(', '\\)']]
  }
};
</script>

<script id="MathJax-script" async
src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-svg.js">
</script>

## A. Hardest Problem

> Credits: Khaled Rezk

Think for a minute, would the number of elements in an array change after sorting it?

So actually the answer is trivial, take the first integer (the number of elements in the array) and print it!

{% gist 737e466a8e3e7709b19169aa52f7c919 hardest-problem.c %}

## B. Count Digits

> Credits: Khaled Rezk

## C. Cashier

> Credits: Khaled Rezk

## D. Sum Them All

> Idea by Khaled Rezk, written by Kerollos Magdy

This part "Khaled told Koko about the problem after an exam" is true by the way.

"$(0 \leq S \leq 10^{100})$ the first integer". $10^{100}$ WHAT! Is there even a data type that can handle this huge integer. Yup, a string, why not? And we can easily convert the second integer to a string and compare them!

{% gist 737e466a8e3e7709b19169aa52f7c919 sum-them-all.cpp %}

## E. Sort my marks

> Credits: Kerollos Magdy

You are asked to calculate the $percent = score/total$ for every subject and sort the subjects according to the results of the percent, highest percent first.

{% gist 737e466a8e3e7709b19169aa52f7c919 sort-my-marks.cpp %}

Same solution written in a different way.

{% gist 737e466a8e3e7709b19169aa52f7c919 sort-my-marks-v2.cpp %}

---

You can [view](https://gist.github.com/kerolloz/737e466a8e3e7709b19169aa52f7c919) or [download](https://gist.github.com/kerolloz/737e466a8e3e7709b19169aa52f7c919/archive/master.zip) all the solutions.
