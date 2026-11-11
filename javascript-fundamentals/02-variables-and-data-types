
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=VARIABLES%20AND%20DATA%20TYPES&fontSize=30&fontColor=ffffff&animation=fadeIn&desc=Storing%20And%20Understanding%20Data&descSize=13" width="100%">
</p>

<h1 align="center">MODULE 02: VARIABLES AND DATA TYPES</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Variables%20%26%20Data%20Types-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-BEGINNER-2E86C1?style=for-the-badge">
</p>

## Welcome!

In the previous module, you learned what JavaScript is and how to execute your first JavaScript statements.

Now that you can write and execute JavaScript code, it is time to learn how programmes store and work with information.

Almost every application works with data. A registration form collects names and email addresses. An online store stores product names and prices. A banking application works with account balances and transaction amounts.

JavaScript uses **variables** to store information and **data types** to define the kind of information being stored.

In this module, you will learn how to declare variables, assign values, understand data types and work with basic JavaScript data.

## Learning Objectives

By the end of this module, you should be able to:

- Explain what variables are.
- Declare and initialise variables using `let`, `const` and `var`.
- Understand the difference between variable declaration, assignment and initialisation.
- Apply JavaScript variable naming conventions.
- Identify JavaScript primitive data types.
- Differentiate between primitive and reference values.
- Use the `typeof` operator.
- Convert values from one data type to another.
- Avoid common variable and data type errors.

---

## 1. What is a Variable?

A variable is a named storage location used to hold a value that a programme can access and use.

Think of a variable as a labelled container.

For example, imagine storing a student's information:

- Name: Alex
- Age: 21
- Country: Kenya
- Course: Software Engineering

Instead of repeatedly writing these values throughout a programme, we can store them in variables.

### Example

```javascript
let studentName = "Alex";

let studentAge = 21;

let studentCountry = "Kenya";

console.log(studentName);

console.log(studentAge);

console.log(studentCountry);
```

Output:

```text
Alex
21
Kenya
```

Each variable stores a value that can be accessed later.

### Understanding Variable Components

Consider:

```javascript
let productName = "Laptop";
```

| Component | Explanation |
|---|---|
| `let` | Declares a variable |
| `productName` | Variable name |
| `=` | Assignment operator |
| `"Laptop"` | Value assigned to the variable |
| `;` | Ends the statement |

---

## 2. Declaring and Initialising Variables

JavaScript provides three keywords for declaring variables:

- `let`
- `const`
- `var`

Each keyword has different behaviour.

### A. The let Keyword

`let` declares a variable whose value can be reassigned.

Example:

```javascript
let age = 20;

console.log(age);

age = 21;

console.log(age);
```

Output:

```text
20
21
```

The value changes because `let` allows reassignment.

Use `let` when you expect a variable's value to change.

### B. The const Keyword

`const` declares a variable that cannot be reassigned after initialisation.

Example:

```javascript
const country = "Kenya";

console.log(country);
```

The following is not allowed:

```javascript
const country = "Kenya";

country = "Uganda";
```

This produces a `TypeError` because a constant variable cannot be reassigned.

Use `const` when the variable should continue referring to the same value.

Important: A `const` object or array can still have its contents modified. The variable binding itself cannot be reassigned.

Example:

```javascript
const student = {
    name: "Alex",
    age: 21
};

student.age = 22;

console.log(student);
```

This is allowed because the object is being modified, not reassigned.

### C. The var Keyword

`var` is an older way of declaring variables in JavaScript.

Example:

```javascript
var studentName = "Alex";

console.log(studentName);
```

Variables declared using `var` can be reassigned.

```javascript
var age = 20;

age = 21;

console.log(age);
```

Although `var` is still supported, modern JavaScript development generally favours `let` and `const` because their scope behaviour is more predictable.

### Comparison of let, const and var

| Feature | `let` | `const` | `var` |
|---|---|---|---|
| Can be reassigned | Yes | No | Yes |
| Can be redeclared in the same scope | No | No | Yes |
| Block-scoped | Yes | Yes | No |
| Must be initialised immediately | No | Yes | No |
| Recommended for modern code | Yes | Yes | Generally avoid |

**Best Practice:** Use `const` by default. Use `let` when reassignment is necessary. Avoid `var` in modern JavaScript unless you have a specific reason to use it.

---

## 3. Declaration, Initialisation and Reassignment

