
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=JAVASCRIPT%20EVENTS&fontSize=32&fontColor=ffffff&animation=fadeIn&desc=Responding%20To%20User%20Interactions&descSize=12" width="100%">
</p>

<h1 align="center">MODULE 11: JAVASCRIPT EVENTS</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Events-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-BEGINNER-2E86C1?style=for-the-badge">
</p>

## Welcome!

In the previous module, you learned how JavaScript can access and modify HTML elements through the DOM.

However, a webpage becomes truly interactive when it can respond to user actions.

Consider the following:

- A user clicks a button.
- A user types into a search field.
- A user submits a registration form.
- A user moves their mouse over an image.
- A user selects an option from a dropdown menu.
- A user presses a key on the keyboard.

These actions generate **events**.

JavaScript events allow developers to respond to interactions and execute specific instructions.

In this module, you will learn how to listen for events, handle user interactions, validate forms and build interactive interfaces.

## Learning Objectives

By the end of this module, you should be able to:

- Explain what JavaScript events are.
- Understand event listeners.
- Use `addEventListener()`.
- Handle click events.
- Handle keyboard events.
- Handle mouse events.
- Handle form submission events.
- Understand the event object.
- Use `preventDefault()`.
- Understand event bubbling.
- Use event delegation.
- Build an interactive application.

---

## 1. What Are JavaScript Events?

An event is an action or occurrence that happens in the browser and can be detected by JavaScript.

Events can be triggered by users or by the browser itself.

### Examples of User Events

| Event | Description |
|---|---|
| `click` | User clicks an element |
| `dblclick` | User double-clicks an element |
| `mouseover` | Mouse moves over an element |
| `mouseout` | Mouse leaves an element |
| `keydown` | User presses a keyboard key |
| `keyup` | User releases a keyboard key |
| `input` | User changes an input value |
| `change` | A form control's value is committed |
| `submit` | A form is submitted |
| `focus` | An element receives focus |
| `blur` | An element loses focus |

### Why Are Events Important?

Events allow developers to build applications that respond to user interactions.

For example, without event handling, a button may simply appear on a webpage without performing any action.

With JavaScript events, the button can:

- Submit information.
- Open a menu.
- Add an item to a cart.
- Change the page theme.
- Display a notification.

---

## 2. Understanding Event Listeners

An event listener is a function that waits for a specific event to occur.

JavaScript provides the `addEventListener()` method to register event listeners.

### Syntax

```javascript
element.addEventListener("event", callback);
```

| Component | Explanation |
|---|---|
| `element` | The HTML element being monitored |
| `addEventListener()` | Registers an event listener |
| `"event"` | The event type |
| `callback` | Function executed when the event occurs |

### Example

**HTML:**

```html
<button id="myButton">Click Me</button>
```

**JavaScript:**

```javascript
const button = document.querySelector("#myButton");

button.addEventListener("click", () => {

    console.log("Button clicked!");

});
```

When the user clicks the button, the message appears in the console.

### Why Use addEventListener()?

It separates JavaScript behaviour from HTML structure and allows multiple listeners to be registered for the same event.

---

## 3. Handling Click Events

The `click` event occurs when a user clicks an element.

It is one of the most frequently used events in frontend development.

### Example: Changing a Heading

**HTML:**

```html
<h1 id="heading">Original Heading</h1>

<button id="changeButton">Change Heading</button>
```

**JavaScript:**

```javascript
const heading = document.querySelector("#heading");

const button = document.querySelector("#changeButton");

button.addEventListener("click", () => {

    heading.textContent = "The Heading Has Changed!";

});
```

When the button is clicked, the heading changes.

### Example: Click Counter

**HTML:**

```html
<h2 id="counter">0</h2>

<button id="incrementButton">Increase</button>
```

**JavaScript:**

```javascript
let count = 0;

const counter = document.querySelector("#counter");

const button = document.querySelector("#incrementButton");

button.addEventListener("click", () => {

    count++;

    counter.textContent = count;

});
```

