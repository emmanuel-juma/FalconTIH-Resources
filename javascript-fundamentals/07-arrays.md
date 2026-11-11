
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=JAVASCRIPT%20ARRAYS&fontSize=32&fontColor=ffffff&animation=fadeIn&desc=Storing%20Collections%20Of%20Data&descSize=13" width="100%">
</p>

<h1 align="center">MODULE 07: ARRAYS</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Arrays-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-BEGINNER-2E86C1?style=for-the-badge">
</p>

## Welcome!

In the previous modules, you learned how to work with variables, operators, conditional statements, loops and functions.

So far, most examples have stored one value in each variable.

But what happens when an application needs to store hundreds of products, students, employees or transactions?

Creating a separate variable for every item would quickly become difficult to manage.

JavaScript provides **arrays** to solve this problem.

An array is an ordered collection of values stored under a single variable name.

In this module, you will learn how to create arrays, access elements, update values, add and remove items, and process collections using loops.

## Learning Objectives

By the end of this module, you should be able to:

- Explain what arrays are.
- Create arrays using array literals.
- Access array elements using indexes.
- Update array elements.
- Understand array length.
- Add and remove array elements.
- Use common array methods.
- Loop through arrays.
- Check whether an array contains a value.
- Work with multidimensional arrays.
- Build simple applications using arrays.

---

## 1. What is an Array?

An array is a data structure used to store multiple values in an ordered collection.

Instead of creating separate variables for related information, you can store the values in one array.

### Without an Array

```javascript
const fruitOne = "Apple";

const fruitTwo = "Mango";

const fruitThree = "Orange";

const fruitFour = "Banana";
```

This approach becomes difficult to manage as the number of values increases.

### Using an Array

```javascript
const fruits = [
    "Apple",
    "Mango",
    "Orange",
    "Banana"
];

console.log(fruits);
```

Output:

```text
["Apple", "Mango", "Orange", "Banana"]
```

The array stores all four values under one variable.

---

## 2. Creating an Array

There are several ways to create an array in JavaScript.

The most common approach is using square brackets `[]`.

### Example

```javascript
const students = ["Alex", "Brian", "Mary"];

console.log(students);
```

An array can contain different types of values.

```javascript
const studentInformation = [
    "Alex",
    21,
    true,
    "Software Engineering"
];

console.log(studentInformation);
```

However, when designing applications, it is generally better to keep collections logically organised.

### Creating an Empty Array

```javascript
const products = [];

console.log(products);
```

Output:

```text
[]
```

You can add values to the array later.

---

## 3. Understanding Array Indexes

Each element in an array has a position called an index.

JavaScript arrays use zero-based indexing.

This means the first element has index `0`, not index `1`.

### Example

```javascript
const fruits = ["Apple", "Mango", "Orange", "Banana"];
```

| Index | Value |
|---|---|
| 0 | Apple |
| 1 | Mango |
| 2 | Orange |
| 3 | Banana |

### Accessing Array Elements

Use the index inside square brackets to access an element.

```javascript
const fruits = ["Apple", "Mango", "Orange", "Banana"];

console.log(fruits[0]);

console.log(fruits[1]);

console.log(fruits[2]);
```

Output:

```text
Apple
Mango
Orange
```

### Accessing the Last Element

You can use the array's `length` property to access its last element.

```javascript
const fruits = ["Apple", "Mango", "Orange", "Banana"];

console.log(fruits[fruits.length - 1]);
```

Output:

```text
Banana
```

### Accessing an Invalid Index

```javascript
const fruits = ["Apple", "Mango"];

console.log(fruits[5]);
```

Output:

```text
undefined
```

The requested index does not contain an element.

---

## 4. Updating Array Elements

Array elements can be updated using their indexes.

Example:

```javascript
const fruits = ["Apple", "Mango", "Orange"];

fruits[1] = "Pineapple";

console.log(fruits);
```

