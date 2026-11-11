
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=JAVASCRIPT%20INTRODUCTION&fontSize=32&fontColor=ffffff&animation=fadeIn&desc=Bringing%20Websites%20To%20Life&descSize=13" width="100%">
</p>

<h1 align="center">MODULE 01: INTRODUCTION TO JAVASCRIPT</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-First%20Steps-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-BEGINNER-2E86C1?style=for-the-badge">
</p>

## Welcome!

You have already learned how to structure web pages using HTML and style them using CSS.

But how does a website respond when you click a button? How does a shopping cart calculate the total price of products? How does a website validate information entered into a form?

The answer is **JavaScript**.

JavaScript is a programming language that makes websites interactive and dynamic.

In this module, you will learn what JavaScript is, where it is used, how it works and how to write your first JavaScript programme.

## Learning Objectives

By the end of this module, you should be able to:

- Explain what JavaScript is.
- Understand the role of JavaScript in web development.
- Differentiate between HTML, CSS and JavaScript.
- Identify common JavaScript development environments.
- Understand basic JavaScript syntax.
- Display information using `console.log()`.
- Connect an external JavaScript file to an HTML document.
- Execute JavaScript code in a web browser.

---

## 1. What is JavaScript?

JavaScript is a high-level programming language primarily used to make websites interactive and dynamic.

It allows developers to implement functionality such as:

- Interactive buttons.
- Dropdown menus.
- Form validation.
- Image sliders.
- Shopping carts.
- Dynamic content updates.
- Interactive dashboards.
- Real-time notifications.

HTML provides the structure of a webpage, CSS controls its presentation, while JavaScript controls its behaviour.

### Understanding HTML, CSS and JavaScript

Think of a house:

| Technology | Responsibility | House Example |
|---|---|---|
| HTML | Structure | Walls and rooms |
| CSS | Presentation | Paint and decoration |
| JavaScript | Behaviour | Electricity and controls |

Together, these technologies form the foundation of frontend web development.

### Example

Imagine building a simple button.

**HTML:**

```html
<button>Click Me</button>
```

**CSS:**

```css
button {
    background-color: blue;
    color: white;
    padding: 12px 20px;
}
```

**JavaScript:**

```javascript
console.log("The button is ready!");
```

HTML creates the button, CSS styles it, and JavaScript can make it respond to user interactions.

---

## 2. Where is JavaScript Used?

JavaScript is not limited to creating interactive websites. It is used in different areas of software development.

| Area | Application |
|---|---|
| Frontend Development | Interactive websites and web applications |
| Backend Development | Server-side applications using Node.js |
| Mobile Development | Cross-platform mobile applications |
| Desktop Development | Desktop applications |
| Game Development | Browser-based games |
| API Integration | Communicating with external services |

### JavaScript Development Technologies

Some common technologies associated with JavaScript include:

- **React:** Building user interfaces.
- **Node.js:** Running JavaScript outside the browser.
- **Express.js:** Building backend applications.
- **Next.js:** Developing full-stack web applications.
- **React Native:** Building mobile applications.

These technologies build upon JavaScript fundamentals.

---

## 3. How Does JavaScript Work?

JavaScript code is executed by a JavaScript engine.

Modern browsers have built-in JavaScript engines that process and execute JavaScript programmes.

Examples include:

| Browser | JavaScript Engine |
|---|---|
| Google Chrome | V8 |
| Microsoft Edge | V8 |
| Mozilla Firefox | SpiderMonkey |
| Safari | JavaScriptCore |

When a browser encounters JavaScript code, its JavaScript engine processes and executes it.

### Example

```javascript
console.log("Hello, World!");
```

The browser executes the statement and displays:

```text
Hello, World!
```

This output appears in the browser's Developer Console, not directly on the webpage.

---

## 4. Understanding JavaScript Syntax

Syntax refers to the rules that determine how JavaScript code must be written.

Consider the following example:

```javascript
console.log("Welcome to JavaScript");
```

Let's break it down:

| Code | Explanation |
|---|---|
| `console` | Provides access to the browser console |
| `.` | Accesses a property or method |
| `log()` | Displays information in the console |
| `"Welcome to JavaScript"` | The text being displayed |
| `;` | Marks the end of the statement |

### JavaScript Statements

A statement is an instruction that JavaScript executes.

Example:

```javascript
console.log("My name is Alex");

console.log("I am learning JavaScript");

console.log("I want to become a software engineer");
```

