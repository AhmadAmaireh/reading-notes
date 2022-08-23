# Provider Pattern with React Context API

 React’s provider pattern is a powerful concept. React uses provider pattern in Context API to share data across the tree descendant nodes. You may not find this useful when you are using plain react. However, this pattern comes handy when you are designing a complex app since it solves multiple problems.  
 
 ----

 ## What is React’s context API?
According to React docs, “Context provides a way to pass data through the component tree without having to pass props down manually at every level.”

This means Context API helps us to skip the mandatory hierarchy of passing props for each component in its component tree.

----

## Provider pattern and Context API
Provider pattern, however, is not only about react context. You might have used a state management library like redux and mobX. Here provider is the top most component and it is provided by react-redux. We write it the following way:
```
import React from 'react';
import ReactDOM from 'react-dom';
import { Provider } from 'react-redux';
import store from './store';
import App from './App';

const rootElement = document.getElementById('root');
ReactDOM.render(  
   <Provider store={store}>    
     <App />  
   </Provider>,  
   rootElement
);
```

In fact, react-redux has implemented the provider pattern where Provider component receives the state as props, and post that, each child component has implicit access to the managed state.

Let’s now look at what problem(s) provider pattern can solve in react.

----

## Use of provider pattern in React
You might have heard about props-drilling. While building your application, you may be at a stage where you are drilling through many layers of components.

----

## Where can you use Context API?
Some sample use cases where the Context API proves helpful are:

  * Theming — Pass down app theme
  * i18n — Pass down translation messages
  * Authentication — Pass down current authenticated user.
  
Let’s now dig into a real-world example applying all that we learnt about the provider pattern and context API.