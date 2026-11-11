
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=JAVASCRIPT%20OPERATORS&fontSize=32&fontColor=ffffff&animation=fadeIn&desc=Working%20With%20Values%20And%20Expressions&descSize=13" width="100%">
</p>

<h1 align="center">MODULE 03: JAVASCRIPT OPERATORS</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Operators-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-BEGINNER-2E86C1?style=for-the-badge">
</p>

## Welcome!

In the previous module, you learned how to store information using variables and how to identify different JavaScript data types.

Now that you understand how JavaScript stores data, you need to learn how to work with that data.

For example:

- How do you calculate the total price of products?
- How do you determine whether a student has passed an examination?
- How do you check whether a user is old enough to register?
- How do you compare two account balances?
- How do you combine multiple conditions?

JavaScript uses **operators** to perform these operations.

In this module, you will explore arithmetic, assignment, comparison, logical, string and other useful JavaScript operators.

## Learning Objectives

By the end of this module, you should be able to:

- Explain what JavaScript operators are.
- Use arithmetic operators to perform calculations.
- Apply assignment operators to update variables.
- Compare values using comparison operators.
- Understand strict and loose equality.
- Combine conditions using logical operators.
- Use increment and decrement operators.
- Understand the conditional operator.
- Apply operator precedence.
- Build simple calculations using JavaScript.

---

## 1. What are JavaScript Operators?

An operator is a symbol or keyword that performs an operation on one or more values.

Consider:

```javascript
let result = 10 + 5;
```

In this example:

- `10` is an operand.
- `5` is an operand.
- `+` is the operator.
- `15` is the result.

Operators allow JavaScript programmes to calculate values, compare information, assign data and make logical decisions.

### Types of JavaScript Operators

| Operator Category | Purpose |
|---|---|
| Arithmetic | Performs mathematical calculations |
| Assignment | Assigns or updates variable values |
| Comparison | Compares two values |
| Logical | Combines or reverses conditions |
| Increment and Decrement | Increases or decreases a value |
| String | Combines strings |
| Conditional | Selects a value based on a condition |
| Type | Checks or identifies data types |

---

## 2. Arithmetic Operators

Arithmetic operators perform mathematical calculations.

JavaScript supports several arithmetic operators.

| Operator | Name | Example | Result |
|---|---|---|---|
| `+` | Addition | `10 + 5` | `15` |
| `-` | Subtraction | `10 - 5` | `5` |
| `*` | Multiplication | `10 * 5` | `50` |
| `/` | Division | `10 / 5` | `2` |
| `%` | Modulus | `10 % 3` | `1` |
| `**` | Exponentiation | `2 ** 3` | `8` |

### A. Addition

The addition operator adds two values.

```javascript
let firstNumber = 10;

let secondNumber = 5;

let result = firstNumber + secondNumber;

console.log(result);
```

Output:

```text
15
```

### B. Subtraction

The subtraction operator finds the difference between two values.

```javascript
let price = 1000;

let discount = 200;

let finalPrice = price - discount;

console.log(finalPrice);
```

Output:

```text
800
```

### C. Multiplication

The multiplication operator multiplies values.

```javascript
let price = 500;

let quantity = 4;

let total = price * quantity;

console.log(total);
```

Output:

```text
2000
```

### D. Division

The division operator divides one value by another.

```javascript
let totalAmount = 1000;

let numberOfPeople = 4;

let amountPerPerson = totalAmount / numberOfPeople;

console.log(amountPerPerson);
```

Output:

```text
250
```

### E. Modulus

The modulus operator `%` returns the remainder after division.

```javascript
let result = 10 % 3;

console.log(result);
```

Output:

```text
1
```

The remainder is `1` because 3 goes into 10 three times, leaving 1.

A common use of modulus is checking whether a number is even or odd.

```javascript
let number = 8;

console.log(number % 2);
```

Output:

```text
0
```

If a number divided by 2 has a remainder of zero, it is even.

### F. Exponentiation

The exponentiation operator raises a number to a power.

```javascript
let result = 2 ** 3;

console.log(result);
```

Output:

```text
8
```

This is equivalent to:

```text
2 × 2 × 2 = 8
```

---

## 3. Assignment Operators

Assignment operators assign values to variables or update their existing values.

The basic assignment operator is `=`.

Example:

```javascript
let age = 21;

console.log(age);
```

Output:

```text
21
```

### Compound Assignment Operators

JavaScript provides shorthand operators that combine an arithmetic operation with assignment.

