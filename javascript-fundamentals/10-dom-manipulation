
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=DOM%20MANIPULATION&fontSize=32&fontColor=ffffff&animation=fadeIn&desc=Controlling%20Webpage%20Content%20With%20JavaScript&descSize=12" width="100%">
</p>

<h1 align="center">MODULE 10: DOM MANIPULATION</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-DOM%20Manipulation-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-BEGINNER-2E86C1?style=for-the-badge">
</p>

## Welcome!

So far, you have learned how to write JavaScript programmes that execute instructions and process data.

However, most frontend applications need to interact directly with the webpage.

For example:

- A button changes a heading when clicked.
- A shopping cart updates its displayed total.
- A form displays an error message when information is missing.
- A website adds new products without reloading the page.
- A navigation menu opens and closes when selected.

JavaScript makes these interactions possible through the **Document Object Model (DOM)**.

The DOM allows JavaScript to access, read and modify HTML elements.

In this module, you will learn how to select HTML elements, change their content, update styles, create new elements and remove existing elements.

## Learning Objectives

By the end of this module, you should be able to:

- Explain what the DOM is.
- Understand the relationship between HTML and the DOM.
- Select HTML elements using JavaScript.
- Change text and HTML content.
- Modify element attributes.
- Change CSS styles using JavaScript.
- Add and remove CSS classes.
- Create HTML elements dynamically.
- Append and remove elements.
- Understand basic DOM traversal.
- Build a simple interactive webpage.

---

## 1. What is the DOM?

DOM stands for **Document Object Model**.

It is a programming interface that represents an HTML document as a structured tree of objects.

When a browser loads an HTML page, it creates a DOM representation of the document.

JavaScript can then interact with this structure.

### Example HTML

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
</head>
<body>

    <h1>Welcome</h1>

    <p>This is my first webpage.</p>

</body>
</html>
```

The browser represents the document as a tree of nodes.

A simplified structure looks like this:

```text
Document
│
└── html
    │
    ├── head
    │   │
    │   └── title
    │
    └── body
        │
        ├── h1
        │
        └── p
```

JavaScript can access these elements and modify them.

### Why is the DOM Important?

The DOM allows developers to:

- Update webpage content.
- Change element styles.
- Respond to user interactions.
- Create new elements.
- Remove existing elements.
- Build dynamic interfaces.

---

## 2. Accessing the DOM

JavaScript provides several methods for selecting elements from an HTML document.

These methods allow you to locate elements before modifying them.

### A. getElementById()

The `getElementById()` method selects an element using its unique ID.

**HTML:**

```html
<h1 id="heading">Welcome to JavaScript</h1>
```

**JavaScript:**

```javascript
const heading = document.getElementById("heading");

console.log(heading);
```

The selected heading is stored in the `heading` variable.

### B. getElementsByClassName()

The `getElementsByClassName()` method selects elements using a class name.

**HTML:**

```html
<p class="description">First paragraph</p>

<p class="description">Second paragraph</p>

<p class="description">Third paragraph</p>
```

**JavaScript:**

```javascript
const descriptions = document.getElementsByClassName("description");

console.log(descriptions);
```

This method returns a live HTMLCollection containing matching elements.

You can access individual elements using indexes:

```javascript
console.log(descriptions[0]);

console.log(descriptions[1]);
```

### C. getElementsByTagName()

The `getElementsByTagName()` method selects elements using their HTML tag names.

**JavaScript:**

```javascript
const paragraphs = document.getElementsByTagName("p");

console.log(paragraphs);
```

This returns a live HTMLCollection of paragraph elements.

### D. querySelector()

The `querySelector()` method selects the first element matching a CSS selector.

**HTML:**

```html
<h1 id="heading">Welcome</h1>

<p class="description">Learning JavaScript</p>
```

**JavaScript:**

```javascript
const heading = document.querySelector("#heading");

const paragraph = document.querySelector(".description");

console.log(heading);

console.log(paragraph);
```

You can use CSS selector syntax:

| Selector | Meaning |
|---|---|
| `#heading` | Element with ID heading |
| `.description` | Element with class description |
| `p` | Paragraph elements |
| `div p` | Paragraph inside a div |
| `button.primary` | Button with primary class |