Each click increases the counter by one.

### Adding Multiple Event Listeners

```javascript
button.addEventListener("click", () => {

    console.log("First listener");

});

button.addEventListener("click", () => {

    console.log("Second listener");

});
```

Both listeners execute when the button is clicked.

---

## 4. Handling Double-Click Events

The `dblclick` event occurs when an element is double-clicked.

Example:

**HTML:**

```html
<p id="message">Double-click this paragraph.</p>
```

**JavaScript:**

```javascript
const message = document.querySelector("#message");

message.addEventListener("dblclick", () => {

    message.textContent = "You double-clicked the paragraph!";

});
```

---

## 5. Handling Mouse Events

JavaScript can respond to mouse movement and interaction.

Common mouse events include:

- `click`
- `dblclick`
- `mouseover`
- `mouseout`
- `mousedown`
- `mouseup`
- `mousemove`

### Example: Mouse Over

**HTML:**

```html
<div id="box">Move your mouse here</div>
```

**JavaScript:**

```javascript
const box = document.querySelector("#box");

box.addEventListener("mouseover", () => {

    box.style.backgroundColor = "blue";

});
```

When the mouse enters the element, the background changes.

### Example: Mouse Out

```javascript
box.addEventListener("mouseout", () => {

    box.style.backgroundColor = "lightgray";

});
```

When the mouse leaves the element, the background returns to its original colour.

### Example: Mouse Movement

```javascript
box.addEventListener("mousemove", event => {

    console.log("Mouse X:", event.clientX);

    console.log("Mouse Y:", event.clientY);

});
```

The event object provides information about the mouse position.

---

## 6. Handling Keyboard Events

JavaScript can respond to keyboard actions.

Common keyboard events include:

- `keydown`
- `keyup`

### A. keydown

The `keydown` event occurs when a key is pressed.

Example:

**HTML:**

```html
<input type="text" id="username" placeholder="Type something">
```

**JavaScript:**

```javascript
const input = document.querySelector("#username");

input.addEventListener("keydown", event => {

    console.log("Key pressed:", event.key);

});
```

### B. keyup

The `keyup` event occurs when a key is released.

```javascript
input.addEventListener("keyup", event => {

    console.log("Key released:", event.key);

});
```

### Example: Detecting the Enter Key

```javascript
input.addEventListener("keydown", event => {

    if (event.key === "Enter") {

        console.log("Enter key pressed.");

    }

});
```

### Common Keyboard Event Properties

| Property | Description |
|---|---|
| `event.key` | The key value |
| `event.code` | The physical key identifier |
| `event.shiftKey` | Whether Shift is pressed |
| `event.ctrlKey` | Whether Ctrl is pressed |
| `event.altKey` | Whether Alt is pressed |

---

## 7. Handling Input Events

The `input` event occurs whenever the value of an input element changes through user interaction.

It is useful for:

- Live search.
- Character counters.
- Real-time validation.
- Dynamic previews.

### Example: Live Text Preview

**HTML:**

```html
<input type="text" id="nameInput" placeholder="Enter your name">

<p id="preview"></p>
```

**JavaScript:**

```javascript
const nameInput = document.querySelector("#nameInput");

const preview = document.querySelector("#preview");

nameInput.addEventListener("input", () => {

    preview.textContent = `Hello, ${nameInput.value}`;

});
```

The preview updates as the user types.

### Example: Character Counter

**HTML:**

```html
<textarea id="messageInput"></textarea>

<p id="characterCount">0 characters</p>
```

**JavaScript:**

```javascript
const messageInput = document.querySelector("#messageInput");

const characterCount = document.querySelector("#characterCount");

messageInput.addEventListener("input", () => {

    const count = messageInput.value.length;

    characterCount.textContent = `${count} characters`;

});
```

---

## 8. Handling Form Submission

Forms are used to collect information from users.

