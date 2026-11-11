
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=JAVASCRIPT%20ARRAY%20METHODS&fontSize=30&fontColor=ffffff&animation=fadeIn&desc=Transforming%20And%20Processing%20Data&descSize=13" width="100%">
</p>

<h1 align="center">MODULE 09: ARRAY METHODS</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Array%20Methods-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-BEGINNER-2E86C1?style=for-the-badge">
</p>

## Welcome!

In the previous modules, you learned how to create arrays and objects and how to store collections of information.

However, real applications often need to do more than simply store data.

A shopping application may need to:

- Display only available products.
- Find a particular product.
- Calculate the total value of an order.
- Sort products by price.
- Convert product information into a different format.

JavaScript provides built-in **array methods** that make these operations easier.

Array methods allow developers to process, search, transform and organise collections of data.

In this module, you will explore important methods such as `forEach()`, `map()`, `filter()`, `find()`, `reduce()`, `some()`, `every()` and `sort()`.

## Learning Objectives

By the end of this module, you should be able to:

- Explain what array methods are.
- Use `forEach()` to process array elements.
- Use `map()` to transform arrays.
- Use `filter()` to select matching elements.
- Use `find()` and `findIndex()` to search arrays.
- Use `reduce()` to calculate accumulated values.
- Apply `some()` and `every()` to test array conditions.
- Sort and reverse arrays.
- Chain multiple array methods.
- Understand the difference between mutating and non-mutating methods.
- Process arrays of objects.

---

## 1. What Are Array Methods?

Array methods are built-in JavaScript functions that operate on arrays.

They help developers perform common operations without manually writing every instruction.

Example:

```javascript
const numbers = [10, 20, 30, 40];

console.log(numbers.length);
```

The `length` property provides the number of elements.

Other methods allow you to search, transform and process the values.

### Common Array Methods

| Method | Purpose |
|---|---|
| `forEach()` | Executes a function for each element |
| `map()` | Creates a new array by transforming elements |
| `filter()` | Creates a new array containing matching elements |
| `find()` | Returns the first matching element |
| `findIndex()` | Returns the index of the first matching element |
| `reduce()` | Accumulates values into one result |
| `some()` | Checks whether at least one element satisfies a condition |
| `every()` | Checks whether all elements satisfy a condition |
| `sort()` | Sorts array elements |
| `reverse()` | Reverses array order |

---

## 2. The forEach() Method

The `forEach()` method executes a callback function once for each element in an array.

It is useful when you want to perform an operation on every element.

### Syntax

```javascript
array.forEach(callback);
```

### Example

```javascript
const students = ["Alex", "Brian", "Mary"];

students.forEach(function(student) {

    console.log(student);

});
```

Output:

```text
Alex
Brian
Mary
```

### Using Arrow Functions

```javascript
const students = ["Alex", "Brian", "Mary"];

students.forEach(student => {

    console.log(student);

});
```

### Accessing the Index

The callback can receive three arguments:

1. The current element.
2. The current index.
3. The original array.

Example:

```javascript
const students = ["Alex", "Brian", "Mary"];

students.forEach((student, index) => {

    console.log(`${index}: ${student}`);

});
```

Output:

```text
0: Alex
1: Brian
2: Mary
```

**Important:** `forEach()` returns `undefined`. It is intended for performing actions on elements, not for creating a transformed array.

---

## 3. The map() Method

The `map()` method creates a new array by applying a function to every element in the original array.

It is commonly used when you want to transform data.

### Syntax

```javascript
const newArray = array.map(callback);
```

### Example: Multiplying Numbers

```javascript
const numbers = [1, 2, 3, 4, 5];

const doubledNumbers = numbers.map(number => {

    return number * 2;

});

console.log(doubledNumbers);
```

Output:

```text
[2, 4, 6, 8, 10]
```

The original array remains unchanged.

### Shorter Syntax

```javascript
const numbers = [1, 2, 3, 4, 5];

const doubledNumbers = numbers.map(number => number * 2);

console.log(doubledNumbers);
```

### Example: Extracting Names from Objects

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

const studentNames = students.map(student => student.name);

console.log(studentNames);
```

Output:

```text
["Alex", "Brian", "Mary"]
```

### Example: Formatting Product Prices

```javascript
const products = [

    {
        name: "Laptop",
        price: 75000
    },

    {
        name: "Mouse",
        price: 1500
    }

];

const formattedProducts = products.map(product => {

    return {
        name: product.name,
        displayPrice: `KES ${product.price}`
    };

});

