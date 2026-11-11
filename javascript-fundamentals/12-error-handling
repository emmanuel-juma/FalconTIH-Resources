
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=JAVASCRIPT%20ERROR%20HANDLING&fontSize=29&fontColor=ffffff&animation=fadeIn&desc=Identifying%20And%20Managing%20Errors&descSize=12" width="100%">
</p>

<h1 align="center">MODULE 12: ERROR HANDLING</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Error%20Handling-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-BEGINNER-2E86C1?style=for-the-badge">
</p>

## Welcome!

As you build more complex JavaScript applications, you will encounter errors.

A variable may be undefined, a function may be called incorrectly, a network request may fail, or a user may enter invalid information.

Errors are a normal part of software development.

The important skill is learning how to identify, understand and handle them properly.

**Error handling** allows developers to manage unexpected situations without allowing an application to fail unnecessarily.

In this module, you will learn about common JavaScript errors, debugging techniques, `try...catch`, `finally`, `throw` and custom errors.

## Learning Objectives

By the end of this module, you should be able to:

- Explain what errors are.
- Identify common types of JavaScript errors.
- Understand syntax, reference and type errors.
- Read JavaScript error messages.
- Use browser developer tools for debugging.
- Understand the `try...catch` structure.
- Use `finally`.
- Throw errors using `throw`.
- Create custom error messages.
- Validate input before processing it.
- Build programmes that handle unexpected situations.

---

## 1. What is an Error?

An error is a problem that occurs when JavaScript code cannot execute as intended.

Errors may occur because of:

- Incorrect syntax.
- Misspelled variable names.
- Invalid operations.
- Unexpected data types.
- Missing values.
- Failed network requests.
- Incorrect assumptions about data.

### Example

```javascript
console.log("Application started");

console.log(userName);

console.log("Application finished");
```

If `userName` has not been declared, JavaScript throws a `ReferenceError`.

The execution of the current script is interrupted at that point unless the error is handled.

---

## 2. Types of JavaScript Errors

JavaScript provides several built-in error types.

Understanding them helps developers identify the source of a problem.

### A. SyntaxError

A `SyntaxError` occurs when JavaScript code does not follow the language's syntax rules.

Example:

```javascript
if (true {
    console.log("Hello");
}
```

The opening parenthesis is not correctly matched.

Correct version:

```javascript
if (true) {
    console.log("Hello");
}
```

Another example:

```javascript
const student = {
    name: "Alex"
    age: 21
};
```

A comma is missing between the object properties.

Correct version:

```javascript
const student = {
    name: "Alex",
    age: 21
};
```

### B. ReferenceError

A `ReferenceError` occurs when code attempts to access a variable or identifier that cannot be resolved.

Example:

```javascript
console.log(studentName);
```

If `studentName` has not been declared, JavaScript throws a `ReferenceError`.

Correct version:

```javascript
const studentName = "Alex";

console.log(studentName);
```

### C. TypeError

A `TypeError` occurs when an operation is performed on a value in an invalid way.

Example:

```javascript
const age = 21;

age.toUpperCase();
```

A number does not have a `toUpperCase()` method.

Correct version:

```javascript
const name = "Alex";

console.log(name.toUpperCase());
```

### D. RangeError

A `RangeError` occurs when a value is outside the allowed range for an operation.

Example:

```javascript
const numbers = new Array(-5);
```

An array length cannot be negative.

### E. URIError

A `URIError` occurs when URI-related functions receive malformed URI data.

Example:

```javascript
decodeURIComponent("%");
```

The percent sign is not followed by a valid encoded sequence.

---

## 3. Understanding Error Messages

When JavaScript encounters an error, the browser console displays information that helps identify the problem.

Example:

```javascript
const age = 21;

console.log(studentName);
```

The console may display an error similar to:

```text
ReferenceError: studentName is not defined
```

### Important Parts of an Error Message

| Part | Explanation |
|---|---|
| Error type | Identifies the category of error |
| Error message | Explains what went wrong |
| File name | Identifies the source file |
| Line number | Shows where the error occurred |
| Stack trace | Shows the sequence of function calls |

### How to Investigate an Error

1. Read the error message.
2. Identify the error type.
3. Check the file and line number.
4. Inspect the relevant code.
5. Check variable names and data types.
6. Reproduce the error.
7. Apply a correction.
8. Test the programme again.

Do not ignore errors. Understand why they occur before attempting to fix them.

---

## 4. Using console Methods for Debugging

The browser console provides methods that help developers inspect programme behaviour.