These terms describe different operations.

### Declaration

Creating a variable without assigning a value.

```javascript
let studentName;
```

### Initialisation

Assigning the first value to a variable.

```javascript
let studentName = "Alex";
```

### Reassignment

Giving an existing variable a new value.

```javascript
let studentName = "Alex";

studentName = "Brian";

console.log(studentName);
```

Output:

```text
Brian
```

### Practical Difference

```javascript
// Declaration
let score;

// Initialisation
score = 50;

// Reassignment
score = 75;

console.log(score);
```

Output:

```text
75
```

---

## 4. JavaScript Variable Naming Rules

Variables should have meaningful names that explain the information they store.

JavaScript has rules governing valid variable names.

### Rules

1. A variable name cannot begin with a number.
2. A variable name can contain letters, numbers, underscores and dollar signs.
3. Spaces are not allowed in variable names.
4. Reserved JavaScript keywords cannot be used as variable names.
5. Variable names are case-sensitive.
6. Variable names should communicate their purpose.

### Valid Variable Names

```javascript
let studentName;

let age;

let totalPrice;

let _username;

let $amount;

let product2;
```

### Invalid Variable Names

```javascript
let 2product;

let student name;

let const;

let total-price;
```

These examples are invalid because they violate JavaScript naming rules.

### Naming Convention: camelCase

JavaScript developers commonly use camelCase for variable names.

In camelCase, the first word starts with a lowercase letter, while subsequent words begin with uppercase letters.

Examples:

```javascript
let firstName = "Alex";

let lastName = "Morgan";

let studentRegistrationNumber = "SE2026001";

let totalProductPrice = 2500;
```

Avoid unclear names:

```javascript
let x = 20;

let a = "Laptop";

let p = 500;
```

Prefer descriptive names:

```javascript
let studentAge = 20;

let productName = "Laptop";

let productPrice = 500;
```

---

## 5. Understanding JavaScript Data Types

A data type describes the kind of value a variable stores.

JavaScript has several built-in data types.

They are generally grouped into:

1. Primitive data types.
2. Non-primitive or reference types.

### A. Primitive Data Types

Primitive values represent individual pieces of data.

JavaScript has seven primitive data types.

#### 1. String

A string represents text.

Strings are written inside single quotes, double quotes or backticks.

```javascript
let firstName = "Alex";

let country = 'Kenya';

let message = `Welcome to JavaScript`;

console.log(firstName);

console.log(country);

console.log(message);
```

Output:

```text
Alex
Kenya
Welcome to JavaScript
```

#### 2. Number

The number data type represents both integers and decimal numbers.

```javascript
let age = 21;

let price = 1500;

let temperature = 28.5;

console.log(age);

console.log(price);

console.log(temperature);
```

JavaScript uses one general `number` type for ordinary integer and decimal values.

#### 3. Boolean

A Boolean represents one of two values:

- `true`
- `false`

Example:

```javascript
let isStudent = true;

let isEmployed = false;

console.log(isStudent);

console.log(isEmployed);
```

Booleans are commonly used in conditions and decision-making.

#### 4. Undefined

A variable that has been declared but has not been assigned a value contains `undefined`.

Example:

```javascript
let studentName;

console.log(studentName);
```

Output:

```text
undefined
```

#### 5. Null

`null` represents the intentional absence of a value.

Example:

```javascript
let selectedProduct = null;

console.log(selectedProduct);
```

Output:

```text
null
```

The distinction is important:

- `undefined` often means a value has not been assigned.
- `null` is commonly used to represent an intentionally empty value.

#### 6. BigInt

`BigInt` is used to represent integers larger than the maximum safe integer supported by the ordinary JavaScript `number` type.

Example:

```javascript
let largeNumber = 123456789012345678901234567890n;

console.log(largeNumber);
```

The `n` at the end indicates a BigInt literal.

#### 7. Symbol

A `Symbol` creates a unique primitive value.

Example:

```javascript
let userId = Symbol("id");

let anotherUserId = Symbol("id");

console.log(userId === anotherUserId);
```

Output:

```text
false
```

Although both symbols use the same description, each symbol is unique.

### Summary of Primitive Data Types

