# Hook
 A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We’ll learn other Hooks later.

---------------------

### What was the motivation for introducing Hooks?

Hooks solve a wide variety of seemingly unconnected problems in React that we’ve encountered over five years of writing and maintaining tens of thousands of components. Whether you’re learning React, use it daily, or even prefer a different library with a similar component model, you might recognize some of these problems.

-----------------

### What changes are important regarding implementing Hooks versus Component Classes?

* There are no plans to remove classes from React. You can read more about the gradual adoption strategy for Hooks in the bottom section of this page.

* Hooks don’t replace your knowledge of React concepts. Instead, Hooks provide a more direct API to the React concepts you already know: props, state, context, refs, and lifecycle. As we will show later, Hooks also offer a new powerful way to combine them.
 
---------------------

## State Hook
This example renders a counter. When you click the button, it increments the value:

```
import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}

```
--------

## Using the State Hook
Hooks are a new addition in React 16.8. They let you use state and other React features without writing a class.

The introduction page used this example to get familiar with Hooks:

```
import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

We’ll start learning about Hooks by comparing this code to an equivalent class example.

Equivalent Class Example
If you used classes in React before, this code should look familiar:

```
class Example extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
  }

  render() {
    return (
      <div>
        <p>You clicked {this.state.count} times</p>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>
          Click me
        </button>
      </div>
    );
  }
}

```

The state starts as { count: 0 }, and we increment state.count when the user clicks a button by calling this.setState(). We’ll use snippets from this class throughout the page.

----

## Hooks and Function Components
As a reminder, function components in React look like this:

```
const Example = (props) => {
  // You can use Hooks here!
  return <div />;
}
```
or this:

```
function Example(props) {
  // You can use Hooks here!
  return <div />;
}
```

You might have previously known these as “stateless components”. We’re now introducing the ability to use React state from these, so we prefer the name “function components”.

Hooks don’t work inside classes. But you can use them instead of writing classes.

------

## What’s a Hook?
Our new example starts by importing the useState Hook from React:

```
import React, { useState } from 'react';

function Example() {
  // ...
}
```

### What is a Hook? 
A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We’ll learn other Hooks later.

### When would I use a Hook?
 If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component. We’re going to do that right now!



