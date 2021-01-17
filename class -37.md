### Readings: React 1
![img](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSH7wS6CPAq0I6cl9z0gaiRiMMHhg-iQzzPzA&usqp=CAU)

React is a JavaScript library

Hello World
The smallest React example looks like this:
```javascript
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```


Rendering Elements
Elements are the smallest building blocks of React apps.

An element describes what you want to see on the screen:

```javascript
const element = <h1>Hello, world</h1>;
```

Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

Why JSX?
React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both. We will come back to components in a further section, but if you’re not yet comfortable putting markup in JS, this talk might convince you otherwise.

React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages.

With that out of the way, let’s get started!

Embedding Expressions in JSX
In the example below, we declare a variable called name and then use it inside JSX by wrapping it in curly braces:

```javascript
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

ReactDOM.render(
  element,
  document.getElementById('root')
);
```

You can put any valid JavaScript expression inside the curly braces in JSX. For example, 2 + 2, user.firstName, or formatName(user) are all valid JavaScript expressions.

In the example below, we embed the result of calling a JavaScript function, formatName(user), into an <h1> element.

```javascript
function formatName(user) {
  return user.firstName + ' ' + user.lastName;
}

const user = {
  firstName: 'Harper',
  lastName: 'Perez'
};

const element = (
  <h1>
    Hello, {formatName(user)}!
  </h1>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
```


We split JSX over multiple lines for readability. While it isn’t required, when doing this, we also recommend wrapping it in parentheses to avoid the pitfalls of automatic semicolon insertion.

JSX is an Expression Too
After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.

This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions:

```javascript
function getGreeting(user) {
  if (user) {
    return <h1>Hello, {formatName(user)}!</h1>;
  }
  return <h1>Hello, Stranger.</h1>;
}
```

```javascript
Specifying Attributes with JSX
You may use quotes to specify string literals as attributes:
```
const element = <div tabIndex="0"></div>;
You may also use curly braces to embed a JavaScript expression in an attribute:

```javascript
const element = <img src={user.avatarUrl}></img>;
```
