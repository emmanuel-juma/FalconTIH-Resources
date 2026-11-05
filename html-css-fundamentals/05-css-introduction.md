
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:242b36,100:264de4&height=180&section=header&text=CSS%20INTRODUCTION&fontSize=32&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Bring%20your%20HTML%20to%20life&descSize=13&descAlignY=60" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CSS3-Styling-264de4?style=for-the-badge&logo=css3&logoColor=white"/>
  <img src="https://img.shields.io/badge/Level-Beginner-2ea44f?style=for-the-badge"/>
</p>

# Introduction to CSS

Welcome to CSS! In this lesson, you will learn how to style HTML pages and transform plain documents into attractive, professional websites.

## 🎯 Learning Objectives

By the end of this lesson, you should be able to:

- Explain what CSS is and why it is important.
- Understand CSS syntax and rules.
- Apply inline, internal, and external CSS.
- Use colors, backgrounds, fonts, and spacing.
- Connect an external stylesheet to an HTML document.

## 1. What is CSS?

**CSS (Cascading Style Sheets)** is a language used to control the appearance and layout of HTML elements.

HTML provides the structure of a webpage, while CSS controls how that structure looks.

Think of a website as a house:

| Technology | Responsibility |
|---|---|
| HTML | Structure — walls, doors, rooms |
| CSS | Appearance — paint, decoration, layout |
| JavaScript | Behaviour — electricity, automation, interaction |

## 2. CSS Syntax

A CSS rule contains a selector and a declaration block.

```css
h1 {
    color: blue;
    font-size: 32px;
}
```

- `h1` — selector: identifies the HTML element.
- `color` — property: identifies what you want to change.
- `blue` — value: defines the chosen style.
- `font-size` — another property.
- `32px` — its value.

## 3. Three Ways to Add CSS

### A. Inline CSS

CSS is written directly inside an HTML element using the `style` attribute.

```html
<h1 style="color: blue; font-size: 32px;">
    Welcome to My Website
</h1>
```

**Best for:** Quick experiments, not large projects.

### B. Internal CSS

CSS is written inside a `<style>` element in the HTML document.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Internal CSS</title>

    <style>
        body {
            background-color: #f4f4f4;
            font-family: Arial, sans-serif;
        }

        h1 {
            color: #264de4;
            text-align: center;
        }
    </style>
</head>
<body>
    <h1>Hello, CSS!</h1>
</body>
</html>
```

**Best for:** Small pages with a single stylesheet.

### C. External CSS

CSS is stored in a separate `.css` file and connected to HTML.

**index.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>External CSS</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Learning External CSS</h1>
    <p>My webpage is now styled using an external file.</p>
</body>
</html>
```

**style.css**

```css
body {
    background-color: #f4f7fb;
    font-family: Arial, sans-serif;
}

h1 {
    color: #264de4;
    text-align: center;
}

p {
    color: #444;
    font-size: 18px;
}
```

**Recommended:** External CSS is usually best for larger projects because it keeps structure and styling separate.

## 4. Working with Colors

CSS supports several color formats.

```css
h1 {
    color: red;
}

p {
    color: #264de4;
}

section {
    background-color: rgb(240, 245, 255);
}
```

Common formats:

- Color names: `red`, `blue`, `white`.
- HEX: `#264de4`.
- RGB: `rgb(38, 77, 228)`.
- RGBA: `rgba(38, 77, 228, 0.5)`.

## 5. Backgrounds

```css
body {
    background-color: #f4f7fb;
}

.hero {
    background-image: url("images/background.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}
```

## 6. Typography

Typography controls how text appears.

```css
h1 {
    font-family: Arial, sans-serif;
    font-size: 36px;
    font-weight: bold;
    text-align: center;
}

p {
    font-size: 16px;
    line-height: 1.7;
    letter-spacing: 0.3px;
}
```

Important properties:

| Property | Purpose |
|---|---|
| `font-family` | Changes the font |
| `font-size` | Changes text size |
| `font-weight` | Controls thickness |
| `text-align` | Aligns text |
| `line-height` | Controls line spacing |
| `text-decoration` | Adds or removes decoration |

## 7. CSS Units

| Unit | Meaning | Example |
|---|---|---|
| `px` | Pixels | `20px` |
| `%` | Percentage | `80%` |
| `em` | Relative to parent font size | `2em` |
| `rem` | Relative to root font size | `1.5rem` |
| `vw` | Viewport width | `50vw` |
| `vh` | Viewport height | `50vh` |

## 8. Mini Project: A Styled Profile Card

Create an HTML file and a CSS file.

**index.html**

```html
<div class="profile-card">
    <img src="https://placehold.co/120x120" alt="Profile placeholder">
    <h2>Jane Doe</h2>
    <p>Frontend Developer</p>
    <button>View Profile</button>
</div>
```

**style.css**

```css
body {
    background: #eef2ff;
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}

.profile-card {
    background: white;
    padding: 30px;
    width: 260px;
    text-align: center;
    border-radius: 16px;
    box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
}

.profile-card img {
    width: 120px;
    height: 120px;
    border-radius: 50%;
}

.profile-card button {
    background: #264de4;
    color: white;
    border: none;
    padding: 12px 20px;
    border-radius: 8px;
    cursor: pointer;
}
```

##  Practice Exercises

1. Create an HTML page with a heading and three paragraphs.
2. Connect an external CSS file.
3. Change the background color of the page.
4. Give the heading a different font, color, and size.
5. Create a profile card with a border radius and shadow.

##  Knowledge Check

1. What does CSS stand for?
2. What is the purpose of a CSS selector?
3. Which method is recommended for larger websites?
4. What is the difference between `color` and `background-color`?
5. What does `font-size` control?

##  Key Takeaways

- CSS controls the appearance of HTML pages.
- CSS rules consist of selectors and declarations.
- You can use inline, internal, or external CSS.
- Colors, backgrounds, typography, and spacing help create attractive websites.

<p align="center">
  <b>Keep styling. Keep creating. Keep learning! </b>
</p>