| Data Type | Example | Description |
|---|---|---|
| String | `"Hello"` | Text |
| Number | `100` | Numeric values |
| Boolean | `true` | True or false |
| Undefined | `undefined` | Missing assigned value |
| Null | `null` | Intentional absence of value |
| BigInt | `123n` | Large integers |
| Symbol | `Symbol("id")` | Unique identifiers |

---

## 6. Non-Primitive Data Types

Non-primitive values are reference types.

They can represent collections of information or more complex structures.

Two important examples are objects and arrays.

### A. Objects

An object stores related information using key-value pairs.

Example:

```javascript
const student = {
    name: "Alex",
    age: 21,
    country: "Kenya"
};

console.log(student);
```

The object contains three properties:

- `name`
- `age`
- `country`

### B. Arrays

An array stores multiple values in an ordered collection.

Example:

```javascript
const fruits = ["Apple", "Mango", "Orange"];

console.log(fruits);
```

Output:

```text
["Apple", "Mango", "Orange"]
```

Objects and arrays will be covered in greater detail in later modules.

---

## 7. Understanding the typeof Operator

The `typeof` operator identifies the type of a value.

Example:

```javascript
let studentName = "Alex";

let age = 21;

let isStudent = true;

console.log(typeof studentName);

console.log(typeof age);

console.log(typeof isStudent);
```

Output:

```text
string
number
boolean
```

### More Examples

```javascript
console.log(typeof "JavaScript");

console.log(typeof 100);

console.log(typeof 10.5);

console.log(typeof true);

console.log(typeof undefined);

console.log(typeof 123n);

console.log(typeof Symbol("id"));
```

Output:

```text
string
number
number
boolean
undefined
bigint
symbol
```

### An Important JavaScript Behaviour

```javascript
console.log(typeof null);
```

Output:

```text
object
```

This is a historical behaviour in JavaScript. Although `typeof null` returns `"object"`, `null` is a primitive value.

Do not use `typeof` alone to determine whether a value is null. Use:

```javascript
let value = null;

console.log(value === null);
```

Output:

```text
true
```

---

## 8. Type Conversion

Type conversion means changing a value from one data type to another.

JavaScript supports explicit and implicit type conversion.

### A. Explicit Type Conversion

Explicit conversion happens when a developer intentionally converts a value.

#### Converting to String

```javascript
let age = 21;

let ageText = String(age);

console.log(ageText);

console.log(typeof ageText);
```

Output:

```text
21
string
```

#### Converting to Number

```javascript
let price = "1500";

let numericPrice = Number(price);

console.log(numericPrice);

console.log(typeof numericPrice);
```

Output:

```text
1500
number
```

#### Converting to Boolean

```javascript
let value = 1;

let result = Boolean(value);

console.log(result);
```

Output:

```text
true
```

### B. Implicit Type Conversion

Implicit conversion happens when JavaScript automatically converts a value during an operation.

Example:

```javascript
let result = "5" + 2;

console.log(result);
```

Output:

```text
52
```

The number `2` is converted to a string because the `+` operator is performing string concatenation.

Another example:

```javascript
let result = "10" - 2;

console.log(result);
```

Output:

```text
8
```

In this case, JavaScript converts the string `"10"` into a number before subtraction.

**Best Practice:** Convert values intentionally when working with user input, calculations and external data. This makes your code easier to understand and reduces unexpected results.

---

## 9. Common Mistakes When Working with Variables

### Mistake 1: Reassigning a const Variable

Incorrect:

```javascript
const country = "Kenya";

country = "Uganda";
```

Correct:

```javascript
let country = "Kenya";

country = "Uganda";
```

### Mistake 2: Using a Variable Before Initialisation

Incorrect:

```javascript
console.log(studentName);

let studentName = "Alex";
```

This produces a `ReferenceError` because the `let` variable cannot be accessed before its declaration is initialised.

Correct:

```javascript
let studentName = "Alex";

console.log(studentName);
```

### Mistake 3: Confusing Strings and Numbers

```javascript
let firstNumber = "10";

let secondNumber = "5";

console.log(firstNumber + secondNumber);
```

Output:

```text
105
```

The values are strings, so JavaScript joins them.

To perform arithmetic:

```javascript
let firstNumber = Number("10");

let secondNumber = Number("5");

console.log(firstNumber + secondNumber);
```

Output:

```text
15
```

---

## 10. Practical Activity

### Activity: Student Information System

Create a JavaScript programme that stores and displays student information.

### Requirements

Declare variables for:

