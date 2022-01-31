---
layout: post
---

Notes and highlights from lecture

## Today's Objectives

* MATLAB grader
* linear combinations
* convex combinations
* built-in MATLAB functions

## Reading assignments

* <a target="_parent" href="../../../extras/textbook.pdf">primary text (link)</a>: chapter 3 section 1 + 2
* When Life is Linear: chapter 3

## MATLAB grader
For some of our homework, we will submit solutions through MATLAB grader, which
is already integrated into Canvas.  You will enter your MATLAB code into the
**Script Window** on Canvas.  You can check your code by pressing the **Run Script**
button, which will run the code and display any output.  This also gives you a
chance to see if there are any errors in your code which make MATLAB unhappy.

When you are ready to hand over your code for grading, you should hit
**Submit** button to submit the assignment.  You have exactly three chances to
submit the assignment, so if things don't go perfectly the first time, you can
attempt to correct some mistakes.

Important notes:

* Make sure to complete the entire assignment before submitting!! All of your answers are checked during submission and missing answers are counted as incorrect.  Don't waste a submission!
* If your submission has a mistake, be sure to read the error feedback in order to get a better idea of what might have gone wrong!
* You must submit at least once in order for your homework to be graded.  Be sure to hit **Submit** at least once before the homework deadline.

## Linear combinations

Remember that the principal algebraic operations in linear algebra are

* vector/matrix addition
* scalar multiplication

When we combine these two operations together we get linear combinations.

**Definition:** A **linear combination** of two vectors $$u$$ and $$v$$ is a vector of the form

$$au + bv$$

for some scalars $$a$$ and $$b$$.

Likewise, a **linear combination** of two matrices $$A$$ and $$B$$ is a matrix of the form

$$aA + bB.$$

A linear combination of this form is called a **convex combination** when
$$0\leq a,b\leq 1$$ and $$a + b=1$$.  In other words, a convex combination is a
sort of weighted average of the matrices $$A$$ and $$B$$

$$aA + (1-a)A$$

for some $$0\leq a\leq 1$$ whose value determines the relative amounts of $$A$$ or $$B$$ we include.

## MATLAB built-in functions

As we have already seen, MATLAB comes with some pretty sweet pre-built functions, such as size(), zeros(), ones(), imread(), etc.  Here we will list many such functions along with example use cases.

### Basic math functions

MATLAB comes pre-built with the following basic math functions.  We can also input matrices in these functions, with the result being the function is applied to every entry of the matrix.

* **trigonometric functions:** sin(), cos(), tan(), csc(), sec(), cot()

```Matlab
sin(pi/2)    % returns 1
```

* **exponential functions:** exp(), log(), log10(), log2()

```Matlab
log(exp(3)) % returns 3
log10(100)  % returns 2
log2(8)     % returns 3
```

* **root functions:** sqrt(), nthroot()

```Matlab
sqrt(9)      % returns 3
nthroot(8,3) % returns 2 (cube root of 8)
```
### Statistics

MATLAB also has various built-in functions for statistics.  We'll cover the basics.


* **average values** mean(), median(), mode()

```Matlab 
mean([1,1,1,2,2,3,4])   % returns 2
median([1,1,1,2,2,3])   % returns 2
mode([1,1,1,2,2,3])     % returns 1
```
We can also put in a matrix into these functions.  The result is a row vector whose entries are the various column averages

```Matlab
A = [1 2; 3 4];
mean(A)           % returns [2 3]
```

* **standard deviation** std()

```Matlab
std([1,1,1,2,2,3])  % returns the standard deviation of the entries: 1.1547
```

### Sorting

* **ordering entries** % sort()

```Matlab
sort([3,1,9,2])   % returns [1,2,3,9]
```

* **ordering rows** sortrows()

```Matlab
A = [1 2; 5 6; 3 4]
sortrows(A)           % returns [1 2; 3 4; 5 6]
```

* **flipping** flipud(), fliplr()

```Matlab
A = [1 2; 3 4]
flipud(A)        % returns [3 4; 1 2] (flipped up-to-down)
fliplr(A)        % returns [2 1; 4 3] (flipped left-to-right)
```

### Locating

MATLAB also has a function to find the locations of values in a matrix

* **finding values** find()

```Matlab
find(A==1)   % returns index or indices where the entries of A are equal to 1
find(A>=2)   % returns index or indices where the entries of A are 2 or greater
```

* ****

## Additional resources

**Lecture code:** <a target="_parent" href="https://wcasper.github.io/math107spring2021/MATLAB/lecture4.m">mfile for lecture (link)</a>

**Lecture notes:** <a target="_parent" href="https://wcasper.github.io/math107spring2021/extras/notes/2021-02-03-Note-11-11.pdf">notes for lecture (link)</a>

**Lecture video:** <a target="_parent" href="https://fullerton.zoom.us/rec/share/L_AB9vN9xAJQ0jst8EpXClJYabiyTo3jcSNa5TPIZb43iZTBqWFVXP7cTze6R1qs.ZFjqxW__ZQU8-nmW">recording of lecture (link)</a>

The passcode can be found on the <a target="_parent" href="https://csufullerton.instructure.com/courses/3127326/pages/video-lecture-keys">passcode page (link)</a>

**images for lecture:**
* <a target="_parent" href="https://wcasper.github.io/math107spring2021/extras/img/mittens.jpg">mittens.jpg</a>
* <a target="_parent" href="https://wcasper.github.io/math107spring2021/extras/img/space.jpg">mittens.jpg</a>
* <a target="_parent" href="https://wcasper.github.io/math107spring2021/extras/img/ghost.jpg">ghost.jpg</a>
* <a target="_parent" href="https://wcasper.github.io/math107spring2021/extras/img/spooky-woods.jpg">spooky-woods.jpg</a>



