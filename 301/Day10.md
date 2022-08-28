What is a ‘call’?
ans---)A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions (Links to an external site.) — what function is currently being run and what functions are called from within that function

How many ‘calls’ can happen at once?
ans---) The call stack has a fixed size, depending on the implementation of the host environment, either the web browser or Node.js.

What does LIFO mean?
ans---)The word LIFO stands for Last In First Out

in which we will enter the data elements into the data structure. Here, we will pop out the data elements which are recently added. It means that the last element will be the first to be popped out.

Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
ans---) we start from the left call stack have main then call average then add then execute add execute average then main and call stack empty

![call stack](https://www.javascripttutorial.net/wp-content/uploads/2019/12/JavaScript-Call-Stack.png)
What causes a Stack Overflow?
ans---) In software, a stack overflow occurs if the call stack pointer exceeds the stack bound. The call stack may consist of a limited amount of address space, often determined at the start of the program. The size of the call stack depends on many factors, including the programming language, machine architecture, multi-threading, and amount of available memory. When a program attempts to use more space than is available on the call stack (that is, when it attempts to access memory beyond the call stack's bounds, which is essentially a buffer overflow), the stack is said to overflow, typically resulting in a program crash.

What is a ‘reference error’?
ans---) The ReferenceError object represents an error when a variable that doesn't exist (or hasn't yet been initialized) in the current scope is referenced.

What is a ‘syntax error’?
ans---) a syntax error may be detected during program execution (Links to an external site.), and an interpreter's error messages might not differentiate syntax errors from errors of other kinds.

it is like if I want to solve code challenge and then typing something like console.ahmad that's not js that's will make all my test fail because it is syntax error

What is a ‘range error’?
ans---) The RangeError object indicates an error when a value is not in the set or range of allowed values.

What is a ‘tyep error’?
ans---) The TypeError object represents an error when an operation could not be performed, typically (but not exclusively) when a value is not of the expected type.

What is a breakpoint?
ans---) a breakpoint is an intentional stopping or pausing place in a program, put in place for debugging purposes. It is also sometimes simply referred to as a pause.

More generally, a breakpoint is a means of acquiring knowledge about a program during its execution.

What does the word ‘debugger’ do in your code?
ans---) Debugging is the process of analyzing how your program runs, how it generates data in order to find defects and issues in your code. These errors or defects are referred to as “bugs”, hence the term “debugging.”
