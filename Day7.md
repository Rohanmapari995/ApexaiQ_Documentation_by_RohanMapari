# JavaScript Basics

This README covers the fundamental concepts of JavaScript, including variables, data types, control flow, functions, arrays, objects, the DOM, and event handling.

---

# 1. Variable Declarations (`let`, `const`, and `var`)

Variables are used to store data.

## `let`
- Block-scoped
- Can be reassigned
- Cannot be redeclared in the same scope

```javascript
let age = 20;
age = 21;

console.log(age); // 21
```

---

## `const`
- Block-scoped
- Cannot be reassigned
- Must be initialized during declaration

```javascript
const PI = 3.14159;

// PI = 3.14; // Error
```

Objects and arrays declared with `const` can still have their contents modified.

```javascript
const person = {
    name: "Rohan"
};

person.name = "Rahul";

console.log(person.name);
```

---

## `var`
- Function-scoped
- Can be reassigned
- Can be redeclared

```javascript
var x = 10;
var x = 20;

console.log(x);
```

### Comparison

| Feature | var | let | const |
|---------|-----|-----|-------|
| Scope | Function | Block | Block |
| Reassign | ✅ | ✅ | ❌ |
| Redeclare | ✅ | ❌ | ❌ |

**Recommendation:** Prefer `const` by default and use `let` when reassignment is needed. Avoid `var` in modern JavaScript.

---

# 2. Data Types and Operators

## Primitive Data Types

```javascript
let name = "John";              // String
let age = 22;                   // Number
let isStudent = true;           // Boolean
let value = null;               // Null
let city;                       // Undefined
let id = Symbol("id");          // Symbol
let big = 1234567890123456789n; // BigInt
```

## Non-Primitive Data Types

```javascript
let person = {
    name: "Rohan",
    age: 20
};

let numbers = [10, 20, 30];
```

---

## Operators

### Arithmetic Operators

```javascript
+
-
*
/
%
**
```

Example:

```javascript
let a = 10;
let b = 3;

console.log(a + b);
console.log(a % b);
```

---

### Assignment Operators

```javascript
=
+=
-=
*=
/=
%=
```

---

### Comparison Operators

```javascript
==
===
!=
!==
>
<
>=
<=
```

Example:

```javascript
console.log(10 == "10");   // true
console.log(10 === "10");  // false
```

---

### Logical Operators

```javascript
&&
||
!
```

Example:

```javascript
let age = 20;

console.log(age > 18 && age < 60);
```

---

# 3. Control Flow Statements

## if

```javascript
let age = 18;

if (age >= 18) {
    console.log("Adult");
}
```

---

## if...else

```javascript
if (age >= 18) {
    console.log("Adult");
} else {
    console.log("Minor");
}
```

---

## else if

```javascript
let marks = 80;

if (marks >= 90) {
    console.log("Grade A");
} else if (marks >= 75) {
    console.log("Grade B");
} else {
    console.log("Grade C");
}
```

---

## switch

```javascript
let day = 2;

switch (day) {
    case 1:
        console.log("Monday");
        break;
    case 2:
        console.log("Tuesday");
        break;
    default:
        console.log("Invalid Day");
}
```

---

## Loops

### for Loop

```javascript
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```

### while Loop

```javascript
let i = 1;

while (i <= 5) {
    console.log(i);
    i++;
}
```

### do...while Loop

```javascript
let i = 1;

do {
    console.log(i);
    i++;
} while (i <= 5);
```

### for...of Loop

Used to iterate over arrays.

```javascript
let fruits = ["Apple", "Banana", "Mango"];

for (let fruit of fruits) {
    console.log(fruit);
}
```

### for...in Loop

Used to iterate over object properties.

```javascript
let person = {
    name: "Rohan",
    age: 20
};

for (let key in person) {
    console.log(key, person[key]);
}
```

---

# 4. Functions

Functions are reusable blocks of code.

## Function Declaration

```javascript
function greet() {
    console.log("Hello");
}

greet();
```

---

## Function with Parameters

```javascript
function add(a, b) {
    return a + b;
}

console.log(add(5, 3));
```

---

## Function Expression

```javascript
const greet = function () {
    console.log("Hello");
};
```

---

## Arrow Function

```javascript
const add = (a, b) => {
    return a + b;
};
```

Short Form

```javascript
const add = (a, b) => a + b;
```

---

## Anonymous Function

```javascript
setTimeout(function () {
    console.log("Executed");
}, 1000);
```

---

## Immediately Invoked Function Expression (IIFE)

```javascript
(function () {
    console.log("Executed");
})();
```

---

## Callback Function

```javascript
function greet(name, callback) {
    console.log("Hello " + name);
    callback();
}

function goodbye() {
    console.log("Goodbye");
}

greet("Rohan", goodbye);
```

---

## Higher-Order Function

