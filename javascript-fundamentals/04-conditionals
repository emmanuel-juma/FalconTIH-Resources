
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=JAVASCRIPT%20CONDITIONALS&fontSize=32&fontColor=ffffff&animation=fadeIn&desc=Making%20Decisions%20With%20Code&descSize=13" width="100%">
</p>

<h1 align="center">MODULE 04: CONDITIONAL STATEMENTS</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Control%20Flow-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-BEGINNER-2E86C1?style=for-the-badge">
</p>

## Welcome!

Programmes often need to make decisions.

A login system checks whether a password is correct. A school system determines whether a student has passed an examination. An online store checks whether a product is available before allowing a customer to purchase it.

These decisions are made possible through **conditional statements**.

Conditional statements allow JavaScript to execute different blocks of code depending on whether certain conditions are true or false.

In this module, you will learn how to use `if`, `else`, `else if`, `switch` and the ternary operator to control the flow of a programme.

## Learning Objectives

By the end of this module, you should be able to:

- Explain what conditional statements are.
- Understand how conditions evaluate to Boolean values.
- Write `if` statements.
- Use `if...else` statements.
- Apply `else if` to evaluate multiple conditions.
- Use nested conditional statements.
- Understand and use `switch` statements.
- Apply the ternary operator.
- Combine conditions using logical operators.
- Build simple decision-making applications.

---

## 1. What Are Conditional Statements?

Conditional statements allow a programme to make decisions based on specific conditions.

A condition is an expression that evaluates to either `true` or `false`.

For example:

```javascript
let age = 20;

console.log(age >= 18);
```

Output:

```text
true
```

The expression `age >= 18` is true because the age is 20.

JavaScript can use this result to decide which instructions to execute.

### Real-World Example

Imagine a school system that determines whether a student has passed an examination.

The rule is:

- A score of 50 or higher means Pass.
- A score below 50 means Fail.

A programme can evaluate the student's score and display the appropriate result.

---

## 2. The if Statement

The `if` statement executes a block of code only when a specified condition is true.

### Syntax

```javascript
if (condition) {
    // Code executes when the condition is true
}
```

### Example

```javascript
let age = 20;

if (age >= 18) {
    console.log("You are eligible to register.");
}
```

Output:

```text
You are eligible to register.
```

### Explanation

1. The variable `age` stores the value 20.
2. JavaScript evaluates `age >= 18`.
3. The condition evaluates to `true`.
4. The code inside the `if` block executes.

### Example: Checking a Student's Score

```javascript
let score = 75;

if (score >= 50) {
    console.log("You have passed.");
}
```

Output:

```text
You have passed.
```

If the score were 40, the condition would be false and nothing inside the `if` block would execute.

---

## 3. The if...else Statement

The `if...else` statement allows a programme to execute one block of code when a condition is true and another block when it is false.

### Syntax

```javascript
if (condition) {
    // Executes when condition is true
} else {
    // Executes when condition is false
}
```

### Example

```javascript
let age = 16;

if (age >= 18) {
    console.log("You are an adult.");
} else {
    console.log("You are a minor.");
}
```

Output:

```text
You are a minor.
```

### Example: Pass or Fail

```javascript
let score = 45;

if (score >= 50) {
    console.log("Result: Pass");
} else {
    console.log("Result: Fail");
}
```

Output:

```text
Result: Fail
```

The programme evaluates the condition and executes exactly one of the two blocks.

---

## 4. The if...else if...else Statement

Sometimes a programme needs to evaluate more than two possible outcomes.

For example, a grading system may assign different grades depending on a student's score.

The `else if` statement allows you to check additional conditions.

### Syntax

```javascript
if (condition1) {
    // First condition is true
} else if (condition2) {
    // Second condition is true
} else if (condition3) {
    // Third condition is true
} else {
    // None of the conditions are true
}
```

### Example: Student Grading System

