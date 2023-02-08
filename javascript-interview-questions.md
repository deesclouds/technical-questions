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
In the past, I've used Backbone for my models which encourages a more OOP approach, creating Backbone models and attaching methods to them.

The module pattern is still great, but these days, I use React/Redux which utilize a single-directional data flow based on Flux architecture. I would represent my app's models using plain objects and write utility pure functions to manipulate these objects. State is manipulated using actions and reducers like in any other Redux application.

I avoid using classical inheritance where possible. When and if I do, I stick to these rules.

- [x] What's the difference between host objects and native objects?
The differences between host objects and native objects:

-Native objects are built-in objects that are part of the JavaScript language defined by the ECMAScript specification, such as String, Math, RegExp, Object, Function, etc.

Host objects are provided by the runtime environment (browser or Node), such as window, XMLHTTPRequest, etc.

References
https://stackoverflow.com/questions/7614317/what-is-the-difference-between-native-objects-and-host-objects

- [x] Difference between: function Person(){}, var person = Person(), and var person = new Person()?

- **Explain:**
function Person() {}
Declares (instantiates) a named function in memory, but does not execute it. This function can be called at a later point with the code Person(); . An important not here is that declared functions are available for use even before they are declared (as long as they are eventually declared).

var person = Person()

Declares a new function, Person, invokes it and then assigns the return value to the variable person. Important to understand here is that the variable is first hoisted to the top of the current scope and then when the assignment is encountered in the flow of code, the function Person is run and the result assigned. Until that point, the value of person is undefined.

var person = new Person()

In this case, we have the introduction of the new keyword which means that Person is an object constructor function which returns a new object instance. So while person in the example above is the returned value of Person (a string, number or whatever), the value of person in this example is actually an object.

- [x] What's the difference between .call and .apply?

The difference between .call and .apply is that the call() method takes arguments separately, while the apply() method takes arguments as an array[1][2]. This makes apply() very handy if you want to use an array instead of an argument list[1]. Both methods invoke a function with a specified this context and optional arguments[3], but the only difference between them is that call() passes all arguments after the first one on to the invoked function, while apply() takes an array of arguments[4][5].

- [x] Explain Function.prototype.bind.

The bind() method on the Function.prototype creates a new function that, when called, has its this keyword set to the provided value, with a given sequence of arguments preceding any provided when the new function is called[1]. It allows you to create a new function from an existing function and pre-configure its arguments[2][3]. The bind() method can take any number of arguments and return a new function[4]. It is useful for understanding how 'this' keyword works in JavaScript[5].

- [x] When would you use document.write()?

The document.write() method is mostly used for testing purposes and to delete all the content from the HTML document and insert new content[1]. It can also be used to write a string of text to a document stream opened by document.open()[2]. The only appropriate usage for document.write() is when working with third parties like Google Analytics and such for including their scripts[3][4], as it is always available (mostly) and is a convenient way to include code[4]. However, it is considered a "bad practice" as it is mostly used to write content to the screen as soon as that content is needed, which means it happens anywhere, either in a JavaScript or an HTML file[5].

- [x] What's the difference between feature detection,feature inference, and using the UA string?

The difference between feature detection, feature inference, and using the user agent string is that feature detection involves checking for the presence of a specific feature or API[1][2], while feature inference assumes that because one feature exists, another will also exist[1][2]. Using the user agent string involves identifying which browser is being used by examining its string[3][4][5].

- [x] Explain Ajax in as much detail as possible.

Asynchronous JavaScript and XML (AJAX) is a programmatic technique that utilizes JavaScript and the XMLHTTPRequest object to exchange data between a web browser and a web server[1]. It is nearly synonymous with web 2.0 applications and is used to enhance the interactivity of webpages[1]. AJAX combines several programming tools, including HTML, CSS, JavaScript, DOM, XML, JSON, and the XMLHttpRequest object[2][3][4]. It is a client-sided web development technique that is used to produce interactive Web applications[5].

