
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=JAVASCRIPT%20FUNCTIONS&fontSize=32&fontColor=ffffff&animation=fadeIn&desc=Reusable%20Blocks%20Of%20Code&descSize=13" width="100%">
</p>

<h1 align="center">MODULE 06: FUNCTIONS</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Functions-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-BEGINNER-2E86C1?style=for-the-badge">
</p>

## Welcome!

In the previous module, you learned how to repeat instructions using loops.

However, imagine having to write the same calculation or operation in several different places in your programme.

This can lead to duplicated code, unnecessary complexity and difficult maintenance.

JavaScript solves this problem using **functions**.

A function is a reusable block of code designed to perform a particular task.

For example, an application might need to:

- Calculate the total price of an order.
- Validate a user's email address.
- Calculate an employee's salary.
- Display a welcome message.
- Convert temperatures.
- Process customer information.

Instead of writing the same instructions repeatedly, you can define a function once and call it whenever needed.

In this module, you will learn how to create, call and work with JavaScript functions.

## Learning Objectives

By the end of this module, you should be able to:

- Explain what functions are.
- Understand why functions are important.
- Declare and call functions.
- Work with parameters and arguments.
- Return values from functions.
- Understand function expressions.
- Write arrow functions.
- Understand local and global scope.
- Apply default parameters.
- Understand callback functions at an introductory level.
- Build reusable programmes using functions.

---

## 1. What is a Function?

A function is a reusable block of code that performs a specific task.

Functions help developers organise programmes into smaller, manageable sections.

### Example Without a Function

```javascript
let firstNumber = 10;

let secondNumber = 5;

console.log(firstNumber + secondNumber);

let thirdNumber = 20;

let fourthNumber = 15;

console.log(thirdNumber + fourthNumber);
```

The addition operation is repeated.

### Example Using a Function

```javascript
function addNumbers() {

    let firstNumber = 10;

    let secondNumber = 5;

    console.log(firstNumber + secondNumber);

}

addNumbers();
```

Output:

```text
15
```

The function contains the instructions, and the function call executes them.

---

## 2. Declaring a Function

A function declaration creates a named function.

### Syntax

```javascript
function functionName() {
    // Code to execute
}
```

The declaration contains:

| Component | Explanation |
|---|---|
| `function` | Keyword used to declare a function |
| `functionName` | Name of the function |
| `()` | Holds parameters |
| `{}` | Contains the function body |

### Example

```javascript
function greetUser() {

    console.log("Welcome to JavaScript!");

}
```

This code declares the function, but it does not execute it yet.

To execute the function, you must call it.

---

## 3. Calling a Function

Calling a function means instructing JavaScript to execute its code.

A function is called using its name followed by parentheses.

Example:

```javascript
function greetUser() {

    console.log("Welcome to JavaScript!");

}

greetUser();
```

Output:

```text
Welcome to JavaScript!
```

### Calling a Function Multiple Times

```javascript
function greetUser() {

    console.log("Welcome to our application!");

}

greetUser();

greetUser();

greetUser();
```

Output:

```text
Welcome to our application!
Welcome to our application!
Welcome to our application!
```

The same function can be reused as many times as required.

---

## 4. Function Parameters and Arguments

Functions can receive information when they are called.

This allows one function to work with different values.

### Parameters

Parameters are variables listed in a function definition.

### Arguments

Arguments are the actual values passed into a function when it is called.

### Example

```javascript
function greetUser(name) {

    console.log(`Welcome, ${name}!`);

}

greetUser("Alex");

greetUser("Brian");

greetUser("Mary");
```

Output:

```text
Welcome, Alex!
Welcome, Brian!
Welcome, Mary!
```

In this example:

- `name` is a parameter.
- `"Alex"`, `"Brian"` and `"Mary"` are arguments.

### Multiple Parameters

A function can accept more than one parameter.

Example:

```javascript
function introduceStudent(name, age, course) {

    console.log(`Name: ${name}`);

    console.log(`Age: ${age}`);

    console.log(`Course: ${course}`);

}

introduceStudent("Alex", 21, "Software Engineering");
```

Output:

```text
Name: Alex
Age: 21
Course: Software Engineering
```

The arguments are assigned to parameters according to their position.

---

## 5. The return Statement

