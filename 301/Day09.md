1- What is functional programming?
ans--) Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data

What is a pure function and how do we know if something is a pure function?
ans--)The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts

What are the benefits of a pure function?
ans--)A simple example would be a function to receive a collection of numbers and expect it to increment each element of this collection.

What is immutability?
ans---) Unchanging over time or unable to be changed.

What is Referential transparency?
ans---) Basically, if a function consistently yields the same result for the same input, it is referentially transparent.

pure functions + immutable data = referential transparency

With this concept, a cool thing we can do is to memoize the function.

What is a module?
ans---) module is just another js file just to make your code easier to read and to refactor like component in react

What does the word ‘require’ do?
ans ---) it is for connecting other module in the app.js or main it I like import in react

How do we bring another module into the file the we are working in?
ans---) we require the module inside the app.js and then we exported from the module

What do we have to do to make a module available?
ans---) we need to make a call to the variable in the module we need to call with require in the main and export in the variable
