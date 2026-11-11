
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=JAVASCRIPT%20LOOPS&fontSize=32&fontColor=ffffff&animation=fadeIn&desc=Repeating%20Tasks%20Efficiently&descSize=13" width="100%">
</p>

<h1 align="center">MODULE 05: LOOPS</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Loops-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-BEGINNER-2E86C1?style=for-the-badge">
</p>

## Welcome!

Imagine writing a programme that needs to display the numbers from 1 to 100.

Would you write 100 separate `console.log()` statements?

What if you needed to display 1,000 product names or process 10,000 customer records?

Writing the same instruction repeatedly would be inefficient.

JavaScript solves this problem using **loops**.

Loops allow developers to execute a block of code repeatedly while a specified condition is satisfied or while there are items left to process.

In this module, you will learn how to use `for`, `while`, `do...while`, `for...of` and `for...in` loops.

## Learning Objectives

By the end of this module, you should be able to:

- Explain what loops are.
- Understand why loops are used.
- Write `for` loops.
- Use `while` loops.
- Apply `do...while` loops.
- Understand `for...of` and `for...in`.
- Use `break` and `continue`.
- Avoid infinite loops.
- Loop through arrays and objects.
- Build simple programmes that repeat operations.

---

## 1. What Are Loops?

A loop is a programming structure that repeats a block of code.

Loops are useful when a task needs to be performed multiple times.

### Example Without a Loop

```javascript
console.log(1);

console.log(2);

console.log(3);

console.log(4);

console.log(5);
```

This works, but writing separate instructions becomes inefficient when the number of repetitions increases.

### Example Using a Loop

```javascript
for (let number = 1; number <= 5; number++) {
    console.log(number);
}
```

Output:

```text
1
2
3
4
5
```

The loop performs the same task repeatedly without requiring separate statements.

---

## 2. The for Loop

A `for` loop is commonly used when the number of repetitions is known or when a counter controls the repetition.

### Syntax

```javascript
for (initialisation; condition; update) {
    // Code to execute
}
```

A `for` loop has three main components.

| Component | Purpose |
|---|---|
| Initialisation | Creates or assigns the starting value |
| Condition | Determines whether the loop should continue |
| Update | Changes the counter after each iteration |

### Example

```javascript
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```

Output:

```text
1
2
3
4
5
```

### Understanding the Execution

1. `let i = 1` sets the starting value.
2. `i <= 5` checks whether the loop should continue.
3. `console.log(i)` displays the current value.
4. `i++` increases the counter by one.
5. The condition is checked again.
6. The loop stops when the condition becomes false.

### Example: Counting Backwards

```javascript
for (let i = 5; i >= 1; i--) {
    console.log(i);
}
```

Output:

```text
5
4
3
2
1
```

### Example: Even Numbers

```javascript
for (let i = 2; i <= 10; i += 2) {
    console.log(i);
}
```

Output:

```text
2
4
6
8
10
```

### Example: Multiplication Table

```javascript
let number = 5;

for (let i = 1; i <= 10; i++) {

    console.log(`${number} x ${i} = ${number * i}`);

}
```

Output:

```text
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```

---

## 3. The while Loop

A `while` loop executes a block of code as long as its condition remains true.

Unlike a `for` loop, the initialisation and update are generally written separately.

### Syntax

```javascript
while (condition) {
    // Code to execute
}
```

### Example

```javascript
let count = 1;

while (count <= 5) {

    console.log(count);

    count++;

}
```

Output:

```text
1
2
3
4
5
```

### Understanding the Execution

1. The variable `count` starts at 1.
2. JavaScript checks whether `count <= 5`.
3. If true, the current value is displayed.
4. The counter increases by one.
5. The condition is checked again.
6. The loop stops when the condition becomes false.

### Example: Countdown

```javascript
let countdown = 5;

while (countdown >= 1) {

    console.log(countdown);

    countdown--;

}

console.log("Finished!");
```

Output:

```text
5
4
3
2
1
Finished!
```

---

## 4. The do...while Loop

A `do...while` loop is similar to a `while` loop, but it checks the condition after executing the code block.

This means the code executes at least once, even when the condition is initially false.

### Syntax

```javascript
do {
    // Code to execute
} while (condition);
```

### Example

```javascript
let number = 1;

do {

    console.log(number);

    number++;

} while (number <= 5);
```

Output:

```text
1
2
3
4
5
```

### Understanding the Difference

Consider the following examples.

**While loop:**

```javascript
let number = 10;

while (number < 5) {
    console.log(number);
}
```

Output:

```text
```

Nothing is displayed because the condition is false before the loop begins.

**Do...while loop:**

```javascript
let number = 10;

do {
    console.log(number);
} while (number < 5);
```

Output:

```text
10
```

The code executes once before JavaScript checks the condition.

