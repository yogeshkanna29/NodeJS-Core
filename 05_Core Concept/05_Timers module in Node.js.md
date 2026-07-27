# Timers module in Node.js

The Timers module in Node.js allows execution of code after a specified delay or at repeated intervals. It is a global module, so it can be used without importing it.

- Helps control when and how often a function runs in an application.
- Useful for creating delays, scheduling tasks, and handling asynchronous events.
- Works with the Node.js event loop to manage timed callbacks.
- Widely used in server operations, background tasks, and periodic updates.

<details>
    <summary><strong>Types of Timers</strong></summary>
    
In Node.js, timers can be categorized into two types based on their purpose.

<details>
    <summary><strong>A. Scheduling Timers</strong></summary>
    
Scheduling timers allow functions to execute after a delay or at repeated intervals. They help manage timed and asynchronous execution of code.

- Used to schedule tasks and control delayed or repeated execution of functions without blocking the event loop.
- Useful for handling asynchronous operations and timed callbacks in applications.

<details>
    <summary><strong>1. setImmediate() method</strong></summary>
    
schedules a callback to execute immediately after I/O events in the event loop. Callbacks run in the order they are created after each event loop iteration.

```js
setImmediate(function A() {
    setImmediate(function B() {
        console.log(1);
        setImmediate(function D() {
            console.log(2);
        });
    });
    setImmediate(function C() {
        console.log(3);
        setImmediate(function E() {
            console.log(4);
        });
    });
});
console.log('Started...');
```
Output
```
Started...
1
3
2
4
```

A runs first and schedules B and C using setImmediate().
B and C execute in the next iterations, printing 1 and 3, and they schedule D and E.
D and E run later, printing 2 and 4, because nested setImmediate() callbacks execute in subsequent event loop iterations.
</details>

<details>
    <summary><strong>2. setInterval() method</strong></summary>
    
repeatedly executes a callback function after every specified time interval (in milliseconds) until it is stopped using clearInterval().

```js
// Executed after every 1000 milliseconds
// from the start of the program
setInterval(function A() {
    return console.log('Hello World!');
}, 1000);
// Executed right away
console.log('Executed before A...');
```
Output
```
Executed before A...
Hello World!
Hello World!
Hello World!
Hello World!
Hello World!
...
```
</details>



<details>
    <summary><strong>3. setTimeout() method</strong></summary>

schedules the execution of a callback function once after a specified delay (in milliseconds).

```js
// Executed after 3000 milliseconds 
// from the start of the program
setTimeout(function A() {
    return console.log('Hello World!');
}, 3000);
// executed right away
console.log('Executed before A...');
```

Output
```
Executed before A...
Hello World!
```
</details>
</details>

---

<details>
    <summary><strong>B. Canceling Timers</strong></summary>
    
Canceling timers is used to stop or prevent the execution of previously scheduled timer functions. It helps control timer-based operations in Node.js applications.

- Allows stopping timers that were scheduled for future execution.
- Helps prevent unnecessary or repeated execution of callbacks.
- Useful for managing and controlling asynchronous tasks.

<details>
    <summary><strong>1. clearImmediate() method</strong></summary>
    
cancels an Immediate object created by setImmediate(), preventing the scheduled callback from executing.

```js
let si = setImmediate(function A() {
    console.log(1);
});
// clears setInterval si
clearImmediate(si);
console.log(2);
```
</details>

<details>
    <summary><strong>2. clearInterval() method</strong></summary>
    
cancels the timer created by setInterval(), stopping the repeated execution of the callback function.

```js
let si = setInterval(function A() {
    return console.log("Hello World!");
}, 500);
setTimeout(function () {
    clearInterval(si);
}, 2000);
```
Output
```
Hello World!
Hello World!
Hello World!
Hello World!
```
</details>

<details>
    <summary><strong>3. clearTimeout() method</strong></summary>
    
cancels the timer created by setTimeout(), preventing the scheduled callback from executing.

```js
// si1 is cleared by clearTimeout()
let si1 = setTimeout(function A() {
    return console.log("Hello World!");
}, 3000);
// only si2 is executed
let si2 = setTimeout(function B() {
    return console.log("Hello Geeks!");
}, 3000);
clearTimeout(si1);
```
Output
```
Hello Geeks!
```
</details>

</details>
</details>

---