# JavaScript Quiz

## 1. What will be the output of the following code?
```js
console.log(1 + "2" + 3);
```
a) 6
b) "123"
c) 15
d) Error

## 2. How do you declare a constant variable in JavaScript?
a) let x = 10;
b) const x = 10;
c) var x = 10;
d) constant x = 10;

## 3. What will be the output of this code?
```js
console.log(typeof NaN);
```
a) "undefined"
b) "number"
c) "object"
d) "null"

## 4. Which method is used to remove the last element from an array?
a) pop()
b) shift()
c) splice()
d) removeLast()

## 5. What does the map() method return?
a) A new array
b) The original array
c) undefined
d) A single value

## 6. What will be logged to the console?
```js
let a = 0;
console.log(a++ === 0);
console.log(a);
```
a) true, 1
b) false, 1
c) true, 0
d) false, 0

## 7. What does setTimeout do in JavaScript?
a) Executes a function after a specified delay
b) Runs a function immediately
c) Stops execution of JavaScript
d) Loops a function indefinitely

## 8. What will console.log(!!"false"); print?
a) false
b) true
c) "false"
d) undefined

## 9. Which keyword is used to handle errors in JavaScript?
a) catch
b) error
c) throw
d) try

## 10. What will be the output of the following?
```js
let x = 5;
let y = "5";
console.log(x == y, x === y);
```
a) true, true
b) false, true
c) true, false
d) false, false

## Answers
1. b) "123"
2. b) const x = 10;
3. b) "number"
4. a) pop()
5. a) A new array
6. a) true, 1
7. a) Executes a function after a specified delay
8. b) true
9. d) try
10. c) true, false

Basic Level:
What is the output of console.log(typeof null)?

Output: "object" (This is a well-known JavaScript quirk.)

How do you declare a variable in JavaScript?

Using var, let, or const. Example:

js
Copy
Edit
var a = 10;
let b = 20;
const c = 30;
What is the difference between let, const, and var?

var: Function-scoped, can be redeclared.

let: Block-scoped, cannot be redeclared but can be reassigned.

const: Block-scoped, cannot be redeclared or reassigned.

How do you check if a variable is an array in JavaScript?

Use Array.isArray():

js
Copy
Edit
Array.isArray([1, 2, 3]); // true
What does NaN === NaN return?

false, because NaN is not equal to anything, even itself.

Intermediate Level:
What will be the output of console.log(1 + '1' - 1)?

Output: 10

'1' + 1 results in '11' (string concatenation).

'11' - 1 results in 10 (string gets coerced to a number).

How do you create a shallow copy of an object in JavaScript?

Using the spread operator (...) or Object.assign():

js
Copy
Edit
let obj = { a: 1, b: 2 };
let copy1 = { ...obj };
let copy2 = Object.assign({}, obj);
Explain the difference between == and ===.

== checks for value equality (allows type coercion).

=== checks for both value and type equality.

What is event delegation in JavaScript?

A technique where a parent element handles events for its child elements using event bubbling.

js
Copy
Edit
document.getElementById('parent').addEventListener('click', (event) => {
  if (event.target.matches('.child')) {
    console.log('Child clicked!');
  }
});
What does setTimeout return?

It returns a timer ID (a number in browsers, an object in Node.js).

Advanced Level:
What is the difference between map() and forEach()?

map() returns a new array, whereas forEach() just loops through the array without returning anything.

How do you debounce a function in JavaScript?

Using setTimeout:

js
Copy
Edit
function debounce(fn, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn(...args), delay);
  };
}
Explain the concept of closures with an example.

A closure is when an inner function has access to variables from an outer function even after the outer function has finished executing.

js
Copy
Edit
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}
let counter = outer();
counter(); // 1
counter(); // 2
What is the purpose of Object.freeze()?

It makes an object immutable (prevents modifications).

js
Copy
Edit
let obj = { a: 1 };
Object.freeze(obj);
obj.a = 2; // No effect
How do you implement memoization in JavaScript?

Using a cache to store computed results.

js
Copy
Edit
function memoize(fn) {
  let cache = {};
  return function (arg) {
    if (cache[arg]) return cache[arg];
    return (cache[arg] = fn(arg));
  };
}
