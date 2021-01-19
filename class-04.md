# Link, Layout and JavaScript Functions, Methods and Objects

## Link

As you might already know, links are used to take you from one webpage to another or even from one part of a website to another part of the same site. They are how we "Surf" or browse the web. Let's look at what the link looks like in html.

```<a href="https://www.apple.com">Apple</a>```

The opening and closing  ```<a></a>``` tag is how the link is started. Just inside the opening tag is the href attribute that allows us to specify which site address we want to link to. As you can see in the above example the href attribute equals "https://apple.com" then the closing bracket of the opening tag is put in place. This isn't the same as the closing tag of the ```</a>``` element so be sure to pay attention to that. The word 'Apple' is typed right after and then the closing ```</a>``` tag is applied. When the page is rendered the browser knows to only display the word *Apple* and is usually blue in color to signify that it is a link. If the user clicks on the link they will be taken to the website address that is equal to href, which in this case is "https://apple.com". This is considered an **_Absoulte_** URLs (Uniform Resource Locator) linking to another site outside of the site that you might currently be visiting.

As stated earlier links can also take you to different parts of the same page. For instance you may want to visit the "Contact" section of a website but you are currently on the home page. If no link was present on the home page (usually near the bottom somewhere) how would you access the websites owners contact information? You would need a link to it. It may show up as a button or words titled "Contact Us' that you can click on. That's the link!

See the below example created by a student from Code Fellows: This is how links are created using markdown. Each link will take you to a differnt part of that website. These are all considered **_Relative_** URLs because they keep you in the same website address.

Code Fellows Class 102  TABLE OF CONTENTS

   ```[GrowthMindset](/GrowthMindset.md)```

   ```[Markdown](/markdown.md)```

   ```[Choosing A Text Editor](/Choosing-text-editor.md)```

   ```[Git-some](/Git-some.md)```

   ```[Reading Resources](/Resources.md)```

   ```[Intro to HTML](/html.md)```

   ```[Intro to CSS](/css.md)```

   ```[Intro to the Computer](/cpu.md)```

   ```[Intro to JavaScript](/java.md)```

   ```[Comparisons and Loops](/loop.md)```

This last link is actually clickable! Try it!

[Comparisons and Loops](/loop.md)

Links can be used to do other things like open email programs like Microsoft Outlook or Gmail as well.

### Layouts with CSS

Using CSS we can control the layout or design process of our webpage. This is accomplished by controlling where block and inline elements are positioned on a webpage.

**Block-level** elements start on a new line and are essentially the main building blocks of the page payout. Examples of block-level elements are ```<h1>```, ```<ul>```, ```<ol>```, and ```<p>``` and more.

**Inline elements** generally flow in between text on a webpage. This might appear as an image inside a different element like a ```<p>```(paragraph element) that illustrates some point the designer is trying to make.
Examples: ```<img>```, ```<b>```, and ```<i>``` and more.

In order to control the position of elements we use position schemes. There are 5 schemes for positioning.

    1.Normal Flow: Causes every block-level element to appear on a new line.

    1. Relative Positioning: Moves the element from its normal position to top, right, bottom and left. Does not affect position of surrounding elements.

    1. Absolute Positioning:Positions the element based on the element that it is contained in. Moves as users scroll up and down and does not affect surrounding elements

    1. Fixed Positioning: Positions in relation to the browser window. Does not move when the user scrolls up or down and does not affect surrounding elements.

    1. Floating Elements: Positions to the far left or right of a containing box. Other elements flow around it.

There are other types of layouts like the fixed-width layout or the liquid layout.Each does something unique. Pages are usually designed within 960-1000 pixels in width and around 600 in height so that the user can see what the page is about before they scroll down to see the remaining content. 

Multiple CSS style sheets can be used on one page.

#### Functions, Methods and Objects

    1. Functions: Gives the ability to group a set of related statements together that represent a single task. They can evaluate perameters and return a value or output. In order for the function to execute it must be ordered to operate. This is called "Calling the function". 

    1. Objects: a group of variables and functions that represent something from the world around you. Variables are considered to be properties of an object whereas functions are considered to be methods of the object.

    1. Browsers ahve rules that are associated with objects that represent the browser window and the document that is being rendered or displayed in the window.

    1. Objects in JavaScript are 'strings', math, dates and numbers. 
    1. Arrays and objects might be used to create in depth data sets.

[Back to Table of Contents](/README.md)