### When Should You Use do...while?

It is useful when an operation must happen at least once before checking whether it should continue.

---

## 5. The for...of Loop

The `for...of` loop is used to iterate over iterable values such as arrays and strings.

It provides a simple way to access each value without manually managing an index.

### Syntax

```javascript
for (const value of iterable) {
    // Code to execute
}
```

### Example: Looping Through an Array

```javascript
const fruits = ["Apple", "Mango", "Orange", "Banana"];

for (const fruit of fruits) {
    console.log(fruit);
}
```

Output:

```text
Apple
Mango
Orange
Banana
```

### Example: Looping Through a String

```javascript
const word = "CODE";

for (const character of word) {
    console.log(character);
}
```

Output:

```text
C
O
D
E
```

### When Should You Use for...of?

Use `for...of` when you want to process each value in an array, string or another iterable collection.

---

## 6. The for...in Loop

The `for...in` loop iterates over the enumerable property keys of an object.

### Syntax

```javascript
for (const key in object) {
    // Code to execute
}
```

### Example: Looping Through an Object

```javascript
const student = {
    name: "Alex",
    age: 21,
    course: "Software Engineering"
};

for (const key in student) {

    console.log(key);

}
```

Output:

```text
name
age
course
```

### Accessing Object Values

You can use the key to access its corresponding value.

```javascript
const student = {
    name: "Alex",
    age: 21,
    course: "Software Engineering"
};

for (const key in student) {

    console.log(`${key}: ${student[key]}`);

}
```

Output:

```text
name: Alex
age: 21
course: Software Engineering
```

**Important:** Use `for...of` for iterable values such as arrays and `for...in` for object property keys. Avoid using `for...in` as the default way to process arrays.

---

## 7. The break Statement

The `break` statement immediately terminates a loop.

It is useful when a loop should stop once a particular condition has been satisfied.

### Example

```javascript
for (let i = 1; i <= 10; i++) {

    if (i === 5) {
        break;
    }

    console.log(i);

}
```

Output:

```text
1
2
3
4
```

When `i` becomes 5, JavaScript executes `break` and exits the loop.

---

## 8. The continue Statement

The `continue` statement skips the current iteration and moves to the next iteration.

### Example

```javascript
for (let i = 1; i <= 5; i++) {

    if (i === 3) {
        continue;
    }

    console.log(i);

}
```

Output:

```text
1
2
4
5
```

The value 3 is skipped, but the loop continues.

### Example: Displaying Odd Numbers

```javascript
for (let i = 1; i <= 10; i++) {

    if (i % 2 === 0) {
        continue;
    }

    console.log(i);

}
```

Output:

```text
1
3
5
7
9
```

---

## 9. Nested Loops

A nested loop is a loop placed inside another loop.

Nested loops are useful when working with rows and columns, tables and combinations of data.

### Example: Multiplication Pattern

```javascript
for (let i = 1; i <= 3; i++) {

    for (let j = 1; j <= 3; j++) {

        console.log(`i: ${i}, j: ${j}`);

    }

}
```

Output:

```text
i: 1, j: 1
i: 1, j: 2
i: 1, j: 3
i: 2, j: 1
i: 2, j: 2
i: 2, j: 3
i: 3, j: 1
i: 3, j: 2
i: 3, j: 3
```

### Example: Creating a Number Grid

```javascript
for (let row = 1; row <= 3; row++) {

    let output = "";

    for (let column = 1; column <= 3; column++) {

        output += `${column} `;

    }

    console.log(output);

}
```

Output:

```text
1 2 3
1 2 3
1 2 3
```

The inner loop completes all its iterations for every single iteration of the outer loop.

---

## 10. Infinite Loops

An infinite loop is a loop that continues executing because its stopping condition is never reached.

Example:

```javascript
let number = 1;

while (number <= 5) {

    console.log(number);

}
```

This loop never stops because `number` is never updated.

### Correct Version

```javascript
let number = 1;

while (number <= 5) {

    console.log(number);

    number++;

}
```

Always ensure that a loop has a valid stopping condition and that its variables are updated correctly.

---

## 11. Choosing the Right Loop

Different loops are appropriate for different situations.

| Loop | Best Use |
|---|---|
| `for` | When the number of repetitions is known |
| `while` | When repetition depends on a condition |
| `do...while` | When code must execute at least once |
| `for...of` | When processing values in an iterable |
| `for...in` | When processing object property keys |

---

## 12. Practical Activity

### Activity: Student Marks Processor

Create a JavaScript programme that processes a collection of student marks.

### Student Marks

```javascript
const marks = [75, 82, 45, 90, 60, 38, 95, 70];
```

### Requirements

Your programme should:

1. Loop through all student marks.
2. Display each mark.
3. Calculate the total marks.
4. Calculate the average mark.
5. Count how many students passed.
6. Count how many students failed.
7. Identify the highest mark.
8. Identify the lowest mark.

