# Introduction to Node.js

<details>
    <summary><strong>Node JS Introduction</strong></summary>
    
- Node.js is a runtime environment that lets you run JavaScript on the server side. It is built on Chrome's V8 JavaScript engine and uses an **event-driven, non-blocking I/O model**. It is widely used to build web servers, APIs, and command-line tools.
<details>
    <summary><strong>What is Node.js?</strong></summary>
    
- Node.js is a **cross-platform, open-source JavaScript** runtime that executes code outside of a browser.
- Node.js processes requests asynchronously, making it well-suited for **I/O-heavy applications**.
</details>

---

<details>
    <summary><strong>Why use Node.js?</strong></summary>
    
- Node.js is a good choice when you need **high-throughput, real-time applications like chat servers, APIs, or streaming services.** Its **non-blocking architecture** means it can handle many concurrent connections without spawning a new thread for each one. The npm ecosystem also gives access to a large library of reusable packages.
</details>

---

<details>
    <summary><strong>History of Node.js</strong></summary>
    
- Node.js was first released in 2009 by Ryan Dahl, who wanted a way to build scalable network applications using JavaScript. The project was eventually forked in 2014 to create io.js, which was later merged back in 2015 under the Node.js Foundation. Since then, it has grown into one of the most widely used server-side runtimes.
</details>

---

<details>
    <summary><strong>Node.js vs Browser</strong></summary>
    
- Node.js and the browser both run JavaScript but in different environments with different APIs. The browser provides access to the DOM, window, and browser-specific APIs, while Node.js provides access to the file system, operating system, and network. Code written for one environment does not always work in the other without adjustments.
</details>

---

<details>
    <summary><strong>Running Node.js Code</strong></summary>
    
- You can run Node.js code from the terminal using the node command followed by a filename. For quick experiments, Node.js also includes a REPL (Read-Eval-Print Loop) that lets you execute JavaScript interactively. Understanding how to run scripts and interpret output is the starting point for working with Node.js.
</details>

---

<details>
    <summary><strong>CommonJS vs ESM</strong></summary>
    
- CommonJS and ES (EcmaScript) are module systems used in Node. CommonJS is the default module system. However, a new module system was recently added to NodeJS - ES modules. CommonJS modules use the require() statement for module imports and module.exports for module exports while it's import and export for ES.
</details>

---

<details>
    <summary><strong>ESM</strong></summary>
    
- ESM (ECMAScript Modules) is a standardized module system in JavaScript that allows for the organized, maintainable, and reusable structuring of code. It uses import and export statements for including and sharing functions, objects, or primitives between files. ESM supports static analysis, enabling better optimization and tooling, and is always in strict mode to reduce common JavaScript issues. Node.js fully supports ESM, which can be used with **.mjs** file extensions or configured in the package.json for .js files, making it easier to write modular and efficient JavaScript applications.
</details>

---

<details>
    <summary><strong>Node.js Modules</strong></summary>
    
- We split our code into different files to maintain, organize and reuse code whenever possible. A module system allows us to split and include code and import code written by other developers whenever required. In simple terms, a module is nothing but a JavaScript file. Node.js has many built-in modules that are part of the platform and comes with Node.js installation, for example, HTTP, fs, path, and more.
</details>

---

<details>
    <summary><strong>Creating & Importing</strong></summary>
    
- Creating a module means writing JavaScript in a file and exporting the parts you want to share. Importing means pulling those exports into another file using require() in CommonJS or import in ESM. This mechanism is how Node.js applications are structured into separate, connected files.
</details>

---

<details>
    <summary><strong>global keyword</strong></summary>
    
- In browsers, the top-level scope is the global scope, and its global object is called the window object. Within the browser, var something will define a new global variable inside the window object. In Node.js, this is different. The top-level scope is not the global scope; var something inside a Node.js module will be local to that module.
</details>
</details>

---

<details>
    <summary><strong>NPM</strong></summary>
    
- npm (Node Package Manager) is the default package manager for Node.js. It lets you install, update, and manage third-party libraries and tools for your project. npm also provides a registry at npmjs.com where developers publish and share their packages.

<details>
    <summary><strong>npx</strong></summary>
    