### E. querySelectorAll()

The `querySelectorAll()` method selects all elements matching a CSS selector.

**HTML:**

```html
<p class="description">First paragraph</p>

<p class="description">Second paragraph</p>

<p class="description">Third paragraph</p>
```

**JavaScript:**

```javascript
const paragraphs = document.querySelectorAll(".description");

console.log(paragraphs);
```

This returns a static NodeList.

You can loop through the selected elements:

```javascript
paragraphs.forEach(paragraph => {

    console.log(paragraph.textContent);

});
```

### Comparison of Selection Methods

| Method | Returns |
|---|---|
| `getElementById()` | One matching element |
| `getElementsByClassName()` | Live HTMLCollection |
| `getElementsByTagName()` | Live HTMLCollection |
| `querySelector()` | First matching element |
| `querySelectorAll()` | Static NodeList |

**Best Practice:** `querySelector()` and `querySelectorAll()` are flexible because they support CSS selectors.

---

## 3. Changing Text Content

JavaScript can change the text displayed inside an HTML element.

The `textContent` property reads or updates an element's text.

### HTML

```html
<h1 id="heading">Original Heading</h1>
```

### JavaScript

```javascript
const heading = document.querySelector("#heading");

heading.textContent = "Welcome to JavaScript";
```

The webpage now displays:

```text
Welcome to JavaScript
```

### Reading Text Content

```javascript
const heading = document.querySelector("#heading");

console.log(heading.textContent);
```

### Updating Paragraphs

```html
<p id="description">Original description</p>
```

```javascript
const description = document.querySelector("#description");

description.textContent = "This paragraph was updated using JavaScript.";
```

---

## 4. Understanding innerHTML

The `innerHTML` property reads or updates the HTML markup inside an element.

Unlike `textContent`, it interprets HTML tags.

### Example

**HTML:**

```html
<div id="container"></div>
```

**JavaScript:**

```javascript
const container = document.querySelector("#container");

container.innerHTML = "<h2>Welcome</h2><p>Learning JavaScript</p>";
```

The browser creates a heading and paragraph inside the container.

### Difference Between textContent and innerHTML

| Property | Behaviour |
|---|---|
| `textContent` | Treats assigned content as text |
| `innerHTML` | Parses assigned content as HTML |

Example:

```javascript
const container = document.querySelector("#container");

container.textContent = "<h1>Hello</h1>";
```

This displays the literal text:

```text
<h1>Hello</h1>
```

However:

```javascript
container.innerHTML = "<h1>Hello</h1>";
```

This creates an actual heading element.

**Security Warning:** Avoid inserting untrusted user input using `innerHTML`. It can introduce cross-site scripting (XSS) vulnerabilities. Use `textContent` for ordinary user-provided text.

---

## 5. Changing HTML Attributes

HTML elements have attributes such as:

- `src`
- `href`
- `alt`
- `title`
- `disabled`
- `type`

JavaScript can read and update these attributes.

### Using getAttribute()

```html
<img id="profileImage" src="profile.jpg" alt="Profile">
```

```javascript
const image = document.querySelector("#profileImage");

console.log(image.getAttribute("src"));
```

Output:

```text
profile.jpg
```

### Using setAttribute()

```javascript
const image = document.querySelector("#profileImage");

image.setAttribute("src", "new-profile.jpg");

image.setAttribute("alt", "Updated profile image");
```

### Using removeAttribute()

```javascript
const button = document.querySelector("#submitButton");

button.removeAttribute("disabled");
```

### Updating a Link

```html
<a id="websiteLink" href="https://example.com">Visit Website</a>
```

```javascript
const link = document.querySelector("#websiteLink");

link.setAttribute("href", "https://developer.mozilla.org/");
```

---

## 6. Changing CSS Styles with JavaScript

JavaScript can modify an element's inline styles using the `style` property.

### Example

**HTML:**

```html
<h1 id="heading">Welcome</h1>
```

**JavaScript:**

```javascript
const heading = document.querySelector("#heading");

heading.style.color = "blue";

heading.style.fontSize = "36px";

heading.style.backgroundColor = "lightgray";
```

### CSS Property Naming

CSS properties that use hyphens are written in camelCase when accessed through JavaScript.

