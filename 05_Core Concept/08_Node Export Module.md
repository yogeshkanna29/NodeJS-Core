# Node Export Module

In NodeJS, module.exports is used to share functions, objects, or values from one file to the other file so that other files can use them. This is an essential part of organizing and reusing code across different parts of your application, making it easier to manage and maintain.

Here’s how exporting modules in NodeJS can help:

- Share code between files easily.
- Organize projects into smaller files.
- Reuse code without repetition.
- Control access to file contents.

Syntax

```js
module.exports = literal | function | object
```

<details>
    <summary><strong>Using the module.exports</strong></summary>
    
In NodeJS, you can share code from one file so that it can be used in another file. This is done by using module.exports to export the code.

<details>
    <summary><strong>1. Exporting a Function</strong></summary>
    
In NodeJS, you can export a function from one module (file) so that it can be used in another module. This is done using module.exports. By exporting a function, you allow other files to import and use that function in their code.

```js
//math.js (module file)
// Define a function that adds two numbers
function add(a, b) {
  return a + b;
}
// Export the function using module.exports
module.exports = add;

//app.js(main file)
// Import the add function from the math.js module
const add = require('./math');
// Use the imported function
console.log(add(2, 3));  // Output: 5
```
</details>

---

<details>
    <summary><strong>2. Exporting function as a class</strong></summary>
    
Create a file named app.js. Define a function using this keyword and export the function. module.exports and Create a file named index.js and import the file app.js to use the exported function as a class.

```js
const Company = require('./app');
const firstCompany = new Company();
firstCompany.info();

module.exports = function () {
    this.name = 'GeeksforGeeks';
    this.website = 'https://www.geeksforgeeks.org/';
    this.info = () => {
        console.log(`Company name - ${this.name}`);
        console.log(`Website - ${this.website}`);
    }
}
```
</details>

---

<details>
    <summary><strong>3. Exporting Literals</strong></summary>
    
Exporting Literals in NodeJS means sharing simple values like strings, numbers, or arrays from one file to app.js and exporting the literal using. module.exports.

```js
module.exports = "GeeksforGeeks";

const message = require("./app");
console.log(message);
```
</details>

---

<details>
    <summary><strong>4. Exporting Object</strong></summary>
    
It allows sharing multiple related values from one file to another. An object can store properties and methods, which can be accessed in other files.

```js
module.exports = {
  name: "GeeksforGeeks",
  website: "https://www.geeksforgeeks.org/"
};

const company = require("./app");
console.log(company.name);
console.log(company.website);
```
</details>
</details>