console.log(formattedProducts);
```

---

## 4. The filter() Method

The `filter()` method creates a new array containing only the elements that satisfy a specified condition.

It is useful when selecting specific records from a collection.

### Syntax

```javascript
const filteredArray = array.filter(callback);
```

### Example: Filtering Numbers

```javascript
const numbers = [10, 15, 20, 25, 30, 35];

const evenNumbers = numbers.filter(number => {

    return number % 2 === 0;

});

console.log(evenNumbers);
```

Output:

```text
[10, 20, 30]
```

### Example: Filtering Students Who Passed

```javascript
const marks = [75, 40, 85, 30, 60, 90];

const passedStudents = marks.filter(mark => mark >= 50);

console.log(passedStudents);
```

Output:

```text
[75, 85, 60, 90]
```

### Example: Filtering Products by Price

```javascript
const products = [

    {
        name: "Laptop",
        price: 75000
    },

    {
        name: "Mouse",
        price: 1500
    },

    {
        name: "Keyboard",
        price: 3000
    },

    {
        name: "Monitor",
        price: 25000
    }

];

const affordableProducts = products.filter(
    product => product.price < 10000
);

console.log(affordableProducts);
```

The result contains only products priced below KES 10,000.

---

## 5. The find() Method

The `find()` method returns the first element that satisfies a condition.

If no matching element exists, it returns `undefined`.

### Example

```javascript
const numbers = [10, 20, 30, 40, 50];

const result = numbers.find(number => number > 25);

console.log(result);
```

Output:

```text
30
```

Although 40 and 50 also satisfy the condition, `find()` returns only the first matching value.

### Example: Finding a Product

```javascript
const products = [

    {
        id: "P001",
        name: "Laptop",
        price: 75000
    },

    {
        id: "P002",
        name: "Mouse",
        price: 1500
    },

    {
        id: "P003",
        name: "Keyboard",
        price: 3000
    }

];

const selectedProduct = products.find(
    product => product.id === "P002"
);

console.log(selectedProduct);
```

---

## 6. The findIndex() Method

The `findIndex()` method returns the index of the first element that satisfies a condition.

If no matching element exists, it returns `-1`.

Example:

```javascript
const numbers = [10, 20, 30, 40, 50];

const index = numbers.findIndex(number => number > 25);

console.log(index);
```

Output:

```text
2
```

### Example: Finding a Student

```javascript
const students = [

    {
        id: 1,
        name: "Alex"
    },

    {
        id: 2,
        name: "Brian"
    },

    {
        id: 3,
        name: "Mary"
    }

];

const index = students.findIndex(
    student => student.id === 2
);

console.log(index);
```

Output:

```text
1
```

---

## 7. The reduce() Method

The `reduce()` method processes an array and combines its elements into a single accumulated result.

It is commonly used for:

- Calculating totals.
- Finding averages.
- Counting occurrences.
- Combining data.
- Calculating shopping cart values.

### Syntax

```javascript
array.reduce(callback, initialValue);
```

The callback receives:

| Parameter | Explanation |
|---|---|
| Accumulator | The accumulated result |
| Current Value | The current array element |
| Current Index | The current element's index |
| Array | The original array |

### Example: Calculating a Total

```javascript
const numbers = [10, 20, 30, 40];

const total = numbers.reduce((sum, number) => {

    return sum + number;

}, 0);

console.log(total);
```

Output:

```text
100
```

### Understanding the Calculation

| Iteration | Accumulator Before | Current Value | Accumulator After |
|---|---:|---:|---:|
| 1 | 0 | 10 | 10 |
| 2 | 10 | 20 | 30 |
| 3 | 30 | 30 | 60 |
| 4 | 60 | 40 | 100 |

The initial value is `0`.

### Example: Calculating Shopping Cart Total

```javascript
const cart = [

    {
        name: "Laptop",
        price: 75000,
        quantity: 1
    },

    {
        name: "Mouse",
        price: 1500,
        quantity: 2
    },

    {
        name: "Keyboard",
        price: 3000,
        quantity: 1
    }

];

const total = cart.reduce((sum, product) => {

    return sum + product.price * product.quantity;

}, 0);

console.log(total);
```

Output:

```text
81000
```

### Example: Counting Students Who Passed

```javascript
const marks = [75, 40, 85, 30, 60, 90];

const passedCount = marks.reduce((count, mark) => {

    return mark >= 50 ? count + 1 : count;

}, 0);

