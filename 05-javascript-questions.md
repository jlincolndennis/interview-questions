# JavaScript Interview Questions

## Resources
- http://lucybain.com/blog/tags/interview-questions/
- http://www.toptal.com/javascript/interview-questions
- http://www.careerride.com/Object-oriented-programming-Interview-Questions.aspx
- https://medium.com/javascript-scene/10-interview-questions-every-javascript-developer-should-know-6fa6bdf5ad95


NaN
>

Difference between document load event and document ready event?
>

Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
>

Why would you use something like the load event? Does this event have disadvantages? Do you know any alternatives, and
>

What are the pros and cons of using Promises instead of callbacks?
>

What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
>

What tools and techniques do you use debugging JavaScript code?
>

What language constructions do you use for iterating over object properties and array items?
>

Explain the difference between mutable and immutable objects.
>

What is an example of an immutable object in JavaScript?
>

What are the pros and cons of immutability?
>

How can you achieve immutability in your own code?
>

Explain the difference between synchronous and asynchronous functions.
>

What is event loop?
> Mechanism by which JS runs async (concurrent) calls in a non blocking way. There are three parts, the stack, the heap and queue. Callbacks go to the heap so other code can execute until the async call is done. Then the callback is moved from the heap to the queue. Once the stack has completely finished executing, callbacks are moved from the queue into the stack to be executed.

What is the difference between call stack and task queue?
>

What is isomorphic JavaScript?
> JavaScript can that be run on both the client (in the browser) and in Node (on the server)

What are the data types in JavaScript?
>
* Boolean
* String
* Undefined
* Number
* Null
* Symbol
* Object

> Functions and Arrays are kinds of Objects.

What's the difference between `null` and `undefined`?
> Something with a value of `null` is empty, while something with the value of `undefined` hasn't been initialized.

What does the `this` keyword refer to in JavaScript?
>   1. The first value passed to `call()` or `apply()`
    2. The value that was `bind()`ed to the function
    3. The calling object
    4. The global scope

How are errors usually handled in JavaScript?
> Try/Catch/Finally blocks for synchronous code.  `catch` methods for promises.

How does inheritance work in JavaScript?
> JavaScript has prototypal inheritance, a style of OOP where objects have prototypes, which are pointers to other objects. Objects can delegate property look up to their prototype. Any object can be a prototype to any other object.

Name two programming paradigms.
> Procedural, functional, and object-oriented.

What's the difference between imperative programming and declarative programming?
> Imperative programming tells the computer what to do. Declarative programming tells the computer what you want, ignorant of the steps required to produce it.

What are some tenets of functional programming?
> * Functional purity (no side-effects, output derived only from input)
* Simple functions
* First-class functions (functions as variables)
* Higher-order functions (functions that return functions)

What is immutability?
> When a stored value can't be changed. Functional programs/languages replace values with new values, rather than changing (or "mutating") the existing ones.

What is async in JavaScript?
> When a function does not immediately return a value. The rest of the program continues executing, requiring special handling and "callback functions" for when function calls complete.


Explain how the factory pattern works.
> A factory is when you need an object with a particular interface, but you let a constructor decide which specific object you get back.
```js
myEmployee = Employee.byType("fullTime");
// myEmployee is actually an instance of FullTimeEmployee
```

Name as many kinds of loops as you can.
> For, While, For-In, For-Each, Map, Reduce

Name as many different kinds of conditionals as you can.
> if/then/elseIf/else, switch, ternary.

What creates scope in Javascript?
> There's global scope and function scope in ES5.  In ES2015 there's also Block scope.

How can variables be assigned in Javascript in ES2015?
> `var` for function scope, `let` for block scope, `const` for block scope protected against reassignment.

What is a typical use case for anonymous functions?
>Callbacks, like in the .then() of an AJAX call.

Name 2 or more ways to define a global variable in Javascript
>Leave off the `var` or assign it to the `window`

What does AJAX stand for?  Explain how it works in as much detail as possible
>Asynchronous javascript and xml, it just makes a request to a specific url with a verb and data (and callbacks). Then it makes the call with the appropriate headers.

What’s the difference between `==` and `===` in JS?
>Type Coercion
>
> == doesn't care about type (i.e. type coercion), so "2" == 2 will evaluate to true. === does care about type, so "2" === 2 will evaluate to false.

What is "callback hell" and how can it be avoided?
>_

What's the difference between Primitive and Reference types in Javascript?
>A primitive type has a fixed amount of memory that it takes up, where as a reference type does not. Examples of primitive types are boolean values or integers, where as examples of ref types would be arrays and objects. Ref types like arrays are made up of references, or pointers to their values, hence the name

Explain how `this` works in JavaScript
> The 'this' reference refers to (and holds the value of) the singular object that invoked the function where 'this' is used.

> #### Rules of This
* window/global
  * 'use strict' this => undefined
* call function on object, this => object
* Fixed by bind
  * changed by apply, call
* constructor - 'this' refers to the new object
* fat arrow, 'this' becomes lexically scoped, takes the value of this from its parent execution context

Explain how prototypal inheritance works
> In JavaScript, objects have prototypes, which are pointers to other objects. Objects can delegate property look up to their prototype. Any object can be a prototype to any other object.

What's the difference between a variable that is: null, undefined or undeclared?  How would you go about checking for these?
>An undefined value typically comes from a variable that has been declared, but was not assigned a value.
  ```js
  var a;
  ```
> A null value is a value that explicitly represents nothingness or a lack of a value.
  ```js
  var a = null;
  ```
>An undeclared variable will throw an error if used in code. Here, `b` is undeclared and will throw an error.
  ```js
  var a = 1;
  var c = a + b
  ```

What is a closure, and how/why would you use one?
> Functions that refer to variables from a parent function. They  maintain a reference to their outer scope. One use of closures is to create private variables.

What's a typical use case for anonymous functions?
> These are most commonly used in callbacks and IIFEs.

What's the difference between host objects and native objects?
>

What's the difference between .call and .apply?
> They both server the same purpose, but one accepts an array or arguments instead of a comma separated list.

- Explain Function.prototype.bind.
> Bind works like call and apply, but instead of invoking the function it's applied to, it returns a new function with the bound context and arguments.


Explain how JSONP works (and how it's not really AJAX).
>_

Explain "hoisting".
> Hoisting is JavaScript's behavior of moving declarations to the top of their scope, populating Scope Tables

> Allows you to call named (declared) functions before you declare them.

Why is extending built-in JavaScript objects not a good idea?
>

What is the difference between == and ===?
> Loose equality `==` uses type coercion, whereas strict equality `===` does not.

>`==` uses coercion to loosely equate primitive values.

Why is it called a Ternary expression, what does the word "Ternary" indicate?
> Ternary refers to the fact that there are three parts to the statement, a condition and two different actions to take, one if the statement is evaluated as true, and the other if the statement evaluates to false.

What is "use strict";? what are the advantages and disadvantages to using it?
>

What tools can be used to assure consistent style?
> jsLint etc...
