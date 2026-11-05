
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:242b36,100:1572b6&height=180&section=header&text=RESPONSIVE%20DESIGN&fontSize=31&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=One%20website.%20Every%20screen.&descSize=13&descAlignY=60" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CSS3-Responsive%20Design-1572b6?style=for-the-badge&logo=css3"/>
  <img src="https://img.shields.io/badge/Level-Intermediate-orange?style=for-the-badge"/>
</p>

# 📱 Responsive Web Design

Responsive Web Design is an approach to building websites that adapt to different screen sizes and devices.

A responsive website should work well on:

- Smartphones.
- Tablets.
- Laptops.
- Desktop computers.

## 🎯 Learning Objectives

By the end of this lesson, you should be able to:

- Explain responsive web design.
- Use the viewport meta tag.
- Understand fluid layouts.
- Apply CSS media queries.
- Use responsive images.
- Build a mobile-friendly webpage.

## 1. What Is Responsive Design?

Responsive design ensures that a webpage adjusts its layout and appearance according to the screen or viewport size.

For example:

- On a desktop, a navigation menu may appear horizontally.
- On a phone, the same navigation items may be arranged vertically.
- A three-column card layout may become a single column on a small screen.

## 2. The Viewport Meta Tag

Every responsive HTML page should include the viewport meta tag.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

This tells the browser to use the device's actual viewport width and an initial zoom level of 1.

Example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Website</title>
</head>
<body>
    <h1>Welcome to Responsive Design</h1>
</body>
</html>
```

## 3. Fluid Layouts

Fluid layouts use relative units such as percentages instead of relying entirely on fixed pixel widths.

```css
.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}
```

This allows the container to shrink on smaller screens while keeping a maximum width on larger screens.

## 4. Responsive Images

Images should adapt to the width of their containers.

```css
img {
    max-width: 100%;
    height: auto;
}
```

This prevents images from overflowing their containers.

## 5. CSS Media Queries

Media queries allow you to apply styles depending on device or viewport characteristics.

Example:

```css
body {
    background: white;
}

@media (max-width: 768px) {
    body {
        background: #e0f2fe;
    }
}
```

The background changes when the viewport is 768px wide or smaller.

## 6. Common Breakpoints

Breakpoints are viewport widths at which a layout changes to improve usability.

Example breakpoints:

| Device category | Example breakpoint |
|---|---|
| Small phones | 480px |
| Tablets | 768px |
| Small laptops | 1024px |
| Large screens | 1200px |

These are common starting points, not strict device rules. Choose breakpoints based on when your content needs a layout change.

## 7. Mobile-First Design

Mobile-first design means writing the basic styles for smaller screens first, then adding styles for larger screens.

```css
.container {
    display: grid;
    grid-template-columns: 1fr;
    gap: 20px;
}

@media (min-width: 768px) {
    .container {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (min-width: 1024px) {
    .container {
        grid-template-columns: repeat(3, 1fr);
    }
}
```

The layout starts with one column, changes to two columns on wider screens, and then changes to three.

## 8. Responsive Typography

Use flexible font sizes to improve readability across devices.

```css
h1 {
    font-size: clamp(2rem, 5vw, 4rem);
}
```

`clamp()` accepts three values:

- Minimum size.
- Preferred flexible size.
- Maximum size.

The browser chooses a size within the specified range.

## 9. Responsive Navigation

A simple navigation layout can change direction on smaller screens.

```css
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
}

.nav-links {
    display: flex;
    gap: 20px;
}

@media (max-width: 600px) {
    .navbar {
        flex-direction: column;
    }

    .nav-links {
        flex-direction: column;
        align-items: center;
    }
}
```

## 10. Mini Project: Responsive Website

**HTML**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Website</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="header">
        <h1>MyWebsite</h1>

        <nav>
            <a href="#">Home</a>
            <a href="#">About</a>
            <a href="#">Services</a>
            <a href="#">Contact</a>
        </nav>
    </header>

    <main class="container">
        <section class="hero">
            <h2>Build for Every Screen</h2>
            <p>Learn how to create websites that look great on phones, tablets, and computers.</p>
            <button>Explore More</button>
        </section>

        <section class="cards">
            <article class="card">
                <h3>HTML</h3>
                <p>Build the structure of your website.</p>
            </article>

            <article class="card">
                <h3>CSS</h3>
                <p>Style your website beautifully.</p>
            </article>

            <article class="card">
                <h3>Responsive Design</h3>
                <p>Make your website work on every screen.</p>
            </article>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 MyWebsite. All rights reserved.</p>
    </footer>

</body>
</html>
```

**style.css**

```css
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    color: #172554;
    background: #f8fafc;
}

.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 5%;
    background: #172554;
    color: white;
}

.header nav {
    display: flex;
    gap: 20px;
}

.header nav a {
    color: white;
    text-decoration: none;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: 30px auto;
}

.hero {
    padding: 60px 30px;
    text-align: center;
    background: linear-gradient(135deg, #264de4, #172554);
    color: white;
    border-radius: 16px;
}

.hero h2 {
    font-size: clamp(2rem, 5vw, 3.5rem);
}

.hero p {
    line-height: 1.7;
}

.hero button {
    padding: 12px 24px;
    border: none;
    border-radius: 8px;
    background: #facc15;
    cursor: pointer;
}

.cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    margin-top: 30px;
}

.card {
    padding: 25px;
    background: white;
    border-radius: 12px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.06);
}

footer {
    padding: 20px;
    text-align: center;
    background: #172554;
    color: white;
}

/* Tablet and smaller screens */
@media (max-width: 768px) {
    .header {
        flex-direction: column;
        gap: 15px;
    }

    .cards {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* Mobile screens */
@media (max-width: 480px) {
    .header nav {
        flex-direction: column;
        align-items: center;
    }

    .cards {
        grid-template-columns: 1fr;
    }

    .hero {
        padding: 35px 20px;
    }
}
```

## 11. Testing Responsive Websites

Test your website at different viewport sizes.

In Chrome:

1. Open your webpage.
2. Right-click and select **Inspect**.
3. Click the device toolbar icon.
4. Select a phone or tablet size.
5. Resize the viewport and check your layout.

Also test with a real mobile device when possible.

## 📝 Practice Exercises

1. Create a webpage with a header, main section, and footer.
2. Make the content container 90% wide.
3. Create three cards using CSS Grid.
4. Change the cards to two columns on tablets.
5. Change the cards to one column on phones.
6. Make all images responsive.
7. Test your page at different screen sizes.

## 🧠 Knowledge Check

1. What is responsive web design?
2. Why is the viewport meta tag important?
3. What does `max-width: 100%` do for images?
4. What is a CSS media query?
5. Explain the mobile-first approach.
6. What does the `clamp()` function do?

## 🏁 Key Takeaways

- Responsive design makes websites adapt to different screens.
- The viewport meta tag is essential.
- Fluid layouts use flexible sizing.
- Media queries apply styles at different viewport sizes.
- Mobile-first design starts with smaller screens.
- Always test your layouts at multiple sizes.

<p align="center">
  <b>Design once. Adapt everywhere. 📱💻</b>
</p>