console.log(passedCount);
```

Output:

```text
4
```

---

## 8. The some() Method

The `some()` method checks whether at least one element in an array satisfies a condition.

It returns a Boolean value.

### Example

```javascript
const marks = [35, 40, 55, 60];

const hasPassed = marks.some(mark => mark >= 50);

console.log(hasPassed);
```

Output:

```text
true
```

At least one mark is 50 or higher.

### Example: Checking Product Availability

```javascript
const products = [

    {
        name: "Laptop",
        quantity: 0
    },

    {
        name: "Mouse",
        quantity: 10
    },

    {
        name: "Keyboard",
        quantity: 0
    }

];

const hasAvailableProduct = products.some(
    product => product.quantity > 0
);

console.log(hasAvailableProduct);
```

Output:

```text
true
```

---

## 9. The every() Method

The `every()` method checks whether all elements in an array satisfy a condition.

It returns a Boolean value.

### Example

```javascript
const marks = [75, 80, 65, 90];

const allPassed = marks.every(mark => mark >= 50);

console.log(allPassed);
```

Output:

```text
true
```

### Example: Checking Product Prices

```javascript
const products = [

    {
        name: "Laptop",
        price: 75000
    },

    {
        name: "Mouse",
        price: 1500
    },

    {
        name: "Keyboard",
        price: 3000
    }

];

const allAffordable = products.every(
    product => product.price < 100000
);

console.log(allAffordable);
```

Output:

```text
true
```

---

## 10. The sort() Method

The `sort()` method sorts the elements of an array.

It modifies the original array.

### Sorting Strings

```javascript
const fruits = ["Orange", "Apple", "Mango", "Banana"];

fruits.sort();

console.log(fruits);
```

Output:

```text
["Apple", "Banana", "Mango", "Orange"]
```

### Sorting Numbers

When sorting numbers, use a comparison function.

Without a comparison function, JavaScript sorts elements as strings.

Incorrect for numeric sorting:

```javascript
const numbers = [100, 5, 20, 30];

numbers.sort();

console.log(numbers);
```

This may produce an unexpected order because the values are compared as strings.

Correct ascending order:

```javascript
const numbers = [100, 5, 20, 30];

numbers.sort((a, b) => a - b);

console.log(numbers);
```

Output:

```text
[5, 20, 30, 100]
```

### Sorting in Descending Order

```javascript
const numbers = [100, 5, 20, 30];

numbers.sort((a, b) => b - a);

console.log(numbers);
```

Output:

```text
[100, 30, 20, 5]
```

### Sorting Objects by Price

```javascript
const products = [

    {
        name: "Laptop",
        price: 75000
    },

    {
        name: "Mouse",
        price: 1500
    },

    {
        name: "Keyboard",
        price: 3000
    }

];

products.sort((a, b) => a.price - b.price);

console.log(products);
```

The products are sorted from the lowest price to the highest price.

---

## 11. The reverse() Method

The `reverse()` method reverses the order of array elements.

It modifies the original array.

Example:

```javascript
const numbers = [1, 2, 3, 4, 5];

numbers.reverse();

console.log(numbers);
```

Output:

```text
[5, 4, 3, 2, 1]
```

### Important Note

Because `sort()` and `reverse()` modify the original array, create a copy first if you need to preserve the original order.

Example:

```javascript
const numbers = [5, 2, 8, 1];

const sortedNumbers = [...numbers].sort((a, b) => a - b);

console.log(numbers);

console.log(sortedNumbers);
```

Output:

```text
[5, 2, 8, 1]
[1, 2, 5, 8]
```

---

## 12. Method Chaining

Method chaining means using multiple array methods in one expression.

This is useful when several operations need to be performed in sequence.

### Example

```javascript
const numbers = [1, 2, 3, 4, 5, 6, 7, 8];

const result = numbers
    .filter(number => number % 2 === 0)
    .map(number => number * 2);

console.log(result);
```

Output:

```text
[4, 8, 12, 16]
```

### Understanding the Process

1. `filter()` selects even numbers.
2. `map()` multiplies each selected number by two.
3. The final result is stored in `result`.

### Example: Processing Products

```javascript
const products = [

    {
        name: "Laptop",
        price: 75000
    },

    {
        name: "Mouse",
        price: 1500
    },

    {
        name: "Keyboard",
        price: 3000
    },

    {
        name: "Monitor",
        price: 25000
    }

];

const affordableProductNames = products
    .filter(product => product.price < 10000)
    .map(product => product.name);