Use a loop to process the array.

### Example Implementation

```javascript
const marks = [75, 82, 45, 90, 60, 38, 95, 70];

let total = 0;

let passed = 0;

let failed = 0;

let highest = marks[0];

let lowest = marks[0];

for (let i = 0; i < marks.length; i++) {

    const mark = marks[i];

    total += mark;

    if (mark >= 50) {
        passed++;
    } else {
        failed++;
    }

    if (mark > highest) {
        highest = mark;
    }

    if (mark < lowest) {
        lowest = mark;
    }

}

const average = total / marks.length;

console.log("STUDENT MARKS REPORT");

console.log("Total Marks:", total);

console.log("Average:", average);

console.log("Passed:", passed);

console.log("Failed:", failed);

console.log("Highest Mark:", highest);

console.log("Lowest Mark:", lowest);
```

### Additional Tasks

1. Use a `for...of` loop to display the marks.
2. Use a `while` loop to count from 1 to 10.
3. Use `continue` to skip marks below 50.
4. Use `break` to stop processing when a mark of 100 is found.
5. Create a multiplication table using nested loops.

---

## 13. Knowledge Check

**1. What is a loop?**

A. A variable declaration.

B. A structure that repeats a block of code.

C. A comparison operator.

D. An object property.

**2. Which loop is commonly used when the number of iterations is known?**

A. `while`

B. `do...while`

C. `for`

D. `switch`

**3. Which loop always executes at least once?**

A. `for`

B. `while`

C. `do...while`

D. `for...in`

**4. Which loop is best suited for iterating through the values of an array?**

A. `for...of`

B. `for...in`

C. `switch`

D. `if`

**5. What does break do inside a loop?**

A. Skips one iteration.

B. Terminates the loop.

C. Restarts the loop.

D. Increases the counter.

**6. What does continue do?**

A. Terminates the entire programme.

B. Skips the current iteration.

C. Stops all future iterations.

D. Changes a variable's data type.

**7. What is an infinite loop?**

A. A loop that runs exactly once.

B. A loop that never reaches its stopping condition.

C. A loop that contains an array.

D. A loop that uses a string.

**8. Which loop is commonly used to iterate over object property keys?**

A. `for...of`

B. `for...in`

C. `do...while`

D. `switch`

---

## 14. Module Challenge

### Challenge: Simple ATM Transaction Simulator

Build a programme that simulates a basic ATM transaction system.

### Initial Account Information

```javascript
let balance = 50000;
```

### Requirements

Your programme should:

1. Display the account balance.
2. Simulate a series of withdrawal amounts.
3. Process each withdrawal.
4. Reject withdrawals that exceed the available balance.
5. Reject negative withdrawal amounts.
6. Update the account balance after successful withdrawals.
7. Display the remaining balance after every transaction.
8. Stop processing when the balance reaches zero or the transaction list ends.

Use an array of withdrawal amounts and a loop.

### Example Implementation

```javascript
// ATM Transaction Simulator

let balance = 50000;

const withdrawals = [5000, 10000, 3000, 40000, 2000];

console.log("ATM TRANSACTION SYSTEM");

console.log("Starting Balance:", balance);

for (const amount of withdrawals) {

    console.log("----------------------");

    console.log("Withdrawal Request:", amount);

    if (amount <= 0) {

        console.log("Invalid withdrawal amount.");

        continue;

    }

    if (amount > balance) {

        console.log("Insufficient funds.");

        continue;

    }

    balance -= amount;

    console.log("Withdrawal successful.");

    console.log("Remaining Balance:", balance);

    if (balance === 0) {

        console.log("Account balance exhausted.");

        break;

    }

}

console.log("----------------------");

console.log("FINAL BALANCE:", balance);
```

### Submission Requirements

1. Create a GitHub repository named `javascript-loops`.
2. Create an `index.html` file.
3. Create an external `script.js` file.
4. Implement the ATM transaction simulator.
5. Use at least one `for` loop.
6. Use conditional statements to validate withdrawals.
7. Include both `break` and `continue`.
8. Test different transaction amounts.
9. Submit your GitHub repository link.

---

## Key Takeaways

- Loops repeat blocks of code.
- `for` loops are useful when the number of repetitions is known.
- `while` loops continue while a condition is true.
- `do...while` loops execute at least once.
- `for...of` iterates over iterable values.
- `for...in` iterates over object property keys.
- `break` terminates a loop.
- `continue` skips the current iteration.
- Nested loops allow one loop to execute inside another.
- Every loop should have a clear stopping condition.

---

<p align="center">
  <strong>Congratulations! You have successfully completed JavaScript Loops.</strong>
</p>

<p align="center">
  NEXT: MODULE 06 — FUNCTIONS
</p>