| CSS Property | JavaScript Property |
|---|---|
| `background-color` | `backgroundColor` |
| `font-size` | `fontSize` |
| `margin-top` | `marginTop` |
| `border-radius` | `borderRadius` |
| `text-align` | `textAlign` |

### Example: Styling a Button

```javascript
const button = document.querySelector("#submitButton");

button.style.backgroundColor = "blue";

button.style.color = "white";

button.style.padding = "12px 20px";

button.style.borderRadius = "8px";
```

Although direct styling is possible, using CSS classes is generally better for managing larger interfaces.

---

## 7. Adding and Removing CSS Classes

JavaScript provides the `classList` property for managing CSS classes.

Important methods include:

- `add()`
- `remove()`
- `toggle()`
- `contains()`

### HTML

```html
<h1 id="heading">Welcome</h1>
```

### CSS

```css
.highlight {
    color: blue;
    background-color: lightgray;
}

.active {
    font-weight: bold;
}
```

### Adding a Class

```javascript
const heading = document.querySelector("#heading");

heading.classList.add("highlight");
```

### Removing a Class

```javascript
heading.classList.remove("highlight");
```

### Toggling a Class

The `toggle()` method adds a class if it does not exist and removes it if it already exists.

```javascript
heading.classList.toggle("active");
```

### Checking Whether a Class Exists

```javascript
console.log(heading.classList.contains("active"));
```

Output:

```text
true
```

Class manipulation is useful when implementing:

- Dark mode.
- Active navigation links.
- Dropdown menus.
- Modal windows.
- Interactive buttons.

---

## 8. Creating HTML Elements Dynamically

JavaScript can create new HTML elements without writing them directly in the original HTML file.

The `document.createElement()` method creates an element.

### Example

**HTML:**

```html
<div id="container"></div>
```

**JavaScript:**

```javascript
const container = document.querySelector("#container");

const heading = document.createElement("h2");

heading.textContent = "Created Using JavaScript";

container.appendChild(heading);
```

The heading is created and inserted into the container.

### Creating a Paragraph

```javascript
const paragraph = document.createElement("p");

paragraph.textContent = "This paragraph was created dynamically.";

container.appendChild(paragraph);
```

### Creating a Button

```javascript
const button = document.createElement("button");

button.textContent = "Click Me";

container.appendChild(button);
```

---

## 9. Adding Elements to the DOM

JavaScript provides several methods for inserting elements into the DOM.

### A. append()

The `append()` method adds content at the end of an element.

```javascript
const container = document.querySelector("#container");

const paragraph = document.createElement("p");

paragraph.textContent = "New paragraph";

container.append(paragraph);
```

### B. prepend()

The `prepend()` method inserts content at the beginning of an element.

```javascript
container.prepend(paragraph);
```

### C. appendChild()

The `appendChild()` method appends a node as the last child of a parent element.

```javascript
container.appendChild(paragraph);
```

### D. before() and after()

These methods insert elements before or after a selected element.

```javascript
const heading = document.querySelector("#heading");

const paragraph = document.createElement("p");

paragraph.textContent = "Additional information";

heading.after(paragraph);
```

---

## 10. Removing HTML Elements

JavaScript can remove elements from the DOM.

The `remove()` method removes an element directly.

### Example

**HTML:**

```html
<p id="description">This paragraph will be removed.</p>
```

**JavaScript:**

```javascript
const description = document.querySelector("#description");

description.remove();
```

The paragraph is removed from the webpage.

### Removing a Child Element

```javascript
const container = document.querySelector("#container");

const paragraph = container.querySelector("p");

if (paragraph) {
    container.removeChild(paragraph);
}
```

The `removeChild()` method removes a specific child from its parent.

---

## 11. DOM Traversal

DOM traversal means moving between related elements in the DOM tree.

JavaScript provides properties that allow you to access parent, child and sibling elements.

### A. parentElement

Returns the parent element.

```javascript
const paragraph = document.querySelector("#description");

console.log(paragraph.parentElement);
```

### B. children

Returns the child elements of an element.

```javascript
const container = document.querySelector("#container");

console.log(container.children);
```

### C. firstElementChild

Returns the first child element.

