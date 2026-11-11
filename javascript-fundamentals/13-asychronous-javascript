
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=ASYNCHRONOUS%20JAVASCRIPT&fontSize=28&fontColor=ffffff&animation=fadeIn&desc=Managing%20Operations%20That%20Take%20Time&descSize=12" width="100%">
</p>

<h1 align="center">MODULE 13: ASYNCHRONOUS JAVASCRIPT</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Asynchronous%20Programming-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-INTERMEDIATE-2E86C1?style=for-the-badge">
</p>

## Welcome!

So far, most of the JavaScript code you have written has executed one instruction after another.

However, real-world applications often perform operations that take time.

For example:

- Downloading information from an API.
- Loading images from a server.
- Reading files.
- Waiting for a timer.
- Communicating with a database.
- Sending information to an external service.

If JavaScript had to wait for every operation to finish before doing anything else, applications would become slow and unresponsive.

JavaScript supports **asynchronous programming**, which allows certain operations to be started without blocking the rest of the programme.

In this module, you will learn about synchronous and asynchronous execution, the JavaScript runtime, callbacks, timers, the event loop and the role of asynchronous operations.

## Learning Objectives

By the end of this module, you should be able to:

- Explain synchronous and asynchronous programming.
- Understand why asynchronous JavaScript is important.
- Understand the JavaScript call stack.
- Identify the roles of the browser runtime and Web APIs.
- Understand the task queue and microtask queue.
- Explain the event loop.
- Use `setTimeout()`.
- Use `setInterval()`.
- Cancel scheduled operations.
- Understand callback-based asynchronous code.
- Explain how asynchronous operations affect application execution.

---

## 1. What is Synchronous JavaScript?

Synchronous JavaScript executes instructions in sequence.

Each operation normally completes before the next instruction begins.

### Example

```javascript
console.log("First");

console.log("Second");

console.log("Third");
```

Output:

```text
First
Second
Third
```

JavaScript executes each statement in order.

### Understanding Synchronous Execution

1. The first statement executes.
2. The second statement executes.
3. The third statement executes.

This is straightforward, but some operations may take a long time.

---

## 2. What is Asynchronous JavaScript?

Asynchronous JavaScript allows certain operations to be initiated without requiring the entire programme to wait for their completion.

Other instructions can continue executing while an asynchronous operation is being handled.

### Example

```javascript
console.log("First");

setTimeout(() => {

    console.log("Second");

}, 2000);

console.log("Third");
```

Output:

```text
First
Third
Second
```

The second message appears later because the callback is scheduled to run after approximately two seconds.

### Understanding the Execution

1. JavaScript displays `First`.
2. `setTimeout()` schedules a callback.
3. JavaScript continues executing.
4. JavaScript displays `Third`.
5. After the timer delay has elapsed and the callback can run, `Second` is displayed.

The timer does not pause the entire JavaScript programme.

---

## 3. Why is Asynchronous Programming Important?

Modern applications depend on operations that may take an unpredictable amount of time.

Examples include:

| Operation | Why It May Take Time |
|---|---|
| API requests | Requires communication with a remote server |
| Database queries | Requires data retrieval or modification |
| File operations | Requires reading or writing data |
| Image loading | Requires retrieving image resources |
| Timers | Wait for a specified delay |
| User interactions | Depend on events from the user |

Asynchronous programming helps applications remain responsive while these operations are in progress.

---

## 4. Understanding the JavaScript Runtime

JavaScript execution involves more than the JavaScript engine.

In a browser, the runtime environment provides additional capabilities that help manage asynchronous operations.

Important components include:

- Call stack.
- JavaScript engine.
- Browser Web APIs.
- Task queue.
- Microtask queue.
- Event loop.

### A. JavaScript Engine

The JavaScript engine processes and executes JavaScript code.

Examples include:

- V8.
- SpiderMonkey.
- JavaScriptCore.

### B. Call Stack

The call stack keeps track of the functions currently being executed.

When a function is called, it is placed on the stack.

When the function completes, it is removed.

Example:

```javascript
function first() {

    second();

}

function second() {

    console.log("Second function");

}

first();
```

The call stack manages the execution order of these functions.

### C. Web APIs

Browsers provide Web APIs for operations such as:

- Timers.
- DOM events.
- Network requests.
- Browser storage.

These operations are not all performed directly by the JavaScript call stack.

### D. Task Queue

The task queue stores callbacks that are ready to be processed.

Examples include callbacks from timers and certain browser events.

### E. Microtask Queue

The microtask queue stores high-priority asynchronous callbacks.

Promise reactions, such as `.then()` and `.catch()` callbacks, are examples of microtasks.

### F. Event Loop

The event loop coordinates the execution of queued callbacks.

It checks whether the call stack is available and allows queued work to execute according to the runtime's scheduling rules.

