# Node.js Third-Party Modules

Third-party modules are external libraries installed via npm that extend Node.js functionality, such as handling HTTP requests and other complex tasks.

- Not included by default in Node.js and must be installed manually.
- Installed and managed using npm, which handles dependencies and updates.
- Provide ready-made solutions for routing, authentication, database integration, and other backend tasks.

<strong>Installing and Using Third-Party Modules</strong>

- Node.js uses npm, the world’s largest software registry, to manage third-party packages. To install A module is straightforward; you just need to give the command "npm install express".

<strong>Popular Third-Party Modules</strong>

<details>
    <summary><strong>1. Express</strong></summary>

Express is a fast, minimalist web framework for Node.js that simplifies the process of building web applications and APIs. It provides robust routing, middleware support, and HTTP utility methods.  

```js
const express= require('express');
const app= express();
app.get('/',(req,res)=>{
    res.send('Hello from Express')
});
app.listen(8080,()=>{
    console.log('app created successfully');
})
```
</details>

---
<details>
    <summary><strong>2. Mongoose</strong></summary>

Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node.js. It provides a straightforward way to define schemas and interact with MongoDB using JavaScript objects.
```js
const mongoose = require('mongoose');
mongoose.connect('mongodb://localhost:27017/testDB');
const userSchema = new mongoose.Schema({
  name: String,
  age: Number
});
const User = mongoose.model('User', userSchema);
const newUser = new User({ name: 'Alex', age: 25 });
newUser.save().then(() => console.log('User saved!'));
``` 
</details>

---
<details>
    <summary><strong>3. Axios</strong></summary>
    
Axios is a promise-based HTTP client for Node.js and the browser. It simplifies making HTTP requests, handling responses, and managing errors.

```js
const axios = require('axios');
axios.get('https://jsonplaceholder.typicode.com/posts/1')
  .then(response => {
    console.log(response.data);
  })
  .catch(error => {
    console.error(error);
  });
```
</details>

---
<details>
    <summary><strong>4. lodash</strong></summary>
    
Lodash is a utility library that provides helpful functions for manipulating arrays, objects,strings, and more—making JavaScript code cleaner and more readable.
```js
const _ = require('lodash');
const numbers = [10, 5, 8, 3];
const sorted = _.sortBy(numbers);
console.log(sorted);
```
</details>

---
<details>
    <summary><strong>5. dotenv</strong></summary>

dotenv is a zero-dependency module that loads environment variables from a .env file into process.env. It helps manage configuration settings securely and separately from code.

```js
//app.js
require('dotenv').config();
console.log(process.env.PORT); // 4000
```

```env
//env
PORT=4000
```

</details>

---
<details>
    <summary><strong>6. Nodemon</strong></summary>
    
Nodemon is a development utility that automatically restarts your Node.js Application whenever file change. It is very useful during development to avoid manually stopping and restarting the server after every change.

```js
const fs = require('fs');

// Append data to a file
fs.appendFile('demo.txt', 'New data added\n', (err) => {
    if (err) {
        console.error("Error writing to file:", err);
    } else {
        console.log("Data added in my file Successfully");
    }
});
```
</details>

---
<details>
    <summary><strong>7. Jsonwebtoken</strong></summary>
    
Jsonwebtoken (or jwt) is a module that enables you to generate and verify JSON Web Tokens, commonly used for implementing secure authentication in APIs.

```js
const jwt = require('jsonwebtoken');
const token = jwt.sign({ username: 'Martin' }, 'secretKey');
console.log('JWT:', token);
const decoded = jwt.verify(token, 'secretKey');
console.log('Decoded:', decoded);
```
</details>

---

<details>
    <summary><strong>Advantages of Third-Party Modules</strong></summary>
    
- Faster Development: Reduces development time by providing pre-built functionality.
- Reliability: Well-maintained modules receive regular updates and community support.
- Security: Popular modules are frequently patched to address known vulnerabilities.
- Maintainability: Promotes modular, reusable code and simplifies application maintenance.
</details>