```javascript
console.log(container.firstElementChild);
```

### D. lastElementChild

Returns the last child element.

```javascript
console.log(container.lastElementChild);
```

### E. nextElementSibling

Returns the next sibling element.

```javascript
const heading = document.querySelector("#heading");

console.log(heading.nextElementSibling);
```

### F. previousElementSibling

Returns the previous sibling element.

```javascript
console.log(heading.previousElementSibling);
```

---

## 12. Working with Input Values

JavaScript can read values entered into HTML input fields.

The `value` property provides the current value of an input.

### HTML

```html
<input type="text" id="username" placeholder="Enter your name">

<button id="submitButton">Submit</button>

<p id="output"></p>
```

### JavaScript

```javascript
const username = document.querySelector("#username");

const submitButton = document.querySelector("#submitButton");

const output = document.querySelector("#output");

submitButton.addEventListener("click", () => {

    output.textContent = `Welcome, ${username.value}!`;

});
```

When the user clicks the button, the entered name is displayed.

### Reading Numeric Inputs

Input values are usually returned as strings.

If you need to perform calculations, convert the value into a number.

```html
<input type="number" id="price" placeholder="Enter price">

<button id="calculateButton">Calculate</button>

<p id="result"></p>
```

```javascript
const priceInput = document.querySelector("#price");

const calculateButton = document.querySelector("#calculateButton");

const result = document.querySelector("#result");

calculateButton.addEventListener("click", () => {

    const price = Number(priceInput.value);

    result.textContent = `Price: KES ${price}`;

});
```

---

## 13. Practical Activity

### Activity: Interactive Profile Card

Build a webpage that displays a user profile and allows the user to update information using JavaScript.

### HTML Requirements

Your page should contain:

1. A main heading.
2. A profile card.
3. A profile image.
4. A name.
5. A short description.
6. An input field for changing the name.
7. A button for updating the profile.
8. A button for changing the profile description.

### JavaScript Requirements

Your programme should:

- Select the profile elements.
- Read values from input fields.
- Update the profile name.
- Update the profile description.
- Change the profile image source.
- Add a CSS class to highlight the profile.
- Display a message after an update.

### Suggested HTML

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Interactive Profile Card</title>

    <link rel="stylesheet" href="style.css">

    <script src="script.js" defer></script>
</head>

<body>

    <main>

        <div class="profile-card" id="profileCard">

            <img
                id="profileImage"
                src="https://placehold.co/150"
                alt="Profile"
            >

            <h2 id="profileName">Alex Morgan</h2>

            <p id="profileDescription">
                Frontend Engineering Student
            </p>

        </div>

        <section>

            <input
                type="text"
                id="nameInput"
                placeholder="Enter new name"
            >

            <button id="updateNameButton">
                Update Name
            </button>

            <button id="updateDescriptionButton">
                Update Description
            </button>

            <button id="highlightButton">
                Highlight Profile
            </button>

        </section>

        <p id="message"></p>

    </main>

</body>

</html>
```

### Suggested JavaScript

```javascript
const profileName = document.querySelector("#profileName");

const profileDescription = document.querySelector("#profileDescription");

const nameInput = document.querySelector("#nameInput");

const updateNameButton = document.querySelector("#updateNameButton");

const updateDescriptionButton = document.querySelector("#updateDescriptionButton");

const highlightButton = document.querySelector("#highlightButton");

const profileCard = document.querySelector("#profileCard");

const message = document.querySelector("#message");

updateNameButton.addEventListener("click", () => {

    const newName = nameInput.value.trim();

    if (newName === "") {

        message.textContent = "Please enter a name.";

        return;

    }

    profileName.textContent = newName;

    message.textContent = "Profile name updated successfully.";

});

updateDescriptionButton.addEventListener("click", () => {

    profileDescription.textContent =
        "Learning JavaScript and frontend engineering.";

});