```javascript
let score = 78;

if (score >= 80) {
    console.log("Grade: A");
} else if (score >= 70) {
    console.log("Grade: B");
} else if (score >= 60) {
    console.log("Grade: C");
} else if (score >= 50) {
    console.log("Grade: D");
} else {
    console.log("Grade: F");
}
```

Output:

```text
Grade: B
```

### Understanding the Evaluation

JavaScript evaluates the conditions from top to bottom.

For a score of 78:

1. Is the score at least 80? No.
2. Is the score at least 70? Yes.
3. Display Grade B.
4. Stop evaluating the remaining branches.

**Important:** The order of conditions matters. Place more specific or higher-threshold conditions before lower-threshold conditions when designing a grading system.

---

## 5. Nested if Statements

A nested conditional is an `if` statement placed inside another conditional statement.

Nested conditions are useful when one decision depends on another decision.

### Example: Login Validation

Imagine a login system that first checks whether a user has entered an email address and then checks whether the password is correct.

```javascript
let email = "alex@example.com";

let password = "secure123";

if (email !== "") {

    if (password === "secure123") {
        console.log("Login successful.");
    } else {
        console.log("Incorrect password.");
    }

} else {
    console.log("Please enter your email address.");
}
```

Output:

```text
Login successful.
```

### Explanation

1. JavaScript checks whether the email is empty.
2. If the email is provided, it checks the password.
3. If the password is correct, it displays a success message.
4. Otherwise, it displays an error message.

Nested conditions should be used carefully. Too many levels can make code difficult to read.

---

## 6. The switch Statement

The `switch` statement is used when a programme needs to compare one expression against several possible values.

It is often useful when evaluating fixed options.

### Syntax

```javascript
switch (expression) {
    case value1:
        // Code for value1
        break;

    case value2:
        // Code for value2
        break;

    default:
        // Code when no case matches
}
```

### Example: Days of the Week

```javascript
let day = "Monday";

switch (day) {

    case "Monday":
        console.log("Start of the working week.");
        break;

    case "Friday":
        console.log("End of the working week.");
        break;

    case "Saturday":
        console.log("Weekend.");
        break;

    case "Sunday":
        console.log("Weekend.");
        break;

    default:
        console.log("Regular working day.");
}
```

Output:

```text
Start of the working week.
```

### Understanding break

The `break` statement stops execution from continuing into the next case.

Without `break`, JavaScript may continue executing subsequent cases. This behaviour is called fall-through.

### Understanding default

The `default` block executes when none of the cases match.

Example:

```javascript
let paymentMethod = "Cash";

switch (paymentMethod) {

    case "M-Pesa":
        console.log("Pay using M-Pesa.");
        break;

    case "Card":
        console.log("Pay using a bank card.");
        break;

    case "Cash":
        console.log("Pay using cash.");
        break;

    default:
        console.log("Unsupported payment method.");
}
```

---

## 7. The Ternary Operator

The ternary operator provides a shorter way to write a simple conditional expression.

It uses three parts:

1. A condition.
2. A value returned when the condition is true.
3. A value returned when the condition is false.

### Syntax

```javascript
condition ? valueIfTrue : valueIfFalse;
```

### Example

```javascript
let age = 20;

let result = age >= 18 ? "Adult" : "Minor";

console.log(result);
```

Output:

```text
Adult
```

### Example: Examination Result

```javascript
let score = 65;

let result = score >= 50 ? "Pass" : "Fail";

console.log(result);
```

Output:

```text
Pass
```

The ternary operator is useful for simple decisions. For complex logic, use ordinary conditional statements.

---

## 8. Combining Conditions with Logical Operators

Conditional statements become more powerful when combined with logical operators.

The three main logical operators are:

| Operator | Meaning |
|---|---|
| `&&` | Both conditions must be true |
| `||` | At least one condition must be true |
| `!` | Reverses a Boolean value |

### Example: Registration Eligibility

A person can register if they are at least 18 years old and have a valid identification document.

```javascript
let age = 22;

let hasIdentification = true;

if (age >= 18 && hasIdentification) {
    console.log("Registration approved.");
} else {
    console.log("Registration denied.");
}
```