Output:

```text
["Apple", "Pineapple", "Orange"]
```

Although the array was declared using `const`, its contents can be modified.

The `const` declaration prevents reassignment of the array variable itself, not modification of its elements.

This is allowed:

```javascript
const numbers = [10, 20, 30];

numbers[0] = 100;

console.log(numbers);
```

This is not allowed:

```javascript
const numbers = [10, 20, 30];

numbers = [40, 50, 60];
```

The second example attempts to reassign the constant variable.

---

## 5. Understanding Array Length

The `length` property returns the number of elements in an array.

Example:

```javascript
const students = ["Alex", "Brian", "Mary", "John"];

console.log(students.length);
```

Output:

```text
4
```

### Example: Using length in a Loop

```javascript
const students = ["Alex", "Brian", "Mary"];

for (let i = 0; i < students.length; i++) {

    console.log(students[i]);

}
```

Output:

```text
Alex
Brian
Mary
```

Using `length` makes your code adaptable when the array changes.

---

## 6. Adding Elements to an Array

JavaScript provides methods for adding elements to arrays.

### A. push()

The `push()` method adds one or more elements to the end of an array.

```javascript
const fruits = ["Apple", "Mango"];

fruits.push("Orange");

console.log(fruits);
```

Output:

```text
["Apple", "Mango", "Orange"]
```

You can add multiple elements:

```javascript
const fruits = ["Apple", "Mango"];

fruits.push("Orange", "Banana");

console.log(fruits);
```

### B. unshift()

The `unshift()` method adds elements to the beginning of an array.

```javascript
const fruits = ["Mango", "Orange"];

fruits.unshift("Apple");

console.log(fruits);
```

Output:

```text
["Apple", "Mango", "Orange"]
```

---

## 7. Removing Elements from an Array

JavaScript provides methods for removing array elements.

### A. pop()

The `pop()` method removes the last element from an array.

```javascript
const fruits = ["Apple", "Mango", "Orange"];

fruits.pop();

console.log(fruits);
```

Output:

```text
["Apple", "Mango"]
```

### B. shift()

The `shift()` method removes the first element from an array.

```javascript
const fruits = ["Apple", "Mango", "Orange"];

fruits.shift();

console.log(fruits);
```

Output:

```text
["Mango", "Orange"]
```

### C. splice()

The `splice()` method can remove, replace or insert elements at specific positions.

Syntax:

```javascript
array.splice(start, deleteCount, item1, item2);
```

Example: Removing an Element

```javascript
const fruits = ["Apple", "Mango", "Orange", "Banana"];

fruits.splice(1, 1);

console.log(fruits);
```

Output:

```text
["Apple", "Orange", "Banana"]
```

Example: Inserting an Element

```javascript
const fruits = ["Apple", "Orange"];

fruits.splice(1, 0, "Mango");

console.log(fruits);
```

Output:

```text
["Apple", "Mango", "Orange"]
```

Example: Replacing an Element

```javascript
const fruits = ["Apple", "Mango", "Orange"];

fruits.splice(1, 1, "Pineapple");

console.log(fruits);
```

Output:

```text
["Apple", "Pineapple", "Orange"]
```

---

## 8. Searching Arrays

JavaScript provides methods that help locate values inside arrays.

### A. includes()

The `includes()` method checks whether an array contains a specific value.

It returns `true` or `false`.

```javascript
const fruits = ["Apple", "Mango", "Orange"];

console.log(fruits.includes("Mango"));

console.log(fruits.includes("Banana"));
```

Output:

```text
true
false
```

### B. indexOf()

The `indexOf()` method returns the index of the first matching value.

If the value does not exist, it returns `-1`.

```javascript
const fruits = ["Apple", "Mango", "Orange"];

console.log(fruits.indexOf("Mango"));

console.log(fruits.indexOf("Banana"));
```

Output:

```text
1
-1
```

### C. lastIndexOf()

