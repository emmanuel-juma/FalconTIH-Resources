
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:134e5e,100:71b280&height=160&section=header&text=SEMANTIC%20HTML&fontSize=34&fontColor=ffffff&animation=fadeIn&desc=Give%20Your%20Content%20Meaning&descSize=13" width="100%">
</p>

<h1 align="center">🏛️ MODULE 03: SEMANTIC HTML</h1>

## 🌟 Introduction

A good website is not just about how it looks. It is also about how well its content is organised and understood.

Semantic HTML allows developers to describe the purpose of different parts of a web page.

Instead of using generic containers everywhere, semantic elements communicate what each section represents.

## 🎯 Learning Objectives

By the end of this module, you should be able to:

- Define semantic HTML.
- Identify common semantic elements.
- Structure a web page using semantic elements.
- Understand the importance of accessibility.
- Differentiate between semantic and non-semantic elements.

---

## 📖 1. What is Semantic HTML?

Semantic HTML means using HTML elements according to their meaning and purpose.

For example:

```html
<div>
    Welcome to my website
</div>
```

This is a generic container.

A more meaningful alternative is:

```html
<header>
    <h1>Welcome to my website</h1>
</header>
```

The `<header>` element communicates that the content is introductory or belongs to a page or section header.

---

## 📖 2. Common Semantic Elements

| Element | Purpose |
|---|---|
| `<header>` | Introductory content |
| `<nav>` | Navigation links |
| `<main>` | Main page content |
| `<section>` | Groups related content |
| `<article>` | Independent content |
| `<aside>` | Related or supporting content |
| `<footer>` | Footer information |
| `<figure>` | Self-contained media |
| `<figcaption>` | Caption for a figure |

---

## 📖 3. Understanding Header

The `<header>` element contains introductory information.

```html
<header>
    <h1>My Learning Website</h1>
    <p>Learn something new every day.</p>
</header>
```

A page can have a header, and individual sections or articles can also have their own headers.

---

## 📖 4. Understanding Navigation

The `<nav>` element contains important navigation links.

```html
<nav aria-label="Main navigation">
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="courses.html">Courses</a>
    <a href="contact.html">Contact</a>
</nav>
```

Navigation helps users move between pages or sections.

---

## 📖 5. Understanding Main

The `<main>` element contains the primary content of a page.

```html
<main>
    <h2>Welcome to Our Courses</h2>

    <p>
        Explore our learning resources.
    </p>
</main>
```

A document should normally have one visible `<main>` element.

---

## 📖 6. Understanding Section

A `<section>` groups related content.

```html
<section>
    <h2>Our Courses</h2>

    <p>
        We offer HTML, CSS and JavaScript courses.
    </p>
</section>
```

Use a section when the content forms a meaningful thematic group.

---

## 📖 7. Understanding Article

An `<article>` represents independent content that can make sense on its own.

Examples include:

- Blog posts.
- News articles.
- Forum posts.
- Individual resource cards when they are self-contained.

```html
<article>
    <h2>Why Learn HTML?</h2>

    <p>
        HTML is the foundation of web development.
    </p>
</article>
```

---

## 📖 8. Understanding Aside

The `<aside>` element contains related or supporting information.

```html
<aside>
    <h3>Did You Know?</h3>

    <p>
        HTML is used to structure web content.
    </p>
</aside>
```

It can be used for tips, related links or supplementary information.

---

## 📖 9. Understanding Footer

The `<footer>` element contains information about a page or section.

```html
<footer>
    <p>&copy; 2026 My Learning Website</p>
    <p>All rights reserved.</p>
</footer>
```

---

## 💻 10. Complete Semantic HTML Example

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Student Learning Hub</title>
</head>

<body>

    <header>
        <h1>Student Learning Hub</h1>
        <p>Resources for curious learners.</p>
    </header>

    <nav aria-label="Main navigation">
        <a href="#home">Home</a>
        <a href="#courses">Courses</a>
        <a href="#about">About</a>
    </nav>

    <main id="home">

        <section id="courses">
            <h2>Our Courses</h2>

            <article>
                <h3>HTML Fundamentals</h3>
                <p>Learn how to structure websites.</p>
            </article>

            <article>
                <h3>CSS Fundamentals</h3>
                <p>Learn how to style websites.</p>
            </article>
        </section>

        <aside>
            <h2>Study Tip</h2>
            <p>Practise a little every day.</p>
        </aside>

    </main>

    <footer id="about">
        <p>&copy; 2026 Student Learning Hub</p>
    </footer>

</body>
</html>
```

---

## ♿ 11. Why Semantic HTML Matters

Semantic HTML improves:

- **Accessibility:** Assistive technologies can identify page regions and content roles.
- **Maintainability:** Developers can understand the code more easily.
- **Organisation:** Content has a clear structure.
- **Navigation:** Users can move through meaningful page landmarks.
- **Search understanding:** Clear structure can help search engines interpret content.

Semantic HTML is one part of accessibility. You should also use good colour contrast, keyboard-friendly controls, meaningful link text and form labels.

## 💻 Practical Activity

Create a college homepage using:

- Header.
- Navigation.
- Main content.
- Two sections.
- Two articles.
- Aside.
- Footer.

Give each major section a meaningful heading.

## 🧪 Knowledge Check

1. What is semantic HTML?
2. What is the purpose of `<main>`?
3. Which element is used for navigation?
4. What is the difference between `<section>` and `<article>`?
5. Why is semantic HTML important for accessibility?

## 🏆 Module Challenge

Build a complete semantic blog page with at least three articles.

## ✅ Key Takeaways

Semantic HTML makes websites more meaningful, organised and accessible.

<p align="center"><strong>🌟 Write meaningful code, not just working code!</strong></p>