The `return` statement sends a value from a function back to the code that called it.

This allows the result of a function to be stored, displayed or used in another calculation.

### Example

```javascript
function addNumbers(a, b) {

    return a + b;

}

let result = addNumbers(10, 5);

console.log(result);
```

Output:

```text
15
```

### Understanding return

1. The function receives two arguments.
2. It adds the values.
3. The `return` statement sends the result back.
4. The result is stored in the `result` variable.
5. `console.log()` displays the returned value.

### Returning a Value Without Storing It

```javascript
function multiply(a, b) {

    return a * b;

}

console.log(multiply(4, 5));
```

Output:

```text
20
```

### A Function Without return

Consider:

```javascript
function greet() {

    console.log("Hello!");

}

let result = greet();

console.log(result);
```

Output:

```text
Hello!
undefined
```

The function displays a message but does not return a value. A function without an explicit return value returns `undefined`.

### Important Difference

| `console.log()` | `return` |
|---|---|
| Displays information in the console | Sends a value back to the caller |
| Mainly useful for output and debugging | Useful for calculations and reusable results |
| Does not automatically provide a result to the calling code | Makes the returned value available to the calling code |

---

## 6. Function Expressions

A function expression stores a function in a variable.

Example:

```javascript
const greetUser = function() {

    console.log("Welcome to our application.");

};

greetUser();
```

Output:

```text
Welcome to our application.
```

### Function Expression with Parameters

```javascript
const calculateTotal = function(price, quantity) {

    return price * quantity;

};

let total = calculateTotal(1500, 3);

console.log(total);
```

Output:

```text
4500
```

### Function Declaration vs Function Expression

| Feature | Function Declaration | Function Expression |
|---|---|---|
| Uses a named declaration | Yes | Function may be anonymous |
| Stored in a variable | Not required | Usually |
| Can be called before its declaration due to hoisting | Yes | Depends on variable declaration and initialisation |
| Example | `function greet() {}` | `const greet = function() {}` |

---

## 7. Arrow Functions

Arrow functions provide a shorter way to write functions.

They were introduced in modern JavaScript and are widely used in contemporary development.

### Syntax

```javascript
const functionName = (parameters) => {
    // Code to execute
};
```

### Example

```javascript
const greetUser = () => {

    console.log("Hello, Developer!");

};

greetUser();
```

Output:

```text
Hello, Developer!
```

### Arrow Function with Parameters

```javascript
const addNumbers = (a, b) => {

    return a + b;

};

console.log(addNumbers(10, 5));
```

Output:

```text
15
```

### Short Arrow Function

When an arrow function contains a single expression, you can omit the curly braces and the `return` keyword.

```javascript
const addNumbers = (a, b) => a + b;

console.log(addNumbers(10, 5));
```

Output:

```text
15
```

### One Parameter

Parentheses can be omitted when an arrow function has exactly one parameter.

```javascript
const squareNumber = number => number * number;

console.log(squareNumber(5));
```

Output:

```text
25
```

### Returning an Object

When returning an object directly from a concise arrow function, wrap the object in parentheses.

```javascript
const createStudent = (name, age) => ({
    name: name,
    age: age
});

console.log(createStudent("Alex", 21));
```

Output:

```text
{ name: "Alex", age: 21 }
```

---

## 8. Default Parameters

Default parameters provide a fallback value when an argument is not supplied or when `undefined` is passed.

Example:

```javascript
function greetUser(name = "Guest") {

    console.log(`Welcome, ${name}!`);

}

greetUser("Alex");

greetUser();
```

Output:

```text
Welcome, Alex!
Welcome, Guest!
```

### Another Example

```javascript
function calculatePrice(price, quantity = 1) {

    return price * quantity;

}

console.log(calculatePrice(1000, 3));

console.log(calculatePrice(1000));
```

Output:

```text
3000
1000
```

Default parameters make functions more flexible.

---

## 9. Variable Scope

Scope determines where a variable can be accessed in a programme.

Understanding scope helps prevent unexpected errors.

JavaScript has different kinds of scope, including global scope, function scope and block scope.

### A. Global Scope

A variable declared outside a function or block is generally available throughout its accessible scope.

Example:

```javascript
const applicationName = "Student Portal";

function displayApplication() {

    console.log(applicationName);

}

displayApplication();

console.log(applicationName);
```

