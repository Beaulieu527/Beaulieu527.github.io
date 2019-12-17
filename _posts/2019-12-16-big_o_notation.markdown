---
layout: post
title:      "Big O Notation"
date:       2019-12-17 01:12:54 +0000
permalink:  big_o_notation
---


One of the most important subjects I realised I had to learn quickly before I started my job search was algorithms and data structures.  Before you can start learning algorithms you need to know what they are! An algorithm is a procedure for solving a problem, based on conducting a sequence of specified actions. In mathematics and computer science, an algorithm usually means a small procedure that solves a recurrent problem.

One of the most important things to Know about algorithms is that they are not all equally efficient or take the same amount of time to run. We use Big O to measure the efficiency of an algorithm. Big O notation is used in computer science to describe the performance or complexity of an algorithm.

Let's dive into Big O:

![](https://res.cloudinary.com/practicaldev/image/fetch/s--0mOYX8w0--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/r38ytuycnzi6hd8dnevh.pnghttp://)

1.** O(1) - Constant Runtime**
In this case, your algorithm runs the same time, regardless of the given input data set.

An example of this is returning the first element in the given data like in the example below.

```
function returnFirst(elements) {
   return elements[0]
}

```

The runtime is constant no matter the size of the input given.

2. **O(n) - Linear Runtime**
Linear runtime occurs when the runtime grows in proportion with the size of the input data set. n is the size of the input data set.

A good example of this is searching for a particular value in a data set using an iteration like in the example below.
```
function constainsValue(elements, value) {
  for (let element in elements) {
    if (element === value) return true;
  }
  return false
}
```
We see that the time taken to loop through all elements in the array grows with an increase in the size of the array. But what if the element is found before it reaches the last element in the array? Does the runtime complexity change?

Remember that the Big O notation considers the worst-case scenario. In this instance, it's the case where the loops run through all elements in the array. So that is what determines the runtime complexity of the algorithm.

3. **O(n2 ) - Quadratic Runtime**
O(n2 ) denotes an algorithm whose runtime is directly proportional to the square of the size of the input data set.
An example of this is a nested iteration or loop to check if the data set contains duplicates.

```
function constainsDuplicate(elements) {
  for (let element in elements) {
     for (let item in elements){
       if (element === item) return true;
     }
  }
  return false
}
```

4. **O(log n) - Logarithmic runtime**
In this case, the runtime it takes for the algorithm to run will plateau no matter the size of the input data set.

A common example of this is a search algorithm like the binary search. The idea of a binary search is not to work with the entire data. Rather, reduce the amount of work done by half with each iteration. The number of operations required to arrive at the desired result will be log base 2 of the input size.

5. **O(n log n) - Linearithmic runtime**
Here, the runtime of the algorithm depends on running a logarithm operation n times.

Most sorting algorithms have a runtime complexity of O(n log n)

6. **O(2n ) - Exponential runtime**
This occurs in algorithms where for each increase in the size of the data set, the runtime is doubled. For a small data set, this might not look bad. But as the size of the data increase, the time taken to execute this algorithm increases rapidly.

A common example of this is a recursive solution for finding Fibonacci numbers.

```
function fibonacci(num) {
if (num <= 1) return 1;

return fibonacci(num - 2) + fibonacci(num - 1)
}
```
7 **O(n!) - Factorial runtime**
In this case, the algorithm runs in factorial time. The factorial of a non-negative integer (n!) is the product of all positive integers less than or equal to n. This is a pretty horrible runtime.
