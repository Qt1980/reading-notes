# REACT: STATE AND PROPS

Below is a little about State and LifeCycles from [Reactjs.org](/https://reactjs.org/docs/state-and-lifecycle.html)

State and Lifecycle
This page introduces the concept of state and lifecycle in a React component. You can find a detailed component API reference here.

Consider the ticking clock example from one of the previous sections. In Rendering Elements, we have only learned one way to update the UI. We call ReactDOM.render() to change the rendered output:

```function tick() {```

  ```const element = (```

    ```<div>```

      ```<h1>Hello, world!</h1>```

      ```<h2>It is {new Date().toLocaleTimeString()}.</h2>```

    ```</div>```

  ```);```

  ```ReactDOM.render(```

    ```element,```

    ```document.getElementById('root')```

  ```);```

```}```

```setInterval(tick, 1000);```

Practice with the code on CodePen!

In this section, we will learn how to make the Clock component truly reusable and encapsulated. It will set up its own timer and update itself every second.

We can start by encapsulating how the clock looks:

```function Clock(props) {```

  ```return (```

    ```<div>```


      ```<h1>Hello, world!</h1>```

      ```<h2>It is {props.date.toLocaleTimeString()}.</h2>```

    ```</div>```

  ```);```

```}```

```function tick() {```

  ```ReactDOM.render(```

    ```<Clock date={new Date()} />,```

    ```document.getElementById('root')```

  ```);```

```}```

```setInterval(tick, 1000);```


However, it misses a crucial requirement: the fact that the Clock sets up a timer and updates the UI every second should be an implementation detail of the Clock.

Ideally we want to write this once and have the Clock update itself:

```ReactDOM.render(```

  ```<Clock />,```

  ```document.getElementById('root')```

```);```

To implement this, we need to add “state” to the Clock component.

State is similar to props, but it is private and fully controlled by the component.

Converting a Function to a Class
You can convert a function component like Clock to a class in five steps:

Create an ES6 class, with the same name, that extends React.Component.
Add a single empty method to it called render().
Move the body of the function into the render() method.
Replace props with this.props in the render() body.
Delete the remaining empty function declaration.

```class Clock extends React.Component {```

  ```render() {```

    ```return (```

    ```<div>```

    ```<h1>Hello, world!</h1>```

    ```<h2>It is {this.props.date.toLocaleTimeString()}.</h2>```

    ```</div>```

    ```);```

  ```}```

```}```

## Handling Events in React JS

Read more on Handling events at [Reactjs.org](/https://reactjs.org/docs/handling-events.html)

Handling Events
Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:

React events are named using camelCase, rather than lowercase.
With JSX you pass a function as the event handler, rather than a string.
For example, the HTML:

```<button onclick="activateLasers()">```

  ```Activate Lasers```

```</button>```

is slightly different in React:

```<button onClick={activateLasers}>```

  ```Activate Lasers```

```</button>```

Another difference is that you cannot return false to prevent default behavior in React. You must call preventDefault explicitly. For example, with plain HTML, to prevent the default link behavior of opening a new page, you can write:

```<a href="#" onclick="console.log('The link was clicked.'); return false">```

  ```Click me```

```</a>```

In React, this could instead be:

```function ActionLink() {```

  ```function handleClick(e) {```

    ```e.preventDefault();```

    ```console.log('The link was clicked.');```

  ```}```

  ```return (```

    ```<a href="#" onClick={handleClick}>```

      ```Click me```

    ```</a>```

  ```);```

```}```

Here, e is a synthetic event. React defines these synthetic events according to the W3C spec, so you don’t need to worry about cross-browser compatibility. React events do not work exactly the same as native events. See the SyntheticEvent reference guide to learn more.

When using React, you generally don’t need to call addEventListener to add listeners to a DOM element after it is created. Instead, just provide a listener when the element is initially rendered.

When you define a component using an ES6 class, a common pattern is for an event handler to be a method on the class. For example, this Toggle component renders a button that lets the user toggle between “ON” and “OFF” states:

```class Toggle extends React.Component {```

  ```constructor(props) {```

    ```super(props);```

    ```this.state = {isToggleOn: true};```

    ```This binding is necessary to make `this` work in the callback```
    ```this.handleClick = this.handleClick.bind(this);```

  ```}```

  ```handleClick() {```

    ```this.setState(state => ({```

      ```isToggleOn: !state.isToggleOn```

    ```}));```

  ```}```

  ```render() {```

    ```return (```

      ```<button onClick={this.handleClick}>```

        ```{this.state.isToggleOn ? 'ON' : 'OFF'}```

      ```</button>```

    ```);```

  ```}```

```}```

```ReactDOM.render(```

  ```<Toggle />,```

  ```document.getElementById('root')```

```);```


## Conditional Rendering

Read more on Condition Rendering at [Reactjs.org](/https://reactjs.org/docs/conditional-rendering.html)

Conditional Rendering
In React, you can create distinct components that encapsulate behavior you need. Then, you can render only some of them, depending on the state of your application.

Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them.

Consider these two components:

```function UserGreeting(props) {```

  ```return <h1>Welcome back!</h1>;```

```}```

```function GuestGreeting(props) {```

  ```return <h1>Please sign up.</h1>;```

```}```

We’ll create a Greeting component that displays either of these components depending on whether a user is logged in:

```function Greeting(props) {```

  ```const isLoggedIn = props.isLoggedIn;```

  ```if (isLoggedIn) {```

    ```return <UserGreeting />;```

  ```}```

  ```return <GuestGreeting />;```

```}```

```ReactDOM.render(```

  ```// Try changing to isLoggedIn={true}:```

  ```<Greeting isLoggedIn={false} />,```

  ```document.getElementById('root')```
  
```);```


All content found at [Reactjs.org](/reactjs.org/docs)

[Back to Table of Contents](/README.md)