Both statements can access the global variable.

### B. Function Scope

A variable declared inside a function is generally accessible only within that function.

Example:

```javascript
function calculateTotal() {

    let total = 5000;

    console.log(total);

}

calculateTotal();
```

Trying to access `total` outside the function will produce a `ReferenceError`.

```javascript
console.log(total);
```

### C. Block Scope

Variables declared using `let` and `const` are limited to the block in which they are declared.

Example:

```javascript
if (true) {

    let message = "Hello";

    console.log(message);

}
```

The variable `message` cannot be accessed outside the block.

### Scope Comparison

| Scope | Description |
|---|---|
| Global | Accessible throughout its containing global scope |
| Function | Accessible within the function where it is declared |
| Block | Accessible within the block where it is declared |

---

## 10. Callback Functions

A callback is a function passed as an argument to another function.

The receiving function can execute the callback when needed.

### Example

```javascript
function greetUser(name, callback) {

    console.log(`Hello, ${name}`);

    callback();

}

function showMessage() {

    console.log("Welcome to our application.");

}

greetUser("Alex", showMessage);
```

Output:

```text
Hello, Alex
Welcome to our application.
```

In this example:

- `showMessage` is a function.
- It is passed into `greetUser`.
- `greetUser` executes it by calling `callback()`.

### Callback Using an Arrow Function

```javascript
function processOrder(callback) {

    console.log("Processing order...");

    callback();

}

processOrder(() => {

    console.log("Order completed.");

});
```

Output:

```text
Processing order...
Order completed.
```

Callbacks are widely used in JavaScript, including event handling and asynchronous programming.

---

## 11. Functions and Code Reusability

One of the most important reasons to use functions is code reusability.

Instead of writing the same calculation multiple times, you can define a function once and reuse it.

### Example: Calculating Product Prices

```javascript
function calculateProductTotal(price, quantity) {

    return price * quantity;

}

const laptopTotal = calculateProductTotal(75000, 1);

const mouseTotal = calculateProductTotal(1500, 2);

const keyboardTotal = calculateProductTotal(3000, 1);

console.log("Laptop:", laptopTotal);

console.log("Mouse:", mouseTotal);

console.log("Keyboard:", keyboardTotal);
```

Output:

```text
Laptop: 75000
Mouse: 3000
Keyboard: 3000
```

### Benefits of Functions

- Reduce duplicated code.
- Improve organisation.
- Make programmes easier to maintain.
- Allow code to be reused.
- Make testing easier.
- Separate complex tasks into smaller units.

---

## 12. Practical Activity

### Activity: Employee Salary Calculator

Create a JavaScript programme that calculates employee salaries.

### Requirements

Your programme should:

1. Create a function called `calculateGrossSalary`.
2. Accept basic salary and allowances as parameters.
3. Return the gross salary.
4. Create a function called `calculateDeductions`.
5. Accept gross salary and deduction rate.
6. Return the deduction amount.
7. Create a function called `calculateNetSalary`.
8. Calculate the final salary after deductions.
9. Display the employee's salary summary.

### Example Implementation

```javascript
// Employee Salary Calculator

function calculateGrossSalary(basicSalary, allowances) {

    return basicSalary + allowances;

}

function calculateDeductions(grossSalary, deductionRate) {

    return grossSalary * deductionRate;

}

function calculateNetSalary(grossSalary, deductions) {

    return grossSalary - deductions;

}

// Employee Information

const employeeName = "Alex Morgan";

const basicSalary = 50000;

const allowances = 10000;

const deductionRate = 0.10;

// Calculations

const grossSalary = calculateGrossSalary(
    basicSalary,
    allowances
);

const deductions = calculateDeductions(
    grossSalary,
    deductionRate
);

const netSalary = calculateNetSalary(
    grossSalary,
    deductions
);

// Display Results

console.log("EMPLOYEE SALARY SUMMARY");

console.log("Employee:", employeeName);

console.log("Basic Salary:", basicSalary);

console.log("Allowances:", allowances);

console.log("Gross Salary:", grossSalary);

console.log("Deductions:", deductions);

console.log("Net Salary:", netSalary);
```

### Additional Tasks

