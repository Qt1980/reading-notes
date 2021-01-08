# HTML and JAVASCIPT

HTML (HyperText Markup Language) and JavaScript are programming languages that are used by software developers to create webpages, data models and more through communicating with computers. 

Computers understand programming languages and this is how we as developers talk to them. Using **HTML, CSS and JavaScript** we can tell the computer how we want it to display a webpage for instance. There is generally an order in building a webpage. Let's look at the first step, HTML.

HTML as stated in the paragraph above is a markup langauage. HTML specifcally is used to structure the content of the webpage. It will define the layout of content on your webpage. Understanding how to structure means you must understand what elements HTML provide. Keep reading to learn more below: 

Before bouncing into building a webpage there are important question one should consider. Questions like:

     Why would someone visit your site?
     What are they looking for or trying to achieve?
     What information do they need?
     How often will they visit your site?

There are many elements in HTML. Here are a some elements start with:

     - <html> </html>
     - <body> </body>
     - <h1></h1>
     - <p></p>

Let's take a closer look at the examples above. 

First let's look at the how HTML structures a webpage.

![HTML Structure Example](https://3.bp.blogspot.com/-sgm6BBz6KbM/VuarmPKRJ1I/AAAAAAAAG4Q/5GDCRhO09IgiCE2DQXhA0OVaxlylGWvvw/s400/html-structure.png)

Above is a very basic example of what HTML structure would look like as code. You can find many examples by googling "html structure images". 
For example within the body of an html element:

```<body> Will be text that might explain what the body of the message on the page is about.</body>```. Looking at the image above you can see each element type as:

    <html>(Opening Tag) and </html>(Closing Tag)
    <head>(Opening Tag) and </head>(closing Tag)
    <body>(Opening Tag) and </body>(Closing Tag)

The ```<!DOCTYPE>``` explains what version of HTML is being used. Older versions of HTML might not have the ability to read newer versions of HTML like HTML5. The solution for this is to include a Javascript link currenty hosted by Google in the "Doctype" element. When an older browser is used to read the newer version it will read the link as an executable in order to render the page. Some of the newest elements may still not be visible to the user. 

HTML uses these elements to structure the webpage. 
Within the elements are "Attributes and Values". There are specific reasons and moments to use Attributes. Attributes have a name, and value. For example:

```<p lang = "en-us">``` is an opening Tag. To close this simply type ```</p>```.

## HTML 5 Layout, Process and Design

HTML 5 is the latest version of HTML being used by developers. Structure is still its main purpose and function but with new elements that seek to simplify the code which is designed to make the code easier to understand. This is done by removing the many div elements that older versions used and replacing them with new elements that describe their function like:

    1. <header> - appears at the top of the page of every site.
    1. <footer> - appears at the bottom of the page of every site.
    1. <nav>    - used to move around the page or to other pages of the same site. 

These are just a few of the new elements. There are many others.
Unfortunately some users have not updated their web browsers and so those browsers may not be able to read HTML 5. If this is the case JavaScript is used to help with this.  

Remember those questions from earlier? 

     Why would someone visit your site?
     What are they looking for or trying to achieve?
     What information do they need?
     How often will they visit your site?

These questions are a part of the process and design aspect of building your website. Knowing the answer to these question will help you in buiding the right structure for your specific site. 

After these have been answered the next step is creating a site map to plan out the structure and a wireframe. A wireframe is a drawing of what you'd like your webpage to look like, think layout or organizing the information that will be on the page. 



**Next up JavaScript**


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

Functions have to be declared like variables in order for it to be recognized in a script. Writing the word "function" is how it's done. The statement of the function is: "sayHello()". 

This tells the script to look for the function and then write Hello! on the webpage. 
The function will not work unless it is activated. The activation process or code is called "Calling the function".
Example:

```function sayMessage("msg"){```
```alert(msg);```
```}```

Calling the function: ```sayMessage("Hello from me")```

Refactoring: Changing existing code but having the end results are the same.