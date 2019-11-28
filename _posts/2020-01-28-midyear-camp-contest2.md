---
title: Midyear Online Camp - Contest 02
tags: [Editorial]
style: fill
color: dark
description: Editorial of the second contest, Midyear Online Camp.
---

Contest link: [https://codeforces.com/contests/267343](https://codeforces.com/contests/267343)

{%- capture list_items -%}
A. Whatever
B. Koko's Hair
C. khaled cheating
D. Count my colors
E. Who gets it first
F. Kerollos and OS
{%- endcapture -%}

{% include elements/list.html title="Solutions" type="toc" %}

## A. Whatever

> Credits: Kerollos Magdy

As always this was the **easiest** problem of the contest.  
You are asked to concatenate two characters.

{%- gist 5ffa716a772c568a9be1589dd947486e %}

## B. Koko's Hair

> Credits: Khaled Rezk


```cpp
#include <iostream>

int score (int n){
    int number_of_operations = 0;

    while(n != 1){
        if(n % 2 == 0) {
            n /= 2;
        }else {
            n = 3 * n + 1;
        }
        number_of_operations++;
    }

    return number_of_operations;

}

int main () {
    int r, k;
    scanf("%d %d", &r, &k);

    if(score(r) >= score(k))
        printf("Rokaia wins!\n");
    else 
        printf("Koko wins!\n");

}
```

## C. khaled cheating

> Credits: Khaled Rezk

## D. Count my colors

> Credits: Kerollos Magdy

## E. Who gets it first

> Credits: Kerollos Magdy

## F. Kerollos and OS

> Credits: Kerollos Magdy
