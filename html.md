# HTML: Introduction to Building Websites

HTML (Hyper Text Markup Language): It is the standard markup language for building webpages from scratch. Using HTML we will learn about "structuring a webpage", "wireframes", "site maps" and more. Keep reading to learn more below: 

Before bouncing into building a webpage there are important question one should consider. Questions like:

     Why would someone visit your site?
     What are they looking for or trying to achieve?
     What information do they need?
     How often will they visit your site?

There are many other question to consider but we'll stick with those for now. Take some time to ponder those questions because having the answers will in turn prep you in how to structure your website.

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

```<p lang = "en-us">``` is an opening Tag.