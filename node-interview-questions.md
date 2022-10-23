# Node - Interview Questions

## Questions: 

- [x] What is Node.js? Where can you use it?
- **Explain:** Node is open source server environment.
- **Use:** Build fast and scalable server-side and networking applications.
- **Example:**Node.js uses JavaScript on the server.

- [x] Why use Node.js?
- **Explain:** Node.js can create, open, read, write, delete, and close files on the server. 
- **Use:**
- **Example:**

- [x] What are the features of Node.js?
- **Explain:**easy, scalable, speed, packages, strong backend, multi-platform and maintainable

Easy—Node.js is quite easy to start with. It’s a go-to choice for web development beginners. With a lot of tutorials and a large community—getting started is very easy.
Scalable—It provides vast scalability for applications. Node.js, being single-threaded, is capable of handling a huge number of simultaneous connections with high throughput.
Speed—Non-blocking thread execution makes Node.js even faster and more efficient.
Packages—A vast set of open-source Node.js packages is available that can simplify your work. There are more than one million packages in the NPM ecosystem today.
Strong backend—Node.js is written in C and C++, which makes it speedy and adds features like networking support.
Multi-platform—Cross-platform support allows you to create SaaS websites, desktop apps, and even mobile apps, all using Node.js.
Maintainable—Node.js is an easy choice for developers since both the frontend and backend can be managed with JavaScript as a single language.
- **Use:**
- **Example:**

- [x] How do you upgrade NPM to a new version in Node.js?
- **Explain:** npm install -g npm @ latest
- **Use:** 
- **Example:**

- [x] Why is Node.js Single-threaded?
- **Explain:** Node's built-in asynchronous I/O operations are more efficient than workers can be. Having said that each thread will use the same Node.js architecture which is single threaded based.
- **Use:**
- **Example:**

- [x] Explain callback in Node.js.
- **Explain:** The callback function is called after a task is completed
- **Use:** Helps in preventing any kind of blocking and a callback function allows other code to run in the meantime.
- **Example:** Callback is called when a task completes and is asynchronous equivalent for a function.

- [x] What is callback hell in Node.js?
- **Explain:** Callback Hell is essentially nested callbacks stacked below one another forming a pyramid structure. Every callback depends/waits for the previous callback, thereby making a pyramid structure that affects the readability and maintainability of the code.
- **Use:**
- **Example:**

- [x] How do you prevent/fix callback hell?
- **Explain:** Write comments, split functions into smaller functions, using promises, and using async/await. 
- **Use:**
- **Example:**

- [x] Explain the role of REPL in Node.js.
- **Explain:** A Read-Eval-Print Loop, or REPL, is a computer environment where user inputs are read and evaluated, and then the results are returned to the user.
- **Use:**  REPLs provide an interactive environment to explore tools available in specific environments or programming languages.
- **Example:**  Some examples include the Node.js console, IPython, the Bash shell, and the developer console found in most web browsers

- [x] Name the types of API functions in Node.js.
- **Explain:**  Asynchronous, Non-blocking functions
Synchronous, Blocking functions
- **Use:** Synchronous: the application will request and wait for a response until the value is returned.
Asynchronous use: these functions allow working further while the request is being handled.
- **Example:** Synchronous, Example: Instant messaging, video meetings Asynchronous: Emails, online forums

- [x] What are the functionalities of NPM in Node.js?
- **Explain:** npm is two things: first and foremost, it is an online repository for the publishing of open-source Node. js projects; second, it is a command-line utility for interacting with said repository that aids in package installation, version management, and dependency management
- **Use:** Manage local dependencies of project's tools.
Manage globally-installed project's tools.
Manage multiple versions of code and code dependencies.
Download standalone tools you can use right away.
NPM provides package-lock. json which displays all dependencies of the project.
- **Example:**

