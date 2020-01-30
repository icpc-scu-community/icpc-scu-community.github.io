---
title: Midyear Online Camp - Contest 02
tags: [Editorial]
style: fill
color: dark
description: Editorial of the second contest, Midyear Online Camp.
---

Contest link: [https://codeforces.com/contests/267343](https://codeforces.com/contests/267343)

{% capture list_items %}
A. Whatever
B. Koko's Hair
C. khaled cheating
D. Count my colors
E. Who gets it first
F. Kerollos and OS
{% endcapture %}
{% include elements/list.html title="Solutions" type="toc" %}

## A. Whatever

> Credits: Kerollos Magdy

As always this was the **easiest** problem of the contest.  
You are asked to concatenate two characters.

{% gist 5ffa716a772c568a9be1589dd947486e whatever.cc %}

## B. Koko's Hair

> Credits: Khaled Rezk

In this problem the only hard part is to calculate the score of each one of the players however the implementation is very straight forward as problem definition. A Good practice is to solve the problem by writing a function. A function `score` that takes parameter a single integer the choice of each player and returns his score instead of copying and pasting same block of code to calculate the score for each of them.

{% gist 5ffa716a772c568a9be1589dd947486e koko-hair.cc %}

## C. khaled cheating

> Credits: Khaled Rezk

In this problem the tricky part is to understand the the mapping from form1 answers to form2 answers and after that the problem is a piece of cake!
Let's take the first Example “If form1 has 3 questions 1,2,3 and their answers are A, B, D. and form2 has the questions of form1 but in order 2,3,1 then answers of form2 should be B, D, A!”
that means answer of question 1 is A, answer of question 2 is B, answer of question 3 is D and so on
answer of question `i` is the `ci` character.
In from 2 order first question is question2 which answer was B, second question is 3 which answer is D, and the third question is 1 which answer is A so form 2 answers should be B,D,A respectively.
Understandings the mapping makes the problem trivially implemented as follows,
first we save array A which is the order of questions in form2
then read second array answers of form1 from index 1 to n as answer[i] is the answer of i-th question
finally we simply print answers of form2 using their order.

{% gist 5ffa716a772c568a9be1589dd947486e khaled-cheating.cc %}

## D. Count my colors

> Credits: Kerollos Magdy

The problem was very simple it needs you to calculate `m` to the power of `n`.  
The tricky part was to figure out how to use `mod` properly.  
You must take `mod` every time you do multiply.  
You must use `long long` datatype.  
You can watch Mostafa Saad's video [Number Theory - Modular Arithmetic](https://www.youtube.com/watch?v=9sqvjnvuLtY&list=PLPt2dINI2MIY7l5zyFd1W28rei3b-AXaJ&index=2).

{% gist 5ffa716a772c568a9be1589dd947486e count-my-colors.cc %}

## E. Who gets it first

> Credits: Kerollos Magdy

Since a queue is FIFO (First in first out), students who came first should receive their paper first. In the input statement you are given the name of the studnets from the last one to the first, so all you have to do is to print them in the reversed order.

{% gist 5ffa716a772c568a9be1589dd947486e who-gets-it-first.cc %}

## F. Kerollos and OS

> Credits: Kerollos Magdy

You are given a number of processes N. You have to determine which process has the maximum response time. All you have to do is to calculate the response time for each process and print the maximum value you get.

{% gist 5ffa716a772c568a9be1589dd947486e kerollos-and-os.cc %}

---

You can find all the solutions [here](https://gist.github.com/kerolloz/5ffa716a772c568a9be1589dd947486e)