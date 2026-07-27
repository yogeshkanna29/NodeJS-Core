# Custom Module in Node.js

A Custom Module in Node.js is a user-defined module that contains reusable code, such as functions, objects, or classes, which can be exported and used in other parts of an application.

- Allows developers to organize and reuse code across multiple files.
- Functions, objects, or classes can be exported using module.exports or exports.
- Custom modules are imported into other files using require().
- Helps improve code maintainability, readability, and modularity in Node.js applications.

<details>
    <summary><strong>Creating a Custom Module</strong></summary>
    
To create a custom module, first define the functions, classes, or objects you want the module to contain, and then export them so they can be used in other parts of your application.

<details>
    <summary><strong>Defining Functions, Classes, or Objects in a Module</strong></summary>
    
Start by creating a new JavaScript file, which will act as your custom module. In this file, you can define functions, classes, or objects as you would in any JavaScript code.

Example: Create a simple utility module named 'math-utils.js' with two functions for adding and multiplying numbers:

```js
// math-utils.js

function add(a, b) {
  return a + b;
}

function multiply(a, b) {
  return a * b;
}
```
</details>

---
<details>
    <summary><strong>Exporting Functions, Classes, or Objects using 'module.exports' or 'exports'</strong></summary>
    
To make the functions, classes, or objects defined in your custom module accessible from other parts of your application, you need to export them using either 'module.exports' or 'exports'. Both methods achieve the same result, but their usage differs slightly.

Using 'module.exports':

```js
// math-utils.js
function add(a, b) {
  return a + b;
}
function multiply(a, b) {
  return a * b;
}
module.exports = {
  add,
  multiply
};
```

Using 'exports':

```js
// math-utils.js
function add(a, b) {
  return a + b;
}
function multiply(a, b) {
  return a * b;
}
exports.add = add;
exports.multiply = multiply;
```

In both cases, the add and multiply functions are exported, allowing them to be imported and used in other files via require().

filename: arthmetic.js
```js
const mathUtils = require('./math-utils');
const sum = mathUtils.add(5, 3);
const product = mathUtils.multiply(5, 3);
console.log(`Sum: ${sum}, Product: ${product}`);
```
</details>

---
<details>
    <summary><strong>Using a Custom Module in Another File</strong></summary>
    
Once a custom module is created and its functionality is exported, it can be imported and utilized in other files of the application using module loading mechanisms like require().

Loading a Custom Module with 'require()'

To load a custom module, you can use the 'require()' function, just as you would for built-in core modules. Pass the relative file path of your custom module as an argument, and 'require()' will return an object containing the exported functionality.

Suppose we have a custom module named 'math-utils.js' with two exported functions, 'add()' and 'multiply()':

filename:math-utils.js

```js
// math-utils.js
function add(a, b) {
  return a + b;
}
function multiply(a, b) {
  return a * b;
}
module.exports = {
  add,
  multiply
};
```

To use this module in another file, say 'arthmetic.js', you can load it like this:
```js
// arthmetic.js
const mathUtils = require('./math-utils');
```

Accessing Exported Functions, Classes, or Objects

After importing the module using require(), its exported functions can be accessed through the returned object and used in app.js, such as calling add() and multiply() from math-utils.js.

```js
// arthmetic.js
const mathUtils = require('./math-utils');
const sum = mathUtils.add(5, 3);
const product = mathUtils.multiply(5, 3);
console.log(`Sum: ${sum}, Product: ${product}`);
```

</details>

---
<details>
    <summary><strong>Organizing Code in Multiple Custom Modules</strong></summary>
    
As applications grow, organizing code into multiple custom modules improves clarity and maintainability. Each module should handle a specific functionality.

For example, a math application can use separate files:

addition.js: contains add()
multiplication.js: contains multiply()
division.js: contains divide()
subtraction.js: contains subtract().

In 'arithmetic.js' file, you can load and use these custom modules like this:

```js
// arthmetic.js
const add = require('./addition');
const multiply = require('./multiplication');
const divide = require('./division');
const subtract = require('./subtraction');
console.log(`Addition: ${add(5, 3)}`);
console.log(`Multiplication: ${multiply(5, 3)}`);
console.log(`Division: ${divide(6, 3)}`);
console.log(`Subtraction: ${subtract(5, 3)}`);
```
</details>
</details>