console.log(affordableProductNames);
```

Output:

```text
["Mouse", "Keyboard"]
```

---

## 13. Mutating and Non-Mutating Array Methods

Some array methods modify the original array, while others return new results without changing it.

Understanding this difference is important when managing application data.

### Mutating Methods

These methods modify the original array:

- `push()`
- `pop()`
- `shift()`
- `unshift()`
- `splice()`
- `sort()`
- `reverse()`

### Non-Mutating Methods

These methods return new results without modifying the original array:

- `map()`
- `filter()`
- `slice()`
- `concat()`
- `toSorted()`
- `toReversed()`

Some methods, such as `find()`, `some()` and `every()`, return a single value rather than a new array.

### Example

```javascript
const numbers = [3, 1, 2];

const sortedNumbers = numbers.toSorted((a, b) => a - b);

console.log(numbers);

console.log(sortedNumbers);
```

Output:

```text
[3, 1, 2]
[1, 2, 3]
```

`toSorted()` creates a sorted copy and leaves the original array unchanged.

---

## 14. Practical Activity

### Activity: Product Data Processing System

Create a programme that processes product information using array methods.

### Initial Data

```javascript
const products = [

    {
        id: 1,
        name: "Laptop",
        price: 75000,
        category: "Electronics",
        stock: 5
    },

    {
        id: 2,
        name: "Mouse",
        price: 1500,
        category: "Accessories",
        stock: 20
    },

    {
        id: 3,
        name: "Keyboard",
        price: 3000,
        category: "Accessories",
        stock: 12
    },

    {
        id: 4,
        name: "Monitor",
        price: 25000,
        category: "Electronics",
        stock: 0
    },

    {
        id: 5,
        name: "Webcam",
        price: 5000,
        category: "Accessories",
        stock: 8
    }

];
```

### Requirements

Your programme should:

1. Display all product names using `forEach()`.
2. Create a new array containing only product names using `map()`.
3. Find products costing less than KES 10,000 using `filter()`.
4. Find a product using its ID with `find()`.
5. Calculate the total inventory value using `reduce()`.
6. Check whether at least one product is out of stock using `some()`.
7. Check whether all products have a positive price using `every()`.
8. Sort products by price using `sort()`.

### Example Implementation

```javascript
// Product Data Processing System

const products = [

    {
        id: 1,
        name: "Laptop",
        price: 75000,
        category: "Electronics",
        stock: 5
    },

    {
        id: 2,
        name: "Mouse",
        price: 1500,
        category: "Accessories",
        stock: 20
    },

    {
        id: 3,
        name: "Keyboard",
        price: 3000,
        category: "Accessories",
        stock: 12
    },

    {
        id: 4,
        name: "Monitor",
        price: 25000,
        category: "Electronics",
        stock: 0
    },

    {
        id: 5,
        name: "Webcam",
        price: 5000,
        category: "Accessories",
        stock: 8
    }

];

// Display Product Names

products.forEach(product => {

    console.log(product.name);

});

// Extract Product Names

const productNames = products.map(product => product.name);

// Filter Affordable Products

const affordableProducts = products.filter(
    product => product.price < 10000
);

// Find a Product

const selectedProduct = products.find(
    product => product.id === 2
);

// Calculate Inventory Value

const inventoryValue = products.reduce((total, product) => {

    return total + product.price * product.stock;

}, 0);

// Check Stock

const hasOutOfStockProducts = products.some(
    product => product.stock === 0
);

// Check Prices

const allPricesValid = products.every(
    product => product.price > 0
);

// Sort Products

const sortedProducts = [...products].sort(
    (a, b) => a.price - b.price
);

// Display Results

console.log("PRODUCT NAMES:", productNames);

console.log("AFFORDABLE PRODUCTS:", affordableProducts);

console.log("SELECTED PRODUCT:", selectedProduct);

console.log("INVENTORY VALUE:", inventoryValue);

console.log("OUT OF STOCK PRODUCTS:", hasOutOfStockProducts);

console.log("ALL PRICES VALID:", allPricesValid);

