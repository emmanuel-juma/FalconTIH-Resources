
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=JAVASCRIPT%20OBJECTS&fontSize=32&fontColor=ffffff&animation=fadeIn&desc=Organising%20Related%20Information&descSize=13" width="100%">
</p>

<h1 align="center">MODULE 08: OBJECTS</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Objects-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-BEGINNER-2E86C1?style=for-the-badge">
</p>

## Welcome!

In the previous module, you learned how to use arrays to store multiple values in an ordered collection.

However, applications often need to store related information using meaningful labels.

Consider a student record:

- Name: Alex
- Age: 21
- Course: Software Engineering
- Country: Kenya

An array could store these values, but it would not clearly identify what each value represents.

JavaScript provides **objects** to organise related information using key-value pairs.

Objects are one of the most important concepts in JavaScript because they are widely used in frontend development, APIs, React applications and backend systems.

In this module, you will learn how to create objects, access properties, update information, work with methods and manage collections of objects.

## Learning Objectives

By the end of this module, you should be able to:

- Explain what JavaScript objects are.
- Create objects using object literals.
- Understand properties and values.
- Access object properties using dot notation and bracket notation.
- Add, update and delete properties.
- Create and execute object methods.
- Understand the `this` keyword.
- Work with nested objects.
- Store objects inside arrays.
- Understand object destructuring.
- Use `Object.keys()`, `Object.values()` and `Object.entries()`.

---

## 1. What is an Object?

An object is a data structure used to store related information as key-value pairs.

Each key is known as a property name, and its corresponding value contains the information.

### Example

```javascript
const student = {
    name: "Alex",
    age: 21,
    country: "Kenya",
    course: "Software Engineering"
};

console.log(student);
```

Output:

```text
{
    name: "Alex",
    age: 21,
    country: "Kenya",
    course: "Software Engineering"
}
```

### Understanding Object Components

| Component | Explanation |
|---|---|
| `student` | Object variable |
| `{}` | Object literal notation |
| `name` | Property name |
| `"Alex"` | Property value |
| `age` | Another property |
| `21` | Corresponding value |

Objects allow you to organise related information in a structured way.

---

## 2. Creating an Object

The most common way to create an object is using object literal notation.

Example:

```javascript
const product = {
    name: "Laptop",
    price: 75000,
    brand: "Lenovo",
    inStock: true
};

console.log(product);
```

An object can contain different data types.

### Object with Multiple Data Types

```javascript
const user = {
    name: "Alex",
    age: 21,
    isActive: true,
    email: "alex@example.com",
    phone: null
};

console.log(user);
```

### Empty Object

You can also create an empty object and add properties later.

```javascript
const employee = {};

employee.name = "Brian";

employee.age = 28;

console.log(employee);
```

Output:

```text
{
    name: "Brian",
    age: 28
}
```

---

## 3. Accessing Object Properties

JavaScript provides two common ways to access object properties.

1. Dot notation.
2. Bracket notation.

### A. Dot Notation

Dot notation uses the object name followed by a period and the property name.

Example:

```javascript
const student = {
    name: "Alex",
    age: 21,
    course: "Software Engineering"
};

console.log(student.name);

console.log(student.age);

console.log(student.course);
```

Output:

```text
Alex
21
Software Engineering
```

### B. Bracket Notation

Bracket notation uses square brackets and a property name written as a string.

Example:

```javascript
const student = {
    name: "Alex",
    age: 21,
    course: "Software Engineering"
};

console.log(student["name"]);

console.log(student["age"]);
```

Output:

```text
Alex
21
```

### When Should You Use Bracket Notation?

Bracket notation is useful when:

- A property name contains spaces.
- A property name contains special characters.
- You need to access a property dynamically using a variable.

Example:

```javascript
const student = {
    name: "Alex",
    "registration number": "SE2026001"
};

console.log(student["registration number"]);
```

### Dynamic Property Access

```javascript
const student = {
    name: "Alex",
    age: 21,
    course: "Software Engineering"
};

const property = "course";

console.log(student[property]);
```

Output:

```text
Software Engineering
```

---

## 4. Adding and Updating Object Properties

Objects can be modified after they are created.

### Adding a Property