---

## 5. Understanding the Event Loop

The event loop is an important part of JavaScript asynchronous execution.

It helps coordinate the call stack and the queues that hold scheduled callbacks.

### Simplified Execution Process

1. JavaScript executes synchronous code on the call stack.
2. An asynchronous operation is initiated.
3. The runtime manages the asynchronous operation.
4. When the operation is complete, its callback becomes eligible to run.
5. The event loop coordinates when queued callbacks can execute.
6. Microtasks are processed before the next task is selected, subject to the runtime's scheduling rules.

### Example

```javascript
console.log("Start");

setTimeout(() => {

    console.log("Timer");

}, 0);

console.log("End");
```

Output:

```text
Start
End
Timer
```

Even though the timer delay is zero, the callback does not interrupt the currently executing synchronous code.

The callback runs after the current JavaScript execution completes and the event loop can process it.

---

## 6. Using setTimeout()

The `setTimeout()` method schedules a function to execute after a specified delay.

### Syntax

```javascript
setTimeout(callback, delay);
```

| Parameter | Explanation |
|---|---|
| `callback` | Function to execute |
| `delay` | Minimum delay in milliseconds |

One second is equal to 1,000 milliseconds.

### Example

```javascript
console.log("Starting...");

setTimeout(() => {

    console.log("This message appears later.");

}, 3000);

console.log("Waiting...");
```

Output:

```text
Starting...
Waiting...
This message appears later.
```

### Example: Welcome Message

```javascript
function showWelcomeMessage() {

    console.log("Welcome to our application!");

}

setTimeout(showWelcomeMessage, 2000);
```

The welcome message is scheduled to appear after approximately two seconds.

**Important:** The delay is not an exact execution time. The callback runs after the specified delay when the runtime is able to process it.

---

## 7. Using setInterval()

The `setInterval()` method schedules a function to execute repeatedly after a specified interval.

### Syntax

```javascript
setInterval(callback, interval);
```

### Example

```javascript
let count = 1;

setInterval(() => {

    console.log(count);

    count++;

}, 1000);
```

Output:

```text
1
2
3
4
5
...
```

The function continues running approximately every second until it is stopped.

### Stopping an Interval

The `clearInterval()` method stops an interval.

Example:

```javascript
let count = 1;

const timer = setInterval(() => {

    console.log(count);

    count++;

    if (count > 5) {

        clearInterval(timer);

        console.log("Timer stopped.");

    }

}, 1000);
```

Output:

```text
1
2
3
4
5
Timer stopped.
```

### Difference Between setTimeout() and setInterval()

| Method | Purpose |
|---|---|
| `setTimeout()` | Schedules a callback once after a delay |
| `setInterval()` | Repeatedly schedules a callback at an interval |

---

## 8. Clearing a Timeout

The `clearTimeout()` method cancels a timeout that has not yet executed.

Example:

```javascript
const timer = setTimeout(() => {

    console.log("This message will not appear.");

}, 5000);

clearTimeout(timer);

console.log("Timeout cancelled.");
```

Output:

```text
Timeout cancelled.
```

The scheduled callback is cancelled before it executes.

### Example: Conditional Timeout

```javascript
const shouldContinue = false;

const timer = setTimeout(() => {

    console.log("Operation completed.");

}, 3000);

if (!shouldContinue) {

    clearTimeout(timer);

}
```

---

## 9. Understanding Callback-Based Asynchronous Code

A callback is a function passed into another function.

Callbacks can be used to execute code after an asynchronous operation completes.

### Example

```javascript
function loadUser(callback) {

    setTimeout(() => {

        const user = {
            name: "Alex",
            age: 21
        };

        callback(user);

    }, 2000);

}

function displayUser(user) {

    console.log(user.name);

    console.log(user.age);

}

loadUser(displayUser);
```

After the timer completes, the callback receives the user information.

### Understanding the Process

1. `loadUser()` is called.
2. A timer is scheduled.
3. JavaScript continues executing other code.
4. The timer callback runs later.
5. The user object is created.
6. `displayUser()` is called with the user object.

This demonstrates how callbacks can be used to process asynchronous results.

---

## 10. Callback Hell

Callback hell occurs when several asynchronous callbacks are nested inside one another.

This can make code difficult to read and maintain.

### Example

```javascript
setTimeout(() => {

    console.log("Step 1");

    setTimeout(() => {

        console.log("Step 2");

        setTimeout(() => {

            console.log("Step 3");

        }, 1000);

    }, 1000);

}, 1000);
```

As more operations are added, the code becomes increasingly difficult to manage.

Modern JavaScript provides Promises and `async/await` to improve asynchronous code organisation.

These concepts will be covered in the next module.

---

## 11. Practical Activity

### Activity: Countdown Timer

Create a JavaScript programme that displays a countdown from 10 to 0.