- [x] What are the advantages and disadvantages of using Ajax?

The advantages of using AJAX include improved performance and usability for web applications[1][2][3], platform independence[2], and the ability to render with no data[2][3]. Disadvantages include the need for a strong knowledge of JavaScript[4] and the potential for increased complexity in development[5].

- [x] Explain how JSONP works (and how it's not really Ajax).

JSONP (JSON with Padding) is a way of requesting an external script from another domain, allowing data to be exchanged between domains despite the cross-domain policy[1]. It is essentially JSON with extra code, like a function call wrapped around the data[2]. This differs from AJAX (Asynchronous JavaScript and XML), which is a programmatic technique that utilizes JavaScript and the XMLHTTPRequest object to exchange data between a web browser and a web server[3][4][5].

- [x] Have you ever used JavaScript templating? If so, what libraries have you used?

Yes I've used EJS, Mustache.js. 

- [x] Explain "hoisting"?

In JavaScript, hoisting is the default behavior of moving all declarations to the top of the current scope (to the top of the current script or the current function) prior to code execution[1][2][3][4][5]. This allows functions and variables to be used before they are declared.

- [x] Describe event bubbling.

Event bubbling is a method of event propagation in the HTML DOM API when an event is in an element inside another element, and both elements receive the event[1][2]. It occurs when an element receives an event and it bubbles up to its parent and ancestor elements in the DOM tree until it reaches the root element[3]. Event bubbling is also known as event propagation[4], and it is indicated by the bubbles read-only property of the Event interface[5].

- [x] What's the difference between an "attribute" and a property?

In JavaScript (the DOM), an element has attributes and properties[1][2][3][4][5]. Attributes are defined by HTML and their value is constant, while properties are defined by the DOM and their value is variable[3]. When the browser loads the page, it parses the HTML and generates DOM objects from it[4]. In most cases, using properties is preferable[5].

- [x] Why is extending built-in JavaScript objects not a good idea?

Extending built-in JavaScript objects is not recommended because it can lead to unexpected behavior and potential conflicts with future browser implementations[1][2]. Additionally, some functionality should not be extended or overridden[3], as extending built-in classes can cause non-static methods to be inherited[4]. Finally, extending the DOM/built-in object prototypes is a bad idea because exposure of "prototype objects" is not part of any specification[5].

- [x] Difference between document load event and document DOMContentLoaded event?
The DOMContentLoaded event is fired when the initial HTML document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading[1][4]. This event does not wait for all resources such as images to finish loading[2][3]. In contrast, the load event fires when all files have finished loading from all resources, including ads and images[2]. The load event on window triggers when the page and all resources are loaded[5].

- [x] What is the difference between == and ===?
- **Explain:** These both are comparison operators. 
- **Use:** The one with two equal signs are for value and the three equal signs are used for value and type.
- **Example:** 3 == '3' would return True 3 === '3' would return false

- [x] Explain the same-origin policy with regards to Javascript.
The same-origin policy is a browser security feature that restricts how documents and scripts on one origin can interact with resources on another origin[1][2][3][4]. It helps isolate potentially malicious documents, reducing possible attack vectors[1], and generally controls the access that JavaScript code has to content that is loaded cross-domain[5].

- [x] Make this work: duplicate ([1,2,3,4,5]); //[1,2,3,4,5,1,2,3,4,5]
There are a couple of ways to duplicate elements in a JavaScript array, such as using the forEach or for loop[1], or using the map method[2][3]. The map method returns a new array with each element being the result of the callback function, which can be used to return the original element and thus duplicate it[2].

```
function duplicate(arr) {
  return arr.concat(arr);
}
```

- [x] Why is it called a Ternary expression, what does the word "Ternary" indicate?
A ternary expression is a type of operator that takes three operands and evaluates a condition, returning one value if the condition is true and another value if the condition is false[1][2].

- [x] What is "use strict";? what are the advantages and disadvantages to using it?

"use strict"; is a directive in JavaScript that enables strict mode, which is a reduced and safer feature set of the language[1][2]. Benefits of using 'use strict' include eliminating some JavaScript silent errors by changing them to throw errors, preventing bad coding, and allowing scripts to run faster[3][4][5]. An example of using "use strict" is putting it at the top of a code or function[3].

- [x] Create a for loop that iterates up to 100 while outputting "fizz" at multiples of 3, "buzz" at multiples of 5 and "fizzbuzz" at multiples of 3 and 5

for (let i = 1; i <= 100; i++) {
  if (i % 3 === 0 && i % 5 === 0) {
    console.log("fizzbuzz");
  } else if (i % 3 === 0) {
    console.log("fizz");
  } else if (i % 5 === 0) {
    console.log("buzz");
  } else {
    console.log(i);
  }
} 

- [x] Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?

Modifying the global scope of a website is generally considered bad practice because it can lead to memory issues, accidental overwriting of variables, and difficulty in debugging[1][2]. Additionally, global variables can be difficult to keep track of and can cause confusion when multiple developers are working on the same project[3][4]. To avoid these issues, developers should strive to limit the number of global variables and functions used in their code[5].

- [x] Why would you use something like the load event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?

The load event in JavaScript fires at the end of the document loading process[1], and is useful for executing code after a page has finished loading. However, it has the disadvantage of not being able to detect if an image or other resource fails to load[2][3]. Alternatives to the load event include using the DOMContentLoaded event, which fires when the initial HTML document has been completely loaded and parsed, but does not wait for resources like images and stylesheets to finish loading[3].

- [x] Explain what a single page app is and how to make one SEO-friendly.

Single-Page Applications (SPAs) are web applications relying on JavaScript to dynamically add content to pages users visit[1]. SEO for SPAs requires covering all code paths, treating views as URLs, optimizing titles and descriptions for each view, and improving how the application is crawled by search engines[2][3][4][5]. Google has also shared tips for optimizing SPAs for search engine visibility[4].

- [x] What is the extent of your experience with Promises and/or their polyfills?

I have experience with Promises and their polyfills, including writing a basic polyfill for the Promise API in JS[1]. I understand the pros and cons of using Promises instead of callbacks, such as improved readability and error handling[2]. I am also familiar with popular polyfills such as Native Promise Only[3] and Javascript Promise Methods with Polyfill Example[4]

- [x] What are the pros and cons of using Promises instead of callbacks?

The main advantages of using promises instead of callbacks are better defined and organized control flow of asynchronous logic, reduced coupling, composability, and the ability to wait for only one promise to resolve[1][2][3][4]. Promises also provide an object to decide the action that needs to be taken after the async task completes[5]. However, promises are just syntactic sugar and everything that can be done with promises can also be done with callbacks[4].

- [x] What are some of the advantages/disadvantages of writing Javascript code in a language that compiles to JavaScript?

Writing JavaScript code in a language that compiles to JavaScript has several advantages, such as speed and ease of reading and writing cross-browser code[1][2]. However, there are also some disadvantages, such as client-side security issues[3], browser support issues[2], lack of debugging facility[4], single inheritance[4], sluggish bitwise function[4], and more[5].

- [x] What tools and techniques do you use debugging Javascript code?

There are several tools and techniques for debugging JavaScript code, such as Google Dev Tools, React Dev Tools, Node Inspect, Postman and Webpack[1], as well as the console.log() method, setting breakpoints, and the debugger keyword[2][3]. Additionally, there are various debugging techniques that can be used to enhance efficient running of codes or programs in JavaScript[4].

- [x] What language constructions do you use for iterating over object properties and array items?

Common language constructions for iterating over object properties and array items include for loops, for..in, for each..in, map, reduce[1][2], and the for...in loop[3][4][5].

- [x] Explain the difference between mutable and immutable objects.
311
In Python, mutable objects are those whose value can be changed over time[1]
312
, while immutable objects are those whose value cannot be changed once they are created
313
. Examples of mutable objects include lists and dictionaries, while strings and tuples are examples of immutable objects

- [x] Explain the difference between synchronous and asycnhronous functions.

Synchronous functions execute code in a particular sequence, while asynchronous functions allow for the execution of upcoming instructions immediately[1][2][3]. Asynchronous programming allows for multiple requests to be performed simultaneously and tasks to be completed faster[4][5].

- [x] What is an event loop? What is the difference between call stack and task queue?
The Call Stack is a built-in component of the JavaScript runtime[1][2], while the Task/Event Queue is a component of the browser[1]. The Event Loop's job is to move stuff out from the callback queue and back onto the call stack when it is empty[2][3]. The Event Loop has responsibility to see if the call-stack is empty and if there are pending tasks in the task queue to process[4][5].

- [x] Explain the differences on the usage of foo between function foo(){} and var foo = function (){}
The difference between function foo(){} and var foo = function (){} is that the former is a function declaration while the latter is a function expression[1][2][3][4]. Function declarations have their body hoisted but function expressions do not[4].

- [x] What are the differences between variables created using let, var or const?

var: Variables declared with var are function scoped, which means they are accessible within the function they are declared in. If a variable is declared with var inside a block, it is hoisted to the top of the function and can be accessed before its declaration. This can lead to unexpected behavior.

let: Variables declared with let are block scoped, which means they are only accessible within the block they are declared in. If a variable is declared with let inside a block, it is not hoisted to the top of the function and cannot be accessed before its declaration.

const: Variables declared with const are also block scoped, and their value cannot be reassigned after they are declared. However, the properties of an object declared with const can be modified.

In summary, let and const are preferred over var for declaring variables in modern JavaScript, due to their block scoping and the ability to prevent accidental reassignment of values.

- [x] What are the differences between ES6 class and ES5 function constructors?

The main difference between ES6 class and ES5 function constructors is that ES6 class allows developers to instantiate objects using the new operator[1][2][3][4], while ES5 function constructors create objects by adding functions to their prototypes (Blueprint)[1]. Additionally, ES6 classes have the ability to subclass native classes like Array[5].

- [x] Can you offer a use case for the new arrow => function syntax? How does this new syntax differ from other functions?

Arrow functions are a more concise syntax for writing functions compared to regular functions[1][2][3][4][5]. The main differences between arrow and regular functions include the lack of an arguments keyword in arrow functions[3], the inability to use the 'new' keyword with arrow functions[2], and the fact that arrow functions do not have their own this value[5]. Arrow functions are often used when writing callbacks or higher-order functions[4].

- [x] What advantage is there for using the arrow syntax for a method in a constructor?

The advantage of arrow syntax in constructor methods is that it reduces code and makes the code more readable[1], while also providing a compact alternative to traditional function expressions[2]. However, arrow functions cannot be used as constructors[3][4].

- [x] What is the definition of a higher-order function?

A higher-order function is a function that takes one or more functions as arguments or returns a function[1][2][3][4][5]. They are often used in functional programming[4] and can perform operations on other functions[3].

- [x] Can you give an example for destructuring an object or an array?

Destructuring is a JavaScript expression that makes it possible to unpack values from arrays or properties from objects into distinct variables[1][2]. For example, to extract the values of an object prior to ES6, one would have to use the syntax `var first = obj.first`[3]. With destructuring, this can be simplified to `let {first} = obj`[4]. Similarly, for an array, one could use `let studentsArr = [John, Jane]` and then destructure it with `let [John, Jane] = studentsArr`[5].

- [x] ES6 Template Literals offer a lot of flexibility in generating strings, can you give an example?

Template literals, also known as template strings, are a new feature introduced in ECMAScript 2015/ ES6[1][2]. They provide an easy way to interpolate variables and expressions into strings[3][4] and create multiline strings[1][5]. Template literals are enclosed by backtick (`) characters instead of double or single quotes[2][4].

- [x] Can you give an example of a curry function and why this syntax offers an advantage?

An example of a curried function in JavaScript is `const add = x => y => x + y`[1]. Currying helps to make code more concise and readable by avoiding the need to pass the same parameters multiple times[2][3][4][5]. It also allows for partial application of functions, which can be useful when dealing with complex data structures[1].

- [x] What are the benefits of using spread syntax and how is it difference from rest syntax?

The spread syntax expands the elements of an array or object into individual variables, while rest syntax condenses multiple elements into a single element[1][2][3]. Spread syntax is useful for copying arrays and objects, as well as combining them[1][2]. Rest syntax is useful for gathering the rest of the list of arguments into an array[4].

- [x] How can you share code between files?

To share code between files in JavaScript, create an ES6 module in a service component and export the variables or functions that you want to share using standard JavaScript syntax[1][2]. Other ways to share code include using Bit, NPM packages, a single shared NPM library, a multi-package repository, or a monorepo[3][4].

- [x] Why you might want to create static class members?

Static class members in JavaScript are useful for creating fields that exist only once per class, not on every instance of the class[1][2]. They can also be used for utility functions and caches[3], as well as for defining methods on the class itself that cannot be called on an object[4][5].

### General Questions

- [x] Can you name two programming paradigms important for JavaScript app developers?

The two programming paradigms important for JavaScript app developers are object-oriented programming and functional programming[1][2][3][4][5]. Other paradigms include imperative/procedural programming, declarative programming, and event-driven programming[5].

- [x] What is functional programming?

Functional programming in JavaScript is a sub-paradigm of the Declarative programming paradigm, where functions are treated as first-class citizens[1][2][3][4][5]. It involves writing code without mutating state and data[1], and allows for passing functions as values[3]. Examples of functional programming in JavaScript include passing functions as arguments to other functions, using higher order functions, and using recursion[5].

- [x] What is the difference between classical inheritance and prototypal inheritance?

In classical inheritance, objects are organized into classes and subclasses, while in prototypal inheritance, objects are cloned and extended from a prototype object[1]. Classical inheritance deals with generalizations (like the overarching Shoe concept) as other objects[2], while prototypal inheritance deals with objects as abstractions of real-world entities[3][4]. In JavaScript, prototypal inheritance is implemented through prototype delegation, which is a built-in language feature[5].

- [x] What are the pros and cons of functional programming vs object-oriented programming?

Functional programming and object-oriented programming are two different paradigms of programming, each with its own advantages and disadvantages. Object-oriented programming (OOP) is procedural programming that uses classes to group code and data together for reusability and simplicity[1], while functional programming (FP) is a declarative programming model that emphasizes the importance of functions over data[2]. OOP works great when the behaviors are fixed but the data types change[3], while FP is a better option when all the objects are clear but the behaviors vary[3]. OOP languages allow developers to establish multiple degrees of visibility for properties and methods, such as private or public[4], while FP does not give importance to data but to functions[2].

- [x] What are two-way data binding and one-way data flow, and how are they different?

Two-way data binding is a technique that allows information to flow in both directions, from the view to the component's logic and vice versa[1][2]. This is in contrast to one-way data binding, which only allows information to flow in one direction, from the component's logic to the view[3][4]. An example of two-way data binding in JavaScript is when a user changes an input field and the change is reflected in the application state[5].

- [x] What is asynchronous programming, and why is it important in JavaScript?

Asynchronous programming in JavaScript enables programs to start long-running tasks and still be able to respond to other events while the task runs[1][2]. This is done through callback functions, promises, and async and await[3][4][5], which allow programs to execute code in the background without blocking the main thread. An example of this is a program that fetches two resources from the network and then combines them[3].
