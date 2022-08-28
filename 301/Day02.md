1---Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?

the render first and then the componentDidMount.

2---What is the very first thing to happen in the lifecycle of React?

instance of a component is being created and inserted into the DOM it occurs during the mounting phase. Constructor, static

3---Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates

constructor, render, componentDidMount, componentWillUnmount, all will happen in the mounting phase then React Updates.

4---What does componentDidMount do?

This method is invoked immediately after a component is mounted. If you need to load anything using a network request or initialize the DOM, it should go here. This method is a good place to set up any subscriptions.

1---What types of things can you pass in the props?

data

2---What is the big difference between props and state?

State: The state represents parts of an Application that can change. Each component can have its State. The state is Mutable and It is local to the component only.

Props: Props are known as properties it can be used to pass data from one component to another. Props cannot be modified, read-only, and Immutable.

3---When do we re-render our application?

The render function should not modify the component state because it would cause a lot of bugs by changing the state every time it rerenders

4---What are some examples of things that we could store in state?

current counter and updating it