The `lastIndexOf()` method returns the index of the last occurrence of a value.

```javascript
const numbers = [10, 20, 30, 20, 40];

console.log(numbers.lastIndexOf(20));
```

Output:

```text
3
```

---

## 9. Extracting Array Elements with slice()

The `slice()` method returns a new array containing selected elements from the original array.

It does not modify the original array.

Syntax:

```javascript
array.slice(start, end);
```

The end position is excluded.

### Example

```javascript
const fruits = ["Apple", "Mango", "Orange", "Banana"];

const selectedFruits = fruits.slice(1, 3);

console.log(selectedFruits);

console.log(fruits);
```

Output:

```text
["Mango", "Orange"]
["Apple", "Mango", "Orange", "Banana"]
```

The original array remains unchanged.

---

## 10. Looping Through Arrays

Arrays are frequently processed using loops.

### A. Using a for Loop

```javascript
const students = ["Alex", "Brian", "Mary"];

for (let i = 0; i < students.length; i++) {

    console.log(students[i]);

}
```

### B. Using for...of

```javascript
const students = ["Alex", "Brian", "Mary"];

for (const student of students) {

    console.log(student);

}
```

### C. Using forEach()

The `forEach()` method executes a callback function once for each array element.

```javascript
const students = ["Alex", "Brian", "Mary"];

students.forEach(function(student) {

    console.log(student);

});
```

Using an arrow function:

```javascript
const students = ["Alex", "Brian", "Mary"];

students.forEach(student => {

    console.log(student);

});
```

All three approaches can be used to process array values.

---

## 11. Multidimensional Arrays

A multidimensional array is an array that contains other arrays.

This structure is useful for representing rows and columns of data.

### Example

```javascript
const studentMarks = [
    [80, 75, 90],
    [65, 70, 85],
    [90, 95, 88]
];

console.log(studentMarks);
```

### Accessing Values

```javascript
console.log(studentMarks[0][0]);

console.log(studentMarks[1][2]);

console.log(studentMarks[2][1]);
```

Output:

```text
80
85
95
```

The first index selects the inner array. The second index selects the value inside that array.

### Looping Through a Multidimensional Array

```javascript
const studentMarks = [
    [80, 75, 90],
    [65, 70, 85],
    [90, 95, 88]
];

for (let i = 0; i < studentMarks.length; i++) {

    for (let j = 0; j < studentMarks[i].length; j++) {

        console.log(studentMarks[i][j]);

    }

}
```

---

## 12. Practical Activity

### Activity: Product Inventory System

Create a JavaScript programme that manages a collection of products.

### Initial Product List

```javascript
const products = [
    "Laptop",
    "Mouse",
    "Keyboard",
    "Monitor",
    "Printer"
];
```

### Requirements

Your programme should:

1. Display all products.
2. Display the total number of products.
3. Add a new product.
4. Remove the last product.
5. Add a product at the beginning.
6. Check whether a specific product exists.
7. Find the index of a product.
8. Display the updated product list.

### Example Implementation

```javascript
// Product Inventory System

const products = [
    "Laptop",
    "Mouse",
    "Keyboard",
    "Monitor",
    "Printer"
];

// Display Initial Products

console.log("INITIAL INVENTORY");

products.forEach(product => {
    console.log(product);
});

// Display Product Count

console.log("Total Products:", products.length);

// Add Product

products.push("Webcam");

// Remove Last Product

products.pop();

// Add Product at the Beginning

products.unshift("Desktop");

// Search for a Product

console.log("Laptop Available:", products.includes("Laptop"));

// Find Product Index

console.log("Keyboard Index:", products.indexOf("Keyboard"));

// Display Updated Inventory

console.log("UPDATED INVENTORY");

console.log(products);
```

### Additional Tasks

1. Remove a product using `splice()`.
2. Extract the first three products using `slice()`.
3. Display all products using a `for` loop.
4. Create a second array containing product prices.
5. Calculate the total value of all products.