| Operator | Example | Equivalent |
|---|---|---|
| `=` | `x = 10` | Assigns 10 |
| `+=` | `x += 5` | `x = x + 5` |
| `-=` | `x -= 5` | `x = x - 5` |
| `*=` | `x *= 5` | `x = x * 5` |
| `/=` | `x /= 5` | `x = x / 5` |
| `%=` | `x %= 5` | `x = x % 5` |
| `**=` | `x **= 2` | `x = x ** 2` |

### Example 1: Addition Assignment

```javascript
let balance = 1000;

balance += 500;

console.log(balance);
```

Output:

```text
1500
```

### Example 2: Subtraction Assignment

```javascript
let balance = 1000;

balance -= 200;

console.log(balance);
```

Output:

```text
800
```

### Example 3: Multiplication Assignment

```javascript
let quantity = 5;

quantity *= 2;

console.log(quantity);
```

Output:

```text
10
```

### Example 4: Division Assignment

```javascript
let total = 100;

total /= 4;

console.log(total);
```

Output:

```text
25
```

---

## 4. Comparison Operators

Comparison operators compare two values and return a Boolean result.

The result is either:

- `true`
- `false`

| Operator | Meaning | Example |
|---|---|---|
| `==` | Equal value | `5 == "5"` |
| `===` | Equal value and type | `5 === 5` |
| `!=` | Not equal value | `5 != 3` |
| `!==` | Not equal value or type | `5 !== "5"` |
| `>` | Greater than | `10 > 5` |
| `<` | Less than | `5 < 10` |
| `>=` | Greater than or equal to | `10 >= 10` |
| `<=` | Less than or equal to | `5 <= 10` |

### A. Equality Operator

The `==` operator compares values after performing type conversion when necessary.

```javascript
console.log(5 == "5");
```

Output:

```text
true
```

JavaScript converts the string `"5"` into a number before comparison.

### B. Strict Equality Operator

The `===` operator compares both value and data type without performing automatic type conversion.

```javascript
console.log(5 === "5");
```

Output:

```text
false
```

The first value is a number, while the second is a string.

Another example:

```javascript
console.log(10 === 10);
```

Output:

```text
true
```

**Best Practice:** Prefer `===` over `==` in most JavaScript comparisons because strict equality produces more predictable results.

### C. Not Equal Operator

The `!=` operator checks whether two values are different after possible type conversion.

```javascript
console.log(10 != 5);
```

Output:

```text
true
```

### D. Strict Not Equal Operator

The `!==` operator checks whether values or their types differ.

```javascript
console.log(10 !== "10");
```

Output:

```text
true
```

### E. Greater Than and Less Than

```javascript
console.log(20 > 10);

console.log(5 < 3);
```

Output:

```text
true
false
```

### F. Greater Than or Equal To

```javascript
console.log(18 >= 18);

console.log(20 >= 18);
```

Output:

```text
true
true
```

### G. Less Than or Equal To

```javascript
console.log(10 <= 20);

console.log(15 <= 10);
```

Output:

```text
true
false
```

---

## 5. Logical Operators

Logical operators combine or reverse Boolean conditions.

They are especially useful when a programme needs to evaluate multiple requirements.

JavaScript has three main logical operators:

| Operator | Name | Description |
|---|---|---|
| `&&` | AND | True when both conditions are true |
| `||` | OR | True when at least one condition is true |
| `!` | NOT | Reverses a Boolean value |

### A. Logical AND

The `&&` operator returns true only when both conditions are true.

Example:

```javascript
let age = 22;

let hasNationalId = true;

console.log(age >= 18 && hasNationalId);
```

Output:

```text
true
```

Both conditions are satisfied.

#### AND Truth Table

| Condition A | Condition B | A && B |
|---|---|---|
| true | true | true |
| true | false | false |
| false | true | false |
| false | false | false |

### B. Logical OR

The `||` operator returns true when at least one condition is true.

Example:

```javascript
let hasEmail = false;

let hasPhoneNumber = true;

console.log(hasEmail || hasPhoneNumber);
```

Output:

```text
true
```

At least one condition is true.

#### OR Truth Table

| Condition A | Condition B | A \|\| B |
|---|---|---|
| true | true | true |
| true | false | true |
| false | true | true |
| false | false | false |

### C. Logical NOT

The `!` operator reverses a Boolean value.

Example:

```javascript
let isLoggedIn = true;

console.log(!isLoggedIn);
```

Output:

```text
false
```

Another example:

```javascript
let isAvailable = false;

console.log(!isAvailable);
```

Output:

```text
true
```

### Practical Example: User Registration

Imagine a registration system that requires a user to be at least 18 years old and have an email address.

```javascript
let age = 21;

let hasEmail = true;

let canRegister = age >= 18 && hasEmail;

console.log(canRegister);
```

Output:

```text
true
```

The user can register because both conditions are true.

---

## 6. Increment and Decrement Operators

