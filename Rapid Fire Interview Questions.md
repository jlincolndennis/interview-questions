### Scope
> Two Types: Global, Function, (Third in ES6: Block) and it refers the visibility of variables in a given piece of code

### Hoisting
> Hoisting is JavaScript's behavior of moving declarations to the top of their scope, populating Scope Tables

> Allows you to call named (declared) functions before you declare them.

### Closure
> Functions that refer to variables from a parent function. They  maintain a reference to their outer scope. One use of closures is to create private variables.

### Event Bubbling and Delegation
> After an event is triggered on a specific element, it travels up the DOM and alerts parent elements in nesting order.

> Event delegation allows you to avoid adding event listeners to specific nodes;  instead, the event listener is added to one parent.

### DOM
> Document Object Model

> Tree representation of all HTML elements on a webpage that creates the structure of a webpage.

### AJAX
> Asynchronous JavaScript and XML

> Makes an asynchronous http request using specific verbs ('get', 'push', etc.) with appropriate headers, and then handles the response

### Strict vs Loose Equality
> Loose equality uses type coercion, whereas strict equality does not.

>`==` uses coercion to loosely equate primitive values.

### Types
> Primitive/immutable: strings, booleans, numbers

> Reference/Mutable: objects, 'arrays'

### Prototypal Inheritance
> A style of OOP where objects have prototypes, which are pointers to other objects. Objects can delegate property look up to their prototype. Any object can be a prototype to any other object.

### Event Loop
> Mechanism by which JS runs async (concurrent) calls in a non blocking way. There are three parts, the stack, the heap and queue. Callbacks go to the heap so other code can execute until the async call is done. Then the callback is moved from the heap to the queue. Once the stack has completely finished executing, callbacks are moved from the queue into the stack to be executed.

### IIFE
> Immediately Invoked Function Expression is a JavaScript function that runs as soon as it is defined.

### How does 'this' work in JavaScript?
> The 'this' reference refers to (and holds the value of) the singular object that invoked the function where 'this' is used.

> #### Rules of This
* window/global
  * 'use strict' this => undefined
* call function on object, this => object
* Fixed by bind
  * changed by apply, call
* constructor - 'this' refers to the new object
* fat arrow, 'this' becomes lexically scoped, takes the value of this from its parent execution context

### Describe how JavaScript handles inheritance
> JS handles inheritance in a prototypal fashion. Any object can be a prototype to any other object. Inheritance allows objects to delegate property lookup to other objects.
  * Two styles of setting up prototypal inheritance in JS
    * Pseudo classical
    * The other one.

### Example of when you would use closures
> Closures allow you to keep the EC of a function active. This allows to keep private variables. (Encapsulation)

### What is jQuery?
> jQuery is a JavaScript front end library for traversing and manipulating the DOM, handling events, and making AJAX calls.

### Describe reference vs primitive types
> References are pointers in memory, whereas primitives are actual values.
> References can be changed, primitives are overwritten
