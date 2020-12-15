# JavaScript: A Peek Into A Logical Language

JavaScript (JS) is a text based language like HTML or CSS. Unlike HTML and CSS, JavaScript intrduces logic in the language.
   With JavaScript any element in a HTML file can be selected to provide interaction to the user.
   JaveScript can modify content, access content, program rules for the browser to follow and react to events when they occur.

## What is a script?

A script is a set of instructions given to the computer to follow in order to achieve a specific goal on the webpage. As a Chef learning to use code, a script would be the equivalent to a recipe.

In order to write a script you need to:

1. Figure out what your goal is.
1. Start with the big picture of that goal.
1. Break it down into smaller steps.

Doing this will allow you to:

    -  Define the goal
    -  Design the script
    -  Write the code for the small steps

For your consideration: Take your time learning these languages. Ask questions if you are in a classroom setting. Use google to try to find answers to things you don't understand. Be patient and give yourself grace. You may not grasp everything all at once. It is ok to learn in small chunks.

**Vocabulary:**
1. *Programmatic*: The systemic step by step way in which a computer follows instructions.
1. *Syntax*: The rules that define the structure of a programming language.
1. *Debugging*: The process of detecting and removing of existing and potential errors in software code.
1. *Flowchart*: A graphical representation of an algorithm.

__Expressions__

An expression evaluates into a single value. There are two types of expressions. The first is on that only assigns values to a varaible.
Example: ```var color ='black'```. This expression shows that only the color black as been assigned to the variable. If no color is assigned then the computer will read the variable as 'Undefined'.

The second type of expression os one that uses two or more values that result ina single value.
Example: ```var area = 3 * 2;```. The browser will read this as a return value of 6.

__Operators__

These allow programmeres to create a single value from one or more values. Operators use values such as (+, =, <,>, *) etc.
Operators are broken down into different types:

*Assignment*
*Arithmetic*
*String* 
*Comparison*
*Logical*

Functions: Is a group of statements put together to perform a specific task.

A function has to be declared just like variables. Declaring a function is easy. Simply write:
```function``` on the line in the appropriate place.
Next it will need a statement:

```function sayHello() {```
 ```document.write('Hello!');```
}```

Parameter: Information given to the function so that it can complete a task. 
Return Value: The answer a function gives.

Functions have to be declared like variables in order for it to be recognized in a script. Writing the word "function" is how it's done. The statement is next: "sayHello()". The full example is below:

```function sayHello(){```
```document.write('Hello!');```
```}```

This tells the script to look for the function and then write Hello! on the webpage. 
The function will not work unless it is activated. The activation process or code is called "Calling the function".
Example:

```function sayMessage("msg"){```
```alert(msg);```
```}```

Calling the function: ```sayMessage("Hello from me")```

Refactoring: Changing existing code but having the end results are the same.