```javascript
const student = {
    name: "Alex",
    age: 21
};

student.country = "Kenya";

console.log(student);
```

### Updating a Property

```javascript
const student = {
    name: "Alex",
    age: 21
};

student.age = 22;

console.log(student.age);
```

Output:

```text
22
```

### Using Bracket Notation

```javascript
const student = {
    name: "Alex"
};

student["course"] = "Software Engineering";

console.log(student);
```

---

## 5. Deleting Object Properties

The `delete` operator removes a property from an object.

Example:

```javascript
const student = {
    name: "Alex",
    age: 21,
    country: "Kenya"
};

delete student.country;

console.log(student);
```

Output:

```text
{
    name: "Alex",
    age: 21
}
```

The `country` property is no longer part of the object.

---

## 6. Object Methods

An object can contain functions as properties.

A function stored inside an object is commonly called a method.

### Example

```javascript
const student = {

    name: "Alex",

    greet: function() {

        console.log("Hello, my name is Alex.");

    }

};

student.greet();
```

Output:

```text
Hello, my name is Alex.
```

### Shorter Method Syntax

Modern JavaScript allows methods to be written more concisely.

```javascript
const student = {

    name: "Alex",

    greet() {

        console.log("Hello, my name is Alex.");

    }

};

student.greet();
```

### Method Using Object Properties

```javascript
const student = {

    name: "Alex",

    course: "Software Engineering",

    introduce() {

        console.log(`My name is ${this.name}.`);

        console.log(`I study ${this.course}.`);

    }

};

student.introduce();
```

Output:

```text
My name is Alex.
I study Software Engineering.
```

---

## 7. Understanding the this Keyword

The `this` keyword refers to the object associated with the current method call.

It is commonly used inside object methods to access the object's properties.

Example:

```javascript
const employee = {

    name: "Brian",

    salary: 50000,

    displayDetails() {

        console.log(this.name);

        console.log(this.salary);

    }

};

employee.displayDetails();
```

Output:

```text
Brian
50000
```

In this example, `this.name` accesses the `name` property of the employee object.

### Important Note About Arrow Functions

Arrow functions do not have their own `this` value.

For object methods that need to refer to the object through `this`, ordinary method syntax is generally the appropriate choice.

Example:

```javascript
const user = {

    name: "Alex",

    greet() {

        console.log(`Hello, ${this.name}`);

    }

};

user.greet();
```

---

## 8. Nested Objects

An object can contain another object as one of its properties.

This is known as a nested object.

### Example

```javascript
const student = {

    name: "Alex",

    age: 21,

    address: {

        city: "Nairobi",

        country: "Kenya",

        postalCode: "00100"

    }

};

console.log(student);
```

### Accessing Nested Properties

Use dot notation to access properties inside nested objects.

```javascript
console.log(student.address.city);

console.log(student.address.country);

console.log(student.address.postalCode);
```

Output:

```text
Nairobi
Kenya
00100
```

### Updating Nested Properties

```javascript
student.address.city = "Mombasa";

console.log(student.address.city);
```

Output:

```text
Mombasa
```

Nested objects are useful when working with complex information such as addresses, user profiles and product specifications.

---

## 9. Arrays of Objects

One of the most common ways to organise application data is by storing objects inside an array.

For example, an online store may contain multiple products.

Each product has its own name, price and category.

### Example

```javascript
const products = [

    {
        name: "Laptop",
        price: 75000,
        category: "Electronics"
    },

    {
        name: "Mouse",
        price: 1500,
        category: "Accessories"
    },

    {
        name: "Keyboard",
        price: 3000,
        category: "Accessories"
    }

];

console.log(products);
```

### Accessing an Object Inside an Array

```javascript
console.log(products[0]);

console.log(products[0].name);

console.log(products[1].price);
```

Output:

```text
{
    name: "Laptop",
    price: 75000,
    category: "Electronics"
}
```

```text
Laptop
1500
```

### Looping Through an Array of Objects

```javascript
for (const product of products) {

    console.log(product.name);

    console.log(product.price);

}
```

### Displaying a Product Summary

```javascript
for (const product of products) {

    console.log(`${product.name} costs KES ${product.price}`);

}
```

Arrays of objects are widely used in real-world JavaScript applications.

---

## 10. Object Destructuring