1. Rewrite the functions using arrow function syntax.
2. Add a default deduction rate.
3. Create a function that calculates annual salary.
4. Create a function that displays an employee introduction.
5. Return values from all calculation functions instead of displaying results inside them.

---

## 13. Knowledge Check

**1. What is a function?**

A. A variable that stores only numbers.

B. A reusable block of code that performs a task.

C. An HTML element.

D. A CSS selector.

**2. Which keyword is used to declare a function?**

A. `create`

B. `function`

C. `method`

D. `define`

**3. What is a function call?**

A. Creating a variable.

B. Executing a function.

C. Declaring an object.

D. Importing CSS.

**4. What is a parameter?**

A. A value passed into a function call.

B. A variable listed in a function definition.

C. A function's return value.

D. A loop condition.

**5. What does return do?**

A. Displays information in the console.

B. Sends a value back to the caller.

C. Stops the browser.

D. Creates a new variable.

**6. Which of the following is an arrow function?**

A. `function add() {}`

B. `const add = () => {}`

C. `let add = function() {}`

D. `if (add) {}`

**7. What happens when a function has no explicit return statement?**

A. It returns `false`.

B. It returns `null`.

C. It returns `undefined`.

D. It returns zero.

**8. What is a callback function?**

A. A function passed as an argument to another function.

B. A function that cannot be reused.

C. A function that always returns a number.

D. A function without parameters.

---

## 14. Module Challenge

### Challenge: Reusable Business Calculator

Build a JavaScript application that performs common business calculations using functions.

Your programme should support:

- Calculating product totals.
- Calculating discounts.
- Calculating VAT.
- Calculating final selling prices.
- Calculating profit.
- Calculating profit margins.

### Technical Requirements

1. Create separate functions for each calculation.
2. Accept required values as parameters.
3. Return calculation results.
4. Use descriptive function names.
5. Use arrow functions for at least two calculations.
6. Use default parameters in at least one function.
7. Display a complete business calculation report.

### Example Implementation

```javascript
// Business Calculator

function calculateSubtotal(price, quantity) {

    return price * quantity;

}

function calculateDiscount(subtotal, discountRate = 0) {

    return subtotal * discountRate;

}

const calculateVAT = (amount, vatRate = 0.16) => {

    return amount * vatRate;

};

const calculateProfit = (sellingPrice, costPrice) => {

    return sellingPrice - costPrice;

};

function calculateFinalPrice(subtotal, discount, vat) {

    return subtotal - discount + vat;

}

// Product Information

const productName = "Laptop";

const costPrice = 60000;

const sellingPrice = 75000;

const quantity = 2;

const discountRate = 0.05;

// Calculations

const subtotal = calculateSubtotal(sellingPrice, quantity);

const discount = calculateDiscount(subtotal, discountRate);

const amountAfterDiscount = subtotal - discount;

const vat = calculateVAT(amountAfterDiscount);

const finalPrice = calculateFinalPrice(
    subtotal,
    discount,
    vat
);

const profit = calculateProfit(sellingPrice, costPrice);

// Display Report

console.log("BUSINESS CALCULATION REPORT");

console.log("Product:", productName);

console.log("Quantity:", quantity);

console.log("Subtotal:", subtotal);

console.log("Discount:", discount);

console.log("VAT:", vat);

console.log("Final Price:", finalPrice);

console.log("Profit Per Unit:", profit);
```

### Submission Requirements

1. Create a GitHub repository named `javascript-functions`.
2. Create an `index.html` file.
3. Create an external `script.js` file.
4. Implement the business calculator.
5. Use function declarations and arrow functions.
6. Include parameters and return values.
7. Test the calculations with different values.
8. Submit your GitHub repository link.

---

## Key Takeaways

- Functions are reusable blocks of code.
- Function declarations define named functions.
- Function calls execute functions.
- Parameters receive information from function calls.
- Arguments are the actual values passed to functions.
- `return` sends a result back to the caller.
- Function expressions store functions in variables.
- Arrow functions provide a concise function syntax.
- Scope determines where variables can be accessed.
- Callback functions allow functions to be passed into other functions.
- Functions improve code reusability and organisation.

---

<p align="center">
  <strong>Congratulations! You have successfully completed JavaScript Functions.</strong>
</p>

<p align="center">
  NEXT: MODULE 07 — ARRAYS
</p>