npx is a tool that comes with npm and lets you run Node.js packages without installing them globally. It downloads and executes the package in a temporary environment, which is useful for running CLI tools like scaffolding scripts or code generators. It avoids cluttering your global environment with one-off tools.
</details>

---

<details>
    <summary><strong>Installing Packages</strong></summary>
    
<details>
    <summary><strong>Global Installation</strong></summary>
    
- A global npm installation places a package in a system-wide location, making it available as a command-line tool from any directory. You use it for tools you want to run across multiple projects, like CLI utilities. It is done with the -g flag: npm install -g <package>.
</details>

---

<details>
    <summary><strong>Local Installation</strong></summary>
    
- Locally installed packages are available only to the project where the packages are installed, while the globally installed packages can be used any where without installing them into a project. Another use case of the global packages is when using CLI tools.
</details>
</details>

---

<details>
    <summary><strong>Updating Packages</strong></summary>
    
- npm provides various features to help install and maintain the project's dependencies. Dependencies get updates with new features and fixes, so upgrading to a newer version is recommended. We use npm update commands for this.
</details>

---

<details>
    <summary><strong>Running Scripts</strong></summary>
    
- In Node.js, npm scripts are used for the purpose of initiating a server, starting the build of a project, and also for running the tests. We can define this scripts in the package.json file of the folder. Also, we can split the huge scripts into many smaller parts if it is needed.
</details>

---

<details>
    <summary><strong>npm workspaces</strong></summary>
    
- npm workspaces allow you to manage multiple packages within a single repository (monorepo). You define workspace packages in the root package.json, and npm handles linking them together during installation. This makes it easier to share code between packages and run scripts across the whole project.
</details>

---

<details>
    <summary><strong>Creating Packages</strong></summary>
    
- npm packages allow you to bundle some specific functionality into a reusable package which can then be uploaded to some package registry such as npm or GitHub packages and then be installed and reused in projects using npm.
</details>

---

<details>
    <summary><strong>Semantic Versioning</strong></summary>
    
- Semantic versioning (SemVer) is a versioning convention used by npm packages. Version numbers follow the format MAJOR.MINOR.PATCH, where breaking changes increment the major number, new features increment the minor, and bug fixes increment the patch. Understanding SemVer helps you manage dependency updates without introducing breaking changes.
</details>
</details>

---

<details>
    <summary><strong>Error Handling</strong></summary>
    
- Error handling is a way to find bugs and solve them as quickly as humanly possible. The errors in Node.js can be either operation or programmer errors.

<details>
    <summary><strong>Types of Errors</strong></summary>
    
<details>
    <summary><strong>System Errors</strong></summary>
    
- System errors occur when Node.js interacts with the underlying operating system and the operation fails. Examples include trying to read a file that does not exist or a network connection being refused. These errors are instances of the SystemError class and include properties like code and syscall to help identify the cause.
</details>

---

<details>
    <summary><strong>User Specified Errors</strong></summary>
    
- User specified errors can be created by extending the base Error object, a built-in error class. When creating errors in this manner, you should pass a message string that describes the error. This message can be accessed through the message property on the object. The Error object also contains a name and a stack property that indicate the name of the error and the point in the code at which it is created.
</details>

---

<details>
    <summary>Assertion Errors</summary>
    
An AssertionError in Node.js is an error that is thrown when the assert module determines that a given expression is not truthy. The assert module is a built-in Node.js module that provides a simple set of assertion tests that can be used to test the behavior of your code.
</details>

---

<details>
    <summary><strong>JavaScript Errors</strong></summary>
    
- JavaScript errors are runtime errors thrown by the language itself, such as TypeError, RangeError, and ReferenceError. These occur when code tries to perform an invalid operation, like calling a method on undefined. They can be caught using try/catch blocks or error event listeners.
</details>
</details>

---

<details>
    <summary><strong>Uncaught Exceptions</strong></summary>
    
- An uncaught exception is an error that is not handled anywhere in the application, causing the Node.js process to crash. You can listen for these with the process.on('uncaughtException', ...) event, though it should be used carefully and mainly for logging before shutting down gracefully. Relying on it as a catch-all is considered bad practice.
</details>

