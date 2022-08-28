Q-What is a ‘Controlled Component’?

ans---take data from the user In HTML, form elements such as <input>, <textarea>, and <select> in React, mutable state is typically kept in the state property of components, and only updated with setState() (Links to an external site.).

We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.

Q-Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.

ans---In HTML, an <input type="file"> lets the user choose one or more files from their device storage to be uploaded to a server or manipulated by JavaScript via the File API (Links to an external site.).

why ? Because its value is read-only, it is an uncontrolled component in React. It is discussed together with other uncontrolled components later in the documentation (Links to an external site.).

Q.How do we target what the user is entering if we have an event handler on an input field?

ans---Specifying the value prop on a controlled component (Links to an external site.) prevents the user from changing the input unless you desire so. If you’ve specified a value but the input is still editable, you may have accidentally set value to undefined or null.

The following code demonstrates this. (The input is locked at first but becomes editable after a short delay.)

Q.Why would we use a ternary operator?

ans---it is easier and it is just one line of code and we can just change the variable accordingly

Q.Rewrite the following statement using a ternary statement:

if(x===y){
console.log(true);
} else {
console.log(false);
}
ans--- x===y ? true: false;
