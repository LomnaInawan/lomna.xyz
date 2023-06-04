---
title: "Example"
date: 2023-04-02T19:49:21+05:30
math: true
---

# Table of Contents

1.  [Lecture 1](#orgb5a8a12)
    1.  [Data structure and Algorithm](#orgebf4933)
    2.  [Characteristics of Algorithms](#orgec3c7fe)
    3.  [Behaviour of algorithm](#org803517e)
        1.  [Best, Worst and Average Cases](#orga3ee61c)
        2.  [Bounds of algorithm](#org9ba75ea)
    4.  [Asymptotic Notations](#orgd43e8f9)
        1.  [Big-Oh Notation [O]](#orgac8b10c)
2.  [Lecture 2](#org5b2bd8e)
    1.  [Asymptotic Notations](#orgf87c914)
        1.  [Omega Notation [ $\Omega$ ]](#org2d13865)
        2.  [Theta Notation [ $\theta$ ]](#orgc4213fb)
        3.  [Little-Oh Notation [o]](#orgd025145)
        4.  [Little-Omega Notation [ $\omega$ ]](#org6ed71a6)
    2.  [Comparing Growth rate of funtions](#org6961244)
        1.  [Applying limit](#org4f6cf37)
        2.  [Using logarithm](#org88e11c6)
        3.  [Common funtions](#org04db27d)
    3.  [Properties of Asymptotic Notations](#orgac349b7)
        1.  [Big-Oh](#orge67af69)
        2.  [Properties](#org9935ba4)
3.  [Lecture 3](#orgeff518e)
    1.  [Calculating time complexity of algorithm](#orge4348f0)
        1.  [Sequential instructions](#org574ee71)
        2.  [Iterative instructions](#orga3e4bc8)
        3.  [An example for time complexities of nested loops](#orgded1bf2)
4.  [Lecture 4](#orga8056b4)
    1.  [Time complexity of recursive instructions](#org211bf23)
        1.  [Time complexity in recursive form](#org48df1a1)
    2.  [Solving Recursive time complexities](#orgb64e109)
        1.  [Iterative method](#orgc028b9f)
        2.  [Master Theorem for Subtract recurrences](#orge90168c)
        3.  [Master Theorem for divide and conquer recurrences](#org50eef77)
    3.  [Square root recurrence relations](#orgee52033)
        1.  [Iterative method](#org3adb528)
        2.  [Master Theorem for square root recurrence relations](#orgc40ded0)
5.  [Lecture 5](#org416e5b8)
    1.  [Extended Master's theorem](#orga5e144d)
        1.  [For (k = -1)](#org28a73b1)
        2.  [For (k < -1)](#orgf9e9eea)
    2.  [Tree method](#org485492c)
    3.  [Space complexity](#org4b6765a)
        1.  [Auxiliary space complexity](#org773f2f4)
    4.  [Calculating auxiliary space complexity](#org4872e22)
        1.  [Data Space used](#orgfc4ead7)



<a id="orgb5a8a12"></a>

# Lecture 1


<a id="orgebf4933"></a>

## Data structure and Algorithm

-   A **data structure** is a particular way of storing and organizing data. The purpose is to effectively access and modify data effictively.
-   A procedure to solve a specific problem is called **Algorithm**.

During programming we use data structures and algorithms that work on that data.


<a id="orgec3c7fe"></a>

## Characteristics of Algorithms

An algorithm has follwing characteristics.

-   **Input** : Zero or more quantities are externally supplied to algorithm.
-   **Output** : An algorithm should produce atleast one output.
-   **Finiteness** : The algorithm should terminate after a finite number of steps. It should not run infinitely.
-   **Definiteness** : Algorithm should be clear and unambiguous. All instructions of an algorithm must have a single meaning.
-   **Effectiveness** : Algorithm must be made using very basic and simple operations that a computer can do.
-   **Language Independance** : A algorithm is language independent and can be implemented in any programming language.


<a id="org803517e"></a>

## Behaviour of algorithm

The behaviour of an algorithm is the analysis of the algorithm on basis of **Time** and **Space**.

-   **Time complexity** : Amount of time required to run the algorithm.
-   **Space complexity** : Amount of space (memory) required to execute the algorithm.

The behaviour of algorithm can be used to compare two algorithms which solve the same problem.
  
The preference is traditionally/usually given to better time complexity. But we may need to give preference to better space complexity based on needs.


<a id="orga3ee61c"></a>

### Best, Worst and Average Cases

The input size tells us the size of the input given to algorithm. Based on the size of input, the time/storage usage of the algorithm changes. **Example**, an array with larger input size (more elements) will taken more time to sort.

-   Best Case : The lowest time/storage usage for the given input size.
-   Worst Case : The highest time/storage usage for the given input size.
-   Average Case : The average time/storage usage for the given input size.


<a id="org9ba75ea"></a>

### Bounds of algorithm

Since algorithms are finite, they have **bounded time** taken and **bounded space** taken. Bounded is short for boundries, so they have a minimum and maximum time/space taken. These bounds are upper bound and lower bound.

-   Upper Bound : The maximum amount of space/time taken by the algorithm is the upper bound. It is shown as a function of worst cases of time/storage usage over all the possible input sizes.
-   Lower Bound : The minimum amount of space/time taken by the algorithm is the lower bound. It is shown as a function of best cases of time/storage usage over all the possible input sizes.


<a id="orgd43e8f9"></a>

## Asymptotic Notations


<a id="orgac8b10c"></a>

### Big-Oh Notation [O]

-   The Big Oh notation is used to define the upper bound of an algorithm.
-   Given a non negative funtion f(n) and other non negative funtion g(n), we say that $f(n) = O(g(n)$ if there exists a positive number $n_0$ and a positive constant $c$, such that $$ f(n) \le c.g(n) \ \ \forall n \ge n_0  $$
-   So if growth rate of g(n) is greater than or equal to growth rate of f(n), then $f(n) = O(g(n))$.


<a id="org5b2bd8e"></a>

# Lecture 2


<a id="orgf87c914"></a>

## Asymptotic Notations


<a id="org2d13865"></a>

### Omega Notation [ $\Omega$ ]

-   It is used to shown the lower bound of the algorithm.
-   For any positive integer $n_0$ and a positive constant $c$, we say that, $f(n) = \Omega (g(n))$ if $$ f(n) \ge c.g(n) \ \ \forall n \ge n_0 $$
-   So growth rate of $g(n)$ should be less than or equal to growth rate of $f(n)$

**Note** : If $f(n) = O(g(n))$ then $g(n) = \Omega (f(n))$


<a id="orgc4213fb"></a>

### Theta Notation [ $\theta$ ]

-   If is used to provide the asymptotic **equal bound**.
-   $f(n) = \theta (g(n))$ if there exists a positive integer $n_0$ and a positive constants $c_1$ and $c_2$ such that $$ c_1 . g(n) \le f(n) \le c_2 . g(n) \ \ \forall n \ge n_0 $$
-   So the growth rate of $f(n)$ and $g(n)$ should be equal.

**Note** : So if $f(n) = O(g(n))$ and $f(n) = \Omega (g(n))$, then $f(n) = \theta (g(n))$


<a id="orgd025145"></a>

### Little-Oh Notation [o]

-   The little o notation defines the strict upper bound of an algorithm.
-   We say that $f(n) = o(g(n))$ if there exists positive integer $n_0$ and positive constant $c$ such that, $$ f(n) < c.g(n) \ \ \forall n \ge n_0 $$
-   Notice how condition is <, rather than $\le$ which is used in Big-Oh. So growth rate of $g(n)$ is strictly  greater than that of $f(n)$.


<a id="org6ed71a6"></a>

### Little-Omega Notation [ $\omega$ ]

-   The little omega notation defines the strict lower bound of an algorithm.
-   We say that $f(n) = \omega (g(n))$ if there exists positive integer $n_0$ and positive constant $c$ such that, $$ f(n) > c.g(n) \ \ \forall n \ge n_0 $$
-   Notice how condition is >, rather than $\ge$ which is used in Big-Omega. So growth rate of $g(n)$ is strictly less than that of $f(n)$.


<a id="org6961244"></a>

## Comparing Growth rate of funtions


<a id="org4f6cf37"></a>

### Applying limit

To compare two funtions $f(n)$ and $g(n)$. We can use limit
$$ \lim_{n\to\infty} \frac{f(n)}{g(n)} $$

-   If result is 0 then growth of $g(n)$ > growth of $f(n)$
-   If result is $\infty$ then growth of $g(n)$ < growth of $f(n)$
-   If result is any finite number (constant), then growth of $g(n)$ = growth of $f(n)$

**Note** : L'Hôpital's rule can be used in this limit.


<a id="org88e11c6"></a>

### Using logarithm

Using logarithm can be useful to compare exponential functions. When comaparing functions $f(n)$ and $g(n)$, 

-   If growth of $\log(f(n))$ is greater than growth of $\log(g(n))$, then growth of $f(n)$ is greater than growth of $g(n)$
-   If growth of $\log(f(n))$ is less than growth of $\log(g(n))$, then growth of $f(n)$ is less than growth of $g(n)$
-   When using log for comparing growth, comaparing constants after applying log is also required. For example, if functions are $2^n$ and $3^n$, then their logs are $n.log(2)$ and $n.log(3)$. Since $log(2) < log(3)$, the growth rate of $3^n$ will be higher.
-   On equal growth after applying log, we can't decide which function grows faster.


<a id="org04db27d"></a>

### Common funtions

Commonly, growth rate in increasing order is
$$  c < c.log(log(n)) < c.log(n) < c.n < n.log(n) < c.n^2 < c.n^3 < c.n^4 ...  $$
$$ n^c < c^n < n! < n^n  $$
Where $c$ is any constant.


<a id="orgac349b7"></a>

## Properties of Asymptotic Notations


<a id="orge67af69"></a>

### Big-Oh

-   **Product** :  $$ Given\ f_1 = O(g_1)\ \ and\ f_2 = O(g_2) \implies f_1 f_2 = O(g_1 g_2) $$ $$ Also\  f.O(g) = O(f g) $$

-   **Sum** : For a sum of two functions, the big-oh can be represented with only with funcion having higer growth rate. $$ O(f_1 + f_2 + ... + f_i) = O(max\ growth\ rate(f_1, f_2, .... , f_i )) $$

-   **Constants** : For a constant $c$ $$ O(c.g(n)) = O(g(n)) $$, this is because the constants don't effect the growth rate.


<a id="org9935ba4"></a>

### Properties

![img](lectures/imgs/asymptotic-notations-properties.png)

-   **Reflexive** :  $f(n) = O(f(n)$ and $f(n) = \Omega (f(n))$ and $f(n) = \theta (f(n))$
-   **Symmetric** : If $f(n) = \theta (g(n))$ then $g(n) = \theta (f(n))$
-   **Transitive** : If $f(n) = O(g(n))$ and $g(n) = O(h(n))$ then $f(n) = O(h(n))$
-   **Transpose** : If $f(n) = O(g(n))$ then we can also conclude that $g(n) = \Omega (f(n))$ so we say Big-Oh is transpose of Big-Omega and vice-versa.
-   **Antisymmetric** : If $f(n) = O(g(n))$ and $g(n) = O(f(n))$ then we conclude that $f(n) = g(n)$
-   **Asymmetric** : If $f(n) = \omega (g(n))$ then we can conclude that $g(n) \ne \omega (f(n))$


<a id="orgeff518e"></a>

# Lecture 3


<a id="orge4348f0"></a>

## Calculating time complexity of algorithm

We will look at three types of situations

-   Sequential instructions
-   Iterative instructions
-   Recursive instructions


<a id="org574ee71"></a>

### Sequential instructions

A sequential set of instructions are instructions in a sequence without iterations and recursions. It is a simple block of instructions with no branches. A sequential set of instructions has **time complexity of O(1)**, i.e., it has **constant time complexity**.


<a id="orga3e4bc8"></a>

### Iterative instructions

A set of instructions in a loop. Iterative instructions can have different complexities based on how many iterations occurs depending on input size. 

-   For fixed number of iterations (number of iterations known at compile time i.e. independant of the input size), the time complexity is constant, O(1). Example for(int i = 0; i < 100; i++) { &#x2026; } will always have 100 iterations, so constant time complexity.
-   For n number of iterations ( n is the input size ), the time complexity is O(n). Example, a loop for(int i = 0; i < n; i++){ &#x2026; } will have n iterations where n is the input size, so complexity is O(n). Loop for(int i = 0; i < n/2; i++){&#x2026;} also has time complexity O(n) because n/2 iterations are done by loop and 1/2 is constant thus not in big-oh notation.
-   For a loop like for(int i = 1; i <= n; i = i\*2){&#x2026;} the value of i is update as \*=2, so the number of iterations will be $log_2 (n)$. Therefore, the time complexity is $O(log_2 (n))$.
-   For a loop like for(int i = n; i > 1; i = i/2){&#x2026;} the value of i is update as \*=2, so the number of iterations will be $log_2 (n)$. Therefore, the time complexity is $O(log_2 (n))$.

**<span class="underline">Nested Loops</span>**

-   If **inner loop iterator doesn't depend on outer loop**, the complexity of the inner loop is multiplied by the number of times outer loop runs to get the time complexity For example, suppose we have loop as

    for(int i = 0; i < n; i++){
      ...
      for(int j = 0; j < n; j *= 2){
        ...
      }
      ...
    }

Here, the outer loop will **n** times and the inner loop will run **log(n)** times. Therefore, the total number of time statements in the inner loop run is n.log(n) times.
Thus the time complexity is **O(n.log(n))**.

-   If **inner loop and outer loop are related**, then complexities have to be computed using sums. Example, we have loop

    for(int i = 0; i <= n; i++){
      ...
      for(int j = 0; j <= i; j++){
        ...
      }
      ...
    }

Here the outer loop will run **n** times, so i goes from **0 to n**. The number of times inner loop runs is j, which depends on **i**. 

<table border="2" cellspacing="0" cellpadding="6" rules="all" frame="border">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Value of i</th>
<th scope="col" class="org-left">Number of times inner loop runs</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">0</td>
<td class="org-left">0</td>
</tr>


<tr>
<td class="org-left">1</td>
<td class="org-left">1</td>
</tr>


<tr>
<td class="org-left">2</td>
<td class="org-left">2</td>
</tr>


<tr>
<td class="org-left">.</td>
<td class="org-left">.</td>
</tr>


<tr>
<td class="org-left">.</td>
<td class="org-left">.</td>
</tr>


<tr>
<td class="org-left">.</td>
<td class="org-left">.</td>
</tr>


<tr>
<td class="org-left">n</td>
<td class="org-left">n</td>
</tr>
</tbody>
</table>

So the total number of times inner loop runs = $1+2+3+....+n$
  
total number of times inner loop runs = $\frac{n.(n+1)}{2}$
  
total number of times inner loop runs = $\frac{n^2}{2} + \frac{n}{2}$
  
***Therefore, time complexity is*** $O(\frac{n^2}{2} + \frac{n}{2}) = O(n^2)$
  
**Another example,**
  
Suppose we have loop

    for(int i = 1; i <= n; i++){
      ...
      for(int j = 1; j <= i; j *= 2){
        ...
      }
      ...
    }

The outer loop will run n times with i from **1 to n**, and inner will run log(i) times.

<table border="2" cellspacing="0" cellpadding="6" rules="all" frame="border">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Value of i</th>
<th scope="col" class="org-left">Number of times inner loop runs</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">1</td>
<td class="org-left">log(1)</td>
</tr>


<tr>
<td class="org-left">2</td>
<td class="org-left">log(2)</td>
</tr>


<tr>
<td class="org-left">3</td>
<td class="org-left">log(3)</td>
</tr>


<tr>
<td class="org-left">.</td>
<td class="org-left">.</td>
</tr>


<tr>
<td class="org-left">.</td>
<td class="org-left">.</td>
</tr>


<tr>
<td class="org-left">.</td>
<td class="org-left">.</td>
</tr>


<tr>
<td class="org-left">n</td>
<td class="org-left">log(n)</td>
</tr>
</tbody>
</table>

Thus, total number of times the inner loop runs is $log(1) + log(2) + log(3) + ... + log(n)$.
  
total number of times inner loop runs = $log(1.2.3...n)$
  
total number of times inner loop runs = $log(n!)$
  
Using ***Stirling's approximation***, we know that $log(n!) = n.log(n) - n + 1$
  
total number of times inner loop runs = $n.log(n) - n + 1$
  
Time complexity = $O(n.log(n))$


<a id="orgded1bf2"></a>

### An example for time complexities of nested loops

Suppose a loop,

    for(int i = 1; i <= n; i *= 2){
      ...
      for(int j = 1; j <= i; j *= 2){
        ...
      }
      ...
    }

Here, outer loop will run **log(n)** times. Let's consider for some given n, it runs **k** times, i.e, let 
$$ k = log(n) $$

The inner loop will run **log(i)** times, so number of loops with changing values of i is

<table border="2" cellspacing="0" cellpadding="6" rules="all" frame="border">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Value of i</th>
<th scope="col" class="org-left">Number of times inner loop runs</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">1</td>
<td class="org-left">log(1)</td>
</tr>


<tr>
<td class="org-left">2<sup>1</sup></td>
<td class="org-left">log(2)</td>
</tr>


<tr>
<td class="org-left">2<sup>2</sup></td>
<td class="org-left">2.log(2)</td>
</tr>


<tr>
<td class="org-left">2<sup>3</sup></td>
<td class="org-left">3.log(2)</td>
</tr>


<tr>
<td class="org-left">.</td>
<td class="org-left">.</td>
</tr>


<tr>
<td class="org-left">.</td>
<td class="org-left">.</td>
</tr>


<tr>
<td class="org-left">.</td>
<td class="org-left">.</td>
</tr>


<tr>
<td class="org-left">2<sup>k-1</sup></td>
<td class="org-left">(k-1).log(2)</td>
</tr>
</tbody>
</table>

So the total number of times inner loop runs is $log(1) + log(2) + 2.log(2) + 3.log(2) + ... + (k-1).log(2)$
$$ \text{number of times inner loop runs} = log(1) + log(2).[1+2+3+...+(k-1)] $$
$$ \text{number of times inner loop runs} = log(1) + log(2). \frac{(k-1).k}{2} $$
$$ \text{number of times inner loop runs} = log(1) + log(2). \frac{k^2}{2} - \frac{k}{2} $$
Putting value $k = log(n)$
$$ \text{number of times inner loop runs} = log(1) + log(2). \frac{log^2(n)}{2} - \frac{log(n)}{2} $$
$$ \text{Time complexity} = O(log^2(n)) $$


<a id="orga8056b4"></a>

# Lecture 4


<a id="org211bf23"></a>

## Time complexity of recursive instructions

To get time complexity of recursive functions/calls, we first also show time complexity as recursive manner. 


<a id="org48df1a1"></a>

### Time complexity in recursive form

We first have to create a way to describe time complexity of recursive functions in form of an equation as,
$$ T(n) = ( \text{Recursive calls by the function} ) + ( \text{Time taken per call, i.e, the time taken except for recursive calls in the function} ) $$

-   Example, suppose we have a recursive function

    int fact(int n){
      if(n == 0 || n == 1)
        return 1;
      else
        return n * fact(n-1);
    }

in this example, the recursive call is fact(n-1), therefore the time complexity of recursive call is T(n-1) and the time complexity of function except for recursive call is constant (let's assume **c**). So the time complexity is 
$$ T(n) = T(n-1) + c $$
$$ T(1) = T(0) = C\ \text{where C is constant time} $$

-   Another example,

    int func(int n){
      if(n == 0 || n == 1)
        return 1;
      else
        return func(n - 1) * func(n - 2);
    }

Here, the recursive calls are func(n-1) and func(n-2), therefore time complexities of recursive calls is T(n-1) and T(n-2). The time complexity of function except the recursive calls is constant (let's assume **c**), so the time complexity is 
$$ T(n) = T(n-1) + T(n-2) + c $$
$$ T(1) = T(0) = C\ \text{where C is constant time} $$

-   Another example,

    int func(int n){
      int r = 0;
      for(int i = 0; i < n; i++)
        r += i;
    
      if(n == 0 || n == 1)
        return r;
      else
        return r * func(n - 1) * func(n - 2);
    }

Here, the recursive calls are func(n-1) and func(n-2), therefore time complexities of recursive calls is T(n-1) and T(n-2). The time complexity of function except the recursive calls is **&theta; (n)** because of the for loop, so the time complexity is 

$$ T(n) = T(n-1) + T(n-2) + n $$
$$ T(1) = T(0) = C\ \text{where C is constant time} $$


<a id="orgb64e109"></a>

## Solving Recursive time complexities


<a id="orgc028b9f"></a>

### Iterative method

-   Take for example,

$$ T(1) = T(0) = C\ \text{where C is constant time} $$
$$ T(n) = T(n-1) + c $$

We can expand T(n-1).
$$ T(n) = [ T(n - 2) + c ] + c $$
$$ T(n) = T(n-2) + 2.c $$
Then we can expand T(n-2)
$$ T(n) =  [ T(n - 3) + c ] + 2.c $$
$$ T(n) =  T(n - 3) + 3.c $$

So, if we expand it k times, we will get

$$ T(n) = T(n - k) + k.c $$
Since we know this recursion **ends at T(1)**, let's put $n-k=1$.
Therefore, $k = n-1$.
$$ T(n) = T(1) + (n-1).c $$

Since T(1) = C
$$ T(n) = C + (n-1).c $$
So time complexity is,
$$ T(n) = O(n) $$

-   Another example,

$$ T(1) = C\ \text{where C is constant time} $$
$$ T(n) = T(n-1) + n $$

Expanding T(n-1),
$$ T(n) = [ T(n-2) + n - 1 ] + n $$
$$ T(n) = T(n-2) + 2.n - 1 $$

Expanding T(n-2),
$$ T(n) = [ T(n-3) + n - 2 ] + 2.n - 1 $$
$$ T(n) = T(n-3) + 3.n  - 1  - 2 $$

Expanding T(n-3),
$$ T(n) = [ T(n-4) + n - 3 ] + 3.n  - 1 - 2 $$
$$ T(n) = T(n-4) + 4.n  - 1 - 2 - 3  $$

So expanding till T(n-k)
$$ T(n) = T(n-k) + k.n - [ 1 + 2 + 3 + .... + k ] $$
$$ T(n) = T(n-k) + k.n - \frac{k.(k+1)}{2} $$

Putting $n-k=1$. Therefore, $k=n-1$.
$$ T(n) = T(1) + (n-1).n - \frac{(n-1).(n)}{2} $$
$$ T(n) = C + n^2 - n - \frac{n^2}{2} + \frac{n}{2} $$

Time complexity is
$$ T(n) = O(n^2) $$


<a id="orge90168c"></a>

### Master Theorem for Subtract recurrences

For recurrence relation of type

$$ T(n) = c\ for\ n \le 1 $$
$$ T(n) = a.T(n-b) + f(n)\ for\ n > 1 $$
$$ \text{where for f(n) we can say, } f(n) = O(n^k) $$
$$ \text{where, a > 0, b > 0 and k}  \ge 0  $$

-   If a < 1, then T(n) = O(n<sup>k</sup>)
-   If a = 1, then T(n) = O(n<sup>k+1</sup>)
-   If a > 1, then T(n) = O(n<sup>k</sup> . a<sup>n/b</sup>)

Example, $$ T(n) = 3T(n-1) + n^2 $$
Here, f(n) = O(n<sup>2</sup>), therfore k = 2,
  
Also, a = 3 and b = 1
  
Since a > 1, $T(n) = O(n^2 . 3^n)$


<a id="org50eef77"></a>

### Master Theorem for divide and conquer recurrences

$$ T(n) = aT(n/b) + f(n).(log(n))^k $$
$$ \text{here, f(n) is a polynomial function} $$
$$ \text{and, a > 0, b > 0 and k } \ge 0 $$
We calculate a value $n^{log_ba}$

-   If $\theta (f(n)) < \theta ( n^{log_ba} )$ then $T(n) = \theta (n^{log_ba})$
-   If $\theta (f(n)) > \theta ( n^{log_ba} )$ then $T(n) = \theta (f(n).(log(n))^k )$
-   If $\theta (f(n)) = \theta ( n^{log_ba} )$ then $T(n) = \theta (f(n) . (log(n))^{k+1})$

For the above comparision, we say higher growth rate is greater than slower growth rate. Eg, &theta; (n<sup>2</sup>) > &theta; (n).

Example, calculating complexity for
$$ T(n) = T(n/2) + 1 $$
Here, f(n) = 1
  
Also, a = 1, b = 2 and k = 0.
  
Calculating n<sup>log<sub>ba</sub></sup> = n<sup>log<sub>21</sub></sup> = n<sup>0</sup> = 1
  
Therfore, &theta; (f(n)) = &theta; (n<sup>log<sub>ba</sub></sup>)
  
So time complexity is 
$$ T(n) = \theta ( 1 . (log(n))^{0 + 1} ) $$
$$ T(n) = \theta (log(n)) $$

Another example, calculate complexity for
$$ T(n) = 2T(n/2) + nlog(n) $$

Here, f(n) = n
  
Also, a = 2, b = 2 and k = 1
  
Calculating n<sup>log<sub>ba</sub></sup> = n<sup>log<sub>22</sub></sup> = n
  
Therefore, &theta; (f(n)) = &theta; (n<sup>log<sub>ba</sub></sup>)
  
So time complexity is,
$$ T(n) = \theta ( n . (log(n))^{2}) $$


<a id="orgee52033"></a>

## Square root recurrence relations


<a id="org3adb528"></a>

### Iterative method

Example, 
$$ T(n) = T( \sqrt{n} ) + 1 $$
we can write this as,
$$ T(n) = T( n^{1/2}) + 1 $$
Now, we expand $T( n^{1/2})$
$$ T(n) = [ T(n^{1/4}) + 1 ] + 1 $$
$$ T(n) = T(n^{1/(2^2)}) + 1 + 1 $$
Expand, $T(n^{1/4})$
$$ T(n) = [ T(n^{1/8}) + 1 ] + 1 + 1 $$
$$ T(n) =  T(n^{1/(2^3)}) + 1  + 1 + 1 $$

Expanding **k** times,
$$ T(n) =  T(n^{1/(2^k)}) + 1  + 1 ... \text{k times } + 1 $$
$$ T(n) =  T(n^{1/(2^k)}) + k $$

Let's consider $T(2)=C$ where C is constant.
  
Putting $n^{1/(2^k)} = 2$
$$ \frac{1}{2^k} log(n) = log(2) $$
$$ \frac{1}{2^k} = \frac{log(2)}{log(n)} $$
$$ 2^k = \frac{log(n)}{log(2)} $$
$$ 2^k = log_2n $$
$$ k = log(log(n)) $$

So putting **k** in time complexity equation,
$$ T(n) = T(2) + log(log(n)) $$
$$ T(n) = C + log(log(n)) $$
Time complexity is,
$$ T(n) = \theta (log(log(n))) $$


<a id="orgc40ded0"></a>

### Master Theorem for square root recurrence relations

For recurrence relations with square root, we need to first convert the recurrance relation to the form with which we use master theorem. Example,
$$ T(n) = T( \sqrt{n} ) + 1 $$
Here, we need to convert $T( \sqrt{n} )$ , we can do that by **substituting** 
$$ \text{Substitute } n = 2^m $$
$$ T(2^m) = T ( \sqrt{2^m} ) + 1 $$
$$ T(2^m) = T ( 2^{m/2} ) + 1 $$

Now, we need to consider a new function such that,
$$ \text{Let, } S(m) = T(2^m) $$
Thus our time recurrance relation will become,
$$ S(m) = S(m/2) + 1 $$
Now, we can apply the master's theorem.
  
Here, f(m) = 1
  
Also, a = 1, and b = 2 and k = 0
  
Calculating m<sup>log<sub>ba</sub></sup> = m<sup>log<sub>21</sub></sup> = m<sup>0</sup> = 1
  
Therefore, &theta; (f(m)) = &theta; ( m<sup>log<sub>ba</sub></sup> )
  
So by master's theorem,
$$ S(m) = \theta (1. (log(m))^{0+1} ) $$
$$ S(m) = \theta (log(m) ) $$
Now, putting back $m = log(n)$
$$ T(n) = \theta (log(log(n))) $$
Another example,
$$ T(n) = 2.T(\sqrt{n})+log(n) $$
Substituting $n = 2^m$
$$ T(2^m) = 2.T(\sqrt{2^m}) + log(2^m) $$
$$ T(2^m) = 2.T(2^{m/2}) + m $$
Consider a function $S(m) = T(2^m)$
$$ S(m) = 2.S(m/2) + m $$
Here, f(m) = m
  
Also, a = 2, b = 2 and k = 0
  
Calculating m<sup>log<sub>ba</sub></sup> = m<sup>log<sub>22</sub></sup> = 1
  
Therefore, &theta; (f(m)) > &theta; (m<sup>log<sub>ba</sub></sup>)
  
Using master's theorem,
$$ S(m) = \theta (m.(log(m))^0 ) $$
$$ S(m) = \theta (m.1) $$
Putting value of m,
$$ T(n) = \theta (log(n)) $$


<a id="org416e5b8"></a>

# Lecture 5


<a id="orga5e144d"></a>

## Extended Master's theorem


<a id="org28a73b1"></a>

### For (k = -1)

$$ T(n) = aT(n/b) + f(n).(log(n))^{-1} $$
$$ \text{Here, } f(n) \text{ is a polynomial function} $$
$$ a > 0\ and\ b > 1 $$

-   If &theta; (f(n)) < &theta; ( n<sup>log<sub>ba</sub></sup> ) then, T(n) = &theta; (n<sup>log<sub>ba</sub></sup>)
-   If &theta; (f(n)) > &theta; ( n<sup>log<sub>ba</sub></sup> ) then, T(n) = &theta; (f(n))
-   If &theta; (f(n)) < &theta; ( n<sup>log<sub>ba</sub></sup> ) then, T(n) = &theta; (f(n).log(log(n)))


<a id="orgf9e9eea"></a>

### For (k < -1)

$$ T(n) = aT(n/b) + f(n).(log(n))^{k} $$
$$ \text{Here, } f(n) \text{ is a polynomial function} $$
$$ a > 0\ and\ b > 1\ and\ k < -1 $$

-   If &theta; (f(n)) < &theta; ( n<sup>log<sub>ba</sub></sup> ) then, T(n) = &theta; (n<sup>log<sub>ba</sub></sup>)
-   If &theta; (f(n)) > &theta; ( n<sup>log<sub>ba</sub></sup> ) then, T(n) = &theta; (f(n))
-   If &theta; (f(n)) < &theta; ( n<sup>log<sub>ba</sub></sup> ) then, T(n) = &theta; (n<sup>log<sub>ba</sub></sup>)


<a id="org485492c"></a>

## Tree method

Tree method is used when there are multiple recursive calls in our recurrance relation. Example,
$$ T(n) = T(n/5) + T(4n/5) + f(n) $$
Here, one call is T(n/5) and another is T(4n/5). So we can't apply master's theorem. So we create a tree of recursive calls which is used to calculate time complexity.
The first node, i.e the root node is T(n) and the tree is formed by the child nodes being the calls made by the parent nodes. Example, let's consider the recurrance relation
$$ T(n) = T(n/5) + T(4n/5) + f(n) $$

          +-----T(n/5)
    T(n)--+
          +-----T(4n/5)

Since T(n) calls T(n/5) and  T(4n/5), the graph for that is shown as drawn above. Now using recurrance relation, we can say that T(n/5) will call T(n/5<sup>2</sup>) and T(4n/5<sup>2</sup>). Also, T(4n/5) will call T(4n/5<sup>2</sup>) and T(4<sup>2</sup> n/ 5<sup>2</sup>).

    		    +--T(n/5^2)
          +-----T(n/5)--+
          +             +--T(4n/5^2)
    T(n)--+
          +             +--T(4n/5^2)
          +-----T(4n/5)-+
    		    +--T(4^2 n/5^2)

Suppose we draw this graph for an unknown number of levels.

    		    +--T(n/5^2)- - - - - - -  etc.
          +-----T(n/5)--+
          +             +--T(4n/5^2) - - - - - - - - - etc.
    T(n)--+
          +             +--T(4n/5^2) - - - - - -  - - - etc.
          +-----T(4n/5)-+
    		    +--T(4^2 n/5^2)- - - - - - etc.

We will now replace T()'s  with the **cost of the call**. The cost of the call is **f(n)**, i.e, the time taken other than that caused by the recursive calls.

    		    +--f(n/5^2)- - - - - - -  etc.
          +-----f(n/5)--+
          +             +--f(4n/5^2) - - - - - - - - - etc.
    f(n)--+
          +             +--f(4n/5^2) - - - - - -  - - - etc.
          +-----f(4n/5)-+
    		    +--f(4^2 n/5^2)- - - - - - etc.

In our example, **let's assume f(n) = n**, therfore,

    		  +--  n/5^2 - - - - - - -  etc.
        +-----  n/5 --+
        +             +-- 4n/5^2  - - - - - - - - - etc.
    n --+
        +             +--  4n/5^2  - - - - - -  - - -etc.
        +-----  4n/5 -+
    		  +--  4^2 n/5^2 - - - - - -  etc.

Now we can get cost of each level.

    			   +--  n/5^2 - - - - - - -  etc.
    	     +-----  n/5 --+
    	     +             +-- 4n/5^2  - - - - - - - - - etc.
    	 n --+
    	     +             +--  4n/5^2  - - - - - -  - - -etc.
    	     +----- 4n/5 --+
    			   +--  4^2 n/5^2 - - - - - -  etc.
    
    
    Sum :    n         n/5         n/25                      
    		  +4n/5       +4n/25
    			      +4n/25
    			      +16n/25
           .....      .....       ......
    	 n          n           n

Since sum on all levels is n, we can say that Total time taken is
$$ T(n) = \Sigma \ (cost\ of\ level_i) $$

Now we need to find the longest branch in the tree. If we follow the pattern of expanding tree in a sequence as shown, then the longest branch is **always on one of the extreme ends of the tree**. So for our example, if tree has **(k+1)** levels, then our branch is either (n/5<sup>k</sup>) of (4<sup>k</sup> n/5<sup>k</sup>). Consider the terminating condition is, $T(a) = C$. Then we will calculate value of k by equating the longest branch as, 
$$ \frac{n}{5^k} = a $$
$$ k = log_5 (n/a) $$
Also,
$$ \frac{4^k n}{5^k} = a $$
$$ k = log_{5/4} n/a $$

So, we have two possible values of k, 
$$ k = log_{5/4}(n/a),\ log_5 (n/a) $$

Now, we can say that, 
$$ T(n) = \sum_{i=1}^{k+1} \ (cost\ of\ level_i) $$
Since in our example, cost of every level is **n**.
$$ T(n) = n.(k+1) $$
Putting values of k,
$$ T(n) = n.(log_{5/4}(n/a) + 1) $$
or
$$ T(n) = n.(log_{5}(n/a) + 1) $$

Of the two possible time complexities, we consider the one with higher growth rate in the big-oh notation.


<a id="org4b6765a"></a>

## Space complexity

The amount of memory used by the algorithm to execute and produce the result for a given input size is space complexity. Similar to time complexity, when comparing two algorithms space complexity is usually represented as the growth rate of memory used with respect to input size. The space complexity includes

-   **Input space** : The amount of memory used by the inputs to the algorithm.
-   **Auxiliary space** : The amount of memory used during the execution of the algorithm, excluding the input space.

**NOTE** : *Space complexity by definition includes both input space and auxiliary space, but when comparing algorithms the input space is often ignored. This is because two algorithms that solve the same problem will have same input space based on input size (Example, when comparing two sorting algorithms, the input space will be same because both get a list as an input). So from this point on, refering to space complexity, we are actually talking about **Auxiliary Space Complexity**, which is space complexity but only considering the auxiliary space*.


<a id="org773f2f4"></a>

### Auxiliary space complexity

The space complexity when we disregard the input space is the auxiliary space complexity, so we basically treat algorithm as if it's input space is zero. Auxiliary space complexity is more useful when comparing algorithms because the algorithms which are working towards same result will have the same input space, Example, the sorting algorithms will all have the input space of the list, so it is not a metric we can use to compare algorithms. So from here, when we calculate space complexity, we are trying to calculate auxiliary space complexity and sometimes just refer to it as space complexity.


<a id="org4872e22"></a>

## Calculating auxiliary space complexity

There are two parameters that affect space complexity,

-   **Data space** : The memory taken by the variables in the algorithm. So allocating new memory during runtime of the algorithm is what forms the data space. The space which was allocated for the input space is not considered a part of the data space.
-   **Code Execution Space** : The memory taken by the instructions themselves is called code execution space. Unless we have recursion, the code execution space remains constant since the instructions don't change during runtime of the algorithm. When using recursion, the instructions are loaded again and again in memory, thus increasing code execution space.


<a id="orgfc4ead7"></a>

### Data Space used

The data space used by the algorithm depends on what data structures it uses to solve the problem. 

