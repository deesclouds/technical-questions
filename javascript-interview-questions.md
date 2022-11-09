# Javascript - Technical Interview Questions 

## Questions:

- [x] Explain event delegation.
- **Explain:** A pattern to handle events efficiently. 
- **Use:** Instead of adding an event listener to each and every similar element, we can add an event listener to a parent element and call an event on a particular target using the . target property of the event object.
- **Example:** Able to hide messages with delegation.

- [x] Explain how this works in Javascript.
- **Explain:** Efficiently handles events within one event listener.
- **Use:**
- **Example:** Create a tree that shows/hides node children on click.

- [x] Explain how prototypal inheritance works?
- **Explain:** Every object with its methods and properties contains an internal and hidden property known as Prototype.
- **Use:** An object can inherit the properties and methods of another object.
- **Example:** 
<!-- using __proto__ to access and set the [[Prototype]] of "anObject"
anObject.__proto__ = someotherObject -->

- [x] What do you think of AMD vs CommonJS?
- **Explain:** AMD(Asynchronous Module Definition) and CommonJS are both Javascript module loader. They accomplish the same task but works different.
- **Use:** Common JS use exports to create exportable/public properties or methods. In AMD, we return any object which we want to make publicly available.
- **Example:**  AMD is better for browser, hence the name "Asynchronous" as it loads each distinct module in async manner instead of loading in one large file. No extra steps needed works out of the box. CommonJS, is a standard, mostly used in servers and it loads modules synchronously, through extra step is required if you want your JS file size to be minified and compressed.

