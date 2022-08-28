1----What does .map() return?  

The map() method in JavaScript creates an array by calling a specific function on each element present in the parent array. It is a non-mutating method. Generally map() method is used to iterate over an array and calling function on every element of array.

2---If I want to loop through an array and display each value in JSX, how do I do that in React?

The map() method is the most commonly used function to iterate over an array of data in JSX. You can attach the map() method to the array and pass a callback function that gets called for each iteration. When rendering the User component, pass a unique value to the key prop. The key prop helps React keep track of JSX elements and identify any changes in the array.

3---Each list item needs a unique ____.

Keys Must Only Be Unique Among Siblings
4---What is the purpose of a key?

Keys serve as a hint to React but they don’t get passed to your components

----------------------------------------------------------------------------------------

1---What is the spread operator?

The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.
-------------------

2---List 4 things that the spread operator can do.
-Spread in array literals
-Copy an array
-Spread in object literals
Apply for new operator
-------------------

3---Give an example of using the spread operator to combine two arrays.

const arr1 = [1,2,3]
const arr2 = [4,5,6]
const arr3 = [...arr1, ...arr2] //arr3 ==> [1,2,3,4,5,6]

let fruits = ["apples", "bananas"];
let vegetables = ["corn", "carrots"];
let produce = [...fruits, ...vegetables];

------------------

4---Give an example of using the spread operator to add a new item to an array.

function sum(x, y, z) {
  return x + y + z;
}

const numbers = [1, 2, 3];

console.log(sum(...numbers));
// expected output: 6

console.log(sum.apply(null, numbers));
// expected output: 6

---------------------

5---Give an example of using the spread operator to combine two objects into one.

let person = {
    firstName: 'John',
    lastName: 'Doe',
    age: 25,
    ssn: '123-456-2356'
};


let job = {
    jobTitle: 'JavaScript Developer',
    location: 'USA'
};

let employee = {
    ...person,
    ...job
};

console.log(employee);

----------------------------------------------------------------------------

1---In the video, what is the first step that the developer does to pass functions between components?

(name) and it refer to the object 

2---In your own words, what does the increment function do?

when the click on person method happen the increment with target the increment function 