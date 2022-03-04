---
layout: page
title: Homework 4 Part 3
permalink: /homework/hw4/hw4-part3
---

## More (random) function practice

**Problem 3:**

Samantha is playing Dungeons and Dragons with his friends one day, but she forgot her **D20** (a $$20$$-sided die with values between $$1$$ and $$20$$).  Luckily, she can use the following command in MATLAB to generate a random integer between $$1$$ and $$20$$.

```Matlab
randi(20,1,1)
```

Using this, write a function called rollD20 whose input is an integer *ac* (representing the armor class of a monster).  Inside the function, it creates a variable *roll* whose value is a random integer between $$1$$ and $$20$$.  Finally, it returns text according to the following rules
* "Critical Hit!" if *roll* is equal to $$20$$
* "Hit!" if *roll* is less than 20 but $$\geq$$ *ac*
* "Miss!" if *roll* is less than *ac* but greater than $$1$$
* "Critical Failure!" if *roll* is less than *ac* and equal to $$1$$

Be sure to include good documentation in the file, including
* USEAGE:
* INPUTS:
* OUTPUT:
* DETAILED DESCRIPTION:


