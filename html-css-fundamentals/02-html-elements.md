
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:42275a,100:734b6d&height=160&section=header&text=HTML%20ELEMENTS&fontSize=34&fontColor=ffffff&animation=fadeIn&desc=Building%20Meaningful%20Web%20Content&descSize=13" width="100%">
</p>

<h1 align="center">🧩 MODULE 02: HTML ELEMENTS</h1>

## 🌟 Introduction

HTML elements are the building blocks of every web page.

In the previous module, you created your first HTML document. Now it is time to learn how to add different types of content.

You will learn how to create headings, paragraphs, links, images, lists and other useful elements.

## 🎯 Learning Objectives

By the end of this module, you should be able to:

- Create headings and paragraphs.
- Format text.
- Insert images.
- Create hyperlinks.
- Build ordered and unordered lists.
- Understand common HTML elements.

---

##  1. HTML Headings

HTML provides six heading levels.

They range from `<h1>` to `<h6>`.

```html
<h1>Main Heading</h1>
<h2>Second Heading</h2>
<h3>Third Heading</h3>
<h4>Fourth Heading</h4>
<h5>Fifth Heading</h5>
<h6>Sixth Heading</h6>
```

### Important!

Use headings to organise your content logically.

A page should generally have one clear main heading, followed by meaningful subheadings.

---

##  2. HTML Paragraphs

The `<p>` element creates paragraphs.

```html
<p>
    HTML is used to structure web pages.
</p>

<p>
    CSS is used to style web pages.
</p>
```

Each paragraph is displayed as a separate block of text.

---

##  3. Text Formatting Elements

HTML provides elements for giving text meaning and emphasis.

```html
<strong>Important information</strong>

<em>Emphasised text</em>

<mark>Highlighted text</mark>

<small>Small text</small>

<del>Deleted text</del>

<ins>Inserted text</ins>

<sub>Subscript</sub>

<sup>Superscript</sup>
```

Example:

```html
<p>
    <strong>HTML</strong> is important when learning
    <em>web development</em>.
</p>
```

---

##  4. HTML Links

Links allow users to navigate between pages and websites.

Use the `<a>` element.

```html
<a href="https://www.google.com">
    Visit Google
</a>
```

### Open a Link in a New Tab

```html
<a href="https://www.wikipedia.org"
   target="_blank"
   rel="noopener noreferrer">
    Visit Wikipedia
</a>
```

### Link to Another Page

```html
<a href="about.html">About Us</a>
```

### Link to a Section

```html
<a href="#contact">Contact Us</a>

<section id="contact">
    <h2>Contact Information</h2>
</section>
```

---

##  5. HTML Images

Images make websites more attractive and informative.

Use the `<img>` element.

```html
<img
    src="images/student.jpg"
    alt="A student studying"
    width="400"
>
```

### Important Image Attributes

| Attribute | Purpose |
|---|---|
| `src` | Image location |
| `alt` | Alternative text |
| `width` | Image width |
| `height` | Image height |

Always provide useful alternative text for informative images.

---

##  6. HTML Lists

HTML supports three common types of lists.

### Unordered Lists

An unordered list uses bullet points.

```html
<h2>My Favourite Subjects</h2>

<ul>
    <li>Mathematics</li>
    <li>Computer Science</li>
    <li>Physics</li>
</ul>
```

### Ordered Lists

An ordered list uses numbers by default.

```html
<h2>Steps to Create a Website</h2>

<ol>
    <li>Plan your website.</li>
    <li>Create your HTML file.</li>
    <li>Add CSS styling.</li>
    <li>Test your website.</li>
</ol>
```

### Description Lists

```html
<dl>
    <dt>HTML</dt>
    <dd>Used to structure web pages.</dd>

    <dt>CSS</dt>
    <dd>Used to style web pages.</dd>
</dl>
```

---

##  7. Line Breaks and Horizontal Rules

### Line Break

```html
<p>Hello!<br>Welcome to my website.</p>
```

### Horizontal Rule

```html
<h2>About Me</h2>
<p>This is my introduction.</p>

<hr>

<h2>My Skills</h2>
<p>HTML and CSS.</p>
```

Use these elements where their meaning fits. Use CSS for general spacing and visual separators.

---

##  8. Div and Span

### The Div Element

`<div>` is a generic block container.

```html
<div class="student-card">
    <h2>Student Profile</h2>
    <p>Learning web development.</p>
</div>
```

### The Span Element

`<span>` is a generic inline container.

```html
<p>
    I am learning
    <span>HTML and CSS</span>.
</p>
```

These elements are useful when you need a container but no more meaningful semantic element is suitable.

---

##  Practical Activity

Create a page called `my-interests.html`.

Include:

- A main heading.
- Three subheadings.
- Three paragraphs.
- An image.
- An external link.
- An ordered list.
- An unordered list.
- Text using `<strong>` and `<em>`.

##  Knowledge Check

1. How many heading levels does HTML provide?
2. Which element creates a hyperlink?
3. What is the purpose of the `alt` attribute?
4. What is the difference between `<ol>` and `<ul>`?
5. What is the difference between `<div>` and `<span>`?
6. Which element creates a horizontal line?

##  Module Challenge

Build a personal portfolio introduction page using all the elements you have learned.

##  Key Takeaways

- HTML elements represent different types of content.
- Headings organise information.
- Links connect pages and websites.
- Images add visual information.
- Lists organise related information.
- Div and span provide generic containers.

<p align="center"><strong> Keep building. Keep experimenting.</strong></p>
