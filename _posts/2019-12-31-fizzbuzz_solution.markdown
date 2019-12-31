---
layout: post
title:      "FizzBuzz Solution"
date:       2019-12-31 23:34:15 +0000
permalink:  fizzbuzz_solution
---


Since I've started my job search I've had a couple of interviews that had one thing in common they all used this very basic coding challenge to see if you coulld code your way out of a wet paper bag. While the solution to this porblem can be very simple i have read that there are  variety of different solutions. 



> **
> Write a program that prints the numbers from 1 to 100. But for multiples of three print “Fizz” instead of the number and for the multiples of five print “Buzz”. For numbers which are multiples of both three and five print “FizzBuzz”.**
> 

This is not the greatets solution but it will get the job done!

```
function fizzBuzz(){
  for (let i = 1; i <= 100; i++) {
      if (i % 3 == 0 && i % 5 == 0) {
          console.log("FizzBuzz");
      } else if (i % 3 == 0) {
          console.log("Fizz");
      } else if (i % 5 == 0) {
          console.log("Buzz");
      } else {
          console.log(i);
      }
   }
} 
```