### A. console.log()

Displays general information.

```javascript
const age = 21;

console.log("Age:", age);
```

### B. console.error()

Displays an error message.

```javascript
console.error("Unable to process the request.");
```

### C. console.warn()

Displays a warning.

```javascript
console.warn("This feature is still under development.");
```

### D. console.table()

Displays structured information in a table.

```javascript
const students = [

    {
        name: "Alex",
        age: 21
    },

    {
        name: "Brian",
        age: 22
    },

    {
        name: "Mary",
        age: 20
    }

];

console.table(students);
```

### E. console.assert()

Displays an assertion error when a condition is false.

```javascript
const age = 15;

console.assert(age >= 18, "Age must be at least 18.");
```

These methods are useful during development, but they should not replace proper error handling.

---

## 5. Using try...catch

The `try...catch` statement allows a programme to handle exceptions.

Code that may throw an error is placed inside the `try` block.

If an exception occurs, JavaScript transfers control to the `catch` block.

### Syntax

```javascript
try {

    // Code that may throw an error

} catch (error) {

    // Handle the error

}
```

### Example

```javascript
try {

    console.log(studentName);

} catch (error) {

    console.log("An error occurred.");

}
```

Output:

```text
An error occurred.
```

The programme handles the exception instead of allowing it to remain uncaught.

### Accessing the Error Message

The `catch` block receives an error object.

```javascript
try {

    console.log(studentName);

} catch (error) {

    console.log(error.name);

    console.log(error.message);

}
```

The error object provides useful information about the exception.

### Example: Handling Invalid Calculations

```javascript
function divideNumbers(a, b) {

    if (b === 0) {

        throw new Error("Cannot divide by zero.");

    }

    return a / b;

}

try {

    const result = divideNumbers(10, 0);

    console.log(result);

} catch (error) {

    console.error(error.message);

}
```

Output:

```text
Cannot divide by zero.
```

---

## 6. The finally Block

The `finally` block executes after the `try` and `catch` process has completed.

It executes whether an exception occurs or not, unless control leaves the function or programme through something like a return or throw in a way that changes execution.

It is commonly used for cleanup operations.

### Syntax

```javascript
try {

    // Code that may throw an error

} catch (error) {

    // Handle the error

} finally {

    // Cleanup code

}
```

### Example

```javascript
try {

    console.log("Starting operation.");

    throw new Error("Something went wrong.");

} catch (error) {

    console.log(error.message);

} finally {

    console.log("Operation completed.");

}
```

Output:

```text
Starting operation.
Something went wrong.
Operation completed.
```

### Example Without an Error

```javascript
try {

    console.log("Operation successful.");

} catch (error) {

    console.log("An error occurred.");

} finally {

    console.log("This block executes at the end.");

}
```

The `finally` block still executes.

---

## 7. Throwing Errors

The `throw` statement allows developers to generate their own exceptions.

This is useful when an application detects invalid information or an operation that should not continue.

### Syntax

```javascript
throw new Error("Error message");
```

### Example: Age Validation

```javascript
function registerUser(age) {

    if (age < 18) {

        throw new Error("You must be at least 18 years old.");

    }

    return "Registration successful.";

}

try {

    console.log(registerUser(16));

} catch (error) {

    console.log(error.message);

}
```

Output:

```text
You must be at least 18 years old.
```

### Example: Product Price Validation

```javascript
function calculateTotal(price, quantity) {

    if (price < 0) {

        throw new Error("Price cannot be negative.");

    }

    if (quantity <= 0) {

        throw new Error("Quantity must be greater than zero.");

    }

    return price * quantity;

}

try {

    const total = calculateTotal(1500, 2);

    console.log(total);

} catch (error) {

    console.error(error.message);

}
```

---

## 8. Creating Custom Error Messages

You can create error messages that are specific to your application.

For more advanced applications, JavaScript also allows you to define custom error classes.

### Example

```javascript
class ValidationError extends Error {

    constructor(message) {

        super(message);

        this.name = "ValidationError";

    }

}
```

### Using the Custom Error

```javascript
function validateEmail(email) {

    if (!email.includes("@")) {

        throw new ValidationError("Invalid email address.");

    }

    return "Email is valid.";

}

try {

    console.log(validateEmail("alexexample.com"));

} catch (error) {

    console.log(error.name);

    console.log(error.message);

}
```

Output:

```text
ValidationError
Invalid email address.
```

Custom errors make it easier to distinguish between different application problems.

---

## 9. Input Validation and Error Handling

