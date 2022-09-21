### What's the difference between Stack and Queue?

stack: is The stack is based on LIFO(Last In First Out) principle

The queue is based on FIFO(First In First Out) principle.

stack: Insertion Operation is called Push Operation

Insertion Operation is called Enqueue Operation

stack :Deletion Operation is called Pop Operation

Deletion Operation is called Dequeue Operation

stack: Push and Pop Operation takes place from one end of the stack

Enqueue and Dequeue Operation takes place from a different end of the queue

stack: The most accessible element is called Top and the least accessible is called the Bottom of the stack

The insertion end is called Rear End and the deletion end is called the Front End.

stack: Simple Implementation

Complex implementation in comparison to stack

stack: Only one pointer is used for performing operations

Two pointers are used to perform operations

stack: Empty condition is checked using Top==-1

Empty condition is checked using  Front==-1||Front==Rear+1

stack: Full condition is checked using Top==Max-1

Full condition is checked using  Rear==Max-1

stack: There are no variants available for stack

There are three types of variants i.e circular queue, double-ended queue and priority queue

stack: Can be considered as a vertical collection visual

Can be considered as a horizontal collection  visual

stack: Used to solve the recursive type problems

Used to solve the problem having sequential processing

### What is Stacks and how to use it?

const stack = function() {
this.count = 0;
this.data = {};

// Puts an element into the Stack
this.push = function(element) {
this.data[this.count] = element;
this.count++;
}
}

stacks is linear data structures that allow operations only on one end, meaning that all basic operations like insertion can only be done at the ends of the structure.

A common real-life example is a stack of plates where you can add or remove from it, which explains Stacks to a 5-year-old.

Browsers use the Stack data structure as well to keep records of your browsing history where the last visit is the first on the record. So, if you use the back button you then go to the last visited site.

### What is Queue?

This data structure is exactly what it means in a real-world application. It follows the pattern that whatever goes in first will go out first.

The data is inserted through the rear/tail of the structure while removing data only happens at the front/head of the structure.