Increment and decrement operators increase or decrease a numeric variable by one.

### A. Increment Operator

The `++` operator increases a value by one.

```javascript
let count = 5;

count++;

console.log(count);
```

Output:

```text
6
```

This is equivalent to:

```javascript
count = count + 1;
```

### B. Decrement Operator

The `--` operator decreases a value by one.

```javascript
let count = 5;

count--;

console.log(count);
```

Output:

```text
4
```

This is equivalent to:

```javascript
count = count - 1;
```

### Prefix and Postfix

Increment and decrement operators can appear before or after a variable.

**Postfix:**

```javascript
let number = 5;

let result = number++;

console.log(result);

console.log(number);
```

Output:

```text
5
6
```

The postfix operator returns the original value before incrementing the variable.

**Prefix:**

```javascript
let number = 5;

let result = ++number;

console.log(result);

console.log(number);
```

Output:

```text
6
6
```

The prefix operator increments the variable before returning its value.

---

## 7. String Operators

The `+` operator can combine strings. This process is known as string concatenation.

Example:

```javascript
let firstName = "Alex";

let lastName = "Morgan";

let fullName = firstName + " " + lastName;

console.log(fullName);
```

Output:

```text
Alex Morgan
```

### Using the += Operator with Strings

```javascript
let message = "Welcome";

message += " to JavaScript";

console.log(message);
```

Output:

```text
Welcome to JavaScript
```

### Template Literals

Template literals provide another way of combining strings and values.

They use backticks.

Example:

```javascript
let studentName = "Alex";

let age = 21;

let message = `My name is ${studentName} and I am ${age} years old.`;

console.log(message);
```

Output:

```text
My name is Alex and I am 21 years old.
```

Template literals are particularly useful when creating dynamic messages.

---

## 8. The Conditional Operator

The conditional operator is also known as the ternary operator.

It provides a shorter way of selecting one of two values based on a condition.

Syntax:

```javascript
condition ? valueIfTrue : valueIfFalse;
```

Example:

```javascript
let age = 20;

let message = age >= 18 ? "Adult" : "Minor";

console.log(message);
```

Output:

```text
Adult
```

Explanation:

- If `age >= 18` is true, JavaScript selects `"Adult"`.
- Otherwise, it selects `"Minor"`.

### Another Example

```javascript
let score = 75;

let result = score >= 50 ? "Pass" : "Fail";

console.log(result);
```

Output:

```text
Pass
```

The conditional operator is useful for simple decisions. For complex decision-making, use `if...else` statements, which will be covered in the next module.

---

## 9. Operator Precedence

Operator precedence determines the order in which JavaScript evaluates operations in an expression.

Consider:

```javascript
let result = 10 + 5 * 2;

console.log(result);
```

Output:

```text
20
```

Multiplication is performed before addition.

JavaScript evaluates:

```text
10 + 10 = 20
```

### Using Parentheses

Parentheses can change the order of evaluation.

```javascript
let result = (10 + 5) * 2;

console.log(result);
```

Output:

```text
30
```

JavaScript first calculates the expression inside the parentheses.

### Practical Recommendation

Use parentheses to make complex expressions easier to understand.

For example:

```javascript
let total = (price * quantity) - discount;
```

This makes the intended calculation clear.

---

## 10. Practical Activity

### Activity: Shopping Cart Calculator

Create a JavaScript programme that calculates the total cost of products purchased by a customer.

### Product Information

| Product | Unit Price | Quantity |
|---|---:|---:|
| Laptop | 75,000 | 1 |
| Mouse | 1,500 | 2 |
| Keyboard | 3,000 | 1 |

### Requirements

Your programme should:

1. Store each product's price.
2. Store the quantity purchased.
3. Calculate the total price of each product.
4. Calculate the total shopping cost.
5. Apply a discount of KES 5,000.
6. Calculate the final amount payable.
7. Display the results using `console.log()`.

### Example Implementation

```javascript
// Product Information

const laptopPrice = 75000;

const laptopQuantity = 1;

const mousePrice = 1500;

const mouseQuantity = 2;

const keyboardPrice = 3000;

const keyboardQuantity = 1;

// Calculate Product Totals

const laptopTotal = laptopPrice * laptopQuantity;

const mouseTotal = mousePrice * mouseQuantity;

const keyboardTotal = keyboardPrice * keyboardQuantity;

// Calculate Shopping Total

const shoppingTotal = laptopTotal + mouseTotal + keyboardTotal;

// Apply Discount

const discount = 5000;

const finalAmount = shoppingTotal - discount;

// Display Results

console.log("SHOPPING CART");

console.log("Laptop:", laptopTotal);

console.log("Mouse:", mouseTotal);

console.log("Keyboard:", keyboardTotal);

console.log("Shopping Total:", shoppingTotal);

console.log("Discount:", discount);

console.log("Final Amount:", finalAmount);
```

