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

Look at the picture below from tutorialrepublic.com
![Types of Borders](https://www.tutorialrepublic.com/lib/images/css-border-style.png)

You can add variety and flair to your content by using differnt border styles.
Borders separate the edge of one box from that of another.
They have 4 sides that can be control. The order of control is top, right, bottom, left. Each side can be control individually and can be colored, thin, medium and thick width. Example:

```h1 {```
  ```border-width: 2px```
  ```border-top-color: red}```

Along with borders are padding and margins. They can be controlled in the same ways