### Example: Alternative Login Methods

A user can log in using either an email address or a phone number.

```javascript
let hasEmail = false;

let hasPhoneNumber = true;

if (hasEmail || hasPhoneNumber) {
    console.log("You can continue.");
} else {
    console.log("Provide an email or phone number.");
}
```

### Example: Negating a Condition

```javascript
let isBlocked = false;

if (!isBlocked) {
    console.log("Access granted.");
}
```

Output:

```text
Access granted.
```

---

## 9. Truthy and Falsy Values

JavaScript conditions do not always require explicit Boolean values.

Some values are automatically treated as true or false when evaluated in a Boolean context.

These values are known as truthy and falsy values.

### Common Falsy Values

| Value | Description |
|---|---|
| `false` | Boolean false |
| `0` | Number zero |
| `-0` | Negative zero |
| `0n` | BigInt zero |
| `""` | Empty string |
| `null` | Intentional absence of value |
| `undefined` | Missing value |
| `NaN` | Not a Number |

All other ordinary values are truthy, including:

- `"Hello"`
- `"0"`
- `1`
- `-1`
- `[]`
- `{}`

### Example

```javascript
let username = "";

if (username) {
    console.log("Username provided.");
} else {
    console.log("Username is required.");
}
```

Output:

```text
Username is required.
```

The empty string is falsy, so the `else` block executes.

### Example with a Truthy Value

```javascript
let username = "Alex";

if (username) {
    console.log("Username provided.");
} else {
    console.log("Username is required.");
}
```

Output:

```text
Username provided.
```

---

## 10. Common Conditional Errors

### Mistake 1: Using Assignment Instead of Comparison

Incorrect:

```javascript
let age = 20;

if (age = 18) {
    console.log("Eligible");
}
```

The single `=` operator assigns a value. It does not compare two values.

Correct:

```javascript
let age = 20;

if (age === 18) {
    console.log("Age is exactly 18.");
}
```

### Mistake 2: Incorrect Condition Ordering

Incorrect:

```javascript
let score = 85;

if (score >= 50) {
    console.log("Pass");
} else if (score >= 80) {
    console.log("Grade A");
}
```

The first condition is already true for 85, so the Grade A condition is never reached.

Correct:

```javascript
let score = 85;

if (score >= 80) {
    console.log("Grade A");
} else if (score >= 50) {
    console.log("Pass");
} else {
    console.log("Fail");
}
```

### Mistake 3: Forgetting break in switch

Incorrect:

```javascript
let choice = 1;

switch (choice) {
    case 1:
        console.log("One");

    case 2:
        console.log("Two");
}
```

The code may execute both cases because there is no `break`.

Correct:

```javascript
let choice = 1;

switch (choice) {
    case 1:
        console.log("One");
        break;

    case 2:
        console.log("Two");
        break;
}
```

---

## 11. Practical Activity

### Activity: Student Grading Application

Create a programme that evaluates a student's examination score and displays the appropriate grade.

### Grading Criteria

| Score | Grade | Result |
|---|---|---|
| 80–100 | A | Excellent |
| 70–79 | B | Very Good |
| 60–69 | C | Good |
| 50–59 | D | Pass |
| 0–49 | F | Fail |

### Requirements

Your programme should:

1. Store a student's name.
2. Store the examination score.
3. Check whether the score is valid.
4. Assign a grade using conditional statements.
5. Display the student's name.
6. Display the score.
7. Display the grade and result.

### Example Implementation

```javascript
const studentName = "Alex Morgan";

const score = 78;

let grade;

if (score < 0 || score > 100) {

    grade = "Invalid score";

} else if (score >= 80) {

    grade = "A";

} else if (score >= 70) {

    grade = "B";

} else if (score >= 60) {

    grade = "C";

} else if (score >= 50) {

    grade = "D";

} else {

    grade = "F";

}

console.log("STUDENT REPORT");

console.log("Name:", studentName);

console.log("Score:", score);

console.log("Grade:", grade);
```

