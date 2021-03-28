# Hello World
The smallest React example looks like this:

```ReactDOM.render(```

  ```<h1>Hello, world!</h1>,```

  ```document.getElementById('root')```
```);```

It displays a heading saying “Hello, world!” on the page.

## Introducing JSX

Consider this variable declaration:

```const element = <h1>Hello, world!</h1>;```

This funny tag syntax is neither a string nor HTML.

It is called JSX, and it is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.

JSX produces React “elements”. We will explore rendering them to the DOM in the next section. Below, you can find the basics of JSX necessary to get you started.

Why JSX?
React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both. We will come back to components in a further section, but if you’re not yet comfortable putting markup in JS, this talk might convince you otherwise.

React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages.

With that out of the way, let’s get started!

Embedding Expressions in JSX
In the example below, we declare a variable called name and then use it inside JSX by wrapping it in curly braces:

```const name = 'Josh Perez';```

```const element = <h1>Hello, {name}</h1>;```

```ReactDOM.render(```

  ```element,```

  ```document.getElementById('root')``

```);```

You can put any valid JavaScript expression inside the curly braces in JSX. For example, 2 + 2, user.firstName, or formatName(user) are all valid JavaScript expressions.

In the example below, we embed the result of calling a JavaScript function, formatName(user), into an <h1> element.

```function formatName(user) {```

  ```return user.firstName + ' ' + user.lastName;```

```}```

```const user = {```

  ```firstName: 'Harper',```

  ```lastName: 'Perez'```

```};```

```const element = (```

  ```<h1>```

    ```Hello, {formatName(user)}!```

  ```</h1>```
```);```

```ReactDOM.render(```

  ```element,```

  ```document.getElementById('root')```

```);```

We split JSX over multiple lines for readability. While it isn’t required, when doing this, we also recommend wrapping it in parentheses to avoid the pitfalls of automatic semicolon insertion.

JSX is an Expression Too
After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.

This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions.

## Rendering Elements

Elements are the smallest building blocks of React apps.

An element describes what you want to see on the screen:

```const element = <h1>Hello, world</h1>;```

Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

## Rendering an Element into the DOM

Let’s say there is a <div> somewhere in your HTML file:

```<div id="root"></div>```

We call this a “root” DOM node because everything inside it will be managed by React DOM.

Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.

To render a React element into a root DOM node, pass both to ReactDOM.render():

```const element = <h1>Hello, world</h1>;```

```ReactDOM.render(element, document.getElementById('root'));```

It displays “Hello, world” on the page.

Updating the Rendered Element
React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.

With our knowledge so far, the only way to update the UI is to create a new element, and pass it to ReactDOM.render().

Consider this ticking clock example:

```function tick() {```

  ```const element = (```

    ```<div>```

      ```<h1>Hello, world!</h1>```

      ```<h2>It is {new Date().toLocaleTimeString()}.</h2>```

    ```</div>```

  ```);```

  ```ReactDOM.render(element, document.getElementById('root'));```

```}```

```setInterval(tick, 1000);```

## Components and Props

Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. This page provides an introduction to the idea of components. You can find a detailed component API reference here.

Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.

Function and Class Components
The simplest way to define a component is to write a JavaScript function:

```function Welcome(props) {```

  ```return <h1>Hello, {props.name}</h1>;```

```}```

This function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element. We call such components “function components” because they are literally JavaScript functions.

[Back to Table of Contents](/README.md)