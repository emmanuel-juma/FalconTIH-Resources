
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=HTML%20INTRODUCTION&fontSize=32&fontColor=ffffff&animation=fadeIn&desc=Your%20First%20Step%20Into%20Web%20Development&descSize=13" width="100%">
</p>

<h1 align="center">🧱 MODULE 01: INTRODUCTION TO HTML</h1>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-First%20Steps-E34F26?style=for-the-badge&logo=html5&logoColor=white">
</p>

## 🌟 Welcome!

Every website you visit has a structure. That structure is created using HTML.

In this module, you will discover what HTML is, how it works and how to create your very first web page.

## 🎯 Learning Objectives

By the end of this module, you should be able to:

- Explain what HTML means.
- Understand how HTML works.
- Identify HTML tags and elements.
- Understand HTML attributes.
- Create a basic HTML document.
- Open an HTML document in a browser.

---

## 📖 1. What is HTML?

HTML stands for **HyperText Markup Language**.

It is the standard markup language used to create the structure of web pages.

HTML tells a browser what different pieces of content represent.

For example:

- A heading.
- A paragraph.
- An image.
- A link.
- A table.
- A form.

HTML does not primarily control how these elements look. That is the responsibility of CSS.

### 🏗️ Understanding HTML, CSS and JavaScript

Think of a house:

| Technology | Responsibility | House Example |
|---|---|---|
| HTML | Structure | Walls and rooms |
| CSS | Presentation | Paint and decoration |
| JavaScript | Behaviour | Electricity and controls |

Together, these technologies make modern websites possible.

---

## 📖 2. How Does HTML Work?

HTML works through elements written using tags.

A browser reads an HTML document and displays its content as a web page.

For example:

```html
<h1>Welcome to My Website</h1>
<p>I am learning HTML.</p>
```

The browser displays:

# Welcome to My Website

I am learning HTML.

---

## 📖 3. Understanding HTML Tags

Most HTML elements have an opening tag and a closing tag.

Example:

```html
<p>This is a paragraph.</p>
```

- `<p>` is the opening tag.
- `This is a paragraph.` is the content.
- `</p>` is the closing tag.

Some elements are void elements and do not require closing tags.

Examples:

```html
<img src="photo.jpg" alt="A photograph">
<br>
<hr>
```

---

## 📖 4. Your First HTML Document

Create a new file named:

`index.html`

Write the following code:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>My First Website</title>
</head>

<body>

    <h1>Hello, World!</h1>

    <p>
        Welcome to my first HTML website.
    </p>

</body>

</html>
```

### 🔍 Understanding the Code

| Element | Explanation |
|---|---|
| `<!DOCTYPE html>` | Declares an HTML5 document |
| `<html>` | Root element of the page |
| `<head>` | Contains document information |
| `<title>` | Sets the browser tab title |
| `<body>` | Contains visible page content |
| `<h1>` | Creates the main heading |
| `<p>` | Creates a paragraph |

---

## 📖 5. HTML Attributes

Attributes provide additional information about HTML elements.

Example:

```html
<a href="https://google.com">Visit Google</a>
```

Here:

- `href` is the attribute.
- `https://google.com` is its value.

Another example:

```html
<img src="student.jpg" alt="A student studying">
```

Common attributes include:

| Attribute | Purpose |
|---|---|
| `id` | Gives an element a unique identifier |
| `class` | Assigns a reusable class name |
| `href` | Specifies a link destination |
| `src` | Specifies a resource location |
| `alt` | Provides alternative text for an image |
| `title` | Provides additional advisory information |

---

## 📖 6. HTML Comments

Comments are notes written inside HTML code.

They are not displayed as normal page content.

```html
<!-- This is my main heading -->

<h1>Welcome!</h1>
```

Comments help developers understand and organise their code.

---

## 💻 7. Practical Activity

Create a personal introduction page.

Your page should contain:

1. Your name as the main heading.
2. A paragraph introducing yourself.
3. A heading called My Hobbies.
4. A list of at least three hobbies.
5. A link to a website you enjoy.
6. An image with appropriate alternative text.

## 🧪 Knowledge Check

1. What does HTML stand for?
2. Is HTML a programming language?
3. Which tag creates a paragraph?
4. Which element contains visible page content?
5. What is the purpose of an HTML attribute?
6. What does `<!DOCTYPE html>` do?

## 🏆 Module Challenge

Build a simple personal profile page using only HTML.

Do not use CSS yet. Focus on writing clean and organised HTML.

## ✅ Key Takeaways

- HTML provides the structure of web pages.
- HTML uses elements and attributes.
- Browsers interpret HTML documents.
- A basic HTML document contains `html`, `head` and `body` elements.

---

<p align="center">
  <strong>🎉 Congratulations! You have created your first HTML document.</strong>
</p>

<p align="center">NEXT: HTML ELEMENTS ➡️</p>
