
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:242b36,100:1572b6&height=180&section=header&text=CSS%20GRID&fontSize=36&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Master%20two-dimensional%20web%20layouts&descSize=12&descAlignY=60" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CSS3-Grid-1572b6?style=for-the-badge&logo=css3"/>
  <img src="https://img.shields.io/badge/Level-Intermediate-orange?style=for-the-badge"/>
</p>

# 🧩 CSS Grid

CSS Grid is a powerful layout system used to arrange webpage elements in rows and columns.

Unlike Flexbox, which is primarily one-dimensional, Grid is designed for two-dimensional layouts.

## 🎯 Learning Objectives

By the end of this lesson, you should be able to:

- Explain CSS Grid and its purpose.
- Create grid containers and grid items.
- Define columns and rows.
- Control spacing using `gap`.
- Make elements span multiple rows and columns.
- Build responsive layouts using Grid.

## 1. What Is CSS Grid?

CSS Grid allows you to divide a webpage into rows and columns.

It is useful for:

- Website dashboards.
- Image galleries.
- Product listings.
- Portfolio layouts.
- Complete webpage structures.

## 2. Creating a Grid Container

To activate CSS Grid, use:

```css
.container {
    display: grid;
}
```

The direct children of the container become grid items.

## 3. Defining Columns

Use `grid-template-columns` to define the number and size of columns.

```css
.container {
    display: grid;
    grid-template-columns: 200px 200px 200px;
}
```

This creates three columns, each 200px wide.

You can also use fractional units:

```css
.container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
}
```

The `fr` unit distributes available space proportionally.

A shorter version:

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
}
```

## 4. Defining Rows

Use `grid-template-rows` to define row sizes.

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 150px 200px;
}
```

This creates three columns and two explicitly sized rows.

## 5. Grid Gap

The `gap` property controls the spacing between rows and columns.

```css
.container {
    display: grid;
    gap: 20px;
}
```

You can also specify separate gaps:

```css
.container {
    row-gap: 15px;
    column-gap: 25px;
}
```

## 6. Grid Column and Row Spanning

Grid items can occupy multiple columns or rows.

### Column Spanning

```css
.item {
    grid-column: span 2;
}
```

The item occupies two columns.

### Row Spanning

```css
.item {
    grid-row: span 2;
}
```

The item occupies two rows.

You can also define exact grid lines:

```css
.item {
    grid-column: 1 / 3;
}
```

This places the item from column line 1 to column line 3.

## 7. Repeat and Minmax

The `repeat()` function reduces repetition.

```css
.container {
    grid-template-columns: repeat(4, 1fr);
}
```

The `minmax()` function sets a minimum and maximum size.

```css
.container {
    grid-template-columns: repeat(3, minmax(150px, 1fr));
}
```

## 8. Responsive Grid Layouts

Use `auto-fit` and `minmax()` to create flexible grids.

```css
.container {
    display: grid;
    grid-template-columns: repeat(
        auto-fit,
        minmax(220px, 1fr)
    );
    gap: 20px;
}
```

The browser automatically fits as many columns as possible based on the available width.

## 9. Grid Template Areas

Grid areas allow you to name sections of a layout.

```css
.layout {
    display: grid;
    grid-template-columns: 1fr 3fr;
    grid-template-areas:
        "header header"
        "sidebar main"
        "footer footer";
    gap: 15px;
}

.header {
    grid-area: header;
}

.sidebar {
    grid-area: sidebar;
}

.main {
    grid-area: main;
}

.footer {
    grid-area: footer;
}
```

**HTML**

```html
<div class="layout">
    <header class="header">Header</header>
    <aside class="sidebar">Sidebar</aside>
    <main class="main">Main Content</main>
    <footer class="footer">Footer</footer>
</div>
```

## 10. Mini Project: Product Gallery

**HTML**

```html
<section class="gallery">
    <div class="product">
        <img src="https://placehold.co/300x200" alt="Product one">
        <h3>Product One</h3>
        <p>Discover something amazing.</p>
    </div>

    <div class="product">
        <img src="https://placehold.co/300x200" alt="Product two">
        <h3>Product Two</h3>
        <p>Quality meets creativity.</p>
    </div>

    <div class="product">
        <img src="https://placehold.co/300x200" alt="Product three">
        <h3>Product Three</h3>
        <p>Designed for everyday use.</p>
    </div>

    <div class="product">
        <img src="https://placehold.co/300x200" alt="Product four">
        <h3>Product Four</h3>
        <p>Explore more possibilities.</p>
    </div>
</section>
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

.gallery {
    display: grid;
    grid-template-columns: repeat(
        auto-fit,
        minmax(220px, 1fr)
    );
    gap: 25px;
}

.product {
    background: white;
    padding: 15px;
    border-radius: 12px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
    transition: transform 0.3s ease;
}

.product:hover {
    transform: translateY(-6px);
}

.product img {
    width: 100%;
    border-radius: 8px;
}

.product h3 {
    color: #172554;
}

.product p {
    color: #64748b;
    line-height: 1.5;
}
```

## 11. Flexbox vs. Grid

| Feature | Flexbox | Grid |
|---|---|---|
| Dimensions | One-dimensional | Two-dimensional |
| Main purpose | Aligning items in a row or column | Organizing rows and columns |
| Layout control | Content-driven | Structure-driven |
| Common use | Navigation bars | Galleries and dashboards |

Both systems can be used together in the same project.

## 📝 Practice Exercises

1. Create a grid with three equal columns.
2. Add six cards to the grid.
3. Add a 20px gap.
4. Make one card span two columns.
5. Create a responsive gallery using `auto-fit` and `minmax()`.
6. Build a simple webpage layout with a header, sidebar, main section, and footer.

## 🧠 Knowledge Check

1. What does `display: grid` do?
2. What is the purpose of `grid-template-columns`?
3. What does `1fr` mean?
4. What does `grid-column: span 2` do?
5. How does CSS Grid differ from Flexbox?

## 🏁 Key Takeaways

- CSS Grid is a two-dimensional layout system.
- Grid containers organize items into rows and columns.
- `fr` distributes available space.
- `gap` controls spacing.
- `repeat()`, `minmax()`, and `auto-fit` help create flexible layouts.

<p align="center">
  <b>Think in rows. Think in columns. Build amazing layouts! 🧩</b>
</p>
