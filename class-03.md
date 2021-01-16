# Lists, Borders and More, Oh my!

There are 3 types of lists:
* Ordered List ```<ol>```: This list will be in numerical order.
* Unordered List ```<ul>```: Will not be in any particular order.
* Definition list ```<dl>```: Used to create words and their definitions.

Nested lists are lists inside a list element ```<li>```. The li stands for list item.

## Borders and Boxes

CSS give developers the ability to change the box size that naturally surrounds an element in html. The default box size is just big enough to hold its own content. The more content in the box the bigger the box will be, with limitations of course. 

Height and width of boxes can be changed using pixels (px), percentages or (ems). Limitations can be applied to the width and height of boxes as well. The purpose of limiting dimensions is render the webpage properly depending on screen size, think mobile device like Android or iPhone. 

The limitations are necessary because other html elements have boxes and there is only sp much content that be displayed on a website without it looking messy or overcrowded. If the content size is more than the size of the box there's a way to control this. It is called overflow.

Overflow gives the developer the ability to either hide extra content or add a scroll bar so that users can continue accessing information.

**Back to Borders**

*Borders* separate the edge of one box from that of another.

Look at the picture below from tutorialrepublic.com
![Types of Borders](https://www.tutorialrepublic.com/lib/images/css-border-style.png)

You can add variety and flair to your content by using differnt border styles.
They have 4 sides that can be controlled. The order of control is top, right, bottom, left. Each side can be controlled individually and can be colored, thin, medium and thick width. Some of the other ways in which borders can be controlled are with images, box shadows, radius and elliptical borders. Here is an Example of what CSS code looks like to control a border:

  ```h1 {```

  ```border-width: 2px;```

  ```border-top-color: red}```

Along with borders are padding and margins. They can be controlled in the most of same ways as borders.

*Padding* is the space between the border and the content of a box.
*Margin* is the area outside the edge of a border.

### The MORE

As stated previously Javascript is used to create interactive webpages for a more enjoyable user experience. One of the ways this can be done is to use a combination of *variables, expressions, if and switch statements*.

JavaScript can use regular variable using the **var** code. There's another type of variable called an *Array*.

**Arrays** - are variables that are able to contain lists of values.

There are two ways to create an array.

Example 1 from JS Duckett Book:

```var colors;```
      ```     ```
        ``` colors = ['white', 'black', 'custom'];```

Example 2 from JS Duckett Book:

```var colors = new Array('White,'Black','Custom');```

The first type is call *Array Literal* and the second type *Array Constructor*.
The items inside an array are given a number sequence that starts with 0. So in the above example the color white would be assigned 0, black=1 and custom=2. This is called an index.

*If* and *else if* statement check a condition, if the condition evaulates to be true then the first block of code will run. If it evalutes to be false then the second block of code associated with the *else if* statement will run. If statements can be slow so to remedy this **switch statements** can be used.

Switch statements start with a variable called a switch value. Ater the value is set then the statement will move to check its cases. Cases are like conditions that are checked. If the case is true then a block of code will run that corresponds to that case. Since switch statements use an array type variable it can contain many cases. Switch statements have default option if no case is true. 

Quiz Break

1. What is Padding?
  a. The edges around a box that separates from other boxes.
  b. An expression that is used to determine whether a conditons is true or false.
  c. The space between the border and the content of a box.
  d. A style type that is used to outline boxes in CSS.

2. CSS is used to:
  a. Add struture to webpages.
  b. Evaluate expressions with logical operators.
  c. Style text, headers, and format words in a document.
  d. Add style, layout and presentation to webpages.

3. What is an Array?
  a. A version control system used to make copies of changes within a repository.
  b. An evaluation that returns a falsy value.
  c. A cascading style sheet.
  d. A type of variable that contains lists of values.

4. How many borders styles can be used in CSS?
  a. 5
  b. 8
  c. 12
  d. 2

Answer Table

Question | Answer
---------|-------
What is Padding | C
CSS is used to | D
What is an Array | D
Number of Border Styles | B

[Back to Table of Contents](/README.md)