
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:242b36,100:1572b6&height=180&section=header&text=THE%20CSS%20BOX%20MODEL&fontSize=30&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Understand%20spacing%20and%20element%20dimensions&descSize=12&descAlignY=60" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CSS3-Box%20Model-1572b6?style=for-the-badge&logo=css3"/>
  <img src="https://img.shields.io/badge/Level-Beginner-2ea44f?style=for-the-badge"/>
</p>

# 📦 The CSS Box Model

Every HTML element is represented as a rectangular box. Understanding the CSS Box Model helps you control the size, spacing, and positioning of elements.

## 🎯 Learning Objectives

By the end of this lesson, you should be able to:

- Explain the four parts of the CSS Box Model.
- Understand margin, border, padding, and content.
- Calculate an element's total dimensions.
- Use `box-sizing` correctly.
- Control spacing in webpage layouts.

## 1. What Is the CSS Box Model?

The CSS Box Model describes how an element's dimensions are calculated.

It consists of four parts:

1. Content
2. Padding
3. Border
4. Margin

## 2. The Four Parts

### A. Content

The actual text, image, or other content inside an element.

```css
.box {
    width: 200px;
    height: 100px;
}
```

### B. Padding

The space between the content and the border.

```css
.box {
    padding: 20px;
}
```

### C. Border

The line surrounding the padding and content.

```css
.box {
    border: 3px solid blue;
}
```

### D. Margin

The space outside the border. It separates an element from other elements.

```css
.box {
    margin: 30px;
}
```

## 3. Visual Representation

```text
+-------------------------------------+
|               MARGIN                |
|   +-----------------------------+   |
|   |           BORDER            |   |
|   |   +---------------------+   |   |
|   |   |       PADDING       |   |   |
|   |   |   +-------------+   |   |   |
|   |   |   |   CONTENT   |   |   |   |
|   |   |   +-------------+   |   |   |
|   |   +---------------------+   |   |
|   +-----------------------------+   |
+-------------------------------------+
```

## 4. Understanding Margin

Margin controls the space outside an element.

```css
.card {
    margin-top: 20px;
    margin-right: 30px;
    margin-bottom: 20px;
    margin-left: 30px;
}
```

You can also use shorthand:

```css
.card {
    margin: 20px;
}
```

Shorthand examples:

```css
/* All four sides */
margin: 20px;

/* Top and bottom, left and right */
margin: 20px 40px;

/* Top, left/right, bottom */
margin: 10px 20px 30px;

/* Top, right, bottom, left */
margin: 10px 20px 30px 40px;
```

## 5. Understanding Padding

Padding controls the space inside an element.

```css
.card {
    padding: 25px;
    background: #e0e7ff;
}
```

Padding shorthand works in the same order as margin.

## 6. Understanding Borders

```css
.card {
    border: 2px solid #264de4;
}
```

You can customize each border property:

```css
.card {
    border-width: 2px;
    border-style: solid;
    border-color: #264de4;
    border-radius: 12px;
}
```

Common border styles include:

- `solid`
- `dashed`
- `dotted`
- `double`
- `none`

## 7. Calculating Element Dimensions

By default, with `box-sizing: content-box`, the declared width applies only to the content.

Example:

```css
.box {
    width: 200px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
}
```

The total horizontal space, including margins, is:

- Content: 200px
- Left and right padding: 40px
- Left and right border: 10px
- Left and right margin: 20px

**Total horizontal space = 270px.**

## 8. The Box-Sizing Property

The `box-sizing` property changes how width and height are calculated.

### Content-box

```css
.box {
    box-sizing: content-box;
    width: 200px;
    padding: 20px;
    border: 5px solid black;
}
```

The rendered border-box width is 250px.

### Border-box

```css
.box {
    box-sizing: border-box;
    width: 200px;
    padding: 20px;
    border: 5px solid black;
}
```

The total border-box width remains 200px.

A common best practice is:

```css
* {
    box-sizing: border-box;
}
```

## 9. Centering an Element

You can center a block element horizontally using automatic left and right margins when it has an appropriate width.

```css
.container {
    width: 80%;
    max-width: 900px;
    margin: 0 auto;
}
```

## 10. Mini Project: Product Card

**HTML**

```html
<div class="product-card">
    <img src="https://placehold.co/300x180" alt="Product placeholder">
    <h2>Smart Watch</h2>
    <p>A modern smartwatch with useful everyday features.</p>
    <button>Buy Now</button>
</div>
```

**CSS**

```css
* {
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background: #f1f5f9;
    padding: 30px;
}

.product-card {
    width: 300px;
    margin: 30px auto;
    padding: 20px;
    background: white;
    border: 1px solid #ddd;
    border-radius: 15px;
    box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
}

.product-card img {
    width: 100%;
    border-radius: 10px;
}

.product-card h2 {
    margin: 15px 0 10px;
}

.product-card p {
    line-height: 1.6;
    color: #555;
}

.product-card button {
    padding: 12px 20px;
    border: none;
    border-radius: 8px;
    background: #264de4;
    color: white;
    cursor: pointer;
}
```

## 📝 Practice Exercises

1. Create a box with a width of 300px and a height of 150px.
2. Add 20px padding.
3. Add a 3px dashed border.
4. Add 30px margin.
5. Apply `box-sizing: border-box`.
6. Create three cards with different spacing values.

## 🧠 Knowledge Check

1. What are the four parts of the CSS Box Model?
2. What is the difference between padding and margin?
3. What does `border-radius` do?
4. What is the default value of `box-sizing`?
5. Why is `border-box` commonly used?

## 🏁 Key Takeaways

- Every HTML element is treated as a box.
- Padding creates space inside the border.
- Margin creates space outside the border.
- Borders surround the content and padding.
- `box-sizing: border-box` makes sizing easier to manage.

<p align="center">
  <b>Understand the box. Master the layout. 📦</b>
</p>