Each line represents an instruction.

### JavaScript is Case-Sensitive

JavaScript treats uppercase and lowercase letters differently.

This works:

```javascript
console.log("Hello World");
```

This produces an error:

```javascript
Console.log("Hello World");
```

This happens because `Console` and `console` are different identifiers.

Always pay attention to spelling and capitalization when writing JavaScript.

---

## 5. Your First JavaScript Programme

Let's create our first JavaScript programme.

### Step 1: Create a Project Folder

Create a folder named:

`my-first-javascript`

Inside it, create a file named:

`script.js`

Your folder structure should look like this:

```text
my-first-javascript/
│
└── script.js
```

### Step 2: Write Your First Code

Open `script.js` and write:

```javascript
console.log("Hello, World!");

console.log("Welcome to JavaScript.");

console.log("I am learning frontend engineering.");
```

### Step 3: Execute Your Code

For this lesson, we will use the browser console.

1. Open Google Chrome.
2. Right-click anywhere on a webpage.
3. Select Inspect.
4. Navigate to the Console tab.
5. Type the following statement:

```javascript
console.log("My first JavaScript programme!");
```

6. Press Enter.

You should see:

```text
My first JavaScript programme!
```

You have successfully executed your first JavaScript statement.

---

## 6. Understanding console.log()

`console.log()` is a JavaScript method used to display information in the browser's developer console.

It is commonly used when testing code and debugging applications.

### Example 1: Displaying Text

```javascript
console.log("Hello, Developer");
```

### Example 2: Displaying Numbers

```javascript
console.log(100);

console.log(50 + 50);
```

Output:

```text
100
100
```

### Example 3: Displaying Multiple Values

```javascript
console.log("Name:", "Alex");

console.log("Age:", 21);

console.log("Country:", "Kenya");
```

### Other Console Methods

JavaScript provides other useful console methods.

| Method | Purpose |
|---|---|
| `console.log()` | Displays general information |
| `console.error()` | Displays error messages |
| `console.warn()` | Displays warning messages |
| `console.table()` | Displays structured data in a table |

Example:

```javascript
console.log("Application started");

console.warn("This is a warning");

console.error("Something went wrong");
```

---

## 7. Connecting JavaScript to HTML

JavaScript can be written directly inside an HTML document or stored in an external `.js` file.

For larger projects, external JavaScript files are generally preferred because they improve code organisation and maintainability.

### A. Internal JavaScript

JavaScript can be written inside an HTML document using the `<script>` element.

Example:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>JavaScript Introduction</title>
</head>

<body>

    <h1>Welcome to JavaScript</h1>

    <script>
        console.log("JavaScript is connected!");
    </script>

</body>

</html>
```

In this example, JavaScript is written directly inside the HTML document.

### B. External JavaScript

This approach involves creating a separate JavaScript file and linking it to HTML.

**Project Structure:**

```text
my-first-website/
│
├── index.html
│
└── script.js
```

**index.html**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>My First JavaScript Website</title>

    <script src="script.js" defer></script>
</head>

<body>

    <h1>Welcome to JavaScript</h1>

    <p>My first webpage with JavaScript.</p>

</body>

</html>
```

**script.js**

```javascript
console.log("JavaScript is successfully connected!");

console.log("Welcome to my website.");
```

### Understanding the Script Element

```html
<script src="script.js" defer></script>
```

| Attribute | Explanation |
|---|---|
| `script` | Defines a JavaScript script |
| `src` | Specifies the location of the JavaScript file |
| `defer` | Executes the external script after HTML parsing |
| `</script>` | Closes the script element |

**Best Practice:** Use external JavaScript files and the `defer` attribute for beginner projects where appropriate.

---

## 8. Understanding Comments in JavaScript

Comments are notes written inside source code to explain what the code does.

Comments are ignored during normal JavaScript execution.

JavaScript supports two main types of comments.

### A. Single-Line Comments

Single-line comments begin with `//`.

```javascript
// This is my first JavaScript comment

console.log("Hello World");
```

### B. Multi-Line Comments

Multi-line comments begin with `/*` and end with `*/`.

```javascript
/*
This is a multi-line comment.

It can extend across
multiple lines.
*/

console.log("Learning JavaScript");
```

### Why Are Comments Important?

Comments help developers:

- Explain complex code.
- Document important functionality.
- Improve code readability.
- Collaborate with other developers.
- Maintain applications more easily.

