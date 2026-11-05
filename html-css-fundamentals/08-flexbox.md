
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:242b36,100:1572b6&height=180&section=header&text=CSS%20FLEXBOX&fontSize=34&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Build%20flexible%20and%20responsive%20layouts&descSize=12&descAlignY=60" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CSS3-Flexbox-1572b6?style=for-the-badge&logo=css3"/>
  <img src="https://img.shields.io/badge/Level-Intermediate-orange?style=for-the-badge"/>
</p>

#  CSS Flexbox

Flexbox is a CSS layout system that makes it easier to arrange, align, and distribute elements inside a container.

It is especially useful for navigation bars, card layouts, toolbars, and centering content.

##  Learning Objectives

By the end of this lesson, you should be able to:

- Explain how Flexbox works.
- Create a flex container.
- Understand main and cross axes.
- Use `justify-content` and `align-items`.
- Control item direction, wrapping, and spacing.
- Build practical layouts using Flexbox.

## 1. What Is Flexbox?

Flexbox means **Flexible Box Layout**.

It helps arrange elements in one dimension:

- Horizontally (row).
- Vertically (column).

To use Flexbox, apply:

```css
.container {
    display: flex;
}
```

The element becomes a flex container, and its direct children become flex items.

## 2. Understanding the Axes

Flexbox has two axes:

- **Main axis:** The direction in which flex items are arranged.
- **Cross axis:** The direction perpendicular to the main axis.

With the default `flex-direction: row`, the main axis is horizontal and the cross axis is vertical.

## 3. Flex Direction

The `flex-direction` property controls the direction of items.

```css
.container {
    display: flex;
    flex-direction: row;
}
```

Available values:

| Value | Description |
|---|---|
| `row` | Left to right |
| `row-reverse` | Right to left |
| `column` | Top to bottom |
| `column-reverse` | Bottom to top |

## 4. Justify Content

`justify-content` controls how items are distributed along the main axis.

```css
.container {
    display: flex;
    justify-content: center;
}
```

Common values:

- `flex-start`
- `flex-end`
- `center`
- `space-between`
- `space-around`
- `space-evenly`

Example:

```css
.container {
    display: flex;
    justify-content: space-between;
}
```

## 5. Align Items

`align-items` aligns items along the cross axis.

```css
.container {
    display: flex;
    align-items: center;
}
```

Common values:

- `stretch`
- `flex-start`
- `flex-end`
- `center`
- `baseline`

## 6. Flex Wrap

By default, flex items try to fit on one line.

Use `flex-wrap` when you want items to move onto additional lines.

```css
.container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
}
```

Values:

- `nowrap`
- `wrap`
- `wrap-reverse`

## 7. Gap

The `gap` property adds spacing between flex items.

```css
.container {
    display: flex;
    gap: 20px;
}
```

You can also use:

```css
.container {
    row-gap: 15px;
    column-gap: 25px;
}
```

## 8. Flex Item Properties

### Flex Grow

Controls how much an item can grow relative to other items.

```css
.item {
    flex-grow: 1;
}
```

### Flex Shrink

Controls how much an item can shrink.

```css
.item {
    flex-shrink: 1;
}
```

### Flex Basis

Sets the initial main size of an item before remaining space is distributed.

```css
.item {
    flex-basis: 200px;
}
```

### Flex Shorthand

```css
.item {
    flex: 1;
}
```

## 9. Align Self

`align-self` allows an individual item to override the container's `align-items` value.

```css
.special-item {
    align-self: flex-end;
}
```

## 10. Centering with Flexbox

One of the most useful Flexbox techniques is centering an element both horizontally and vertically.

```css
body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}
```

## 11. Mini Project: Responsive Navigation Bar

**HTML**

```html
<header class="navbar">
    <h2 class="logo">MyBrand</h2>

    <nav>
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Services</a>
        <a href="#">Contact</a>
    </nav>

    <button>Get Started</button>
</header>
```

**CSS**

```css
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
    padding: 20px 5%;
    background: #172554;
}

.logo {
    color: white;
}

.navbar nav {
    display: flex;
    gap: 20px;
}

.navbar a {
    color: white;
    text-decoration: none;
}

.navbar button {
    background: #facc15;
    border: none;
    padding: 12px 18px;
    border-radius: 8px;
    cursor: pointer;
}

@media (max-width: 650px) {
    .navbar {
        flex-direction: column;
    }

    .navbar nav {
        flex-wrap: wrap;
        justify-content: center;
    }
}
```

## 12. Flexbox vs. Grid

| Flexbox | CSS Grid |
|---|---|
| One-dimensional layout | Two-dimensional layout |
| Works along a row or column | Works across rows and columns |
| Great for navigation bars | Great for page layouts |
| Useful for aligning items | Useful for complex structures |

##  Practice Exercises

1. Create a container with three boxes.
2. Arrange the boxes in a row using Flexbox.
3. Center them horizontally.
4. Align them vertically.
5. Add a 20px gap.
6. Make the boxes wrap on smaller screens.
7. Build a navigation bar using Flexbox.

##  Knowledge Check

1. What does `display: flex` do?
2. What is the main axis?
3. What is the difference between `justify-content` and `align-items`?
4. What does `flex-wrap: wrap` do?
5. Which property creates spacing between flex items?

##  Key Takeaways

- Flexbox is a one-dimensional layout system.
- The flex container controls the arrangement of its children.
- `justify-content` aligns along the main axis.
- `align-items` aligns along the cross axis.
- Flexbox makes alignment and responsive layouts easier.

<p align="center">
  <b>Think flexible. Design responsive. </b>
</p>
