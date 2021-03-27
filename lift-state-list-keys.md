# Lifting State Up

Often, several components need to reflect the same changing data. We recommend lifting the shared state up to their closest common ancestor. Let’s see how this works in action.

In this section, we will create a temperature calculator that calculates whether the water would boil at a given temperature.

We will start with a component called BoilingVerdict. It accepts the celsius temperature as a prop, and prints whether it is enough to boil the water:

```function BoilingVerdict(props) {```

  ```if (props.celsius >= 100) {```

    ```return <p>The water would boil.</p>;```

  ```}```

  ```return <p>The water would not boil.</p>;```

```}```

Next, we will create a component called Calculator. It renders an <input> that lets you enter the temperature, and keeps its value in this.state.temperature.

Additionally, it renders the BoilingVerdict for the current input value.

```class Calculator extends React.Component {```

  ```constructor(props) {```

    ```super(props);```

    ```this.handleChange = this.handleChange.bind(this);```

    ```this.state = {temperature: ''};```
  ```}```

  ```handleChange(e) {```

    ```this.setState({temperature: e.target.value});```

  ```}```

  ```render() {```

    ```const temperature = this.state.temperature;```

    ```return (```

      ```<fieldset>```

        ```<legend>Enter temperature in Celsius:</legend>```
       ``` <input```

          ```value={temperature}```

          ```onChange={this.handleChange} />```

        ```<BoilingVerdict```

          ```celsius={parseFloat(temperature)} />```

      ```</fieldset>```

    ```);```
  ```}```
```}```

## Lists and Keys

First, let’s review how you transform lists in JavaScript.

Given the code below, we use the map() function to take an array of numbers and double their values. We assign the new array returned by map() to the variable doubled and log it:

```const numbers = [1, 2, 3, 4, 5];```

```const doubled = numbers.map((number) => number * 2);```

```console.log(doubled);```

This code logs [2, 4, 6, 8, 10] to the console.

In React, transforming arrays into lists of elements is nearly identical.

Rendering Multiple Components
You can build collections of elements and include them in JSX using curly braces {}.

Below, we loop through the numbers array using the JavaScript map() function. We return a <li> element for each item. Finally, we assign the resulting array of elements to listItems:

```const numbers = [1, 2, 3, 4, 5];```

```const listItems = numbers.map((number) =>```

  ```<li>{number}</li>```
```);```

We include the entire listItems array inside a <ul> element, and render it to the DOM:

```ReactDOM.render(```

  ```<ul>{listItems}</ul>,```

  ```document.getElementById('root')```

```);```

##  Keys

Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity:

```const numbers = [1, 2, 3, 4, 5];```

```const listItems = numbers.map((number) =>```

  ```<li key={number.toString()}>```

    ```{number}```

  ```</li>```
```);```

The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys:

```const todoItems = todos.map((todo) =>```

  ```<li key={todo.id}>```

    ```{todo.text}```

  ```</li>```

```);```

When you don’t have stable IDs for rendered items, you may use the item index as a key as a last resort:

```const todoItems = todos.map((todo, index) =>```

  ```// Only do this if items have no stable IDs```

  ```<li key={index}>```

    ```{todo.text}```

  ```</li>```

```);```

We don’t recommend using indexes for keys if the order of items may change. This can negatively impact performance and may cause issues with component state. Check out Robin Pokorny’s article for an in-depth explanation on the negative impacts of using an index as a key. If you choose not to assign an explicit key to list items then React will default to using indexes as keys.

## Spread Operators

What is the spread operator?

In JavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments.

“When ...arr is used in the function call, it ‘expands’ an iterable object arr into the list of arguments.” — JavaScript.info
The spread operator was added to JavaScript in ES6 (ES2015), just like the rest parameters, which have the same syntax: three magic dots ….

What is ... used for?
“Spread operator to the rescue! It looks similar to rest parameters, also using ..., but does quite the opposite.” — JavaScript.info
Take trying to find the largest number in an array with Math.max():

Trying to pass an array to a JavaScript function expecting separate arguments does not work. In this case it produces a NaN result. Enter …:

The spread syntax “spreads” the array into separate arguments.

What else can … do?
The … spread operator is useful for many different routine tasks in JavaScript, including the following:
Copying an array
Concatenating or combining arrays
Using Math functions
Using an array as arguments
Adding an item to a list
Adding to state in React
Combining objects
Converting NodeList to an array
In each case, the spread syntax expands an iterable object, usually an array, though it can be used on any interable, including a string.

Examples of using …
Here are a couple basic examples of using … in JavaScript, where I demonstrate copying an array, splitting a string into characters, and combining the properties of two JavaScript objects:

```[...["😋😛😜🤪😝"]] // Array [ "😋😛😜🤪😝" ]```

```[..."🙂🙃😉😊😇🥰😍🤩!"] // Array(9) [ "🙂", "🙃", "😉", "😊", "😇", "🥰", "😍", ```

```"🤩", "!" ]```

```const hello = {hello: "😋😛😜🤪😝"}```

```const world = {world: "🙂🙃😉😊😇🥰😍🤩!"}```

```const helloWorld = {...hello,...world}```

```console.log(helloWorld) // Object { hello: "😋😛😜🤪😝", world: "🙂🙃😉😊😇🥰😍🤩!" }```

## Copying an array

Using the … spread operator is a convenient way to copy an array or combine arrays, and it can even add new items:

```const fruits = ['🍏','🍊','🍌','🍉','🍍']```

```const moreFruits = [...fruits];```

```console.log(moreFruits) // Array(5) [ "🍏", "🍊", "🍌", "🍉", "🍍" ]```

```fruits[0] = '🍑'```

```console.log(...[...fruits,'...',...moreFruits]) //  🍑 🍊 🍌 🍉 🍍 ... 🍏 🍊 🍌 🍉 🍍```

[Class 03 Resources](/Resources.md)
[Back to Table of Contents](/README.md)