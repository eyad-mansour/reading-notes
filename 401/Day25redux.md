# redux ToolKit

Redux Toolkit is our official, opinionated, batteries-included toolset for efficient Redux development.
It includes several utility functions that simplify the most common Redux use cases, including store setup, defining reducers, immutable update logic, and even creating entire "slices" of state at once without writing any action creators or action types by hand.

#### Installation​

```
npm install @reduxjs/toolkit
```

### why you should use Redux ToolKit

Redux Toolkit makes it easier to write good Redux applications and speeds up development, by baking in our recommended best practices, providing good default behaviors, catching mistakes, and allowing you to write simpler code. Redux Toolkit is beneficial to all Redux users regardless of skill level or experience. It can be added at the start of a new project, or used as part of an incremental migration in an existing project.

## Note: that you are not required to use Redux Toolkit to use Redux.

### What's Included​

- configureStore(): wraps createStore to provide simplified configuration options and good defaults.

- createReducer(): that lets you supply a lookup table of action types to case reducer functions, rather than writing switch statements. In addition, it automatically uses the immer library to let you write simpler immutable updates with normal mutative code.

- createAction(): generates an action creator function for the given action type string. The function itself has toString() defined, so that it can be used in place of the type constant.

- createSlice(): accepts an object of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types.

- createAsyncThunk: accepts an action type string and a function that returns a promise, and generates a thunk that dispatches pending/fulfilled/rejected action types based on that promise

- createEntityAdapter: generates a set of reusable reducers and selectors to manage normalized data in the store

- The createSelector utility from the Reselect library, re-exported for ease of use.

---

### What is createSlice in Redux Toolkit?

createSlice is a higher order function that accepts an initial state, an object full of reducer functions and a slice name. It automatically generates action creators and action types that correspond to the reducers and state.

In Redux-Toolkit, the createSlice method helps us create a slice of the redux-store. This function aims to reduce the boilerplate required to add data to redux in the canonical way. Internally, it uses createAction and createReducer.

- The initial state value for this slice of state.
  This may also be a "lazy initializer" function, which should return an initial state value when called. This will be used whenever the reducer is called with undefined as its state value, and is primarily useful for cases like reading initial state from localStorage.
- reducers
  An object containing Redux "case reducer" functions (functions intended to handle a specific action type, equivalent to a single case statement in a switch).

---

### extraReducers

One of the key concepts of Redux is that each slice reducer "owns" its slice of state, and that many slice reducers can independently respond to the same action type. extraReducers allows createSlice to respond to other action types besides the types it has generated.

As case reducers specified with extraReducers are meant to reference "external" actions, they will not have actions generated in slice.actions.

As with reducers, these case reducers will also be passed to createReducer and may "mutate" their state safely.

If two fields from reducers and extraReducers happen to end up with the same action type string, the function from reducers will be used to handle that action type.

---

### The extraReducers "builder callback" notation​

The recommended way of using extraReducers is to use a callback that receives a ActionReducerMapBuilder instance.

---

### The extraReducers "map object" notation

Like reducers, extraReducers can be an object containing Redux case reducer functions. However, the keys should be other Redux string action type constants, and createSlice will not auto-generate action types or action creators for reducers included in this parameter.