highlightButton.addEventListener("click", () => {

    profileCard.classList.toggle("highlight");

});
```

### Additional Tasks

1. Add a button that changes the profile image.
2. Add a button that resets the profile information.
3. Add an input field for the user's profession.
4. Display a warning when the name field is empty.
5. Add a CSS class for a dark profile theme.

---

## 14. Knowledge Check

**1. What does DOM stand for?**

A. Data Object Management.

B. Document Object Model.

C. Digital Output Method.

D. Document Operation Manager.

**2. Which method selects an element using its ID?**

A. `querySelectorAll()`

B. `getElementById()`

C. `getElementsByTagName()`

D. `createElement()`

**3. What does querySelector() return?**

A. Every matching element.

B. The first matching element.

C. The entire HTML document.

D. An array of all elements.

**4. Which property changes an element's text content?**

A. `innerStyle`

B. `textContent`

C. `classList`

D. `src`

**5. What is the difference between textContent and innerHTML?**

A. They perform exactly the same operation.

B. textContent handles text, while innerHTML parses HTML markup.

C. innerHTML only changes CSS.

D. textContent removes HTML elements.

**6. Which method creates a new HTML element?**

A. `createElement()`

B. `appendChild()`

C. `remove()`

D. `getElementById()`

**7. Which property is commonly used to read the value of an input field?**

A. `textContent`

B. `innerHTML`

C. `value`

D. `className`

**8. Which classList method switches a class on or off?**

A. `add()`

B. `remove()`

C. `toggle()`

D. `contains()`

---

## 15. Module Challenge

### Challenge: Dynamic Product Listing System

Build a small product listing webpage using JavaScript DOM manipulation.

### Product Information

Each product should contain:

- Product name.
- Product price.
- Product category.
- Product image.
- Product availability.

### Technical Requirements

1. Create an HTML container for displaying products.
2. Store product information in an array of objects.
3. Use JavaScript to create product cards.
4. Display each product's information.
5. Add a button to each product card.
6. Display a message when a product is selected.
7. Change the style of unavailable products.
8. Add a button that clears the product listing.
9. Add a button that restores the product listing.
10. Use `createElement()` or safe DOM insertion methods to create elements.

### Example Implementation

```javascript
// Dynamic Product Listing System

const products = [

    {
        name: "Laptop",
        price: 75000,
        category: "Electronics",
        available: true
    },

    {
        name: "Mouse",
        price: 1500,
        category: "Accessories",
        available: true
    },

    {
        name: "Monitor",
        price: 25000,
        category: "Electronics",
        available: false
    }

];

const productContainer = document.querySelector("#products");

function displayProducts() {

    productContainer.replaceChildren();

    products.forEach(product => {

        const card = document.createElement("div");

        const name = document.createElement("h2");

        const price = document.createElement("p");

        const category = document.createElement("p");

        const status = document.createElement("p");

        const button = document.createElement("button");

        card.classList.add("product-card");

        name.textContent = product.name;

        price.textContent = `KES ${product.price}`;

        category.textContent = product.category;

        status.textContent = product.available
            ? "Available"
            : "Out of Stock";

        button.textContent = "View Product";

        button.disabled = !product.available;

        button.addEventListener("click", () => {

            alert(`Selected: ${product.name}`);

        });

        card.append(
            name,
            price,
            category,
            status,
            button
        );

        productContainer.appendChild(card);

    });

}

displayProducts();
```

### Submission Requirements

1. Create a GitHub repository named `javascript-dom-manipulation`.
2. Create `index.html`, `style.css` and `script.js`.
3. Store products in an array of objects.
4. Generate product cards dynamically.
5. Implement product selection.
6. Add a way to clear and restore the product listing.
7. Test the application in your browser.
8. Submit your GitHub repository link.

---

## Key Takeaways

- The DOM represents an HTML document as a structured tree.
- JavaScript can access and modify DOM elements.
- `getElementById()` selects elements by ID.
- `querySelector()` and `querySelectorAll()` use CSS selectors.
- `textContent` updates text.
- `innerHTML` parses HTML markup.
- `setAttribute()` updates element attributes.
- `classList` manages CSS classes.
- `createElement()` creates new elements.
- `append()` and `appendChild()` insert elements.
- `remove()` deletes elements from the DOM.
- The `value` property reads input values.
- DOM traversal allows developers to move between related elements.

---

<p align="center">
  <strong>Congratulations! You have successfully completed DOM Manipulation.</strong>
</p>

<p align="center">
  NEXT: MODULE 11 — EVENTS
</p>
