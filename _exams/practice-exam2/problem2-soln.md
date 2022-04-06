---
layout: page
title: Practice Exam 2 Problem 2 Solution
permalink: /exams/practice-exam2/problem2-soln
---

## Problem 2

If $$a$$ and $$q$$ are numbers and $$n>0$$ is any integer, then the $$q$$-**pochhammer symbol** is the product

$$(a;q)_n = (1-aq)(1-aq^2)(1-aq^3)\dots(1-aq^{n-1}).$$

Create a function called *qpoch(a,q,n)* which takes in the values $$a$$, $$q$$, and $$n$$, and returns the value of the $$q$$-pochhamer symbol $$(a;q)_n$$, which you calculate by using a single *for loop*.


## Problem 2 Solution

```Matlab
function symbol = qpoch(a,q,n)
%USEAGE: symbol = qpoch(a,q,n)
%INPUTS: a, q, n -- input parameters with n an integer
%OUTPUT: symbol -- q-pochhammer symbol (a;q)_n
%DETAILED DESCRIPTION: This function calulates the q-Pochhammer symbol (a;q)_n for specified values of a, q, and n

symbol = 1;
for k=1:n-1
  symbol = symbol*(1-a*q^k);
end

end


````
