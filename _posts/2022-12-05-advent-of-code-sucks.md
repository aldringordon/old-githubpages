---
layout: post
title: advent of code sucks
date: 2022-12-05 20:48 +0800
categories: [ development, challenges ]
tags: [ challenges, development ]
---

so im participating in the advent of code this year

i think ive tried too every year for the past couple years but always got sidetracked or lost interest

this year i nearly just straight up quit because im an idiot

i tried to be extra and use `regex` which actually fucked me for a long time because i didnt check the expression properly

it was supposed to read the instructions numbers from a sentence like `move 26 crates from stack 3 to stack 6` which the regex parser would convert:

```python
# regex
'\d'

# string parsed into list
x = [26, 3, 6]

# deserializing
move = x[0]
move = x[1]
move = x[2]

# which becomes
move = 26
source = 3
stack = 6
```

unfortunately what was happening becomes im a complete ~~idiot~~ was:

```python
#regex
'\d+'

# string parsed into list
x = [2, 6, 3, 6]

# deserializing
move = x[0]
move = x[1]
move = x[2]

# which becomes
move = 2
source = 6
stack = 3
```

not happy ay, but it was fine i figured it out and works great

**thank god i learned to use the debugger**

![](/assets/2022-12-05/debugger.png)