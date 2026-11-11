
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=JAVASCRIPT%20PROMISES&fontSize=32&fontColor=ffffff&animation=fadeIn&desc=Managing%20Asynchronous%20Results&descSize=13" width="100%">
</p>

<h1 align="center">MODULE 14: PROMISES</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Promises-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-INTERMEDIATE-2E86C1?style=for-the-badge">
</p>

## Welcome!

In the previous module, you learned how asynchronous JavaScript works and how to use timers and callbacks.

You also saw how deeply nested callbacks can make code difficult to read and maintain.

JavaScript provides **Promises** to manage asynchronous operations more effectively.

A Promise represents the eventual result of an asynchronous operation. That result may be a successful value or an error.

Promises are widely used when communicating with APIs, reading data and performing operations that do not complete immediately.

In this module, you will learn how to create Promises, handle successful and failed operations, chain Promises and use modern asynchronous syntax.

## Learning Objectives

By the end of this module, you should be able to:

- Explain what Promises are.
- Identify the three Promise states.
- Create a Promise.
- Understand `resolve()` and `reject()`.
- Handle successful results using `.then()`.
- Handle errors using `.catch()`.
- Use `.finally()`.
- Chain multiple Promises.
- Understand Promise execution order.
- Use `Promise.all()`.
- Understand `Promise.race()`.
- Use `async` and `await`.
- Build a simple asynchronous application.

---

## 1. What is a Promise?

A Promise is a JavaScript object that represents the eventual completion or failure of an asynchronous operation.

It allows code to handle a result that may become available later.

### Real-World Example

Imagine ordering a product from an online store.

After placing the order:

1. The system receives the order.
2. The order is processed.
3. Payment is verified.
4. The order is either confirmed or rejected.

The result is not necessarily available immediately.

A Promise represents this pending operation and its eventual outcome.

### Promise States

A Promise has three possible states.

| State | Description |
|---|---|
| Pending | The operation has not completed |
| Fulfilled | The operation completed successfully |
| Rejected | The operation failed |

Once a Promise is fulfilled or rejected, it is settled and cannot change to another state.

---

## 2. Creating a Promise

A Promise is created using the `Promise` constructor.

### Syntax

```javascript
const myPromise = new Promise((resolve, reject) => {

    // Asynchronous operation

});
```

The constructor receives a function called the executor.

The executor receives two functions:

- `resolve()`
- `reject()`

### Example: Successful Promise

```javascript
const myPromise = new Promise((resolve, reject) => {

    resolve("Operation successful!");

});

console.log(myPromise);
```

The Promise is fulfilled with the value:

```text
Operation successful!
```

### Example: Rejected Promise

```javascript
const myPromise = new Promise((resolve, reject) => {

    reject("Operation failed!");

});

console.log(myPromise);
```

The Promise is rejected with the supplied reason.

---

## 3. Understanding resolve() and reject()

The `resolve()` function fulfils a Promise.

The `reject()` function rejects a Promise.

### Example: Resolving a Promise

```javascript
const paymentPromise = new Promise((resolve, reject) => {

    const paymentSuccessful = true;

    if (paymentSuccessful) {

        resolve("Payment completed.");

    } else {

        reject("Payment failed.");

    }

});
```

### Example: Rejecting a Promise

```javascript
const paymentPromise = new Promise((resolve, reject) => {

    const paymentSuccessful = false;

    if (paymentSuccessful) {

        resolve("Payment completed.");

    } else {

        reject("Payment failed.");

    }

});
```

The Promise will be rejected because the payment condition is false.

---

## 4. Handling Promises with then()

The `.then()` method handles the successful result of a Promise.

It receives a callback that executes when the Promise is fulfilled.

### Syntax

```javascript
promise.then(result => {

    // Handle successful result

});
```

### Example

```javascript
const myPromise = new Promise((resolve, reject) => {

    resolve("Data loaded successfully.");

});

myPromise.then(result => {

    console.log(result);

});
```

Output:

```text
Data loaded successfully.
```

### Example: Loading User Information

```javascript
const userPromise = new Promise((resolve, reject) => {

    const user = {
        name: "Alex",
        age: 21
    };

    resolve(user);

});

userPromise.then(user => {

    console.log(user.name);

    console.log(user.age);

});
```

Output:

```text
Alex
21
```

---

## 5. Handling Errors with catch()

The `.catch()` method handles a rejected Promise or an error thrown during a preceding Promise chain.

### Syntax

```javascript
promise.catch(error => {

    // Handle error

});
```

### Example

```javascript
const paymentPromise = new Promise((resolve, reject) => {

    reject("Payment could not be processed.");

});

paymentPromise.catch(error => {

    console.error(error);

});
```

Output:

```text
Payment could not be processed.
```

### Handling Success and Failure Together

```javascript
const paymentPromise = new Promise((resolve, reject) => {

    const paymentSuccessful = false;

    if (paymentSuccessful) {

        resolve("Payment successful.");

    } else {

        reject("Payment failed.");

    }

});

paymentPromise
    .then(result => {

        console.log(result);

    })
    .catch(error => {

        console.error(error);

    });
```

---

## 6. Using finally()

The `.finally()` method registers a callback that executes when a Promise settles, whether it is fulfilled or rejected.

It is useful for cleanup operations.

### Example

```javascript
const dataPromise = new Promise((resolve, reject) => {

    resolve("Data received.");

});

dataPromise
    .then(result => {

        console.log(result);

    })
    .catch(error => {

        console.log(error);

    })
    .finally(() => {

        console.log("Operation completed.");

    });
```

Output:

```text
Data received.
Operation completed.
```

### Example with a Rejected Promise

```javascript
const dataPromise = new Promise((resolve, reject) => {

    reject("Unable to load data.");

});

dataPromise
    .then(result => {

        console.log(result);

    })
    .catch(error => {

        console.error(error);

    })
    .finally(() => {

        console.log("Request finished.");

    });
```

The `finally()` callback executes even though the Promise is rejected.

---

## 7. Promise Chaining

Promise chaining allows multiple asynchronous operations to be connected.

Each `.then()` can return a value or another Promise.

The next `.then()` receives the previous handler's returned value.

### Example

```javascript
const numberPromise = Promise.resolve(10);

numberPromise
    .then(number => {

        console.log("Initial:", number);

        return number * 2;

    })
    .then(result => {

        console.log("Doubled:", result);

        return result + 5;

    })
    .then(finalResult => {

        console.log("Final:", finalResult);

    })
    .catch(error => {

        console.error(error);

    });
```

Output:

```text
Initial: 10
Doubled: 20
Final: 25
```

### Understanding the Process

1. The first `.then()` receives 10.
2. It multiplies the value by two.
3. The next `.then()` receives 20.
4. It adds five.
5. The final `.then()` receives 25.

Each returned value is passed to the next step.

---

## 8. Returning a Promise from a Function

Functions can return Promises.

This is useful when creating reusable asynchronous operations.

### Example

```javascript
function getUser() {

    return new Promise((resolve, reject) => {

        setTimeout(() => {

            resolve({
                name: "Alex",
                age: 21
            });

        }, 2000);

    });

}

getUser()
    .then(user => {

        console.log(user);

    })
    .catch(error => {

        console.error(error);

    });
```

The function returns a Promise that resolves with user information after the timer completes.

---

## 9. Promise.all()

`Promise.all()` accepts an iterable of Promises and returns a new Promise.

It fulfils when all input Promises fulfil.

If any input Promise rejects, the returned Promise rejects with that reason.

### Example

```javascript
const promiseOne = Promise.resolve("User loaded");

const promiseTwo = Promise.resolve("Products loaded");

const promiseThree = Promise.resolve("Orders loaded");

Promise.all([
    promiseOne,
    promiseTwo,
    promiseThree
])
    .then(results => {

        console.log(results);

    })
    .catch(error => {

        console.error(error);

    });
```

Output:

```text
[
    "User loaded",
    "Products loaded",
    "Orders loaded"
]
```

### Practical Use

Imagine an application that needs to load:

- User information.
- Product information.
- Order information.

If all three operations must succeed before displaying a dashboard, `Promise.all()` can be useful.

---

## 10. Promise.race()

`Promise.race()` returns a Promise that settles with the outcome of the first input Promise to settle.

The first one may fulfil or reject.

### Example

```javascript
const promiseOne = new Promise(resolve => {

    setTimeout(() => {

        resolve("First operation completed.");

    }, 1000);

});

const promiseTwo = new Promise(resolve => {

    setTimeout(() => {

        resolve("Second operation completed.");

    }, 2000);

});

Promise.race([promiseOne, promiseTwo])
    .then(result => {

        console.log(result);

    });
```

Output:

```text
First operation completed.
```

The first Promise settles after approximately one second.

### Difference Between Promise.all() and Promise.race()

| Method | Behaviour |
|---|---|
| `Promise.all()` | Waits for all Promises to fulfil or rejects when one rejects |
| `Promise.race()` | Settles with the first Promise to settle |

---

## 11. Promise.allSettled()

`Promise.allSettled()` waits for all supplied Promises to settle.

Unlike `Promise.all()`, it does not reject simply because one input Promise rejects.

It returns the status and result or reason for every Promise.

### Example

```javascript
const promiseOne = Promise.resolve("User loaded");

const promiseTwo = Promise.reject("Products failed.