- [x] What is the difference between Node.js and Ajax?
- **Explain:** NodeJs is an open-source framework based on JavaScript v8 engine. AJAX is a web development technique for making asynchronous calls to the server.
- **Use:**  Node makes it possible to run JS outside the browser. Ajax works on the browser or outside the browser also. 
- **Example:** Node is for creating a server machine or serving static of dynamic files around the Internet. 
Ajax is for fetching data from API endpoints.

- [x] What are "streams" in Node.js? Explain the different types of streams present in Node.js.
- **Explain:**   Streams are objects that allows developers to read/write data to and from a source in a continuous manner. There are four main types of streams in Node. js; readable, writable, duplex and transform. Each stream is an eventEmitter instance that emits different events at several intervals.

- **Use:** The readable stream is a stream that is used for read operations.
The writable stream as the name suggests is a stream used for write operations.
A duplex stream is a stream that performs both read and write operations.
A transform stream is a stream that uses it input to compute an output.
Example:
Data - Data event is emitted when readable data is available.
Finish - Finish event is emitted when the stream is done writing data.
Error - Error event is emitted when an error occurs while reading/writing data.
End - End event is emitted when the read stream has finished reading data.

- **Example:** Streams are objects that allows developers to read/write data to and from a source in a continuous manner. There are four main types of streams in Node.js; readable, writable, duplex and transform. Each stream is an eventEmitter instance that emits different events at several intervals.

- [x] Explain chaining in Node.js.
- **Explain:** Promise chaining is a syntax that allows you to chain together multiple asynchronous tasks in a specific order
- **Use:** This is great for complex code where one asynchronous task needs to be performed after the completion of a different asynchronous task

- **Example:** parallel chaining parallel(tasks, callback): The tasks is a collection of functions that runs parallel in practice through I/O switching. If any function in the collection tasks returns an error, the callback function is fired. Once all the functions are completed, the data is passed to the callback function as an array. The callback function is optional.
series(tasks, callback): Each function in tasks run only after the previous function is completed. If any of the functions throw an error, the subsequent functions are not executed and the callback is fired with an error value. On completion of tasks, the data is passed into the callback function as an array.or series chaining

- [x] What are Globals in Node.js?
- **Explain:** Node.js global objects are global in nature and they are available in all modules. 
- **Use:** The Buffer class is an inbuilt globally accessible class that means it can be used without importing any module. The Buffer class is used to deal with binary data. Buffer class objects are used to represent binary data as a sequence of bytes. 

console: It is an inbuilt global object used to print to stdout and stderr. 

global: It is a global namespace. Defining a variable within this namespace makes it globally accessible. 
- **Example:**

- [x] What is Event-driven programming?
- **Explain:** Event-driven programming is a paradigm where entities (objects, services, and so on) communicate indirectly by sending messages to one another through an intermediary.
- **Use:** Depending on the specific application, event-driven processing can improve responsiveness, throughput and flexibility.
- **Example:** An Event Handler is a callback function that will be called when an event is triggered.


- [x] What is Event loop in Node.js? And how does it work?
- **Explain:**  Event loop is an endless loop, which waits for tasks, executes them and then sleeps until it receives more tasks. 
- **Use:** The Event Loop starts at the moment Node.js begins to execute your index.js file, or any other application entry point.
- **Example:** A Main Loop listens for event triggers and calls the associated event handler for that event.

- [x] What is the purpose of module.exports in Node.js?
- **Explain:** The main purpose of module. exports is to achieve modular programming
- **Use:**
- **Example:**

- [x] What is the difference between asynchronous and non-blocking?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is tracing in Node.js?
- **Explain:**
- **Use:**
- **Example:**

- [x] How will you debug an application in Node.js?
- **Explain:**
- **Use:**
- **Example:**

- [x] Difference between setImmediate() vs setTimeout()?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is process.nextTick()?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is package.json? What is it used for?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is libuv?
- **Explain:**
- **Use:**
- **Example:**

- [x] What are some of the most popular modules of Node.js?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is EventEmitter in Node.js?
- **Explain:**
- **Use:**
- **Example:**