---

<details>
    <summary><strong>Async errors</strong></summary>
    
- Errors must always be handled. If you are using synchronous programming you could use a try catch. But this does not work if you work asynchronous! Async errors will only be handled inside the callback function!
</details>

---

<details>
    <summary><strong>Callstack / Stack Trace</strong></summary>
    
- The stack trace is used to trace the active stack frames at a particular instance during the execution of a program. The stack trace is useful while debugging code as it shows the exact point that has caused an error.
</details>

---

<details>
    <summary><strong>Using Debugger</strong></summary>
    
- Node.js includes a built-in debugger that can be activated with the --inspect flag or the debugger keyword in code. It lets you pause execution, step through code, and inspect variables at runtime using Chrome DevTools or a compatible IDE. Using a debugger is more efficient than adding console.log statements throughout the code.
</details>

</details>

---

<details>
    <summary><strong>Async Programming</strong></summary>

- Async Programming

<details>
    <summary><strong>Event Emitter</strong></summary>
    
- In Node.js, an event can be described simply as a string with a corresponding callback. An event can be "emitted" (or, in other words, the corresponding callback be called) multiple times or you can choose to only listen for the first time it is emitted.
</details>

---

<details>
    <summary><strong>Event Loop</strong></summary>
    
- The Event Loop is one of the most critical aspects of Node.js. Why is this so important? Because it explains how Node.js can be asynchronous and have non-blocking I/O, it explains the "killer feature" of Node.js, which made it this successful.
</details>

---

- Writing Async Code
<details>
    <summary><strong>Promises</strong></summary>

- A promise is an object representing the eventual result of an async operation. It can be in one of three states: pending, fulfilled, or rejected. Promises provide .then() and .catch() methods for chaining operations, and they are the foundation for async/await.
</details>

---

<details>
    <summary><strong>Async/Await</strong></summary>
    
- Async/Await is a special syntax to work with promises in a more comfortable fashion. It's easy to understand and use. Adding the keyword async before a function ensures that the function returns a promise and the keyword await makes JavaScript wait until that promise settles and returns the result.
</details>

---

<details>
    <summary><strong>Callbacks</strong></summary>
    
- Node.js, being an asynchronous platform, doesn't wait around for things like file I/O to finish - Node.js uses callbacks. A callback is a function called at the completion of a given task; this prevents any blocking, and allows other code to be run in the meantime.
</details>

---

<details>
    <summary><strong>setTimeout</strong></summary>
    
- setTimeout() executes a callback function once, after a specified delay in milliseconds. It does not block other code from running while waiting. It is one of the simplest ways to introduce asynchronous behavior in Node.js.
</details>

---

<details>
    <summary><strong>setInterval</strong></summary>
    
- setInterval() repeatedly executes a callback function at a fixed time interval, in milliseconds. It keeps running until cleared with 
- clearInterval(). It is commonly used for polling, health checks, or any task that needs to run on a schedule.
</details>

---

<details>
    <summary><strong>setImmediate</strong></summary>
    
- setImmediate() schedules a callback to run in the check phase of the event loop, after I/O events have been processed. It is similar to setTimeout(fn, 0) but is guaranteed to run before any timers in some cases. It is used when you want to yield control to the event loop before continuing execution.
</details>

---

<details>
    <summary><strong>process.nextTick()</strong></summary>
    
- Every time the event loop takes a full trip, we call it a tick. When we pass a function to process.nextTick(), we instruct the engine to invoke this function at the end of the current operation before the next event loop tick starts.
</details>
</details>

---

<details>
    <summary><strong>Working with Files</strong></summary>
    
- You can programmatically manipulate files in Node.js with the built-in fs module. The name is short for “file system,” and the module contains all the functions you need to read, write, and delete files on the local machine.

<details>
    <summary><strong>__dirname</strong></summary>
    
- The __dirname in a node script returns the path of the folder where the current JavaScript file resides. __filename and __dirname are used to get the filename and directory name of the currently executing file.
</details>

---

<details>
    <summary><strong>__filename</strong></summary>
    
