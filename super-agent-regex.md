# SuperAgent

SuperAgent is light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve after being frustrated with many of the existing request APIs. It also works with Node.js!

## Request basics

A request can be initiated by invoking the appropriate method on the request object, then calling .then() (or .end() or await) to send the request. For example a simple GET request:

 ```request```
   ```.get('/search')```
   ```.then(res => {```
      ```// res.body, res.headers, res.status```
   ```})```
   ```.catch(err => {```
      ```// err.message, err.response```
   ```});```

## RegExr

RegExr was created by gskinner.com, and is proudly hosted by Media Temple.

Edit the Expression & Text to see matches. Roll over matches or the expression for details. PCRE & JavaScript flavors of RegEx are supported. Validate your expression with Tests mode.

The side bar includes a Cheatsheet, full Reference, and Help. You can also Save & Share with the Community, and view patterns you create or favorite in My Patterns.

Explore results with the Tools below. Replace & List output custom results. Details lists capture groups. Explain describes your expression in plain English.


Content for this page are from online resources found under 301 Resources Class 07 at [Resources](/Resources.md)

[Back to Table of Contents](/README.md)