### Expected Output

```text
SHOPPING CART

Laptop: 75000
Mouse: 3000
Keyboard: 3000
Shopping Total: 81000
Discount: 5000
Final Amount: 76000
```

### Additional Tasks

1. Add another product.
2. Increase the mouse quantity.
3. Calculate a discount percentage instead of a fixed discount.
4. Check whether the final amount exceeds KES 50,000.
5. Use template literals to display a customer summary.

---

## 11. Knowledge Check

**1. What is an operator in JavaScript?**

A. A storage location.

B. A symbol or keyword that performs an operation.

C. An HTML element.

D. A JavaScript file.

**2. Which operator performs multiplication?**

A. `+`

B. `/`

C. `*`

D. `%`

**3. What is the result of `10 % 3`?**

A. `3`

B. `1`

C. `0`

D. `10`

**4. Which operator checks strict equality?**

A. `=`

B. `==`

C. `===`

D. `!=`

**5. What is the result of the following expression?**

```javascript
console.log(5 === "5");
```

A. true

B. false

C. 5

D. Error

**6. Which logical operator requires both conditions to be true?**

A. `||`

B. `&&`

C. `!`

D. `=`

**7. What does the increment operator do?**

A. Decreases a value by one.

B. Increases a value by one.

C. Multiplies a value by two.

D. Divides a value by two.

**8. What is the output of the following code?**

```javascript
let number = 10;

number += 5;

console.log(number);
```

A. 10

B. 5

C. 15

D. 50

**9. Which operator is used to combine strings?**

A. `*`

B. `+`

C. `/`

D. `%`

**10. What is the result of the following expression?**

```javascript
console.log(10 + 5 * 2);
```

A. 30

B. 20

C. 25

D. 15

---

## 12. Module Challenge

### Challenge: Personal Budget Calculator

Build a JavaScript programme that calculates a person's monthly budget.

Your programme should store:

- Monthly income.
- Rent.
- Food expenses.
- Transport expenses.
- Internet expenses.
- Savings contribution.

### Technical Requirements

1. Declare appropriate variables.
2. Calculate total expenses.
3. Calculate the remaining balance.
4. Calculate the percentage of income spent.
5. Calculate the percentage of income saved.
6. Check whether the person has money remaining.
7. Use comparison and logical operators.
8. Display a clear financial summary.

### Example Implementation

```javascript
// Personal Budget Calculator

const monthlyIncome = 50000;

const rent = 15000;

const food = 10000;

const transport = 5000;

const internet = 2000;

const savings = 8000;

// Calculate Total Expenses

const totalExpenses = rent + food + transport + internet;

// Calculate Remaining Balance

const remainingBalance = monthlyIncome - totalExpenses - savings;

// Calculate Percentages

const expensePercentage = (totalExpenses / monthlyIncome) * 100;

const savingsPercentage = (savings / monthlyIncome) * 100;

// Check Financial Status

const hasSurplus = remainingBalance > 0;

const isWithinBudget = totalExpenses + savings <= monthlyIncome;

// Display Results

console.log("MONTHLY BUDGET SUMMARY");

console.log("Monthly Income:", monthlyIncome);

console.log("Total Expenses:", totalExpenses);

console.log("Savings:", savings);

console.log("Remaining Balance:", remainingBalance);

console.log("Expense Percentage:", expensePercentage + "%");

console.log("Savings Percentage:", savingsPercentage + "%");

console.log("Has Surplus:", hasSurplus);

console.log("Within Budget:", isWithinBudget);
```

### Submission Requirements

1. Create a GitHub repository named `javascript-operators`.
2. Create an `index.html` file.
3. Create an external `script.js` file.
4. Implement the budget calculator.
5. Use arithmetic, assignment, comparison and logical operators.
6. Test your programme in the browser.
7. Submit your GitHub repository link.

---

## Key Takeaways

- Operators perform operations on values and variables.
- Arithmetic operators perform mathematical calculations.
- Assignment operators assign or update variable values.
- Comparison operators return Boolean results.
- Strict equality checks both value and data type.
- Logical operators combine or reverse conditions.
- Increment and decrement operators change a numeric value by one.
- Template literals make dynamic strings easier to construct.
- The ternary operator provides a concise way to select between two values.
- Operator precedence determines the order of expression evaluation.

---

<p align="center">
  <strong>Congratulations! You have successfully completed JavaScript Operators.</strong>
</p>

<p align="center">
  NEXT: MODULE 04 — CONDITIONALS
</p>