console.log("SORTED PRODUCTS:", sortedProducts);
```

---

## 15. Knowledge Check

**1. What does `forEach()` do?**

A. Creates a new array.

B. Executes a callback for each array element.

C. Removes an array element.

D. Sorts an array.

**2. Which method transforms every element into a new array?**

A. `filter()`

B. `find()`

C. `map()`

D. `reduce()`

**3. Which method selects elements that satisfy a condition?**

A. `filter()`

B. `push()`

C. `pop()`

D. `reverse()`

**4. What does `find()` return?**

A. All matching elements.

B. The first matching element.

C. The index of every matching element.

D. The length of the array.

**5. Which method is used to calculate an accumulated result?**

A. `map()`

B. `forEach()`

C. `reduce()`

D. `includes()`

**6. What does `some()` check?**

A. Whether all elements satisfy a condition.

B. Whether at least one element satisfies a condition.

C. Whether an array is empty.

D. Whether all values are numbers.

**7. What does `every()` check?**

A. Whether all elements satisfy a condition.

B. Whether one element exists.

C. Whether the array is sorted.

D. Whether the array contains objects.

**8. Which method modifies the original array by sorting its elements?**

A. `map()`

B. `filter()`

C. `sort()`

D. `find()`

---

## 16. Module Challenge

### Challenge: E-Commerce Sales Analytics System

Build a JavaScript application that analyses sales information using array methods.

### Sales Data

Each sale should contain:

- Transaction ID.
- Product name.
- Category.
- Unit price.
- Quantity sold.
- Payment status.

### Technical Requirements

1. Create an array containing at least eight sales records.
2. Use `map()` to calculate each sale's total.
3. Use `filter()` to identify completed transactions.
4. Use `find()` to locate a transaction by ID.
5. Use `reduce()` to calculate total revenue.
6. Use `some()` to check whether any transactions are pending.
7. Use `every()` to check whether all transaction quantities are positive.
8. Use `sort()` to rank sales by total value.
9. Use method chaining to generate a report of completed transactions.
10. Display a summary of the sales performance.

### Example Implementation

```javascript
// E-Commerce Sales Analytics System

const sales = [

    {
        id: "T001",
        product: "Laptop",
        price: 75000,
        quantity: 2,
        status: "Completed"
    },

    {
        id: "T002",
        product: "Mouse",
        price: 1500,
        quantity: 5,
        status: "Completed"
    },

    {
        id: "T003",
        product: "Keyboard",
        price: 3000,
        quantity: 3,
        status: "Pending"
    },

    {
        id: "T004",
        product: "Monitor",
        price: 25000,
        quantity: 1,
        status: "Completed"
    }

];

// Calculate Individual Sales

const salesWithTotals = sales.map(sale => {

    return {
        ...sale,
        total: sale.price * sale.quantity
    };

});

// Filter Completed Sales

const completedSales = salesWithTotals.filter(
    sale => sale.status === "Completed"
);

// Calculate Revenue

const totalRevenue = completedSales.reduce(
    (total, sale) => total + sale.total,
    0
);

// Find Transaction

const selectedSale = salesWithTotals.find(
    sale => sale.id === "T002"
);

// Check Pending Transactions

const hasPendingSales = sales.some(
    sale => sale.status === "Pending"
);

// Check Quantities

const allQuantitiesValid = sales.every(
    sale => sale.quantity > 0
);

// Sort Sales by Total

const rankedSales = [...salesWithTotals].sort(
    (a, b) => b.total - a.total
);

// Display Report

console.log("SALES ANALYTICS REPORT");

console.log("Completed Transactions:", completedSales.length);

console.log("Total Revenue:", totalRevenue);

console.log("Pending Transactions:", hasPendingSales);

console.log("Valid Quantities:", allQuantitiesValid);

console.log("Selected Transaction:", selectedSale);

console.log("Sales Ranking:", rankedSales);
```

### Submission Requirements

1. Create a GitHub repository named `javascript-array-methods`.
2. Create an `index.html` file.
3. Create an external `script.js` file.
4. Implement the sales analytics system.
5. Use at least six different array methods.
6. Use an array of objects.
7. Display the results in a readable format.
8. Test the application with different sales records.
9. Submit your GitHub repository link.

---

## Key Takeaways

- Array methods simplify the processing of collections.
- `forEach()` executes an operation for every element.
- `map()` transforms elements and returns a new array.
- `filter()` selects matching elements.
- `find()` returns the first matching element.
- `findIndex()` returns the index of the first matching element.
- `reduce()` combines values into one accumulated result.
- `some()` checks whether at least one element matches a condition.
- `every()` checks whether all elements match a condition.
- `sort()` arranges elements in a particular order.
- Method chaining allows multiple operations to be combined.
- Understanding mutation helps prevent unexpected changes to data.

---

<p align="center">
  <strong>Congratulations! You have successfully completed JavaScript Array Methods.</strong>
</p>

<p align="center">
  NEXT: MODULE 10 — DOM MANIPULATION
</p>
