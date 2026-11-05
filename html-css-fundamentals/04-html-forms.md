
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:42275a,100:734b6d&height=160&section=header&text=HTML%20FORMS&fontSize=34&fontColor=ffffff&animation=fadeIn&desc=Collect%20Information%20the%20Right%20Way&descSize=13" width="100%">
</p>

<h1 align="center"> MODULE 04: HTML FORMS</h1>

##  Introduction

Imagine creating a website where users can register, log in, send messages or search for information.

How would the website collect information from its users?

The answer is **HTML Forms**.

Forms allow users to enter information and submit it to an application or server.

## 🎯 Learning Objectives

By the end of this module, you should be able to:

- Explain what HTML forms are.
- Create form elements.
- Use different input types.
- Create dropdown menus.
- Use radio buttons and checkboxes.
- Apply basic HTML validation.
- Build a complete registration form.

---

##  1. What is an HTML Form?

An HTML form is a section of a web page that contains controls for collecting information.

Example:

```html
<form action="/register" method="post">

    <!-- Form controls go here -->

</form>
```

### Understanding the Attributes

| Attribute | Purpose |
|---|---|
| `action` | Specifies where form data is sent |
| `method` | Specifies how form data is submitted |
| `name` | Identifies a field in submitted form data |
| `required` | Makes a field mandatory |

The server endpoint must actually exist for the form to submit successfully.

---

##  2. Text Input

The text input allows users to enter ordinary text.

```html
<label for="fullname">Full Name:</label>

<input
    type="text"
    id="fullname"
    name="fullname"
>
```

---

## 3. Email Input

The email input is designed for email addresses.

```html
<label for="email">Email Address:</label>

<input
    type="email"
    id="email"
    name="email"
    required
>
```

The browser can check whether the entered value resembles an email address.

---

##  4. Password Input

Password inputs hide the characters entered by the user.

```html
<label for="password">Password:</label>

<input
    type="password"
    id="password"
    name="password"
    minlength="8"
    required
>
```

Remember: hiding characters in the browser does not encrypt the password. Secure password handling must be implemented by the application on the server.

---

##  5. Other Common Input Types

```html
<input type="number" name="age">

<input type="date" name="birthdate">

<input type="tel" name="phone">

<input type="url" name="website">

<input type="search" name="search">

<input type="time" name="meeting-time">

<input type="file" name="document">
```

Each input type is designed for a particular kind of information.

---

##  6. Radio Buttons

Radio buttons allow users to select one option from a group.

```html
<p>Select your gender:</p>

<label>
    <input type="radio" name="gender" value="male">
    Male
</label>

<label>
    <input type="radio" name="gender" value="female">
    Female
</label>
```

Radio buttons that belong to the same group share the same `name`.

For real forms, ensure the question and available options are appropriate for your users.

---

##  7. Checkboxes

Checkboxes allow users to select one or more options.

```html
<p>Select your interests:</p>

<label>
    <input type="checkbox" name="interest" value="coding">
    Coding
</label>

<label>
    <input type="checkbox" name="interest" value="design">
    Design
</label>

<label>
    <input type="checkbox" name="interest" value="technology">
    Technology
</label>
```

Unlike radio buttons, multiple checkboxes can be selected.

---

##  8. Dropdown Menus

Use `<select>` and `<option>` to create a dropdown menu.

```html
<label for="course">Choose a course:</label>

<select id="course" name="course">

    <option value="">Select a course</option>

    <option value="html">HTML</option>

    <option value="css">CSS</option>

    <option value="javascript">JavaScript</option>

</select>
```

---

##  9. Textarea

The `<textarea>` element allows users to enter longer messages.

```html
<label for="message">Your Message:</label>

<textarea
    id="message"
    name="message"
    rows="5"
    cols="30"
></textarea>
```

---

##  10. Buttons

HTML provides different button types.

```html
<button type="submit">Submit</button>

<button type="reset">Reset</button>

<button type="button">Click Me</button>
```

- `submit` submits the form.
- `reset` resets form controls to their initial values.
- `button` creates a button without automatic form submission behaviour.

---

##  11. Form Validation

Validation helps ensure users provide information in the expected format.

Example:

```html
<form>

    <label for="username">Username:</label>

    <input
        type="text"
        id="username"
        name="username"
        minlength="3"
        maxlength="20"
        required
    >

    <label for="email">Email:</label>

    <input
        type="email"
        id="email"
        name="email"
        required
    >

    <button type="submit">Register</button>

</form>
```

Common validation attributes:

| Attribute | Purpose |
|---|---|
| `required` | Field must be completed |
| `minlength` | Minimum text length |
| `maxlength` | Maximum text length |
| `min` | Minimum numerical value |
| `max` | Maximum numerical value |
| `pattern` | Matches a regular expression |

Client-side validation improves usability but does not replace server-side validation.

---

##  12. Complete Registration Form

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Student Registration</title>
</head>

<body>

    <h1>Student Registration</h1>

    <form action="#" method="get">

        <label for="name">Full Name:</label>

        <input
            type="text"
            id="name"
            name="name"
            required
        >

        <br><br>

        <label for="email">Email:</label>

        <input
            type="email"
            id="email"
            name="email"
            required
        >

        <br><br>

        <label for="password">Password:</label>

        <input
            type="password"
            id="password"
            name="password"
            minlength="8"
            required
        >

        <br><br>

        <label for="course">Course:</label>

        <select id="course" name="course">

            <option value="">Choose Course</option>

            <option value="html">HTML</option>

            <option value="css">CSS</option>

            <option value="javascript">JavaScript</option>

        </select>

        <br><br>

        <button type="submit">Register</button>

    </form>

</body>
</html>
```

This is a learning example. It does not store registrations or create accounts.

##  Practical Activity

Create a student registration form containing:

- Full name.
- Email address.
- Phone number.
- Password.
- Course selection.
- Preferred learning mode.
- Message field.
- Terms and conditions checkbox.
- Submit button.

##  Knowledge Check

1. What is the purpose of an HTML form?
2. What does the `action` attribute do?
3. What is the difference between radio buttons and checkboxes?
4. Which input type is used for email addresses?
5. What does the `required` attribute do?
6. Why should form fields have labels?

##  Module Challenge

Build a complete online course registration form.

Make sure every input has an appropriate label and the form is easy to understand.

##  Key Takeaways

- Forms collect information from users.
- Inputs come in different types.
- Labels make forms more accessible.
- Validation helps prevent incomplete or incorrectly formatted entries.
- Real applications need server-side processing and validation.

<p align="center"><strong> You now know how to collect information using HTML!</strong></p>
