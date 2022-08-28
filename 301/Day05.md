1Q) What is the single responsibility principle and how does it

ans--- that is, a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

Q2) What does it mean to build a ‘static’ version of your application?

ans--- static version requires a lot of typing and no thinking, and adding interactivity requires a lot of thinking and not a lot of typing. We’ll see why.

Q3) Once you have a static application, what do you need to add?

ans--- o build a static version of your app that renders your data model, you’ll want to build components that reuse other components and pass data using props. props are a way of passing data from parent to child. If you’re familiar with the concept of state, don’t use state at all to build this static version. State is reserved only for interactivity, that is, data that changes over time. Since this is a static version of the app, you don’t need it.

Q4) What are the three questions you can ask to determine if something is state?

ans---

Is it passed in from a parent via props? If so, it probably isn’t state.
Does it remain unchanged over time? If so, it probably isn’t state.
Can you compute it based on any other state or props in your component? If so, it isn’t state.

Q- ) How can you identify where state needs to live?

Identify every component that renders something based on that state.
Find a common owner component (a single component above all the components that need the state in the hierarchy).
Either the common owner or another component higher up in the hierarchy should own the state.
If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.
Q-). What is a “higher-order function”?

ans--- Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions

Q-) Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?

ans--- is the m more then the n the n here is the argument that pass in the function

and the m is the argumant in the arrow function

Q-) Explain how either map or reduce operates, with regards to higher-order functions.

ans--- The map method transforms an array by applying a function to all of its elements and building a new array from the returned values.

the reduce : to compute a single value from them
