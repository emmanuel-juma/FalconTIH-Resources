
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:242b36,100:264de4&height=180&section=header&text=CSS%20SELECTORS&fontSize=32&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Target%20elements%20with%20precision&descSize=13&descAlignY=60" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CSS3-Selectors-264de4?style=for-the-badge&logo=css3"/>
  <img src="https://img.shields.io/badge/Level-Beginner-2ea44f?style=for-the-badge"/>
</p>

#  CSS Selectors

CSS selectors allow you to target specific HTML elements and apply styles to them.

##  Learning Objectives

By the end of this lesson, you should be able to:

- Identify common CSS selectors.
- Select elements using tags, classes, and IDs.
- Use grouping and descendant selectors.
- Understand pseudo-classes and pseudo-elements.
- Apply selectors to real webpage components.

## 1. Universal Selector

The universal selector `*` targets every HTML element.

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

This is commonly used as a CSS reset.

## 2. Element Selector

Targets all elements with a particular HTML tag.

```css
h1 {
    color: blue;
}

p {
    font-size: 18px;
}
```

Every `<h1>` becomes blue, and every `<p>` gets an 18px font size.

## 3. Class Selector

A class selector begins with a period (`.`).

**HTML**

```html
<p class="highlight">This is important.</p>
<p class="highlight">This is also important.</p>
```

**CSS**

```css
.highlight {
    color: orange;
    font-weight: bold;
}
```

A class can be reused on multiple elements.

## 4. ID Selector

An ID selector begins with a hash (`#`).

**HTML**

```html
<h1 id="main-title">Welcome to CSS</h1>
```

**CSS**

```css
#main-title {
    color: purple;
    text-align: center;
}
```

An ID should be unique within an HTML document.

## 5. Grouping Selector

Apply the same styles to multiple selectors.

```css
h1, h2, p {
    font-family: Arial, sans-serif;
}
```

This avoids repeating the same declarations.

## 6. Descendant Selector

Targets elements inside another element, at any nesting level.

```css
article p {
    color: #444;
}
```

This targets paragraphs inside an `<article>`.

## 7. Child Selector

Targets direct children only.

```css
.container > p {
    color: green;
}
```

This selects paragraphs that are direct children of `.container`.

## 8. Attribute Selector

Targets elements based on their attributes.

```css
input[type="text"] {
    border: 2px solid blue;
}

a[target="_blank"] {
    color: red;
}
```

## 9. Pseudo-Classes

Pseudo-classes target elements in a particular state.

### Hover

```css
button:hover {
    background-color: darkblue;
    color: white;
}
```

### Focus

```css
input:focus {
    outline: 2px solid blue;
}
```

### First Child

```css
li:first-child {
    color: red;
}
```

### Last Child

```css
li:last-child {
    color: green;
}
```

### Nth Child

```css
li:nth-child(2) {
    font-weight: bold;
}
```

## 10. Pseudo-Elements

Pseudo-elements style a specific part of an element.

### Before

```css
h2::before {
    content: "★ ";
    color: orange;
}
```

### After

```css
h2::after {
    content: " →";
}
```

### First Letter

```css
p::first-letter {
    font-size: 30px;
    font-weight: bold;
}
```

## 11. CSS Specificity

When multiple CSS rules target the same element, specificity helps determine which rule takes priority.

A simplified priority order is:

1. Inline styles.
2. ID selectors.
3. Class, attribute, and pseudo-class selectors.
4. Element and pseudo-element selectors.

Example:

```css
p {
    color: blue;
}

.message {
    color: green;
}

#notice {
    color: red;
}
```

```html
<p id="notice" class="message">Hello CSS!</p>
```

The paragraph will be red because the ID selector has higher specificity than the class and element selectors.

> Note: The cascade also considers origin, importance, layers, and source order. Avoid using `!important` as a shortcut for managing styles.

## 12. Selector Reference Table

| Selector | Example | Meaning |
|---|---|---|
| `*` | `*` | All elements |
| `element` | `p` | All paragraphs |
| `.class` | `.card` | Elements with a class |
| `#id` | `#header` | Element with an ID |
| `A B` | `div p` | Descendant |
| `A > B` | `div > p` | Direct child |
| `A, B` | `h1, p` | Grouping |
| `[attribute]` | `[required]` | Attribute selector |
| `:hover` | `button:hover` | Hover state |
| `::before` | `p::before` | Generated content before |

##  Practical Exercise: Navigation Bar

**HTML**

```html
<nav class="navbar">
    <h2 id="logo">MyWebsite</h2>

    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
    </ul>
</nav>
```

**CSS**

```css
* {
    box-sizing: border-box;
}

.navbar {
    background: #172554;
    padding: 20px;
}

#logo {
    color: white;
}

.navbar ul {
    list-style: none;
    display: flex;
    gap: 20px;
}

.navbar a {
    color: white;
    text-decoration: none;
}

.navbar a:hover {
    color: #facc15;
}
```

##  Practice Exercises

1. Create three headings and style them using an element selector.
2. Create two cards using the same class.
3. Use an ID selector to style a main heading.
4. Change a button's color when a user hovers over it.
5. Use `:first-child` to style the first item in a list.
6. Create a `::before` pseudo-element that adds an icon or symbol before each heading.

##  Knowledge Check

1. Which symbol is used for a class selector?
2. Which symbol is used for an ID selector?
3. What is the difference between a child and descendant selector?
4. What does `:hover` do?
5. Which has higher specificity: `.card` or `#card`?

##  Key Takeaways

- Selectors identify which HTML elements receive styles.
- Classes can be reused; IDs should be unique.
- Pseudo-classes style element states.
- Pseudo-elements style specific parts of elements.
- Specificity helps resolve competing CSS rules.

<p align="center">
  <b>Master selectors. Control your styles. 🎯</b>
</p>