JavaScript can listen for the `submit` event and process form information.

### HTML

```html
<form id="registrationForm">

    <input
        type="text"
        id="fullName"
        placeholder="Full name"
    >

    <input
        type="email"
        id="email"
        placeholder="Email address"
    >

    <button type="submit">Register</button>

</form>

<p id="message"></p>
```

### JavaScript

```javascript
const form = document.querySelector("#registrationForm");

const fullName = document.querySelector("#fullName");

const email = document.querySelector("#email");

const message = document.querySelector("#message");

form.addEventListener("submit", event => {

    event.preventDefault();

    const nameValue = fullName.value.trim();

    const emailValue = email.value.trim();

    if (nameValue === "" || emailValue === "") {

        message.textContent = "Please complete all fields.";

        return;

    }

    message.textContent = `Welcome, ${nameValue}!`;

});
```

### Understanding preventDefault()

Browsers have default behaviours for certain events.

For example, submitting a form normally causes the browser to navigate or reload according to the form's submission settings.

`event.preventDefault()` stops the browser's default action.

This allows JavaScript to handle the form submission itself.

---

## 9. Understanding the Event Object

When an event occurs, JavaScript provides an event object containing information about that event.

The event object is commonly received as a parameter in the event handler.

### Example

```javascript
const button = document.querySelector("#myButton");

button.addEventListener("click", event => {

    console.log(event);

});
```

The event object contains information such as:

| Property | Description |
|---|---|
| `event.type` | Event type |
| `event.target` | Original element where the event occurred |
| `event.currentTarget` | Element whose listener is currently executing |
| `event.key` | Keyboard key |
| `event.clientX` | Mouse horizontal position |
| `event.clientY` | Mouse vertical position |

### Example: Identifying the Clicked Element

```javascript
document.addEventListener("click", event => {

    console.log("Clicked element:", event.target);

});
```

This logs the element where the click originated.

---

## 10. Event Bubbling

Event bubbling is a behaviour where an event starts at the target element and then propagates through its ancestors.

Consider the following HTML:

```html
<div id="parent">

    <button id="child">Click Me</button>

</div>
```

### JavaScript

```javascript
const parent = document.querySelector("#parent");

const child = document.querySelector("#child");

parent.addEventListener("click", () => {

    console.log("Parent clicked");

});

child.addEventListener("click", () => {

    console.log("Child clicked");

});
```

When the button is clicked, the output is:

```text
Child clicked
Parent clicked
```

The event starts at the button and bubbles up to the parent.

### Understanding stopPropagation()

The `stopPropagation()` method prevents an event from continuing to propagate.

```javascript
child.addEventListener("click", event => {

    event.stopPropagation();

    console.log("Child clicked");

});
```

Now clicking the child will not trigger the parent's bubbling listener.

---

## 11. Event Delegation

Event delegation involves attaching one event listener to a parent element instead of attaching separate listeners to every child.

It works because events bubble through the DOM.

### Example

**HTML:**

```html
<ul id="studentList">

    <li>Alex</li>

    <li>Brian</li>

    <li>Mary</li>

</ul>
```

**JavaScript:**

```javascript
const studentList = document.querySelector("#studentList");

studentList.addEventListener("click", event => {

    if (event.target.matches("li")) {

        console.log("Selected student:", event.target.textContent);

    }

});
```

The parent handles clicks from its child list items.

### Why Use Event Delegation?

- Reduces the number of event listeners.
- Works with dynamically added elements.
- Makes event handling easier to maintain.
- Improves organisation when managing many similar elements.

---

## 12. Removing Event Listeners

JavaScript allows event listeners to be removed using `removeEventListener()`.

To remove a listener, you must provide the same function reference that was originally registered.

### Example

```javascript
const button = document.querySelector("#myButton");

function handleClick() {

    console.log("Button clicked.");

}

button.addEventListener("click", handleClick);

button.removeEventListener("click", handleClick);
```