---

## 9. JavaScript Variables: A First Look

Variables are containers used to store information.

Although variables will be covered in detail in Module 02, it is important to understand their basic purpose.

Example:

```javascript
let studentName = "Alex";

console.log(studentName);
```

Output:

```text
Alex
```

Here:

- `let` declares a variable.
- `studentName` is the variable name.
- `"Alex"` is the stored value.
- `console.log()` displays the value.

You will learn more about `let`, `const`, `var` and JavaScript data types in the next module.

---

## 10. Practical Activity

### Activity: Create Your First JavaScript Project

Create a project named:

`javascript-introduction`

Your project should contain:

```text
javascript-introduction/
│
├── index.html
│
└── script.js
```

### Requirements

**Your HTML page should contain:**

1. A main heading titled My First JavaScript Website.
2. A paragraph introducing JavaScript.
3. A heading titled About Me.
4. A paragraph containing your personal introduction.

**Your JavaScript file should:**

1. Display your full name in the console.
2. Display your country.
3. Display your learning goal.
4. Display a welcome message.
5. Include at least two JavaScript comments.

### Expected Console Output

```text
Welcome to my JavaScript project!

Name: Alex
Country: Kenya
Learning Goal: Become a Software Engineer

JavaScript is exciting!
```

---

## 11. Knowledge Check

Test your understanding of the concepts covered in this lesson.

**1. What does JavaScript do in web development?**

A. Creates database tables.

B. Adds behaviour and interactivity to websites.

C. Only styles HTML elements.

D. Creates images.

**2. Which technology is responsible for the structure of a webpage?**

A. CSS

B. JavaScript

C. HTML

D. Node.js

**3. Which method displays information in the browser console?**

A. `display()`

B. `console.log()`

C. `print()`

D. `show()`

**4. Which HTML element is used to connect JavaScript to HTML?**

A. `<style>`

B. `<javascript>`

C. `<script>`

D. `<code>`

**5. What is the purpose of the `src` attribute in a script element?**

A. It defines the text colour.

B. It specifies the JavaScript file location.

C. It creates a variable.

D. It defines a heading.

**6. Is JavaScript case-sensitive?**

A. Yes.

B. No.

**7. Which symbol is used to write a single-line JavaScript comment?**

A. `<!-- -->`

B. `//`

C. `##`

D. `**`

**8. What does the `defer` attribute do?**

A. Deletes JavaScript code.

B. Delays execution of an external script until HTML parsing is complete.

C. Stops JavaScript from executing.

D. Changes the browser language.

---

## 12. Module Challenge

### Challenge: Personal Introduction Console Application

Build a simple JavaScript programme that introduces you.

Your programme should display:

- Full name.
- Age.
- Country.
- Current course or profession.
- Favourite technology.
- Career goal.
- A motivational message.

### Technical Requirements

- Create an `index.html` file.
- Create an external `script.js` file.
- Connect the JavaScript file correctly.
- Use `console.log()` to display information.
- Include meaningful comments.
- Use clean and readable code.

### Example Implementation

```javascript
// Personal Introduction Programme

console.log("==============================");

console.log("PERSONAL INTRODUCTION");

console.log("==============================");

console.log("Name: Alex");

console.log("Age: 21");

console.log("Country: Kenya");

console.log("Profession: Software Engineering Student");

console.log("Favourite Technology: JavaScript");

console.log("Career Goal: Fullstack Software Engineer");

console.log("==============================");

console.log("Keep learning. Keep building!");
```

### Submission Requirements

1. Create a GitHub repository named `javascript-introduction`.
2. Upload your `index.html` and `script.js` files.
3. Ensure the JavaScript file is correctly linked.
4. Test your programme in the browser.
5. Submit your GitHub repository link.

---

## Key Takeaways

- JavaScript is a programming language used to create interactive and dynamic applications.
- HTML provides structure, CSS controls presentation and JavaScript implements behaviour.
- JavaScript executes through a JavaScript engine.
- `console.log()` displays information in the developer console.
- JavaScript can be written internally or externally.
- The `<script>` element connects JavaScript to HTML.
- Comments help developers document and organise their code.
- Variables allow programmes to store and access information.

---

<p align="center">
  <strong>Congratulations! You have successfully completed your introduction to JavaScript.</strong>
</p>

<p align="center">
  NEXT: MODULE 02 — VARIABLES AND DATA TYPES
</p>