Destructuring is a JavaScript feature that allows you to extract values from objects and store them in variables.

### Without Destructuring

```javascript
const student = {
    name: "Alex",
    age: 21,
    course: "Software Engineering"
};

const name = student.name;

const age = student.age;

const course = student.course;
```

### Using Destructuring

```javascript
const student = {
    name: "Alex",
    age: 21,
    course: "Software Engineering"
};

const { name, age, course } = student;

console.log(name);

console.log(age);

console.log(course);
```

Output:

```text
Alex
21
Software Engineering
```

### Renaming Variables During Destructuring

```javascript
const student = {
    name: "Alex",
    age: 21
};

const { name: studentName, age: studentAge } = student;

console.log(studentName);

console.log(studentAge);
```

### Default Values

You can provide a default value when a property does not exist.

```javascript
const student = {
    name: "Alex"
};

const { name, course = "Not assigned" } = student;

console.log(name);

console.log(course);
```

Output:

```text
Alex
Not assigned
```

---

## 11. Useful Object Methods

JavaScript provides built-in methods for working with objects.

### A. Object.keys()

Returns an array containing an object's property names.

```javascript
const student = {
    name: "Alex",
    age: 21,
    course: "Software Engineering"
};

console.log(Object.keys(student));
```

Output:

```text
["name", "age", "course"]
```

### B. Object.values()

Returns an array containing an object's property values.

```javascript
console.log(Object.values(student));
```

Output:

```text
["Alex", 21, "Software Engineering"]
```

### C. Object.entries()

Returns an array containing key-value pairs.

```javascript
console.log(Object.entries(student));
```

Output:

```text
[
    ["name", "Alex"],
    ["age", 21],
    ["course", "Software Engineering"]
]
```

### D. Object.assign()

Copies properties from one or more source objects into a target object.

```javascript
const originalStudent = {
    name: "Alex",
    age: 21
};

const additionalDetails = {
    course: "Software Engineering"
};

const student = Object.assign(
    {},
    originalStudent,
    additionalDetails
);

console.log(student);
```

Output:

```text
{
    name: "Alex",
    age: 21,
    course: "Software Engineering"
}
```

### E. Object.hasOwn()

Checks whether an object directly contains a specified property.

```javascript
const student = {
    name: "Alex",
    age: 21
};

console.log(Object.hasOwn(student, "name"));

console.log(Object.hasOwn(student, "course"));
```

Output:

```text
true
false
```

---

## 12. Practical Activity

### Activity: Employee Management System

Create a programme that stores employee information using JavaScript objects.

### Employee Information

Each employee should have:

- Full name.
- Employee ID.
- Department.
- Job title.
- Monthly salary.
- Employment status.

### Requirements

Your programme should:

1. Create an employee object.
2. Display employee information.
3. Update the employee's salary.
4. Add a new property for the employee's location.
5. Create an object method that displays employee details.
6. Create an array containing multiple employee objects.
7. Loop through the array and display all employees.
8. Use object destructuring to extract employee information.

### Example Implementation

```javascript
// Employee Management System

const employee = {

    name: "Alex Morgan",

    employeeId: "EMP001",

    department: "Technology",

    jobTitle: "Frontend Developer",

    salary: 60000,

    isActive: true,

    location: "Nairobi",

    displayDetails() {

        console.log("EMPLOYEE DETAILS");

        console.log("Name:", this.name);

        console.log("Employee ID:", this.employeeId);

        console.log("Department:", this.department);

        console.log("Job Title:", this.jobTitle);

        console.log("Salary:", this.salary);

        console.log("Location:", this.location);

    }

};

// Display Employee

employee.displayDetails();

// Update Salary

employee.salary = 70000;

// Add Property

employee.email = "alex@example.com";

// Destructure Employee Information

const {
    name,
    department,
    salary
} = employee;

console.log(name);

console.log(department);

console.log(salary);
```

### Additional Tasks

1. Create at least three employee objects.
2. Store the employees inside an array.
3. Display all employee names.
4. Calculate the total monthly salary.
5. Search for an employee using their employee ID.
6. Update an employee's department.
7. Use `Object.keys()` to display the property names.

---

## 13. Knowledge Check

**1. What is a JavaScript object?**

A. An ordered collection of values accessed only by index.