The listener is removed, so clicking the button no longer executes `handleClick`.

An anonymous function cannot normally be removed by writing another anonymous function with the same code because the two functions are different references.

---

## 13. Practical Activity

### Activity: Interactive Registration Form

Build a registration form that responds to user input and validates the submitted information.

### HTML Requirements

Your form should contain:

- Full name.
- Email address.
- Password.
- Confirm password.
- Submit button.
- Message area for feedback.

### JavaScript Requirements

Your programme should:

1. Listen for form submission.
2. Prevent the browser's default form submission.
3. Check that all fields are completed.
4. Check that the email address has a reasonable format.
5. Check that the password meets a minimum length.
6. Check whether both passwords match.
7. Display suitable error messages.
8. Display a success message when validation passes.

### Example HTML

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Registration Form</title>

    <script src="script.js" defer></script>
</head>

<body>

    <h1>Student Registration</h1>

    <form id="registrationForm">

        <input
            type="text"
            id="fullName"
            placeholder="Full name"
        >

        <input
            type="email"
            id="email"
            placeholder="Email address"
        >

        <input
            type="password"
            id="password"
            placeholder="Password"
        >

        <input
            type="password"
            id="confirmPassword"
            placeholder="Confirm password"
        >

        <button type="submit">Register</button>

    </form>

    <p id="message"></p>

</body>

</html>
```

### Example JavaScript

```javascript
const form = document.querySelector("#registrationForm");

const fullName = document.querySelector("#fullName");

const email = document.querySelector("#email");

const password = document.querySelector("#password");

const confirmPassword = document.querySelector("#confirmPassword");

const message = document.querySelector("#message");

form.addEventListener("submit", event => {

    event.preventDefault();

    const nameValue = fullName.value.trim();

    const emailValue = email.value.trim();

    const passwordValue = password.value;

    const confirmPasswordValue = confirmPassword.value;

    if (
        nameValue === "" ||
        emailValue === "" ||
        passwordValue === "" ||
        confirmPasswordValue === ""
    ) {

        message.textContent = "All fields are required.";

        return;

    }

    if (!email.checkValidity()) {

        message.textContent = "Please enter a valid email address.";

        return;

    }

    if (passwordValue.length < 8) {

        message.textContent = "Password must contain at least 8 characters.";

        return;

    }

    if (passwordValue !== confirmPasswordValue) {

        message.textContent = "Passwords do not match.";

        return;

    }

    message.textContent = `Registration successful. Welcome, ${nameValue}!`;

});
```

**Note:** This activity demonstrates client-side validation only. Real applications must also validate information on the server and handle passwords securely.

---

## 14. Knowledge Check

**1. What is a JavaScript event?**

A. A variable declaration.

B. An action or occurrence detected by the browser.

C. A CSS property.

D. An array method.

**2. Which method registers an event listener?**

A. `addEventListener()`

B. `createElement()`

C. `appendChild()`

D. `remove()`

**3. Which event occurs when a button is clicked?**

A. `submit`

B. `keydown`

C. `click`

D. `mouseover`

**4. Which event is useful for monitoring text as a user types?**

A. `mouseout`

B. `input`

C. `dblclick`

D. `blur`

**5. What does preventDefault() do?**

A. Stops JavaScript execution completely.

B. Prevents the browser's default action for an event.

C. Removes an HTML element.

D. Deletes an event listener.

**6. What does event.target identify?**

A. The original element where the event occurred.

B. The browser window.

C. The entire HTML document.

D. The event listener function.

**7. What is event bubbling?**

A. An event moving from an ancestor to its child.

B. An event propagating from the target through its ancestors.

C. An event being deleted.

D. An event being repeated automatically.

**8. What is event delegation?**

A. Creating a new event type.

B. Handling events from child elements using a parent listener.

C. Removing every event listener.

D. Stopping all event propagation.

---

## 15. Module Challenge

### Challenge: Interactive Shopping Cart

Build an interactive shopping cart that responds to user actions.

### Product Information

Create at least four products.

Each product should contain:

- Product ID.
- Product name.
- Price.
- Availability.

### Technical Requirements

1. Display products dynamically.
2. Add an Add to Cart button to each product.
3. Listen for button clicks.
4. Add selected products to the cart.
5. Display the number of items in the cart.
6. Calculate the total cart value.
7. Allow products to be removed from the cart.
8. Display a message when the cart is empty.
9. Use event delegation for product interactions.
10. Prevent invalid actions for unavailable products.

### Example Implementation

```javascript
// Interactive Shopping Cart