### Requirements

Your programme should:

1. Start at 10.
2. Display the current countdown value.
3. Decrease the value every second.
4. Stop automatically when it reaches zero.
5. Display a completion message.
6. Use `setInterval()`.
7. Use `clearInterval()`.

### Example Implementation

```javascript
// Countdown Timer

let countdown = 10;

console.log("COUNTDOWN STARTED");

const timer = setInterval(() => {

    console.log(countdown);

    countdown--;

    if (countdown < 0) {

        clearInterval(timer);

        console.log("Countdown completed!");

    }

}, 1000);
```

### Additional Tasks

1. Create a countdown that starts from a user-provided number.
2. Add a `setTimeout()` that displays a welcome message after three seconds.
3. Cancel a scheduled timeout.
4. Create a timer that displays the current count every second.
5. Display a message when the timer stops.

---

## 12. Knowledge Check

**1. What is synchronous JavaScript?**

A. Code that executes in sequence.

B. Code that never executes.

C. Code that always uses timers.

D. Code that only runs on servers.

**2. What is asynchronous programming?**

A. Programming without functions.

B. Programming that allows certain operations to proceed without blocking the rest of the programme.

C. Programming without variables.

D. Programming that executes only one statement.

**3. Which method schedules a callback to run once after a delay?**

A. `setInterval()`

B. `setTimeout()`

C. `clearInterval()`

D. `reduce()`

**4. Which method schedules repeated callbacks?**

A. `setTimeout()`

B. `clearTimeout()`

C. `setInterval()`

D. `clearInterval()`

**5. Which method cancels a scheduled interval?**

A. `clearInterval()`

B. `setInterval()`

C. `setTimeout()`

D. `remove()`

**6. What is the call stack responsible for?**

A. Storing HTML files.

B. Tracking functions currently being executed.

C. Storing CSS styles.

D. Downloading images.

**7. What is the event loop responsible for?**

A. Creating HTML elements.

B. Coordinating the execution of queued callbacks.

C. Declaring variables.

D. Sorting arrays.

**8. Why does a zero-delay timeout not execute immediately?**

A. JavaScript ignores all timers.

B. The callback must wait until the current synchronous execution finishes and the runtime can process it.

C. The timeout is automatically cancelled.

D. The browser deletes the callback.

---

## 13. Module Challenge

### Challenge: Task Scheduling Simulator

Build a simple task scheduling programme that simulates operations happening at different times.

### Requirements

Your programme should:

1. Display a starting message.
2. Schedule a welcome notification.
3. Schedule three separate tasks.
4. Display each task when its timer completes.
5. Create a repeating timer.
6. Stop the repeating timer after five executions.
7. Cancel one scheduled timeout.
8. Display a final completion message.

### Example Implementation

```javascript
// Task Scheduling Simulator

console.log("APPLICATION STARTED");

setTimeout(() => {

    console.log("Welcome notification displayed.");

}, 1000);

setTimeout(() => {

    console.log("Task 1 completed.");

}, 2000);

setTimeout(() => {

    console.log("Task 2 completed.");

}, 4000);

const cancelledTask = setTimeout(() => {

    console.log("This task should not execute.");

}, 5000);

clearTimeout(cancelledTask);

let count = 1;

const interval = setInterval(() => {

    console.log(`Repeating task: ${count}`);

    count++;

    if (count > 5) {

        clearInterval(interval);

        console.log("Repeating task stopped.");

    }

}, 1000);

setTimeout(() => {

    console.log("Scheduled operations completed.");

}, 7000);
```

### Submission Requirements

1. Create a GitHub repository named `javascript-asynchronous-fundamentals`.
2. Create an `index.html` file.
3. Create an external `script.js` file.
4. Implement the task scheduling simulator.
5. Use `setTimeout()`.
6. Use `setInterval()`.
7. Use `clearTimeout()` and `clearInterval()`.
8. Test the execution order.
9. Submit your GitHub repository link.

---

## Key Takeaways

- Synchronous JavaScript executes instructions in sequence.
- Asynchronous programming allows certain operations to proceed without blocking the rest of the programme.
- The call stack tracks currently executing functions.
- Browser Web APIs manage operations such as timers and network requests.
- The event loop coordinates queued callbacks.
- The microtask queue handles Promise reactions and other microtasks.
- `setTimeout()` schedules a callback once.
- `setInterval()` schedules repeated callbacks.
- `clearTimeout()` cancels a timeout.
- `clearInterval()` cancels an interval.
- Callbacks can be used to process asynchronous results.
- Excessive nested callbacks can lead to callback hell.

---

<p align="center">
  <strong>Congratulations! You have successfully completed Asynchronous JavaScript.</strong>
</p>

<p align="center">
  NEXT: MODULE 14 — PROMISES
</p>
