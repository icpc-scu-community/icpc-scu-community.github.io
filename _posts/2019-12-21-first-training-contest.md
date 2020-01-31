---
title: Training Contest 01
tags: [Editorial]
style: fill
color: light
description: Editorial of the first training contest.
---

Hello, everybody. I hope that you had fun with the contest. :smiley:

I wrote the following problems:

- [A - In search of a HARD problem](https://codeforces.com/gym/263691/problem/A)
- [D - Arya and Sansa](https://codeforces.com/gym/263691/problem/D)
- [E - Arya Stark](https://codeforces.com/gym/263691/problem/E)

Your feedback is welcomed :heart:!  
[kerolloz@yahoo.com](mailto:kerolloz@yahoo.com?subject=Contest feedback)

{% capture list_items %}
A. In search of a HARD problem
B. In Search of an Easy Problem
C. Hulk
D. Arya and Sansa
E. Arya Stark
{% endcapture %}
{% include elements/list.html title="Solutions" type="toc" %}

## A. In search of a HARD problem

This was the **easiest** problem of the contest. I think everyone found the problem easy -- except Amr, Khaled, and Koko :joy:.

The main idea is to print the sum of the first two numbers.

```cpp
#include <stdio.h>

int main (){
  int x, y; // no need to take z
  scanf("%d%d", &x, &y);
  printf("%d\n", x+y);
  return 0;
}
```

That is it :smiley:! Just three lines of code.

## B. In Search of an Easy Problem

I was told that you have already solved this problem. but I didn't change it anyway.

The main idea is to take `n` integers and print `HARD` if any one of them is equal to `1`, otherwise print `EASY`.

```cpp
#include <stdio.h>

int main() {
  int n;
  scanf("%d", &n);

  for(int i = 0; i < n; i++) {
    int x;
    scanf("%d", &x);
    if(x == 1) {
      printf("HARD\n");
      return 0; // no need to continue! we found the hard problem
    }
  }
  printf("EASY\n");
  return 0;
}
```

## C. Hulk

```cpp
#include <stdio.h>

int main() {
  int n;
  scanf("%d", &n);

  for (int i = 0; i < n; i++){
    printf("I ");
    if(i % 2 == 0) // we start with 0 (even)
      printf("hate");
    else // odd
      printf("love");
    if(i < n-1) printf(" that ");
    // we should print "that" every time except the last time
  }
  printf(" it\n"); // finally print "it" for the last time
  return 0;
}
```

A shorter solution

```cpp
#include <stdio.h>

int main() {
  int n;
  scanf("%d", &n);

  for (int i = 0; i < n; i++){
    printf("I %s ", (i % 2 == 0)? "hate": "love");
    // ternary operator syntax => (condition)? if_true : if_false;
    if(i < n-1) printf("that ");
  }
  printf("it\n");
  return 0;
}
```

## D. Arya and Sansa

I am a big fan of GOT :heart:.  
I am in love with Arya Stark :heart_eyes:!  
So, why not 2 problems for Arya :relieved:!

The main idea of the problem is that you should print `yes` if Arya and Sansa pass by the same point at any time in their way home.

As in the second test case:

```text
Arya steps = 6    => [0,6,12,18,24,30,36,40]
Sansa steps = 10  => [0,10,20,30,40]
Winterfell position = 40
```

Arya and Sansa meet at point 30. Notice that 30 is divisible by 6(Arya steps), and 10(Sansa steps). That means if there is a number between 0 and Winterfell position that is divisible by Arya steps and Sansa steps, then Arya and Sansa will meet at this position.

```cpp
#include <stdio.h>

int main (){
  int arya_steps, sansa_steps, x;
  bool will_meet = false;
  scanf("%d%d%d", &arya_steps, &sansa_steps, &x);
  int i;
  for (i = 1 ; i < x ; i++){
    if (i % arya_steps == 0 && i % sansa_steps == 0){
      will_meet = true;
      break; // no need to continue
    }
  }
  if (will_meet){
    printf("YES");
  }else {
    printf("NO");
  }
  return 0;
}
```

Can we do better?
YES, let's think of the problem in a different way.  
Where is the first time that Arya and Sansa will meet in their way, given Arya steps and Sansa steps? In other words, what is the first number that is divisible by both steps? The answer is the Least Common Multiple (LCM). So if LCM(arya_steps, sansa_steps) is less than the position of Winterfell, the answer is `yes`.

How can we compute LCM **efficiently**?  
_The implementation is left for you as a practice_ :smiley:

## E. Arya Stark

The main idea is to count the number of vowel letters in the given input.
If the count is prime, print `valar morghulis`. Otherwise, print `valar dohaeris`.

Solution by **Amr Salama** :heart:

```cpp
#include <ctype.h>
#include <stdio.h>
#include <string.h>

int main() {
  char str[1001]; // maximum size of the string is 1000 characters
  fgets(str, sizeof(str),
        stdin); // take input untill end of line (takes spaces too)

  int i, vowels_count = 0;
  int input_length = strlen(str);
  for (i = 0; i < input_length; i++) {
    char c = tolower(str[i]);
    if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u') {
      vowels_count++;
    }
  }

  bool is_prime = vowels_count >= 2;
  // a TRICKY case that most of you didn't consider
  // numbers less than 2 are not primes
  for (i = 2; i < vowels_count; i++) {
    if (vowels_count % i == 0) {
      is_prime = 0;
      break; // no need to continue
    }
  }

  if (is_prime) {
    printf("valar morghulis\n");
  } else {
    printf("valar dohaeris\n");
  }

  return 0;
}
```

---

Feel free to ask :smile:

*[GOT]: Game of Thrones