const products = [

    {
        id: 1,
        name: "Laptop",
        price: 75000,
        available: true
    },

    {
        id: 2,
        name: "Mouse",
        price: 1500,
        available: true
    },

    {
        id: 3,
        name: "Keyboard",
        price: 3000,
        available: true
    },

    {
        id: 4,
        name: "Monitor",
        price: 25000,
        available: false
    }

];

let cart = [];

const productContainer = document.querySelector("#products");

const cartContainer = document.querySelector("#cart");

const cartTotal = document.querySelector("#cartTotal");

const cartCount = document.querySelector("#cartCount");

function displayProducts() {

    productContainer.replaceChildren();

    products.forEach(product => {

        const card = document.createElement("div");

        const name = document.createElement("h3");

        const price = document.createElement("p");

        const button = document.createElement("button");

        name.textContent = product.name;

        price.textContent = `KES ${product.price}`;

        button.textContent = product.available
            ? "Add to Cart"
            : "Unavailable";

        button.disabled = !product.available;

        button.dataset.productId = product.id;

        button.classList.add("add-to-cart");

        card.append(name, price, button);

        productContainer.append(card);

    });

}

function displayCart() {

    cartContainer.replaceChildren();

    let total = 0;

    cart.forEach(product => {

        const item = document.createElement("p");

        item.textContent = `${product.name} - KES ${product.price}`;

        cartContainer.append(item);

        total += product.price;

    });

    cartCount.textContent = cart.length;

    cartTotal.textContent = `KES ${total}`;

}

productContainer.addEventListener("click", event => {

    if (!event.target.matches(".add-to-cart")) {
        return;
    }

    const productId = Number(event.target.dataset.productId);

    const product = products.find(
        item => item.id === productId
    );

    if (product && product.available) {

        cart.push(product);

        displayCart();

    }

});

displayProducts();

displayCart();
```

### Suggested HTML

```html
<div>

    <h1>Products</h1>

    <div id="products"></div>

</div>

<div>

    <h2>Shopping Cart</h2>

    <p>Items: <span id="cartCount">0</span></p>

    <div id="cart"></div>

    <h3>Total: <span id="cartTotal">KES 0</span></h3>

</div>
```

### Submission Requirements

1. Create a GitHub repository named `javascript-events`.
2. Create `index.html`, `style.css` and `script.js`.
3. Implement the shopping cart.
4. Use event listeners.
5. Use event delegation.
6. Display dynamic cart information.
7. Test adding and removing products.
8. Submit your GitHub repository link.

---

## Key Takeaways

- Events allow JavaScript to respond to browser and user interactions.
- `addEventListener()` registers event handlers.
- Click events handle button interactions.
- Keyboard events detect key presses.
- Input events monitor changes in form controls.
- Submit events handle form submissions.
- The event object contains information about an event.
- `preventDefault()` prevents the browser's default event behaviour.
- Event bubbling allows events to propagate through ancestors.
- Event delegation allows a parent to handle events from child elements.
- `removeEventListener()` removes a registered listener when given the same function reference.

---

<p align="center">
  <strong>Congratulations! You have successfully completed JavaScript Events.</strong>
</p>

<p align="center">
  NEXT: MODULE 12 — ERROR HANDLING
</p>