### Additional Tasks

1. Add a condition that checks whether the student passed.
2. Display a different message for each grade.
3. Use a ternary operator to determine whether the student passed.
4. Add a second student and compare their results.

---

## 12. Knowledge Check

**1. What is the purpose of conditional statements?**

A. To store information.

B. To make decisions based on conditions.

C. To create HTML elements.

D. To style webpages.

**2. Which statement executes code only when a condition is true?**

A. `switch`

B. `for`

C. `if`

D. `return`

**3. Which keyword handles the alternative when an if condition is false?**

A. `then`

B. `else`

C. `case`

D. `default`

**4. Which keyword is used to evaluate another condition?**

A. `else if`

B. `otherwise`

C. `continue`

D. `next`

**5. What is the purpose of break in a switch statement?**

A. It declares a variable.

B. It stops execution from continuing into subsequent cases.

C. It restarts the programme.

D. It checks a condition.

**6. What is the result of this expression?**

```javascript
console.log(Boolean(""));
```

A. true

B. false

C. undefined

D. null

**7. Which operator requires both conditions to be true?**

A. `||`

B. `&&`

C. `!`

D. `=`

**8. What is the result of the following code?**

```javascript
let age = 20;

if (age >= 18) {
    console.log("Adult");
} else {
    console.log("Minor");
}
```

A. Minor

B. Adult

C. Error

D. Nothing

---

## 13. Module Challenge

### Challenge: Online Store Discount System

Build a simple programme that determines the discount a customer receives based on the total purchase amount.

### Discount Criteria

| Purchase Amount | Discount |
|---|---|
| Below KES 5,000 | No discount |
| KES 5,000–9,999 | 5% |
| KES 10,000–19,999 | 10% |
| KES 20,000 and above | 15% |

### Technical Requirements

- Store the customer's name.
- Store the purchase amount.
- Validate that the purchase amount is not negative.
- Determine the applicable discount.
- Calculate the discount amount.
- Calculate the final amount payable.
- Display a complete purchase summary.

### Example Implementation

```javascript
// Online Store Discount System

const customerName = "Alex Morgan";

const purchaseAmount = 15000;

let discountRate;

if (purchaseAmount < 0) {

    console.log("Invalid purchase amount.");

} else {

    if (purchaseAmount >= 20000) {
        discountRate = 0.15;

    } else if (purchaseAmount >= 10000) {
        discountRate = 0.10;

    } else if (purchaseAmount >= 5000) {
        discountRate = 0.05;

    } else {
        discountRate = 0;
    }

    const discountAmount = purchaseAmount * discountRate;

    const finalAmount = purchaseAmount - discountAmount;

    console.log("PURCHASE SUMMARY");

    console.log("Customer:", customerName);

    console.log("Purchase Amount:", purchaseAmount);

    console.log("Discount Rate:", discountRate * 100 + "%");

    console.log("Discount Amount:", discountAmount);

    console.log("Final Amount:", finalAmount);
}
```

### Submission Requirements

1. Create a GitHub repository named `javascript-conditionals`.
2. Create an `index.html` file.
3. Create an external `script.js` file.
4. Implement the discount system.
5. Use `if`, `else if` and `else`.
6. Validate the purchase amount.
7. Test different purchase values.
8. Submit your GitHub repository link.

---

## Key Takeaways

- Conditional statements control programme execution.
- An `if` statement executes code when a condition is true.
- `if...else` provides two possible execution paths.
- `else if` allows multiple conditions to be evaluated.
- Nested conditionals allow one decision to depend on another.
- `switch` evaluates an expression against multiple cases.
- `break` prevents unwanted fall-through in switch statements.
- The ternary operator is useful for simple conditional expressions.
- Logical operators allow multiple conditions to be combined.
- Truthy and falsy values influence how conditions are evaluated.

---

<p align="center">
  <strong>Congratulations! You have successfully completed JavaScript Conditional Statements.</strong>
</p>

<p align="center">
  NEXT: MODULE 05 — LOOPS
</p>
