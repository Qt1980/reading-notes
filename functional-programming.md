# Concepts of Functional Programming in Javascript

After a long time learning and working with object-oriented programming, I took a step back to think about system complexity.

“Complexity is anything that makes software hard to understand or to modify." — John Outerhout

Doing some research, I found functional programming concepts like immutability and pure function. Those concepts are big advantages to build side-effect-free functions, so it is easier to maintain systems — with some other benefits.

In this post, I will tell you more about functional programming, and some important concepts, with a lot of code examples. In Javascript!

What is functional programming?
Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data — Wikipedia

## Pure functions

The first fundamental concept we learn when we want to understand functional programming is pure functions. But what does that really mean? What makes a function pure?
So how do we know if a function is pure or not? Here is a very strict definition of purity:

It returns the same result if given the same arguments (it is also referred as deterministic)
It does not cause any observable side effects

It returns the same result if given the same arguments

Imagine we want to implement a function that calculates the area of a circle. An impure function would receive radius as the parameter, and then calculate radius * radius * PI:

```let PI = 3.14;```

```const calculations = (radius) => radius * radius * PI;```

```calculateArea(10); //returns 314.0```

Why is this an impure function? Simply because it uses a global object that was not passed as a parameter to the function.
Now imagine some mathematicians argue that the PI value is actually 42and change the value of the global object.

Our impure function will now result in 10 * 10 * 42 = 4200. For the same parameter (radius = 10), we have a different result. Let's fix it!

```let PI = 3.14;```

```const calculateArea = (radius, pi) => radius * radius * pi;```

```calculateArea(10, PI); // returns 314.0```

## Refactoring Code

Click the link below to read an article about refactoring javascript code. Refactoring is a useful skill to have that creates a more readable code base. Think of it as a way to simplify and make concise statements. 

[Refactoring](/https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)


Content for this page are from online resources found under 301 Resources Class 07 at [Resources](/Resources.md)

[Back to Table of Contents](/README.md)