---

## 13. Knowledge Check

**1. What is an array?**

A. A function that returns a value.

B. An ordered collection of values.

C. A conditional statement.

D. A CSS selector.

**2. Which symbol is used to create an array literal?**

A. `{}`

B. `()`

C. `[]`

D. `<>`

**3. What is the index of the first element in an array?**

A. 1

B. 0

C. -1

D. 2

**4. Which property returns the number of elements in an array?**

A. `size`

B. `count`

C. `length`

D. `total`

**5. Which method adds an element to the end of an array?**

A. `pop()`

B. `push()`

C. `shift()`

D. `slice()`

**6. Which method removes the first element?**

A. `shift()`

B. `pop()`

C. `push()`

D. `includes()`

**7. What does `includes()` return?**

A. An array.

B. A number.

C. A Boolean value.

D. An object.

**8. Which method returns a new array containing selected elements without modifying the original array?**

A. `splice()`

B. `slice()`

C. `push()`

D. `pop()`

---

## 14. Module Challenge

### Challenge: Student Records Manager

Build a simple programme that manages a collection of student names and marks.

### Initial Data

```javascript
const students = [
    "Alex",
    "Brian",
    "Mary",
    "John",
    "Sarah"
];

const marks = [75, 82, 45, 90, 60];
```

### Technical Requirements

Your programme should:

1. Display all student names.
2. Display all student marks.
3. Add a new student and their mark.
4. Remove a student from the collection.
5. Search for a student by name.
6. Find the highest mark.
7. Find the lowest mark.
8. Calculate the average mark.
9. Count students who passed.
10. Count students who failed.

### Example Implementation

```javascript
// Student Records Manager

const students = [
    "Alex",
    "Brian",
    "Mary",
    "John",
    "Sarah"
];

const marks = [75, 82, 45, 90, 60];

// Display Students

console.log("STUDENT RECORDS");

for (let i = 0; i < students.length; i++) {

    console.log(`${students[i]}: ${marks[i]}`);

}

// Calculate Total

let total = 0;

for (const mark of marks) {

    total += mark;

}

// Calculate Average

const average = total / marks.length;

// Find Highest and Lowest

const highestMark = Math.max(...marks);

const lowestMark = Math.min(...marks);

// Count Passes and Failures

let passed = 0;

let failed = 0;

for (const mark of marks) {

    if (mark >= 50) {
        passed++;
    } else {
        failed++;
    }

}

// Search Student

const searchName = "Mary";

const studentIndex = students.indexOf(searchName);

console.log("Average:", average);

console.log("Highest Mark:", highestMark);

console.log("Lowest Mark:", lowestMark);

console.log("Passed:", passed);

console.log("Failed:", failed);

console.log("Student Found:", studentIndex !== -1);
```

### Submission Requirements

1. Create a GitHub repository named `javascript-arrays`.
2. Create an `index.html` file.
3. Create an external `script.js` file.
4. Implement the student records manager.
5. Use arrays to store student information.
6. Use loops to process the records.
7. Use array methods to add, remove and search for values.
8. Test your programme with different records.
9. Submit your GitHub repository link.

---

## Key Takeaways

- Arrays store multiple values in one ordered collection.
- Array indexes start at zero.
- The `length` property returns the number of elements.
- `push()` and `unshift()` add elements.
- `pop()` and `shift()` remove elements.
- `splice()` inserts, removes or replaces elements.
- `slice()` extracts elements without modifying the original array.
- `includes()` checks whether a value exists.
- `indexOf()` returns the first matching index.
- Loops and `forEach()` help process arrays.
- Multidimensional arrays contain nested arrays.

---

<p align="center">
  <strong>Congratulations! You have successfully completed JavaScript Arrays.</strong>
</p>

<p align="center">
  NEXT: MODULE 08 — OBJECTS
</p>
