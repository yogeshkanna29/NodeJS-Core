# Restart Node.js Server Automatically with Nodemon

Nodemon is a development utility for Node.js that monitors project files and automatically restarts the server whenever changes are detected, streamlining the development workflow.

- Automatically detects file changes and restarts the application
- Automatically restarts the application after code updates.
- Enhances development speed and efficiency and is intended for development use only.

<strong>Installation of Nodemon</strong>
Below are the following steps by which we can automatically restart the NodeJS server with Nodemon.

After creating an express application,

Step 1: Create the app.js file.

```js
const express = require('express');
const app = express();
const port = 3000;

// Simple route
app.get('/', (req, res) => {
    res.send('Hello, World!');
});

// Start the server
app.listen(port, () => {
    console.log(`Server is running on http://localhost:${port}`);
});
```

Step 2: Install Nodemon Globally
To install Nodemon globally on your system, run the following command:

```js
npm install -g nodemon
```

Step 3: Create a Nodemon Script in package.json
To simplify running the server with Nodemon, add a script in the package.json file under the "scripts" section:
```json
"scripts": {
    "start": "nodemon app.js"
}
```

This configuration runs app.js using Nodemon when you execute npm start.

Step 4: Run Your Project with Nodemon
Now, instead of running node app.js, you can start the server with Nodemon using:
```bash
npm start
```

Automatically restarts the server when changes are saved in app.js or other monitored files.
Reflects code updates instantly without manual restarts.
Improves development efficiency by providing immediate feedback.

---

<strong>Nodemon’s Benefits for Development</strong>

Here are some of the benefits of using Nodemon for your NodeJS development:

- Improved Workflow: Automatically restarts the server, saving development time.
- Real-time Updates: Detects file changes and reloads the application instantly.
- Flexibility: Offers configurable options to customize behavior.
- Speed: Reduces manual effort, allowing focus on coding and testing.
- Integration with package.json: Easily integrates using npm/yarn and script configuration.

