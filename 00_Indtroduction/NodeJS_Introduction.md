# Node JS

<details>
    <summary><strong>Definition</strong></summary>
    
- Node.js is an open-source, cross-platform JavaScript runtime built on Chrome's V8 engine.
- It enables developers to run JavaScript outside the browser to build fast, scalable server-side applications.

- JavaScript was initially a frontend-only language, and Node.js (2009) enabled backend development as well.
- Non-blocking, event-driven architecture for high performance.
- Supports the creation of REST APIs, real-time applications, and microservices.
- Comes with a rich library of modules through npm (Node Package Manager).
</details>

---

<details>
    <summary><strong>First code example</strong></summary>
    
```js
// Import the http module
const http = require("http");

// Create a server
const server = http.createServer((req, res) => {
res.statusCode = 200;
res.setHeader("Content-Type", "text/plain");
res.end("Welcome to the Node.js Tutorial");
});

// Listen on port 3000
server.listen(3000, () => {
console.log(
"Server is running on http://localhost:3000");
});

```

- It will start a server, and when you visit http://localhost:3000, it will display

```

Welcome to the Node.js Tutorial

```

- The http module is imported to create a basic HTTP server.
- The createServer() method is used to handle incoming requests and send responses.
- The server listens on port 3000, and a message is displayed in the browser when accessed.

</details>

---

<details>
    <summary><strong>Why learn Node.js</strong></summary>

> It allows developers to build fast, scalable server-side applications using JavaScript.

- Enables full-stack development with a single language.
- Ideal for real-time apps like chat and gaming servers.
- Handles I/O-intensive tasks efficiently with non-blocking architecture.
- Supported by a large community and vast npm ecosystem.
</details>

---

<details>
    <summary><strong>Table of Content</strong></summary>
    
<details>
    <summary><strong>Getting Started</strong></summary>
    
> Provides an overview of its runtime environment, architecture, and how it enables server-side JavaScript development.

- Introduction
- Architecture and Components
- Working
- Installation and First Application
- REPL
</details>

---

<details>
    <summary><strong>Node Package Manager</strong></summary>
    
> Manage project dependencies and packages efficiently using NPM.

- NPM (Node.js Package Manager)
- Create and Publish NPM packages
- Global Installation of Dependencies
</details>

---

<details>
    <summary><strong>Modules</strong></summary>
    
> Understand how to organize and reuse code using different types of modules.

- Modules
- Core modules
- Third Party modules
- Custom modules
</details>

---

<details>
    <summary><strong>Asynchronous Programming</strong></summary>

> Learn how Node.js handles multiple tasks efficiently using non-blocking operations.

- Blocking and Non-Blocking
- Callback Concept
- Promise Chaining
- Event Loop
</details>

---

<details>
    <summary><strong>Core Concept</strong></summary>
    
> Understand essential Node.js concepts that control scope, context, and global behavior.

- This Binding
- Global Objects
- Session Variable
</details>

---
<details>
    <summary><strong>Building Applications</strong></summary>

> Create and manage server-side applications using Node.js features and tools.

- Web Server
- Frameworks
- Child Process
</details>

---
<details>
    <summary><strong>Express.js</strong></summary>
    
> Build web applications efficiently using the Express.js framework.

- Introduction to Express.js
- MVC Design Pattern
- Serving Static Files
- Middleware
- EJS Template
</details>

---
<details>
    <summary><strong>Debugging and Utilities</strong></summary>
    
> Tools and techniques to debug code and improve development workflow.

- Debugging
- Set Console Font Color
- Automatic Restart Server with Nodemon
</details>

---
<details>
    <summary><strong>Node.js Complete References</strong></summary>

<details>
    <summary><strong>System & Core Modules</strong></summary>
    
> Handle core functionalities related to system operations and runtime environment.

- Assert
- Console
- Utility
- OS
- Process
- V8
- VM Module
</details>

---
<details>
    <summary><strong>File & Data Handling</strong></summary>

> Manage data processing, file operations, and data transformation.

- Buffer
- String Decoder
- Query String
- File System
- Path Module
- Stream
- URL
</details>

---
<details>
    <summary><strong>Networking, Security & Performance</strong></summary>
    
> Support communication, security features, and performance optimization.

- HTTP Module
- HTTP2
- DNS
- UDP/DataGram
- TLS/SSL Module
- Crypto
- Zlib
- Timers Module
</details>
    

</details>

---
<details>
    <summary><strong>Interview Preparation and Projects</strong></summary>

- Interview Questions and Answers
- Projects
    
</details>

</details>

---