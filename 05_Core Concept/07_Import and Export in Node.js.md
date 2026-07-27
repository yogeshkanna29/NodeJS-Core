# Import and Export in Node.js

Importing and exporting files are important parts of any programming language. Importing functions or modules enhances the reusability of code. When the application grows in size, maintaining a single file with all the functions and logic becomes difficult. It also hinders the process of debugging. Therefore, it is good practice to create separate files for specific functions and later import them as per requirement.

Node.js also allows importing and exporting functions and modules. Functions in one module can be imported and called in other modules saving the effort to copy function definitions into the other files. The module can be edited or debugged separately making it easier to add or remove features.

<details>
    <summary><strong>Table of Content</strong></summary>
    
<details>
    <summary><strong>Steps to include functions from other files</strong></summary>
    
Creating a Module:
Modules are created in Node.js are JavaScript files. Every time a new file with .js extension is created, it becomes a module.
```js
function add(x, y) {
   return x + y;
}
```
Exporting a Module:
```js
// Filename: func.js

function add(x, y) {
   return x + y;
}

function subtract(x, y) {
   return x - y;
}

// Adding the code below to allow importing
// the functions in other files
module.exports = { add }
```
Importing a Module:

We need to import the module to use the functions defined in the imported module in another file. The result returned by require() is stored in a variable which is used to invoke the functions using the dot notation.

```js
// Filename: main.js

// Importing the func.js module

// The ./ says that the func module
// is in the same directory as 
// the main.js file
const f = require('./func');

// Require returns an object with add()
// and stores it in the f variable 
// which is used to invoke the required 

const result = f.add(10, 5);

console.log('The result is:', result);
```
</details>

---
<details>
    <summary><strong>From a Local File</strong></summary>
    
```js
// Filename: func.js

function add(x, y) {
  return x + y;
}

function subtract(x, y) {
  return x - y;
}

module.exports = { add, subtract};

// Filename: main.js

const f = require('./func');

console.log(f.add(4, 4));
console.log(f.subtract(8, 4));
```
We can also use the destructuring syntax to unpack the properties of the object returned by require() function and store them in respective variables.
```js
// Filename: main.js
const { add, subtract} = require('./func');
console.log(add(4, 4)); 
console.log(subtract(8, 4));
```
</details>

---

<details>
    <summary><strong>Using module.exports</strong></summary>
    
Defining the functions inside module.exports object.
```js
module.exports = {
    add: function (x, y) {
        return x + y;
    },

    subtract: function (x, y) {
        return x - y;
    },
};
```
Defining each function independently as a method of module.exports
```js
module.exports.add = function (x, y) {
   return x + y;
};

module.exports.subtract = function (x, y) {
   return x - y;
};
```
</details>

---
<details>
    <summary><strong>From a directory</strong></summary>

Importing lib.js file inside the directory, by prefixing lib.js with the directory name.
```js
const lib = require('./mod/lib');

console.log(lib.add(6, 4));
console.log(lib.subtract(12, 4));
```
</details>

---
<details>
    <summary><strong>Summary</strong></summary>

There are three types of modules Imports in Node.js

1. Importing from local module:
These modules are created by the user and can be imported as:
```js
const fun = require('./filename.js'); // OR
const fun = require('./path/filename.js');
```
2. Importing from core modules:
These modules are inbuilt in Node.js and can be imported as:
```js
const fs = require('fs');
```
3. Importing from third party modules:
These modules are installed using a package manager such as npm. Examples of third party modules are express, mongoose, nodemon, etc. These are imported as:
```js
const express = require('express');
```
Thus above are few examples to import and export functions from different files in Node.js .
</details>
</details>

---