Input validation checks whether information supplied by a user meets the application's requirements.

It is an important part of reliable software development.

### Example: Registration Validation

```javascript
function registerUser(name, email, age) {

    if (name.trim() === "") {

        throw new Error("Name is required.");

    }

    if (!email.includes("@")) {

        throw new Error("Please provide a valid email address.");

    }

    if (age < 18) {

        throw new Error("User must be at least 18 years old.");

    }

    return "Registration successful.";

}

try {

    const result = registerUser(
        "Alex",
        "alex@example.com",
        21
    );

    console.log(result);

} catch (error) {

    console.error(error.message);

}
```

### Important Development Practice

Validation should happen at different levels.

- Frontend validation improves the user experience.
- Backend validation protects application logic and data.
- Database constraints help maintain data integrity.

Frontend validation alone is not sufficient because client-side code can be modified or bypassed.

---

## 10. Debugging with Browser Developer Tools

Browser developer tools provide several debugging features.

### A. Console

The Console displays:

- Error messages.
- Warnings.
- Debugging output.
- JavaScript execution results.

### B. Sources

The Sources panel allows you to inspect JavaScript files and set breakpoints.

### C. Breakpoints

A breakpoint pauses programme execution at a selected line.

This allows you to inspect variable values and understand how the code executes.

### Example

```javascript
function calculateTotal(price, quantity) {

    const total = price * quantity;

    return total;

}

const result = calculateTotal(1500, 3);

console.log(result);
```

You can set a breakpoint on the calculation line and inspect the values of `price`, `quantity` and `total`.

### D. The debugger Statement

JavaScript provides the `debugger` statement.

```javascript
function calculateTotal(price, quantity) {

    debugger;

    return price * quantity;

}
```

When developer tools are open, execution pauses at the debugger statement.

Remove unnecessary debugger statements before deploying your application.

---

## 11. Common Error Handling Mistakes

### Mistake 1: Using Empty catch Blocks

Avoid:

```javascript
try {

    performOperation();

} catch (error) {

}
```

This hides the error and makes debugging difficult.

Better:

```javascript
try {

    performOperation();

} catch (error) {

    console.error("Operation failed:", error.message);

}
```

### Mistake 2: Catching Errors Without Understanding Them

Do not assume every error can be safely ignored.

Inspect the error and determine whether the application can recover.

### Mistake 3: Using try...catch for Every Condition

Ordinary conditions should generally use conditional statements.

For example:

```javascript
if (age < 18) {

    console.log("Not eligible.");

}
```

This is more appropriate than throwing and catching an error for every simple decision.

### Mistake 4: Displaying Technical Errors Directly to Users

Technical error messages may expose implementation details.

Use detailed logs for developers and clear, safe messages for users.

---

## 12. Practical Activity

### Activity: Bank Transaction Validator

Create a programme that validates bank transactions and handles invalid operations.

### Requirements

Your programme should:

1. Store an account balance.
2. Accept a withdrawal amount.
3. Reject negative amounts.
4. Reject withdrawals that exceed the available balance.
5. Reject withdrawals equal to zero.
6. Throw an error when an invalid transaction is attempted.
7. Catch the error.
8. Display a useful message.
9. Update the balance after a successful withdrawal.
10. Use a `finally` block to display the end of each transaction attempt.

### Example Implementation

```javascript
// Bank Transaction Validator

let balance = 50000;

function withdraw(amount) {

    if (amount <= 0) {

        throw new Error("Withdrawal amount must be positive.");

    }

    if (amount > balance) {

        throw new Error("Insufficient account balance.");

    }

    balance -= amount;

    return balance;

}

function processTransaction(amount) {

    console.log("Processing withdrawal:", amount);

    try {

        const remainingBalance = withdraw(amount);

        console.log("Withdrawal successful.");

        console.log("Remaining Balance:", remainingBalance);

    } catch (error) {

        console.error("Transaction failed:", error.message);

    } finally {

        console.log("Transaction attempt completed.");

    }

}

processTransaction(10000);

processTransaction(60000);

processTransaction(-500);
```

### Additional Tasks

1. Create a deposit function.
2. Validate deposit amounts.
3. Prevent withdrawals from reducing the balance below zero.
4. Create a custom `TransactionError`.
5. Record successful transactions in an array.
6. Display the final account balance.

---

## 13. Knowledge Check

**1. What is an error in programming?**

A. A successful operation.

B. A problem that prevents code from executing as intended.

C. A variable declaration.

D. A CSS property.