1. Student's full name.
2. Student's age.
3. Student's country.
4. Student's course.
5. Whether the student is currently enrolled.
6. Student's current grade.
7. Student's registration number.

Use appropriate data types.

### Example Implementation

```javascript
const fullName = "Alex Morgan";

let age = 21;

const country = "Kenya";

const course = "Software Engineering";

const isEnrolled = true;

let currentGrade = null;

const registrationNumber = "SE2026001";

console.log("STUDENT INFORMATION");

console.log("Name:", fullName);

console.log("Age:", age);

console.log("Country:", country);

console.log("Course:", course);

console.log("Currently Enrolled:", isEnrolled);

console.log("Current Grade:", currentGrade);

console.log("Registration Number:", registrationNumber);
```

### Additional Tasks

1. Display the data type of every variable using `typeof`.
2. Change the student's age.
3. Update the student's grade.
4. Convert the age into a string.
5. Display the converted value and its data type.

---

## 11. Knowledge Check

**1. What is a variable?**

A. A JavaScript function.

B. A named storage location for a value.

C. An HTML element.

D. A CSS property.

**2. Which keyword declares a variable that cannot be reassigned?**

A. `var`

B. `let`

C. `const`

D. `static`

**3. Which of the following is a valid variable name?**

A. `2student`

B. `student name`

C. `studentName`

D. `const`

**4. What is the data type of `"JavaScript"`?**

A. Number

B. Boolean

C. String

D. Undefined

**5. What does the following code return?**

```javascript
typeof 25;
```

A. `integer`

B. `number`

C. `string`

D. `boolean`

**6. What is the result of this code?**

```javascript
console.log("10" + 5);
```

A. `15`

B. `105`

C. `10`

D. Error

**7. Which value represents an intentional absence of a value?**

A. `undefined`

B. `false`

C. `null`

D. `0`

**8. Which keyword is generally recommended when a variable does not need reassignment?**

A. `var`

B. `const`

C. `let`

D. `static`

---

## 12. Module Challenge

### Challenge: Personal Finance Information System

Build a simple programme that stores and displays personal finance information.

Your programme should store:

- Account holder's name.
- Account number.
- Account balance.
- Monthly income.
- Monthly expenses.
- Whether the account is active.
- A transaction reference.

### Technical Requirements

- Use `const` for values that should not be reassigned.
- Use `let` for values that may change.
- Use appropriate JavaScript data types.
- Display all information using `console.log()`.
- Use `typeof` to identify at least four data types.
- Convert one numeric string into a number.
- Include comments explaining your code.

### Example Implementation

```javascript
// Personal Finance Information System

const accountHolder = "Alex Morgan";

const accountNumber = "ACC2026001";

let accountBalance = 25000;

let monthlyIncome = 45000;

let monthlyExpenses = 18000;

const isAccountActive = true;

let transactionReference = null;

console.log("PERSONAL FINANCE SYSTEM");

console.log("Account Holder:", accountHolder);

console.log("Account Number:", accountNumber);

console.log("Account Balance:", accountBalance);

console.log("Monthly Income:", monthlyIncome);

console.log("Monthly Expenses:", monthlyExpenses);

console.log("Account Active:", isAccountActive);

console.log("Transaction Reference:", transactionReference);

console.log("DATA TYPES");

console.log(typeof accountHolder);

console.log(typeof accountBalance);

console.log(typeof isAccountActive);
```

### Submission Requirements

1. Create a GitHub repository named `javascript-variables-and-data-types`.
2. Create an `index.html` file.
3. Create an external `script.js` file.
4. Connect the JavaScript file to the HTML document.
5. Implement the finance information programme.
6. Test the programme in your browser.
7. Submit your GitHub repository link.

---

## Key Takeaways

- Variables store information that programmes can access and use.
- JavaScript provides `let`, `const` and `var` for variable declaration.
- `const` prevents reassignment, while `let` allows reassignment.
- JavaScript has seven primitive data types.
- Objects and arrays are reference types.
- The `typeof` operator identifies the type of a value.
- Type conversion changes a value from one data type to another.
- Descriptive variable names improve code readability.
- Modern JavaScript generally favours `const` and `let` over `var`.

---

<p align="center">
  <strong>Congratulations! You have successfully completed Variables and Data Types.</strong>
</p>

<p align="center">
  NEXT: MODULE 03 — OPERATORS
</p>
