# Redux - Asynchronous Actions

## Async Logic and Data Fetching
---
By itself, a Redux store doesn't know anything about async logic. It only knows how to synchronously dispatch actions, update the state by calling the root reducer function, and notify the UI that something has changed. Any asynchronicity has to happen outside the store.

Earlier, we said that Redux reducers must never contain "side effects". A "side effect" is any change to state or behavior that can be seen outside of returning a value from a function. Some common kinds of side effects are things like:
  * Logging a value to the console
  * Saving a file
  * Setting an async timer
  * Making an AJAX HTTP request
  * Modifying some state that exists outside of a function, or mutating arguments to a function
  * Generating random numbers or unique random IDs (such as Math.random() or Date.now())
Redux middleware were designed to enable writing logic that has side effects.

## Redux Async Data Flow
---
ust like with a normal action, we first need to handle a user event in the application, such as a click on a button. Then, we call dispatch(), and pass in something, whether it be a plain action object, a function, or some other value that a middleware can look for.

Once that dispatched value reaches a middleware, it can make an async call, and then dispatch a real action object when the async call completes.


## Using the Redux Thunk Middleware
---
As it turns out, Redux already has an official version of that "async function middleware", called the Redux "Thunk" middleware. The thunk middleware allows us to write functions that get dispatch and getState as arguments. The thunk functions can have any async logic we want inside, and that logic can dispatch actions and read the store state as needed.

---
## Instalation
```
npm install redux-thunk
```

---
## Redux Toolkit
If you're using our official Redux Toolkit package as recommended, there's nothing to install - RTK's configureStore API already adds the thunk middleware by default:
```
import { configureStore } from '@reduxjs/toolkit'

import todosReducer from './features/todos/todosSlice'
import filtersReducer from './features/filters/filtersSlice'

const store = configureStore({
  reducer: {
    todos: todosReducer,
    filters: filtersReducer
  }
})
// The thunk middleware was automatically added
```
---
## Manual Setup
If you're using the basic Redux createStore API and need to set this up manually, first add the redux-thunk package:
```
npm install redux-thunk

yarn add redux-thunk
```
# References
[async actions](https://redux.js.org/tutorials/fundamentals/part-6-async-logic)

[thunk middleware](https://github.com/reduxjs/redux-thunk)

