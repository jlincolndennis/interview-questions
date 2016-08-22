## Code Analysis

In Javascript, what’s the value of x: `var x = 10 + '20'`
>'1020'

What does the following JS code return:
```js
var a = [1,2,3]
var b = [1,2,3]
return a === b
```
>false

What does the following JS code return:
```js
var a = 1
var b = a
a = 2
return b
```

What is the result of running following JS code:

```js
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

What is the value of foo?
```js
var foo = 10 + '20';
```

How would you make this work?

```js
add(2, 5); // 7
add(2)(5); // 7
```

What value is returned from the following statement?
```js
"i'm a lasagna hog".split("").reverse().join("");
```

What is the value of `window.foo`?
```js
( window.foo || ( window.foo = "bar" ) );
```

What is the outcome of the two alerts below?
```js
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

What is the value of foo.length?
```js
var foo = [];
foo.push(1);
foo.push(2);
```

What is the value of foo.x?
```js
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

What does the following code print?
```js
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```

Explain why the following doesn't work as an IIFE:
  - What needs to be changed to properly make it an IIFE?
```js
function foo(){ }();
```

Given a function `function Person(){}`, what's the difference between:
```js
var person = Person()
```

and

```js
var person = new Person()
```

1. What does this evaluate to - `2 + 3 + '7'`.

------------------------------------------------------------------------------------------------------------------------

## Whiteboard Problems

Make this work:
```js
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```

Create a for loop that iterates up to 100 while outputting "fizz" at multiples of 3, "buzz" at multiples of 5 and - "fizzbuzz" at multiples of 3 and 5

Write a method to check if 2 given words are anagrams.

```js
anagram_checker("Dictionary", "Indicatory")
#=> true

anagram_checker("Dictionary", "blahblah")
#=> false
```

Write code to convert a numeric string like “543” and convert it to the integer version 543. Assume numbers will be whole integers.

Whiteboard the schema for zappos.com

Write FizzBuzz with as few if statements as possible. It's possible without any conditionals at all.

Implement a function which calculates the n-th item of Fibonacci sequence

Find largest prime palindrome less than 1000

Implement an algorithm to reverse a singly linked list

Count the number of nodes in a binary tree

Write your own getElementById function

Show an example of the following array methods - `push`, `pop`, `shift`, and `unshift`.