B. A collection of related information stored as key-value pairs.

C. A conditional statement.

D. A function that returns a number.

**2. Which brackets are used to create an object literal?**

A. `[]`

B. `()`

C. `{}`

D. `<>`

**3. What is a property?**

A. A named piece of information stored in an object.

B. A JavaScript loop.

C. A CSS selector.

D. A function call.

**4. Which notation accesses an object property directly?**

A. `student->name`

B. `student.name`

C. `student::name`

D. `student/name`

**5. What does the delete operator do?**

A. Deletes an entire JavaScript programme.

B. Removes a property from an object.

C. Removes an array.

D. Deletes a variable declaration.

**6. What is a method?**

A. A function stored as an object property.

B. An array index.

C. A CSS rule.

D. A variable declaration.

**7. What does this refer to in an ordinary object method call?**

A. The browser.

B. The object associated with the method call.

C. The HTML document in every situation.

D. The JavaScript engine.

**8. Which method returns an array of object property names?**

A. `Object.values()`

B. `Object.keys()`

C. `Object.entries()`

D. `Object.assign()`

---

## 14. Module Challenge

### Challenge: Online Store Product Management System

Build a simple product management programme using objects and arrays.

### Product Structure

Each product should contain:

- Product ID.
- Product name.
- Category.
- Price.
- Quantity in stock.
- Availability status.

### Technical Requirements

1. Create at least five product objects.
2. Store all products inside an array.
3. Display all products.
4. Search for a product using its ID.
5. Update a product's price.
6. Update a product's stock quantity.
7. Display products that are available.
8. Calculate the total inventory value.
9. Use object destructuring.
10. Use object methods where appropriate.

### Example Implementation

```javascript
// Online Store Product Management System

const products = [

    {
        id: "P001",
        name: "Laptop",
        category: "Electronics",
        price: 75000,
        quantity: 5
    },

    {
        id: "P002",
        name: "Mouse",
        category: "Accessories",
        price: 1500,
        quantity: 20
    },

    {
        id: "P003",
        name: "Keyboard",
        category: "Accessories",
        price: 3000,
        quantity: 12
    },

    {
        id: "P004",
        name: "Monitor",
        category: "Electronics",
        price: 25000,
        quantity: 0
    },

    {
        id: "P005",
        name: "Webcam",
        category: "Accessories",
        price: 5000,
        quantity: 8
    }

];

// Display All Products

console.log("PRODUCT INVENTORY");

for (const product of products) {

    console.log(
        `${product.id}: ${product.name} - KES ${product.price}`
    );

}

// Search for a Product

const searchId = "P002";

const selectedProduct = products.find(
    product => product.id === searchId
);

console.log("SEARCH RESULT:", selectedProduct);

// Update Product Price

const productToUpdate = products.find(
    product => product.id === "P001"
);

if (productToUpdate) {

    productToUpdate.price = 72000;

}

// Calculate Inventory Value

let inventoryValue = 0;

for (const product of products) {

    inventoryValue += product.price * product.quantity;

}

// Display Available Products

console.log("AVAILABLE PRODUCTS");

for (const product of products) {

    if (product.quantity > 0) {

        console.log(product.name);

    }

}

console.log("Total Inventory Value:", inventoryValue);
```

### Submission Requirements

1. Create a GitHub repository named `javascript-objects`.
2. Create an `index.html` file.
3. Create an external `script.js` file.
4. Implement the product management system.
5. Use objects and arrays.
6. Use object methods and destructuring.
7. Test product searches and updates.
8. Submit your GitHub repository link.

---

## Key Takeaways

- Objects store related information as key-value pairs.
- Object literals use curly braces.
- Dot notation and bracket notation access properties.
- Properties can be added, updated and deleted.
- Objects can contain methods.
- The `this` keyword can access an object's properties inside ordinary methods.
- Objects can contain other objects.
- Arrays can contain multiple objects.
- Destructuring extracts object properties into variables.
- `Object.keys()`, `Object.values()` and `Object.entries()` help process object data.

---

<p align="center">
  <strong>Congratulations! You have successfully completed JavaScript Objects.</strong>
</p>

<p align="center">
  NEXT: MODULE 09 — ARRAY METHODS
</p>