**2. Which error occurs when a variable cannot be found?**

A. SyntaxError

B. ReferenceError

C. RangeError

D. URIError

**3. Which error occurs when an operation is performed on an incompatible value?**

A. TypeError

B. SyntaxError

C. URIError

D. RangeError

**4. Which statement is used to handle exceptions?**

A. `if...else`

B. `try...catch`

C. `for...of`

D. `switch`

**5. What does the catch block receive?**

A. An array.

B. An error object.

C. A CSS selector.

D. A Boolean value.

**6. What is the purpose of finally?**

A. It creates a function.

B. It executes cleanup code after the try/catch process.

C. It prevents all errors.

D. It restarts the application.

**7. Which keyword creates an exception manually?**

A. `return`

B. `throw`

C. `break`

D. `continue`

**8. What is the purpose of a breakpoint?**

A. To delete code.

B. To pause execution so developers can inspect the programme.

C. To stop the browser.

D. To create an array.

---

## 14. Module Challenge

### Challenge: Secure Registration and Transaction Validation System

Build a JavaScript application that validates user registration and processes basic financial transactions.

### Registration Requirements

The application should collect:

- Full name.
- Email address.
- Age.
- Password.

It should validate:

1. Name is not empty.
2. Email address is valid.
3. Age is at least 18.
4. Password contains at least eight characters.

### Transaction Requirements

The application should:

1. Store an account balance.
2. Process deposits.
3. Process withdrawals.
4. Reject invalid amounts.
5. Reject withdrawals that exceed the balance.
6. Throw meaningful errors.
7. Catch and display errors.
8. Record successful transactions.
9. Display the final account balance.

### Example Implementation

```javascript
// Registration and Transaction Validation System

class ValidationError extends Error {

    constructor(message) {

        super(message);

        this.name = "ValidationError";

    }

}

function validateRegistration(user) {

    if (!user.name.trim()) {

        throw new ValidationError("Name is required.");

    }

    if (!user.email.includes("@")) {

        throw new ValidationError("Invalid email address.");

    }

    if (user.age < 18) {

        throw new ValidationError("User must be at least 18.");

    }

    if (user.password.length < 8) {

        throw new ValidationError("Password must contain at least 8 characters.");

    }

    return true;

}

let balance = 50000;

const transactions = [];

function deposit(amount) {

    if (amount <= 0) {

        throw new Error("Deposit amount must be positive.");

    }

    balance += amount;

    transactions.push({
        type: "Deposit",
        amount: amount,
        balance: balance
    });

}

function withdraw(amount) {

    if (amount <= 0) {

        throw new Error("Withdrawal amount must be positive.");

    }

    if (amount > balance) {

        throw new Error("Insufficient funds.");

    }

    balance -= amount;

    transactions.push({
        type: "Withdrawal",
        amount: amount,
        balance: balance
    });

}

// Registration

const user = {

    name: "Alex Morgan",

    email: "alex@example.com",

    age: 21,

    password: "secure123"

};

try {

    validateRegistration(user);

    console.log("Registration successful.");

} catch (error) {

    console.error(error.name, error.message);

}

// Transactions

try {

    deposit(10000);

    withdraw(5000);

    withdraw(100000);

} catch (error) {

    console.error("Transaction Error:", error.message);

} finally {

    console.log("Transaction processing completed.");

}

// Final Report

console.log("FINAL BALANCE:", balance);

console.table(transactions);
```

### Submission Requirements

1. Create a GitHub repository named `javascript-error-handling`.
2. Create `index.html`, `style.css` and `script.js`.
3. Implement registration validation.
4. Implement deposit and withdrawal functions.
5. Use `try...catch...finally`.
6. Create at least one custom error class.
7. Record successful transactions.
8. Test valid and invalid inputs.
9. Submit your GitHub repository link.

---

## Key Takeaways

- Errors are normal during software development.
- SyntaxError indicates invalid JavaScript syntax.
- ReferenceError indicates an unresolved identifier.
- TypeError indicates an invalid operation on a value.
- Browser developer tools help identify and investigate errors.
- `try...catch` handles exceptions.
- `finally` provides a place for cleanup operations.
- `throw` allows developers to create exceptions.
- Custom errors make application error handling more specific.
- Input validation improves reliability.
- Frontend validation must be supported by backend validation.

---

<p align="center">
  <strong>Congratulations! You have successfully completed JavaScript Error Handling.</strong>
</p>

<p align="center">
  NEXT: MODULE 13 — ASYNCHRONOUS JAVASCRIPT
</p>