```javascript
function calculate(a, b, operation) {
    return operation(a, b);
}

console.log(calculate(5, 3, (x, y) => x + y));
```

---

# 5. Arrays and Their Methods

Arrays store multiple values in a single variable.

```javascript
let fruits = ["Apple", "Banana", "Mango"];
```

## Common Array Methods

| Method | Description |
|---------|-------------|
| push() | Adds an element at the end |
| pop() | Removes the last element |
| shift() | Removes the first element |
| unshift() | Adds an element at the beginning |
| indexOf() | Returns index of an element |
| includes() | Checks if an element exists |
| slice() | Returns part of an array |
| splice() | Adds/removes elements |
| map() | Creates a new transformed array |
| filter() | Filters elements |
| reduce() | Reduces array to a single value |
| find() | Returns the first matching element |
| forEach() | Executes a function for each element |

Example:

```javascript
let numbers = [1, 2, 3, 4];

let squares = numbers.map(num => num * num);

console.log(squares);
```

---

# 6. Objects and Their Methods

Objects store data as key-value pairs.

```javascript
let person = {
    name: "Rohan",
    age: 20
};
```

## Access Properties

```javascript
console.log(person.name);

console.log(person["age"]);
```

---

## Add Property

```javascript
person.city = "Pune";
```

---

## Delete Property

```javascript
delete person.age;
```

---

## Common Object Methods

| Method | Description |
|---------|-------------|
| Object.keys() | Returns all keys |
| Object.values() | Returns all values |
| Object.entries() | Returns key-value pairs |
| Object.assign() | Copies object |
| Object.freeze() | Prevents modifications |
| Object.seal() | Prevents adding/removing properties |

Example:

```javascript
console.log(Object.keys(person));
console.log(Object.values(person));
```

---

# 7. DOM (Document Object Model)

The DOM represents an HTML page as a tree of objects that JavaScript can manipulate.

Example HTML

```html
<h1 id="title">Hello</h1>

<p class="text">Welcome</p>
```

---

## Selecting Elements

```javascript
document.getElementById("title");

document.getElementsByClassName("text");

document.getElementsByTagName("p");

document.querySelector(".text");

document.querySelectorAll("p");
```

---

## Changing Content

```javascript
document.getElementById("title").textContent = "JavaScript";

document.getElementById("title").innerHTML = "<b>JavaScript</b>";
```

---

## Changing CSS

```javascript
document.getElementById("title").style.color = "blue";

document.getElementById("title").style.fontSize = "40px";
```

---

## Creating Elements

```javascript
let para = document.createElement("p");

para.textContent = "New Paragraph";

document.body.appendChild(para);
```

---

## Removing Elements

```javascript
para.remove();
```

---

# 8. Event Handling

Events allow JavaScript to respond to user interactions.

## Click Event

```html
<button id="btn">Click Me</button>
```

```javascript
document.getElementById("btn").addEventListener("click", function () {
    alert("Button Clicked!");
});
```

---

## Input Event

```javascript
document.getElementById("name").addEventListener("input", function () {
    console.log(this.value);
});
```

---

## Keyboard Event

```javascript
document.addEventListener("keydown", function (event) {
    console.log(event.key);
});
```

---

## Mouse Event

```javascript
document.addEventListener("mouseover", function () {
    console.log("Mouse Over");
});
```

---

## Form Submit Event

```javascript
document.querySelector("form").addEventListener("submit", function (event) {
    event.preventDefault();
    console.log("Form Submitted");
});
```

---

# Summary

| Topic | Description |
|--------|-------------|
| Variables | `let`, `const`, `var` |
| Data Types | Primitive and Non-Primitive |
| Operators | Arithmetic, Assignment, Comparison, Logical |
| Control Flow | if, switch, loops |
| Functions | Declaration, Expression, Arrow, Callback, IIFE |
| Arrays | Storage and built-in methods |
| Objects | Properties and object methods |
| DOM | Access and manipulate HTML elements |
| Event Handling | Respond to user actions |

---

# Best Practices

- Prefer `const` whenever possible.
- Use `let` only when reassignment is required.
- Always use `===` instead of `==`.
- Write small and reusable functions.
- Use meaningful variable and function names.
- Prefer `addEventListener()` over inline HTML events.
- Keep JavaScript code modular and well-commented.
- Practice regularly by building small projects.

---

## Next Topics to Learn

After mastering these fundamentals, continue with:

1. ES6 Features
   - Template Literals
   - Destructuring
   - Spread & Rest Operators
   - Modules

2. Asynchronous JavaScript
   - Callbacks
   - Promises
   - Async/Await
   - Fetch API

3. Object-Oriented Programming (OOP)

4. Error Handling

5. JSON

6. Local Storage & Session Storage

7. APIs and AJAX

8. JavaScript Classes

9. Modules

10. Closures, Hoisting, and Scope

Happy Coding! 🚀