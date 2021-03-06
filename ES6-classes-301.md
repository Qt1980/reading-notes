# ES6 Classes

This reading is about ES6 Classes and how they impact JavaScript constructors. Below is Demo Code of ES6 classes from an instrcutor at Code Fellows:

[Code Fellows Demo Code](https://codefellows.github.io/code-301-guide-react/curriculum/prework/classes/DEMO.html)

Inheritance and the prototype chain
JavaScript is a bit confusing for developers experienced in class-based languages (like Java or C++), as it is dynamic and does not provide a class implementation per se (the class keyword is introduced in ES2015, but is syntactical sugar, JavaScript remains prototype-based).

When it comes to inheritance, JavaScript only has one construct: objects. Each object has a private property which holds a link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. By definition, null has no prototype, and acts as the final link in this prototype chain.

Nearly all objects in JavaScript are instances of Object which sits on the top of a prototype chain.

While this confusion is often considered to be one of JavaScript's weaknesses, the prototypal inheritance model itself is, in fact, more powerful than the classic model. It is, for example, fairly trivial to build a classic model on top of a prototypal model.

Inheritance with the prototype chain
Inheriting properties
JavaScript objects are dynamic "bags" of properties (referred to as own properties). JavaScript objects have a link to a prototype object. When trying to access a property of an object, the property will not only be sought on the object but on the prototype of the object, the prototype of the prototype, and so on until either a property with a matching name is found or the end of the prototype chain is reached.

Following the ECMAScript standard, the notation someObject.[[Prototype]] is used to designate the prototype of someObject. Since ECMAScript 2015, the [[Prototype]] is accessed using the accessors Object.getPrototypeOf() and Object.setPrototypeOf(). This is equivalent to the JavaScript property __proto__ which is non-standard but de-facto implemented by many browsers.

It should not be confused with the func.prototype property of functions, which instead specifies the [[Prototype]] to be assigned to all instances of objects created by the given function when used as a constructor. The Object.prototype property represents the Object prototype object.

Here is what happens when trying to access a property:

```Let's create an object o from function f with its own properties a and b:```

```let f = function () {```

   ```this.a = 1;```

   ```this.b = 2;```
}
```let o = new f(); // {a: 1, b: 2}```

```add properties in f function's prototype```

```f.prototype.b = 3;```

```f.prototype.c = 4;```

``` do not set the prototype f.prototype = {b:3,c:4}; this will break the prototype chain```

``` o.[[Prototype]] has properties b and c.```

``` o.[[Prototype]].[[Prototype]] is Object.prototype.```

``` Finally, o.[[Prototype]].[[Prototype]].[[Prototype]] is null.```

```This is the end of the prototype chain, as null,```

``` by definition, has no [[Prototype]].```

``` Thus, the full prototype chain looks like:```

``` {a: 1, b: 2} ---> {b: 3, c: 4} ---> Object.prototype ---> null```

```console.log(o.a);  1```

``` Is there an 'a' own property on o? Yes, and its value is 1.```

```console.log(o.b);  2```

``` Is there a 'b' own property on o? Yes, and its value is 2.```

``` The prototype also has a 'b' property, but it's not visited.```

```This is called Property Shadowing```

```console.log(o.c);  4```

``` Is there a 'c' own property on o? No, check its prototype.```

``` Is there a 'c' own property on o.[[Prototype]]? Yes, its value is 4.```

```console.log(o.d);  undefined```

``` Is there a 'd' own property on o? No, check its prototype.```

``` Is there a 'd' own property on o.[[Prototype]]? No, check its prototype.```

``` o.[[Prototype]].[[Prototype]] is Object.prototype and there is no 'd' property```

```by default, check its prototype.```

``` o.[[Prototype]].[[Prototype]].[[Prototype]] is null, stop searching,```

``` no property found, return undefined.```

## Inheriting "methods"

JavaScript does not have "methods" in the form that class-based languages define them. In JavaScript, any function can be added to an object in the form of a property. An inherited function acts just as any other property, including property shadowing as shown above (in this case, a form of method overriding).

When an inherited function is executed, the value of this points to the inheriting object, not to the prototype object where the function is an own property.

## Using prototypes in JavaScript

Let's look at what happens behind the scenes in a bit more detail.

In JavaScript, as mentioned above, functions are able to have properties. All functions have a special property named prototype. Please note that the code below is free-standing (it is safe to assume there is no other JavaScript on the webpage other than the below code). For the best learning experience, it is highly recommended that you open a console, navigate to the "console" tab, copy-and-paste in the below JavaScript code, and run it by pressing the Enter/Return key. (The console is included in most web browser's Developer Tools.

## 'this'

A function's this keyword behaves a little differently in JavaScript compared to other languages. It also has some differences between strict mode and non-strict mode.

In most cases, the value of this is determined by how a function is called (runtime binding). It can't be set by assignment during execution, and it may be different each time the function is called. ES5 introduced the bind() method to set the value of a function's this regardless of how it's called, and ES2015 introduced arrow functions which don't provide their own this binding (it retains the this value of the enclosing lexical context).

## Classes

Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.

Defining classes
Classes are in fact "special functions", and just as you can define function expressions and function declarations, the class syntax has two components: class expressions and class declarations.

Class declarations
One way to define a class is using a class declaration. To declare a class, you use the class keyword with the name of the class ("Rectangle" here).

```class Rectangle {```

  ```constructor(height, width) {```

    ```this.height = height;```

    ```this.width = width;```

  ```}```

```}```

[Resources for this page](/Resources.md)
[Back To Table of Contents](/README.md)