- [x] Explain why the following doesn't work as an IIFE: function foo (){}();. What needs to be changed to properly make it an IIFE?
- **Explain:** An IIFE function is an immediate invoked function expression that doesn't wait for anything to be called. 
- **Use:** avoiding pollution of global execution context and  to make variables private.
- **Example:** hiding our api keys within a new variable and never calling the original variable.
[!mdn][https://developer.mozilla.org/en-US/docs/Glossary/IIFE]
- [x] What's the difference between a variable that is: null, undefined or undeclared? How would you go about checking for any of these states?
- **Explain:** null is pointing to nothing in memory.
 
 undefined is a variable that has not been assigned any value. 
 
 undeclared is a variable that has not been properly declared using const, var, or let.
- **Use:** to determine that state of a variable. we can check the states with using a console.log();
- **Example:**
null
x = null;

undefined
let x
console.log(x + 'test')
// x is undefined

undeclared
testVar = "This is undeclared"
// as opposed to
let testVar = "This is declared"
[!devto][https://dev.to/nashmeyah/undefined-vs-null-vs-undeclared-9f8#:~:text=Null%20is%20pointing%20to%20nothing,const%2C%20var%2C%20or%20let]

- [x] What is a closure, and how/why would you use one?
- **Explain:** Closures is a neat way to deal with scope issues. 
- **Use:** We use closures because JavaScript it a function-level scope issues. Reasons we use closures is because Javascript is a a function-level scope rather than as with other languages, block-level scope and JavaScript is an asynchronous/ event driven language. Example that Closure is frequently used is jQuery (ex.click()).

- **Example:**Its outer function has been executed and has returned a value, closures can still run. Closures store references to the outer function's variable, hence, we will always have access to the updated values of outer function's variables. Since we have access to the updated values of outer function's variables. We will have issue/bus when a variable changes via for loop, but this can be fixed by using IIFE, Immediately Invoked Function Expression.
[!medium][https://rlynjb.medium.com/js-interview-question-what-is-a-closure-and-how-why-would-you-use-one-b6fd45ea95f6]

- [x] Can you describe the main difference between a .forEach loop and a.map() loop and why you would pick one versus the other?
- **Explain:** forEach() - executed a provided function once for each array element
map() - creates a new array with the results of calling a provided function on every element in the calling array
- **Use:** map() executes a functions on each element inside of an array and returns a new array. forEach() executes a function on each element and returns a value of undefined.
- **Example:**
map [!mdn][https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map]
const array1 = [1, 4, 9, 16];

// pass a function to map
const map1 = array1.map(x => x * 2);

console.log(map1);
// expected output: Array [2, 8, 18, 32]

foreach [!mdn][https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach]
[!medium][https://kevbodyworks.medium.com/difference-between-a-foreach-loop-and-a-map-loop-767c936d5737]

- [x] What's a typical use case for anonymous functions?
- **Explain:** it's declared without an identifier
- **Use:** passing an anonymous function to other function as its argument. in order to invoke and execute a function immediately after its declaration, creating an anonymous function is the best way.
- **Example:**
setTimeout(function () {  
    console.log('Execute later after 1 second')  
}, 1000);  

- [x] How do you organize your code? (module pattern, classical inheritance?)
- **Explain:**
- **Use:**
- **Example:**

- [x] What's the difference between host objects and native objects?
- **Explain:**
- **Use:**
- **Example:**

- [x] Difference between: function Person(){}, var person = Person(), and var person = new Person()?
- **Explain:**
- **Use:**
- **Example:**

- [x] What's the difference between .call and .apply?
- **Explain:**
- **Use:**
- **Example:**

- [x] Explain Function.prototype.bind.
- **Explain:**
- **Use:**
- **Example:**

- [x] When would you use document.write()?
- **Explain:**
- **Use:**
- **Example:**

- [x] What's the difference between feature detection,feature inference, and using the UA string?
- **Explain:**
- **Use:**
- **Example:**

- [x] Explain Ajax in as much detail as possible.
- **Explain:**
- **Use:**
- **Example:**

- [x] What are the advantages and disadvantages of using Ajax?
- **Explain:**
- **Use:**
- **Example:**

- [x] Explain how JSONP works (and how it;s not really Ajax).
- **Explain:**
- **Use:**
- **Example:**

- [x] Have you ever used JavaScript templating? If so, what libraries have you used?
- **Explain:**
- **Use:**
- **Example:**

- [x] Explain "hoisting"?
- **Explain:**
- **Use:**
- **Example:**

- [x] Describe event bubbling.
- **Explain:**
- **Use:**
- **Example:**

- [x] What's the difference between an "attribute" and a property?
- **Explain:**
- **Use:**
- **Example:**

- [x] Why is extending built-in JavaScript objects not a good idea?
- **Explain:**
- **Use:**
- **Example:**

- [x] Difference between document load event and document DOMContentLoaded event?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is the difference between == and ===?
- **Explain:** These both are comparison operators. 
- **Use:** The one with two equal signs are for value and the three equal signs are used for value and type.
- **Example:** 3 == '3' would return True 3 === '3' would return false

- [x] Explain the same-origin policy with regards to Javascript.
- **Explain:**
- **Use:**
- **Example:**

- [x] Make this work: duplicate ([1,2,3,4,5]); //[1,2,3,4,5,1,2,3,4,5]
- **Explain:**
- **Use:**
- **Example:**

- [x] Why is it called a Ternary expression, what does the word "Ternary" indicate?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is "use strict";? what are the advantages and disadvantages to using it?
- **Explain:**
- **Use:**
- **Example:**

- [x] Create a for loop that iterates up to 100 while outputting "fizz" at multiples of 3, "buzz" at multiples of 5 and "fizzbuzz" at multiples of 3 and 5
- **Explain:**
- **Use:**
- **Example:**

- [x] Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
- **Explain:**
- **Use:**
- **Example:**

- [x] Why would you use something like the load event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
- **Explain:**
- **Use:**
- **Example:**

- [x] Explain what a single page app is and how to make one SEO-friendly.
- **Explain:**
- **Use:**
- **Example:**

- [x] What is the extent of your experience with Promises and/or their polyfills?
- **Explain:**
- **Use:**
- **Example:**

- [x] What are the pros and cons of using Promises instead of callbacks?
- **Explain:**
- **Use:**
- **Example:**

- [x] What are some of the advantages/disadvantages of writing Javascript code in a language that compiles to JavaScript?
- **Explain:**
- **Use:**
- **Example:**

- [x] What tools and techniques do you use debugging Javascript code?
- **Explain:**
- **Use:**
- **Example:**

- [x] What language constructions do you use for iterating over object properties and array items?
- **Explain:**
- **Use:**
- **Example:**

- [x] Explain the difference between mutable and immutable objects.
- **Explain:**
- **Use:**
- **Example:**

- [x] Explain the difference between synchronous and asycnhronous functions.
- **Explain:**
- **Use:**
- **Example:**

- [x] What is an event loop? What is the difference between call stack and task queue?
- **Explain:**
- **Use:**
- **Example:**

- [x] Explain the differences on the usage of foo between function foo(){} and var foo = function (){}
- **Explain:**
- **Use:**
- **Example:**

- [x] What are the differences between variables created using let, var or const?
- **Explain:**
- **Use:**
- **Example:**

- [x] What are the differences between ES6 class and ES5 function constructors?
- **Explain:**
- **Use:**
- **Example:**

- [x] Can you offer a use case for the new arrow => function syntax? How does this new syntax differ from other functions?
- **Explain:**
- **Use:**
- **Example:**

- [x] What advantage is there for using the arrow syntax for a method in a constructor?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is the definition of a higher-order function?
- **Explain:**
- **Use:**
- **Example:**

- [x] Can you give an example for destructuring an object or an array?
- **Explain:**
- **Use:**
- **Example:**

- [x] ES6 Template Literals offer a lot of flexibility in generating strings, can you give an example?
- **Explain:**
- **Use:**
- **Example:**

- [x] Can you give an example of a curry function and why this syntax offers an advantage?
- **Explain:**
- **Use:**
- **Example:**

- [x] What are the benefits of using spread syntax and how is it differenct from rest syntax?
- **Explain:**
- **Use:**
- **Example:**

- [x] How can you share code between files?
- **Explain:**
- **Use:**
- **Example:**

- [x] Why you migh want to create static class members?
- **Explain:**
- **Use:**
- **Example:**

### General Questions

- [x] Can you name two programming paradigms important for JavaScript app developers?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is functional programming?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is the difference between classical inheritance and prototypal inheritance?
- **Explain:**
- **Use:**
- **Example:**

- [x] What are the pros and cons of functional programming vs object-oriented programming?
- **Explain:**
- **Use:**
- **Example:**

- [x] What are two-way data binding and one-way data flow, and how are they different?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is asynchronous programming, and why is it important in JavaScript?
- **Explain:**
- **Use:**
- **Example:**