- The __filename in Node.js returns the filename of the executed code. It gives the absolute path of the code file. The following approach covers implementing __filename in the Node.js project.
</details>

---

<details>
    <summary><strong>process.cwd()</strong></summary>
    
- process.cwd() returns the current working directory of the Node.js process, which is the directory from which the script was launched. Unlike __dirname, it reflects the shell's working directory, not the file's location. It is useful when your application needs to resolve paths relative to where it was started.
</details>

---

<details>
    <summary><strong>path module</strong></summary>
    
- The path module provides utilities for working with file and directory paths. It's built-in to Node.js core and can simply be used by requiring it.
</details>

---

<details>
    <summary><strong>fs module</strong></summary>
    
- File System or fs module is a built in module in Node that enables interacting with the file system using JavaScript. All file system operations have synchronous, callback, and promise-based forms, and are accessible using both CommonJS syntax and ES6 Modules.
</details>

---

<details>
    <summary><strong>Open Source Packages</strong></summary>
    
<details>
    <summary><strong>glob</strong></summary>
    
- glob is an npm package for matching files using shell-style wildcard patterns. For example, **/*.js matches all JavaScript files in all subdirectories. It is used in build tools, test runners, and any script that needs to find files matching a pattern.
</details>

---

<details>
    <summary><strong>globby</strong></summary>
    
- globby is a modern alternative to glob that supports promises and multiple patterns at once. It builds on top of fast-glob and provides a cleaner API. It is used when you need to match files asynchronously or want a more ergonomic interface than the original glob package.
</details>

---

<details>
    <summary><strong>fs-extra</strong></summary>
    
- fs-extra adds file system methods that aren't included in the native fs module and adds promise support to the fs methods. It also uses graceful-fs to prevent EMFILE errors. It should be a drop in replacement for fs.
</details>

---

<details>
    <summary><strong>chokidar</strong></summary>
    
- Chokidar is an npm package for watching file system changes. It wraps Node.js's native fs.watch and fs.watchFile with a more reliable and consistent API. It is widely used in development tools like Webpack and Vite to trigger rebuilds when files change.
</details>
</details>
</details>

---

<details>
    <summary><strong>Command Line Applications | Command Line Interface</strong></summary>
    
- Command Line Applications are applications that can be run from the command line. They are also called CLI (Command Line Interface) applications. Users can interact with clients entirely by terminal commands. They are very useful for automation and building tools.

<details>
    <summary><strong>Environment Variables</strong></summary>
    
<details>
    <summary><strong>process.env</strong></summary>
    
- process.env is a Node.js object that contains all environment variables available to the current process. These can be set in the shell, in a .env file via a library like dotenv, or by the deployment platform. Configuration values like port numbers, API keys, and database URLs are commonly stored and accessed this way.
</details>

---

<details>
    <summary><strong>Dotenv Package</strong></summary>
    
- dotenv is an npm package that loads environment variables from a .env file into process.env. It is commonly used in development to manage configuration like API keys and database URLs without hardcoding them in source code. The .env file should not be committed to version control.
</details>
</details>

---

<details>
    <summary><strong>Taking Inputs</strong></summary>

<details>
    <summary><strong>process.stdin</strong></summary>
    
- process.stdin is a stream in Node.js that represents the standard input, typically the keyboard. It allows your Node.js programs to receive text input from the command line. The readline module provides a convenient interface for reading input from process.stdin line by line, making it easier to handle user input in interactive command-line applications.
</details>

---

<details>
    <summary><strong>Inquirer Package</strong></summary>
    
- Inquirer.js is a popular npm package for building rich, interactive command-line interfaces. It supports many input types including text, passwords, lists, checkboxes, and confirmations. It is a good choice for CLIs that require multi-step input flows.
</details>

---

<details>
    <summary><strong>prompts package</strong></summary>

- prompts is a lightweight npm package for building interactive command-line interfaces. It provides a simple API for prompting users with questions and collecting their answers in various formats, like text input, confirmations, and selections. It supports keyboard navigation and works well in scripts that need user input.
</details>
</details>

---

<details>
    <summary><strong>Printing Output</strong></summary>
    
<details>
    <summary><strong>Process stdout</strong></summary>
    
- The process.stdout property is an inbuilt application programming interface of the process module which is used to send data out of our program. A Writable Stream to stdout. It implements a write() method. console.log() prints to the process.stdout.write() with formatted output or new line.
</details>

---

<details>
    <summary><strong>chalk package</strong></summary>
    
- chalk is an npm package for styling terminal output with colors and formatting like bold, underline, and italic. It is used to make CLI output more readable by highlighting errors in red, success messages in green, and so on. It works across different terminal environments.
</details>

---

<details>
    <summary><strong>figlet package</strong></summary>
    
- figlet is an npm package that renders text as ASCII art using large, decorative fonts. It is typically used in CLI tools to display a stylized application name or welcome message at startup. The output is plain text made up of characters arranged to form letters.
</details>

---

<details>
    <summary><strong>cli-progress</strong></summary>
    
- cli-progress is an npm package for displaying progress bars in the terminal. It is useful for long-running operations like file downloads, database migrations, or batch processing where you want to show completion percentage. It supports multiple bars and customizable styles
</details>

</details>

---

<details>
    <summary><strong>Command Line Args</strong></summary>
    
<details>
    <summary><strong>process.argv</strong></summary>
    
- process.argv is an array containing the command-line arguments passed to the Node.js process. The first two elements are the path to Node.js and the script file; the remaining elements are the arguments provided by the user. Parsing process.argv manually is the lowest-level way to read CLI input.
</details>

---

<details>
    <summary><strong>Commander.js</strong></summary>
    
- Commander is a light-weight, expressive, and powerful command-line framework for node.js. with Commander.js you can create your own command-line interface (CLI).
</details>
</details>

</details>

---

<details>
    <summary><strong>Building & Consuming APIs</strong></summary>
    
- Node.js is commonly used to build HTTP APIs that other clients consume, as well as to consume external APIs from within your application. Building an API involves defining routes, handling requests, and returning responses. Consuming an API involves making HTTP requests and processing the returned data.

<details>
    <summary><strong>Frameworks</strong></summary>
    
<details>
    <summary><strong>Express.js</strong></summary>
    
- Express.js is the most widely used Node.js web framework. It provides a minimal set of features for routing HTTP requests and adding middleware. Its simplicity and large ecosystem of plugins make it a popular choice for building APIs and web applications of all sizes.
</details>

---

<details>
    <summary><strong>fastify</strong></summary>
    
- Fastify is a high-performance web framework for Node.js. It is designed to have low overhead and high throughput, making it one of the fastest Node.js HTTP frameworks available. It includes a built-in schema-based validation and serialization system and has a plugin architecture for extending functionality.
</details>

---

<details>
    <summary><strong>NestJS</strong></summary>
    
- NestJS is a framework for building server-side Node.js applications. It uses TypeScript by default and draws heavily from Angular's architecture, using decorators, modules, and dependency injection. It is designed for building scalable, maintainable applications and is well-suited for complex, enterprise-grade APIs.
</details>

---

<details>
    <summary><strong>Hono</strong></summary>
    
- Hono is a lightweight, simple, and fast web framework for Cloudflare Workers, Deno, Bun, and other applications. It is a modern web application that is both fast and flexible. It offers inbuilt support for TypeScript, and easy development in a local environment. Using Hono, It is easy to create publishable web applications with Deno, Bun, and Cloudflare Workers.
</details>
</details>

---

<details>
    <summary><strong>Making API Call</strong></summary>
    
<details>
    <summary><strong>http module</strong></summary>
    
- The http module is Node.js's built-in module for creating HTTP servers and making HTTP requests. It provides low-level access to the HTTP protocol, giving you full control over request and response handling. Most developers use a framework like Express or a library like Axios on top of it.
</details>

---

<details>
    <summary><strong>Axios</strong></summary>
    
- Axios is a promise-based HTTP Client for node.js and the browser. Used for making requests to web servers. On the server-side it uses the native node.js http module, while on the client (browser) it uses XMLHttpRequests.
</details>

---

<details>
    <summary><strong>Ky</strong></summary>
    
- Ky is a tiny and elegant HTTP client based on the browser Fetch API. Ky targets modern browsers and Deno.For older browsers, you will need to transpile and use a fetch polyfill.For Node.js, check out Got.. 1 KB (minified & gzipped), one file, and no dependencies.
</details>

---

<details>
    <summary><strong>fetch</strong></summary>
    
- The fetch() method in JavaScript is used to request to the server and load the information on the webpages. The request can be of any APIs that return the data of the format JSON or XML. This method returns a promise.
</details>

---

<details>
    <summary><strong>Got Package</strong></summary>
    
- Got is a lighter, human-friendly, and powerful HTTP request library explicitly designed to work with Node.js. It supports pagination, RFC compliant caching, makes an API request again if it fails, supports cookies out of the box, etc.
</details>
</details>
</details>

---

<details>
    <summary><strong>Monitor Changes (Dev)</strong></summary>
    
- Keep App Running

- In Node.js, you need to restart the process to make changes take effect. This adds an extra step to your workflow. You can eliminate this extra step by using nodemon to restart the process automatically. Since Node.js 18.11.0, you can run Node with the --watch flag to reload your app every time a file is changed. So you don't need to use nodemon anymore.

<details>
    <summary><strong>--watch</strong></summary>
    
- node --watch your_script.js
- Whenever a change is detected, Node.js automatically restarts the script
</details>

---

<details>
    <summary><strong>Nodemon</strong></summary>
    
- In Node.js, you need to restart the process to make changes take effect. This adds an extra step to your workflow. You can eliminate this extra step by using nodemon or PM2 to restart the process automatically. nodemon is a command-line interface (CLI) utility developed by rem that wraps your Node app, watches the file system, and automatically restarts the process.
</details>
</details>

---

<details>
    <summary><strong>Template Engines</strong></summary>
    
- Template engines allow you to generate HTML dynamically by combining HTML structure with data. In Node.js, they are used in **server-side rendered applications** to produce HTML pages on the server before sending them to the client. Common template engines include EJS, Pug, and Marko.

<details>
    <summary><strong>EJS</strong></summary>
    
- EJS is a template language or engine that allows you to generate HTML markup with pure JavaScript. And this is what makes it perfect for Nodejs applications. In simple words, the EJS template engine helps to embed JavaScript into your HTML template easily.
</details>

---

<details>
    <summary><strong>Pug</strong></summary>

- Pug is a JavaScript template engine. It is a high-performance template engine heavily influenced by Haml and implemented with JavaScript for Node.js and browsers. Pug was formerly called Jade. Pug is a high-performance template engine heavily influenced by Haml and implemented with JavaScript for Node.js and browsers
</details>

---

<details>
    <summary><strong>Marko</strong></summary>
    
- Marko is a fast and lightweight HTML-based templating engine that compiles templates to CommonJS modules and supports streaming, async rendering, and custom tags. It is HTML re-imagined as a language for building dynamic and reactive user interfaces.
</details>
</details>

---

<details>
    <summary><strong>Working with Databases</strong></summary>
    
<details>
    <summary><strong>NoSQL</strong></summary>
    
<details>
    <summary><strong>Mongoose</strong></summary>
    
- Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node.js. Mongoose provides a straight-forward, schema-based solution to model your application data. It includes built-in type casting, validation, query building, business logic hooks and more, out of the box.
</details>

---

<details>
    <summary><strong>Prisma</strong></summary>
    
- Prisma provides an open source next-generation ORM in the TypeScript ecosystem. It offers a dedicated API for relation filters. It provides an abstraction layer that makes you more productive compared to writing SQL. Prisma currently supports PostgreSQL, MySQL, SQL Server, SQLite, MongoDB and CockroachDB.
</details>

---

<details>
    <summary><strong>Native Drivers (NoSQL)</strong></summary>
    
- Native database drivers are npm packages provided by database vendors that let Node.js communicate directly with a NoSQL database. For example, the official MongoDB driver connects to MongoDB and lets you run queries against it. Using a native driver gives you full control but requires writing raw query logic yourself.
</details>
</details>

---

<details>
    <summary><strong>Relational</strong></summary>
    
<details>
    <summary><strong>Drizzle</strong></summary>
    
- Drizzle lets you build your project the way you want, without interfering with your project or structure. Using Drizzle you can define and manage database schemas in TypeScript, access your data in a SQL-like or relational way, and take advantage of opt-in tools to make your developer experience amazing.
</details>

---
<details>
    <summary><strong>TypeORM</strong></summary>
    
- TypeORM is an ORM that can run in NodeJS, Browser, Cordova, PhoneGap, Ionic, React Native, NativeScript, Expo, and Electron platforms and can be used with TypeScript and JavaScript (ES5, ES6, ES7, ES8). Its goal is to always support the latest JavaScript features and provide additional features that help you to develop any kind of application that uses databases - from small applications with a few tables to large scale enterprise applications with multiple databases.
</details>

---

<details>
    <summary><strong>Knex</strong></summary>
    
- Knex.js is a "batteries included" SQL query builder for PostgreSQL, CockroachDB, MSSQL, MySQL, MariaDB, SQLite3, Better-SQLite3, Oracle, and Amazon Redshift designed to be flexible, portable, and fun to use.
</details>

---

<details>
    <summary><strong>Sequelize</strong></summary>
    
- Sequelize is a mature ORM for Node.js that supports PostgreSQL, MySQL, MariaDB, SQLite, and MSSQL. It provides model definitions, associations, query building, and migration support. It uses a promise-based API and has been in the ecosystem for many years.
</details>

---

<details>
    <summary><strong>Prisma</strong></summary>
    
- Prisma is an ORM that helps app developers build faster and make fewer errors. Combined with its Data Platform developers gain reliability and visibility when working with databases.
</details>

---

<details>
    <summary><strong>Native Drivers (Relational)</strong></summary>
    
- Native drivers for relational databases let Node.js connect to databases like PostgreSQL or MySQL directly. Examples include the pg package for PostgreSQL and mysql2 for MySQL. They give you direct access to the database and let you run raw SQL queries.
</details>
</details>
</details>

---

<details>
    <summary><strong>Testing</strong></summary>
    
- Software testing is the process of verifying that what we create is doing exactly what we expect it to do. The tests are created to prevent bugs and improve code quality. The two most common testing approaches are unit testing and end-to-end testing. In the first, we examine small snippets of code, in the second, we test an entire user flow.

<details>
    <summary><strong>Vitest</strong></summary>
    
- Vitest is a Vite-native unit testing framework that's Jest-compatible. Vitest is a powerful testing library built on top of Vite that is growing in popularity. You can use Vitest for a range of testing needs, such as unit, integration, end-to-end (E2E), snapshot, and performance testing of functions and components. ESM, TypeScript, JSX. Out-of-box ESM, TypeScript and JSX support powered by esbuild. Vitest is free and open source.
</details>

---

<details>
    <summary><strong>Jest</strong></summary>
    
- Jest is a delightful JavaScript Testing Framework with a focus on simplicity. It works with projects using: Babel, TypeScript, Node, React, Angular, Vue and more!
</details>

---

<details>
    <summary><strong>node:test</strong></summary>
    
- node:test is Node.js's built-in test runner, added in version 18. It provides a simple API for writing and running tests without any additional dependencies. For projects that want minimal tooling, it is a practical alternative to third-party frameworks.
</details>

---

<details>
    <summary><strong>Cypress</strong></summary>
    
- Cypress is an end-to-end testing framework designed for web applications. It runs tests directly in the browser and provides a visual test runner for debugging. It is primarily used for testing user interactions in the browser rather than pure Node.js code.
</details>

---

<details>
    <summary><strong>Playwright</strong></summary>
    
- Playwright is a browser automation and end-to-end testing tool developed by Microsoft. It supports multiple browsers (Chromium, Firefox, WebKit) and allows you to write tests that simulate real user behavior. It can also be used for scraping and automating web-based workflows.
</details>
</details>

---

<details>
    <summary><strong>Keep your app running in Production</strong></summary>
    
- PM2 lets you run your nodejs scripts forever. In the event that your application crashes, PM2 will also restart it for you..

<details>
    <summary><strong>Pm2</strong></summary>
    
- PM2 is a production process manager for Node.js applications with a built-in load balancer. It allows you to keep applications alive forever, to reload them without downtime and to facilitate common system admin tasks.
</details>
</details>

---

<details>
    <summary><strong>Node.js Logging</strong></summary>
    
- Logging is an essential part of understanding the complete application life cycle of the Node.js application. We can much more easily and quickly fix errors by looking at logs throughout the development process, from creating to debugging to designing new features. Error, warn, info, and debug are the four basic logging levels in Node.js. Logging involves persistently collecting information about an application's runtime behaviour.

<details>
    <summary><strong>Winston</strong></summary>
    
- winston is designed to be a simple and universal logging library with support for multiple transports. A transport is essentially a storage device for your logs. Each winston logger can have multiple transports configured at different levels. For example, one may want error logs to be stored in a persistent remote location (like a database), but all logs output to the console or a local file.
</details>

---

<details>
    <summary><strong>Morgan</strong></summary>
    
- Morgan is a NodeJS and express.js middleware to log the HTTP request and error, simplifying the debugging process. It provides flexibility in defining the format of log messages and helps override the output destination for your logs.
</details>
</details>

---

<details>
    <summary><strong>Nodejs Threads</strong></summary>
    
- Node.js is a single-threaded language and gives us ways to work parallelly to our main process. Taking note of nowadays multicore system single threading is very memory efficient.

<details>
    <summary><strong>Child Process</strong></summary>
    
- The child_process module gives the node the ability to run the child process, established through IPC (inter-process communication) by accessing operating system commands. The three main methods inside this module are : child_process.spawn() child_process.fork() child_process.exec()
</details>

---

<details>
    <summary><strong>Cluster</strong></summary>
    
- The Cluster module allows you to easily create child processes that each runs simultaneously on their own single thread, to handle workloads among their application threads.
</details>

---

<details>
    <summary><strong>Worker Threads</strong></summary>
    
- Worker thread is a continuous parallel thread that runs and accepts messages until it is explicitly closed or terminated. With worker threads, we can achieve a much efficient application without creating a deadlock situation. Workers, unlike children's processes, can exchange memory.
</details>
</details>

---

<details>
    <summary><strong>Streams</strong></summary>
    
- Streams in Node.js are objects that let you read or write data in chunks, rather than loading everything into memory at once. They are useful for handling large files, HTTP requests, or any data that comes in over time. There are four types: readable, writable, duplex (both), and transform (modifies data as it passes through).
</details>

---

<details>
    <summary><strong>Garbage Collection</strong></summary>
    
- Memory management in JavaScript is performed automatically and invisibly to us. We create primitives, objects, functions… All that takes memory. The main concept of memory management in JavaScript is reachability.
</details>

---

<details>
    <summary><strong>Debugging</strong></summary>
    
- Debugging is the process of identifying and fixing issues in a Node.js application. Node.js provides built-in debugging capabilities via the --inspect flag, which connects to Chrome DevTools. Effective debugging involves using breakpoints, inspecting variables at runtime, and understanding the call stack.

<details>
    <summary><strong>Memory Leaks</strong></summary>
    
- Memory leaks are caused when your Node.js app’s CPU and memory usage increases over time for no apparent reason. In simple terms, a Node.js memory leak is an orphan block of memory on the Heap that is no longer used by your app because it has not been released by the garbage collector. It’s a useless block of memory. These blocks can grow over time and lead to your app crashing because it runs out of memory.
</details>

<details>
    <summary><strong>Using APM</strong></summary>
    
- APM (Application Performance Monitoring) tools provide real-time visibility into the performance of a Node.js application in production. They track metrics like response times, error rates, memory usage, and database query performance. Popular APM tools for Node.js include Datadog, New Relic, and Elastic APM.
</details>
</details>

---

<details>
    <summary><strong>Nodejs core modules</strong></summary>
    
- These are the core modules that come with Node.js out of the box. This module provides tools or APIs for performing out certain standard Node.js operations. like interacting with the file system, url parsing, or logging information to the console.

- fs module
- url module
- console module
- util module
- events module
- os module
- worker threads module
- child process module
- process object
- crypto module
</details>
