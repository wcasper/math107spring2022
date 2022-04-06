---
layout: page
title: Practice Exam 2 Problem 1 Solution
permalink: /exams/practice-exam2/problem1-soln
---

## Problem 1

Create a function called *mightyMAT(m,n)* which takes in integers $$m$$ and $$n$$ and returns an $$m\times n$$ matrix $$A$$ whose $$(j,k)$$ entry is

$$A(j,k) = j^k$$

for all integers $$1\leq j\leq m$$ and $$1\leq k\leq n$$.
This is an example of a **Vandermonde matrix**.

## Solution

```Matlab
function A = mightyMAT(m,n)
%USEAGE: A = mightyMAT(m,n)
%INPUTS: m, n -- dimensions of output matrix
%OUTPUT: A    -- a particular Vandermonde matrix
%DETAILED DESCRIPTION: this function returns a particular matrix A whose (j,k) entry is j^k

A = zeros(m,n);

for j = 1:m
  for k = 1:n
    A(j,k) = j^k;
  end
end


end
```

