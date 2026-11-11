
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=160&section=header&text=FETCH%20API&fontSize=36&fontColor=ffffff&animation=fadeIn&desc=Communicating%20With%20External%20APIs&descSize=14" width="100%">
</p>

<h1 align="center">FETCH API</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Fetch%20API-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000">
  <img src="https://img.shields.io/badge/LEVEL-INTERMEDIATE-2E86C1?style=for-the-badge">
  <img src="https://img.shields.io/badge/FOCUS-API%20INTEGRATION-239B56?style=for-the-badge">
</p>

## Welcome!

Welcome to the Fetch API lesson.

So far, you have learned how to write JavaScript programmes, work with variables, manipulate arrays and objects, handle events, and write asynchronous JavaScript using Promises and `async/await`.

However, most real-world applications need to communicate with external systems to retrieve, send, update and delete information.

For example:

- A weather application retrieves weather information from a weather service.
- An e-commerce website retrieves product information from a server.
- A social media application retrieves posts and user profiles.
- A banking application communicates with financial services.
- A student management system retrieves student records from a database through a backend API.

JavaScript provides a built-in tool called the **Fetch API** that allows applications to make HTTP requests and communicate with external resources.

In this lesson, you will learn how to use Fetch API to retrieve information, send data, update resources, delete resources and handle errors.

By the end of this lesson, you should be able to connect a JavaScript application to an external API and display the retrieved information on a webpage.

---

## Learning Objectives

By the end of this lesson, you should be able to:

- Explain what an API is.
- Understand how the Fetch API works.
- Explain the relationship between HTTP and APIs.
- Understand common HTTP request methods.
- Make GET requests using `fetch()`.
- Understand HTTP responses and status codes.
- Convert API responses into JSON.
- Display API data dynamically on a webpage.
- Send information using POST requests.
- Update information using PUT and PATCH requests.
- Delete information using DELETE requests.
- Handle API errors using `try...catch`.
- Use Fetch API with Promises.
- Use Fetch API with `async/await`.

---

# 1. What Is an API?

API stands for **Application Programming Interface**.

An API is a mechanism that allows different software applications to communicate and exchange information.

Consider a restaurant.

A customer does not enter the kitchen to prepare their own food. Instead, they place an order through a waiter.

The waiter communicates the order to the kitchen and brings the prepared food back to the customer.

An API works in a similar way.

A frontend application sends a request to an API. The API communicates with the appropriate backend system and returns a response.

### How an API Works

```text
Frontend Application
        |
        | Sends Request
        |
        v
      API
        |
        | Processes Request
        |
        v
   Backend Server
        |
        | Retrieves or Updates Data
        |
        v
     Database
        |
        | Returns Information
        |
        v
   Backend Server
        |
        v
      API
        |
        | Sends Response
        |
        v
Frontend Application
```

### Example

Imagine building an application that displays information about students.

Instead of manually writing every student record into your JavaScript file, your application can request student information from an API.

The API might return:

```json
[
    {
        "id": 1,
        "name": "Alex Morgan",
        "course": "Software Engineering",
        "age": 21
    },
    {
        "id": 2,
        "name": "Brian Smith",
        "course": "Computer Science",
        "age": 22
    }
]
```

Your JavaScript application can then process this information and display it on a webpage.

### Important Terms

| Term | Explanation |
|---|---|
| API | Allows software applications to communicate. |
| Client | The application making a request. |
| Server | The system receiving and processing requests. |
| Endpoint | A specific URL used to access a resource. |
| Request | A message sent by a client to a server. |
| Response | Information returned by a server. |
| HTTP | A protocol used for communication over the web. |
| JSON | A common format for exchanging data. |

---

# 2. What Is the Fetch API?

The Fetch API is a modern JavaScript interface used to make HTTP requests and retrieve resources from servers.

It allows JavaScript applications to:

- Retrieve information.
- Submit information.
- Update existing information.
- Delete information.

The main function is:

```javascript
fetch()
```

### Basic Syntax

```javascript
fetch(url)
    .then(response => {
        // Handle the response
    })
    .then(data => {
        // Process the returned data
    })
    .catch(error => {
        // Handle errors
    });
```

### Example

```javascript
fetch("https://jsonplaceholder.typicode.com/users")
    .then(response => response.json())
    .then(data => {
        console.log(data);
    })
    .catch(error => {
        console.log("Error:", error);
    });
```

### Explanation

1. `fetch()` sends a request to the specified URL.
2. The server processes the request.
3. The server returns a response.
4. `response.json()` converts the response body into JavaScript data.
5. The second `.then()` receives the converted data.
6. `.catch()` handles rejected requests and other errors in the Promise chain.

**Important:** `fetch()` returns a Promise. It does not immediately return the requested data.

---

# 3. Understanding HTTP Request Methods

When communicating with APIs, different HTTP methods are used to perform different operations.

The most common methods are:

| HTTP Method | Purpose |
|---|---|
| GET | Retrieve information. |
| POST | Create or submit information. |
| PUT | Replace an existing resource. |
| PATCH | Partially update an existing resource. |
| DELETE | Delete a resource. |

### 3.1 GET

GET is used to retrieve information from a server.

Example:

```javascript
fetch("https://jsonplaceholder.typicode.com/users")
    .then(response => response.json())
    .then(users => {
        console.log(users);
    });
```

This request retrieves a collection of users.

### 3.2 POST

POST is used to submit information to a server, commonly to create a new resource.

Example:

```javascript
const newUser = {
    name: "John Doe",
    email: "john@example.com",
    username: "johndoe"
};

fetch("https://jsonplaceholder.typicode.com/users", {

    method: "POST",

    headers: {
        "Content-Type": "application/json"
    },

    body: JSON.stringify(newUser)

})
.then(response => response.json())
.then(data => {
    console.log("User created:", data);
});
```

### Explanation

**method**

Specifies the HTTP request method.

**headers**

Provides additional information about the request.

**Content-Type**

Indicates that the request body contains JSON data.

**body**

Contains the information being sent to the server.

**JSON.stringify()**

Converts a JavaScript object into a JSON string.

### 3.3 PUT

PUT is commonly used to replace an existing resource.

Example:

```javascript
const updatedUser = {
    name: "John Updated",
    email: "johnupdated@example.com",
    username: "johnupdated"
};

fetch("https://jsonplaceholder.typicode.com/users/1", {

    method: "PUT",

    headers: {
        "Content-Type": "application/json"
    },

    body: JSON.stringify(updatedUser)

})
.then(response => response.json())
.then(data => {
    console.log("User replaced:", data);
});
```

### 3.4 PATCH

PATCH is used to update specific properties of an existing resource.

Example:

```javascript
const updatedDetails = {
    name: "John Updated"
};

fetch("https://jsonplaceholder.typicode.com/users/1", {

    method: "PATCH",

    headers: {
        "Content-Type": "application/json"
    },

    body: JSON.stringify(updatedDetails)

})
.then(response => response.json())
.then(data => {
    console.log("User updated:", data);
});
```

Unlike a typical PUT operation, PATCH is intended for partial updates.

### 3.5 DELETE

DELETE is used to request the removal of a resource.

Example:

```javascript
fetch("https://jsonplaceholder.typicode.com/users/1", {

    method: "DELETE"

})
.then(response => {

    if (response.ok) {
        console.log("User deleted successfully");
    }

});
```

### Important Note

JSONPlaceholder is a testing API.

It simulates create, update and delete operations but does not permanently modify its database.

The responses demonstrate how API requests work.

---

# 4. Understanding API Endpoints

An endpoint is a specific URL through which an application accesses a particular resource or performs an operation.

For example:

```text
https://jsonplaceholder.typicode.com/users
```

This endpoint retrieves users.

```text
https://jsonplaceholder.typicode.com/posts
```

This endpoint retrieves posts.

```text
https://jsonplaceholder.typicode.com/comments
```

This endpoint retrieves comments.

You can also access a specific resource by including its ID.

Example:

```text
https://jsonplaceholder.typicode.com/users/1
```

This endpoint retrieves the user whose ID is 1.

### Common API Endpoint Patterns

| Endpoint | Purpose |
|---|---|
| `/users` | Retrieve users. |
| `/users/1` | Retrieve one user. |
| `/posts` | Retrieve posts. |
| `/posts/1` | Retrieve one post. |
| `/comments` | Retrieve comments. |

### Understanding Query Parameters

Query parameters allow you to provide additional information when requesting data.

Example:

```javascript
fetch("https://jsonplaceholder.typicode.com/posts?userId=1")
    .then(response => response.json())
    .then(posts => {
        console.log(posts);
    });
```

The `userId=1` parameter requests posts associated with user 1.

A question mark `?` separates the endpoint from its query parameters.

Multiple parameters are separated using `&`.

Example:

```text
/posts?userId=1&_limit=5
```

---

# 5. Understanding JSON

JSON stands for **JavaScript Object Notation**.

It is a lightweight data format commonly used to exchange information between applications.

JSON is easy for humans to read and easy for programming languages to process.

### Example JSON Data

```json
{
    "id": 1,
    "name": "Alex Morgan",
    "age": 21,
    "course": "Software Engineering",
    "isEnrolled": true
}
```

JSON supports the following data types:

- Strings.
- Numbers.
- Booleans.
- Arrays.
- Objects.
- Null.

### JSON vs JavaScript Objects

JavaScript object:

```javascript
const student = {
    name: "Alex Morgan",
    age: 21,
    course: "Software Engineering"
};
```

JSON:

```json
{
    "name": "Alex Morgan",
    "age": 21,
    "course": "Software Engineering"
}
```

JSON property names and string values must use double quotation marks.

JSON does not support JavaScript functions, `undefined`, or comments.

### JSON.stringify()

Converts a JavaScript object into a JSON string.

```javascript
const student = {
    name: "Alex Morgan",
    age: 21
};

const jsonData = JSON.stringify(student);

console.log(jsonData);
```

### JSON.parse()

Converts a valid JSON string into a JavaScript value.

```javascript
const jsonData = '{"name":"Alex Morgan","age":21}';

const student = JSON.parse(jsonData);

console.log(student.name);
```

### Important Difference

| Method | Purpose |
|---|---|
| `JSON.stringify()` | JavaScript value to JSON string. |
| `JSON.parse()` | JSON string to JavaScript value. |
| `response.json()` | Reads and parses a response body as JSON. |

---

# 6. Understanding HTTP Responses

When an application sends a request to a server, the server returns a response.

The response contains information about the request, including its status.

### Common HTTP Status Codes

| Status Code | Meaning |
|---|---|
| 200 | OK. The request was successful. |
| 201 | Created. A resource was created. |
| 204 | No Content. The request succeeded without a response body. |
| 400 | Bad Request. The request was invalid. |
| 401 | Unauthorized. Authentication is required or invalid. |
| 403 | Forbidden. Access is not permitted. |
| 404 | Not Found. The requested resource does not exist. |
| 500 | Internal Server Error. The server encountered an error. |
| 503 | Service Unavailable. The server cannot currently handle the request. |

### Checking the Response

Example:

```javascript
fetch("https://jsonplaceholder.typicode.com/users")
    .then(response => {

        console.log(response.status);

        console.log(response.ok);

        return response.json();

    })
    .then(data => {
        console.log(data);
    });
```

### Understanding response.ok

The `response.ok` property returns:

- `true` for successful HTTP responses with status codes from 200 to 299.
- `false` for other HTTP status codes.

**Important:** Fetch does not automatically reject its Promise when the server responds with HTTP errors such as 404 or 500.

This means that you should explicitly check `response.ok`.

### Correct Error Checking

```javascript
fetch("https://jsonplaceholder.typicode.com/users")
    .then(response => {

        if (!response.ok) {
            throw new Error("Failed to retrieve users");
        }

        return response.json();

    })
    .then(data => {
        console.log(data);
    })
    .catch(error => {
        console.log(error.message);
    });
```

---

# 7. Retrieving Data Using GET

One of the most common uses of Fetch API is retrieving information from an external server.

Let's retrieve users from JSONPlaceholder.

API endpoint:

```text
https://jsonplaceholder.typicode.com/users
```

### Example

```javascript
fetch("https://jsonplaceholder.typicode.com/users")

    .then(response => response.json())

    .then(users => {

        console.log(users);

    })

    .catch(error => {

        console.log("Something went wrong:", error);

    });
```

### Understanding the Returned Data

The API returns an array of user objects.

Each object contains information such as:

- ID.
- Name.
- Username.
- Email.
- Address.
- Phone.
- Website.
- Company.

You can access individual properties using dot notation.

Example:

```javascript
fetch("https://jsonplaceholder.typicode.com/users")

    .then(response => response.json())

    .then(users => {

        console.log(users[0].name);

        console.log(users[0].email);

        console.log(users[0].phone);

    });
```

### Explanation

- `users[0]` accesses the first user.
- `.name` retrieves the user's name.
- `.email` retrieves the user's email.
- `.phone` retrieves the user's phone number.

Remember that array indexing begins at zero.

---

# 8. Displaying API Data on a Webpage

Retrieving information from an API is useful, but most applications need to display that information to users.

We can combine Fetch API with DOM manipulation to create dynamic interfaces.

### Step 1: Create the HTML File

Create an `index.html` file.

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>User Directory</title>

    <link rel="stylesheet" href="style.css">
</head>

<body>

    <header>
        <h1>User Directory</h1>

        <p>Information retrieved from an external API.</p>
    </header>

    <main>

        <button id="loadUsers">
            Load Users
        </button>

        <p id="status"></p>

        <section id="usersContainer"></section>

    </main>

    <script src="script.js"></script>

</body>

</html>
```

### Step 2: Create the CSS File

Create a `style.css` file.

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background: #f4f6f8;
    padding: 30px;
}

header {
    text-align: center;
    margin-bottom: 30px;
}

header h1 {
    margin-bottom: 10px;
}

button {
    padding: 12px 20px;
    border: none;
    background: #243b55;
    color: white;
    cursor: pointer;
    border-radius: 5px;
    margin-bottom: 20px;
}

#usersContainer {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
}

.user-card {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
}

.user-card h2 {
    margin-bottom: 10px;
}

.user-card p {
    margin-bottom: 8px;
    color: #555;
}
```

### Step 3: Create the JavaScript File

Create a `script.js` file.

```javascript
const usersContainer = document.querySelector("#usersContainer");

const loadUsersButton = document.querySelector("#loadUsers");

const statusMessage = document.querySelector("#status");


function fetchUsers() {

    statusMessage.textContent = "Loading users...";

    usersContainer.innerHTML = "";

    fetch("https://jsonplaceholder.typicode.com/users")

        .then(response => {

            if (!response.ok) {
                throw new Error("Unable to retrieve users");
            }

            return response.json();

        })

        .then(users => {

            statusMessage.textContent = `${users.length} users retrieved successfully.`;

            users.forEach(user => {

                const userCard = document.createElement("div");

                userCard.classList.add("user-card");

                userCard.innerHTML = `
                    <h2>${user.name}</h2>

                    <p>Email: ${user.email}</p>

                    <p>Phone: ${user.phone}</p>

                    <p>Company: ${user.company.name}</p>
                `;

                usersContainer.appendChild(userCard);

            });

        })

        .catch(error => {

            statusMessage.textContent = error.message;

            console.log(error);

        });

}


loadUsersButton.addEventListener("click", fetchUsers);
```

### Explanation

**Selecting HTML elements**

```javascript
const usersContainer = document.querySelector("#usersContainer");
```

Selects the HTML element where user information will be displayed.

**Creating a function**

```javascript
function fetchUsers() {
    // Fetch operation
}
```

Creates a reusable function that retrieves user information.

**Displaying loading information**

```javascript
statusMessage.textContent = "Loading users...";
```

Provides feedback while the request is being processed.

**Making the API request**

```javascript
fetch("https://jsonplaceholder.typicode.com/users")
```

Sends a GET request to the API.

**Converting the response**

```javascript
return response.json();
```

Reads and parses the response body as JSON.

**Looping through users**

```javascript
users.forEach(user => {
    // Display each user
});
```

Processes every user returned by the API.

**Creating HTML elements**

```javascript
const userCard = document.createElement("div");
```

Creates a new HTML element for each user.

**Appending elements**

```javascript
usersContainer.appendChild(userCard);
```

Adds each user card to the webpage.

**Handling errors**

```javascript
.catch(error => {
    console.log(error);
});
```

Handles errors in the Promise chain.

**Handling button clicks**

```javascript
loadUsersButton.addEventListener("click", fetchUsers);
```

Calls the `fetchUsers()` function when the user clicks the button.

### Security Consideration

The example uses `innerHTML` to display information returned by the API.

When displaying untrusted or user-generated data, prefer creating elements and assigning text using `textContent`. This helps prevent cross-site scripting (XSS) vulnerabilities.

---

# 9. Using Fetch API with Async and Await

In the previous lessons, you learned how to use `async` and `await` to write asynchronous JavaScript.

Fetch API works naturally with these features.

Instead of writing multiple `.then()` methods, you can use `await` to make asynchronous code easier to read.

### Example

```javascript
async function fetchUsers() {

    try {

        const response = await fetch(
            "https://jsonplaceholder.typicode.com/users"
        );

        if (!response.ok) {
            throw new Error("Failed to retrieve users");
        }

        const users = await response.json();

        console.log(users);

    } catch (error) {

        console.log("Error:", error.message);

    }

}

fetchUsers();
```

### Explanation

**async**

```javascript
async function fetchUsers() {
}
```

Declares an asynchronous function.

An async function always returns a Promise.

**await**

```javascript
const response = await fetch(url);
```

Waits for the Fetch API Promise to settle before continuing execution inside the async function.

**Response conversion**

```javascript
const users = await response.json();
```

Waits for the response body to be read and parsed.

**try...catch**

```javascript
try {
    // Request operation
} catch (error) {
    // Error handling
}
```

Allows you to handle errors that occur during the awaited operations.

### Why Use Async and Await?

| Promise Chaining | Async and Await |
|---|---|
| Uses `.then()`. | Uses `await`. |
| Uses `.catch()`. | Commonly uses `try...catch`. |
| Can become difficult to read when deeply chained. | Often easier to follow sequentially. |
| Returns a Promise. | Async functions return a Promise. |

Both approaches are valid.

---

# 10. Sending Data Using POST

So far, we have focused on retrieving information.

However, applications also need to send information to servers.

For example:

- Registering a new user.
- Submitting a contact form.
- Creating a product.
- Publishing a post.
- Recording an order.

POST requests are commonly used for these operations.

### Example: Creating a New Post

```javascript
async function createPost() {

    const newPost = {

        title: "Learning JavaScript",

        body: "I am learning how to communicate with APIs.",

        userId: 1

    };

    try {

        const response = await fetch(
            "https://jsonplaceholder.typicode.com/posts",
            {

                method: "POST",

                headers: {
                    "Content-Type": "application/json"
                },

                body: JSON.stringify(newPost)

            }
        );

        if (!response.ok) {
            throw new Error("Failed to create post");
        }

        const data = await response.json();

        console.log("Post created:", data);

    } catch (error) {

        console.log("Error:", error.message);

    }

}

createPost();
```

### Understanding the Request Configuration

```javascript
{
    method: "POST",

    headers: {
        "Content-Type": "application/json"
    },

    body: JSON.stringify(newPost)
}
```

| Property | Purpose |
|---|---|
| `method` | Specifies the HTTP method. |
| `headers` | Provides request metadata. |
| `Content-Type` | Indicates the format of the request body. |
| `body` | Contains the information being submitted. |
| `JSON.stringify()` | Converts the JavaScript object into JSON text. |

---

# 11. Updating and Deleting Information

Applications frequently need to update existing records or remove information.

### Updating Information Using PATCH

```javascript
async function updatePost() {

    const updatedPost = {
        title: "Understanding Fetch API"
    };

    try {

        const response = await fetch(
            "https://jsonplaceholder.typicode.com/posts/1",
            {

                method: "PATCH",

                headers: {
                    "Content-Type": "application/json"
                },

                body: JSON.stringify(updatedPost)

            }
        );

        if (!response.ok) {
            throw new Error("Failed to update post");
        }

        const data = await response.json();

        console.log("Updated post:", data);

    } catch (error) {

        console.log(error.message);

    }

}

updatePost();
```

### Deleting Information Using DELETE

```javascript
async function deletePost() {

    try {

        const response = await fetch(
            "https://jsonplaceholder.typicode.com/posts/1",
            {
                method: "DELETE"
            }
        );

        if (!response.ok) {
            throw new Error("Failed to delete post");
        }

        console.log("Post deleted successfully");

    } catch (error) {

        console.log(error.message);

    }

}

deletePost();
```

### Important Note

A DELETE response may have no body, particularly when the server returns status `204`.

Do not automatically call `response.json()` after every request. Check whether the response contains a body before trying to parse it.

---

# 12. Handling API Errors

API requests can fail for several reasons.

Examples include:

- No internet connection.
- Incorrect API endpoint.
- Server unavailable.
- Invalid request data.
- Authentication failure.
- Access restrictions.
- Resource not found.
- Unexpected response format.

A professional application should handle these situations appropriately.

### Example

```javascript
async function fetchUsers() {

    try {

        const response = await fetch(
            "https://jsonplaceholder.typicode.com/users"
        );

        if (!response.ok) {

            throw new Error(
                `HTTP Error: ${response.status}`
            );

        }

        const users = await response.json();

        console.log(users);

    } catch (error) {

        console.log("Request failed:", error.message);

    }

}

fetchUsers();
```

### Types of Errors

| Error | Possible Cause |
|---|---|
| Network error | Connection unavailable or request blocked. |
| 400 | Invalid request. |
| 401 | Missing or invalid authentication. |
| 403 | Access denied. |
| 404 | Resource does not exist. |
| 500 | Server-side failure. |
| JSON parsing error | Response body is not valid JSON. |

### Important Distinction

Fetch generally rejects its Promise for network-level failures, but not simply because the server returned an unsuccessful HTTP status.

That is why checking `response.ok` is important.

---

# 13. Understanding Loading States

When an application requests information from a server, the response may take some time.

During this period, users should receive feedback.

A loading state tells users that the application is processing their request.

### Example

```javascript
async function loadProducts() {

    const container = document.querySelector("#products");

    const status = document.querySelector("#status");

    status.textContent = "Loading products...";

    try {

        const response = await fetch(
            "https://dummyjson.com/products"
        );

        if (!response.ok) {
            throw new Error("Unable to load products");
        }

        const data = await response.json();

        status.textContent = "";

        data.products.forEach(product => {

            const productElement = document.createElement("div");

            productElement.textContent = product.title;

            container.appendChild(productElement);

        });

    } catch (error) {

        status.textContent = error.message;

    }

}
```

### Recommended API Interface States

A good API-powered application should account for:

1. Initial state: No request has been made.
2. Loading state: The request is in progress.
3. Success state: Information has been retrieved.
4. Empty state: No matching information exists.
5. Error state: The request has failed.

These states improve the usability of an application.

---

# 14. Working with API Data and Array Methods

API responses often contain arrays of objects.

You can use the array methods learned in previous lessons to process the returned information.

Consider this example:

```javascript
const products = [
    {
        id: 1,
        title: "Laptop",
        price: 75000,
        category: "Electronics"
    },

    {
        id: 2,
        title: "Mouse",
        price: 1500,
        category: "Accessories"
    },

    {
        id: 3,
        title: "Keyboard",
        price: 3000,
        category: "Accessories"
    },

    {
        id: 4,
        title: "Monitor",
        price: 25000,
        category: "Electronics"
    }
];
```

### Using map()

Retrieve product names.

```javascript
const productNames = products.map(product => {
    return product.title;
});

console.log(productNames);
```

### Using filter()

Retrieve products that cost more than KES 5,000.

```javascript
const expensiveProducts = products.filter(product => {
    return product.price > 5000;
});

console.log(expensiveProducts);
```

### Using find()

Find the product with ID 2.

```javascript
const selectedProduct = products.find(product => {
    return product.id === 2;
});

console.log(selectedProduct);
```

### Using reduce()

Calculate the total value of all products.

```javascript
const totalValue = products.reduce((total, product) => {

    return total + product.price;

}, 0);

console.log(totalValue);
```

### Using some()

Check whether any product costs more than KES 50,000.

```javascript
const hasExpensiveProduct = products.some(product => {
    return product.price > 50000;
});

console.log(hasExpensiveProduct);
```

### Using every()

Check whether all products have a positive price.

```javascript
const allHavePrices = products.every(product => {
    return product.price > 0;
});

console.log(allHavePrices);
```

---

# 15. Working with API Documentation

Before integrating an external API, developers should read its documentation.

API documentation explains how an API works and how developers should interact with it.

Documentation commonly provides:

- Available endpoints.
- HTTP methods.
- Required request headers.
- Authentication requirements.
- Request parameters.
- Request body structure.
- Response examples.
- Status codes.
- Rate limits.
- Error descriptions.

### Example: JSONPlaceholder

JSONPlaceholder is a free fake REST API used for learning and testing.

Website:

https://jsonplaceholder.typicode.com/

Available resources include:

| Resource | Endpoint |
|---|---|
| Posts | `/posts` |
| Comments | `/comments` |
| Albums | `/albums` |
| Photos | `/photos` |
| Todos | `/todos` |
| Users | `/users` |

### Example: DummyJSON

DummyJSON provides sample data for practising API integration.

Website:

https://dummyjson.com/

Available resources include:

| Resource | Endpoint |
|---|---|
| Products | `/products` |
| Users | `/users` |
| Posts | `/posts` |
| Comments | `/comments` |
| Carts | `/carts` |
| Recipes | `/recipes` |

### Recommended API Learning Resources

1. [MDN Fetch API Documentation](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
2. [MDN Using the Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)
3. [JSONPlaceholder](https://jsonplaceholder.typicode.com/)
4. [DummyJSON](https://dummyjson.com/)
5. [HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status)

---

# 16. Important API Security Practices

When working with APIs, security should always be considered.

### 1. Protect API Keys

Some APIs require API keys.

Do not expose secret API keys in frontend JavaScript.

Frontend code is accessible to users through their browsers.

Sensitive credentials should be stored and used on a secure backend.

### 2. Validate User Input

Always validate information before sending it to an API.

For example, verify that:

- Required fields are not empty.
- Email addresses are valid.
- Numeric values are within acceptable limits.
- User input follows the expected format.

### 3. Handle Errors

Do not assume every request will succeed.

Use appropriate error handling and provide useful feedback.

### 4. Use HTTPS

Use HTTPS endpoints when communicating with external services.

HTTPS encrypts communication between the client and server.

### 5. Avoid Exposing Sensitive Information

Do not display private information such as passwords, access tokens or confidential records in the browser console or user interface.

### 6. Avoid Trusting External Data

Data received from an API should be treated as external input.

Validate and safely display it, particularly when inserting information into the DOM.

---

# 17. Practical Activities

The following activities will help you apply the Fetch API concepts covered in this lesson.

## Activity 1: Retrieve Users

Using:

```text
https://jsonplaceholder.typicode.com/users
```

Write a JavaScript programme that:

1. Retrieves all users.
2. Displays the users in the console.
3. Displays the name of the first user.
4. Displays the email address of the last user.
5. Displays the total number of users.

## Activity 2: Retrieve Posts

Using:

```text
https://jsonplaceholder.typicode.com/posts
```

Write a programme that:

1. Retrieves all posts.
2. Displays the post titles.
3. Displays the total number of posts.
4. Retrieves posts belonging to user ID 1.
5. Displays the first five posts.

## Activity 3: Create a New Post

Use:

```text
https://jsonplaceholder.typicode.com/posts
```

Create a POST request containing:

- Title.
- Body.
- User ID.

Display the returned response.

## Activity 4: Update an Existing Post

Update post ID 1 using PATCH.

Change its title and display the updated response.

## Activity 5: Delete a Post

Send a DELETE request for post ID 1.

Check the response and display an appropriate success or failure message.

## Activity 6: Build a User Directory

Create a webpage that:

1. Retrieves users from an external API.
2. Displays each user in a card.
3. Displays their name, email and phone number.
4. Includes a loading message.
5. Includes an error message.
6. Provides a reload button.
7. Uses CSS to style the interface.

## Activity 7: Build a Product Catalogue

Using:

```text
https://dummyjson.com/products
```

Build a product catalogue that displays:

- Product image.
- Product title.
- Product description.
- Product price.
- Product rating.

Add the following functionality:

1. Search for a product.
2. Filter products by category.
3. Sort products by price.
4. Display the total number of products.
5. Handle API errors.

---

# 18. Knowledge Check

Test your understanding of the Fetch API.

**1. What does API stand for?**

**2. What is the purpose of the Fetch API?**

**3. What does `fetch()` return?**

**4. Which HTTP method is commonly used to retrieve information?**

**5. Which HTTP method is commonly used to create a resource?**

**6. What is the difference between PUT and PATCH?**

**7. What is the purpose of `JSON.stringify()`?**

**8. What does `response.json()` do?**

**9. What does `response.ok` indicate?**

**10. Why does Fetch API not automatically reject its Promise for a 404 response?**

**11. What is an API endpoint?**

**12. What is the purpose of HTTP headers?**

**13. Why is `JSON.stringify()` used when sending JavaScript objects in a JSON request body?**

**14. What is the difference between a network error and an HTTP error response?**

**15. Why should API requests include error handling?**

**16. What is the purpose of `async` and `await` when working with Fetch API?**

**17. What does HTTP status code 404 mean?**

**18. What is the purpose of a loading state?**

**19. Why should secret API keys not be placed in frontend JavaScript?**

**20. What is the difference between retrieving data from an API and displaying data in the DOM?**

---

# 19. Module Challenge

## Project: API-Powered E-Commerce Product Catalogue

### Project Overview

Build an interactive e-commerce product catalogue that retrieves product information from an external API and displays it to users.

The application should simulate the product browsing experience of a real online shopping platform.

Use the following API:

```text
https://dummyjson.com/products
```

### Functional Requirements

Your application must support the following features.

### 1. Product Display

Retrieve products from the API and display:

- Product image.
- Product name.
- Product description.
- Product price.
- Product rating.
- Product category.

### 2. Search Functionality

Allow users to search for products by name.

The results should update based on the search term.

### 3. Category Filtering

Allow users to filter products by category.

### 4. Sorting

Allow users to sort products by:

- Price: Lowest to Highest.
- Price: Highest to Lowest.
- Name: A to Z.

### 5. Shopping Cart

Allow users to:

- Add products to a cart.
- Remove products from the cart.
- View selected products.
- View the total number of items.
- Calculate the total cart value.

### 6. Loading State

Display a loading message while retrieving products.

### 7. Error Handling

Display an appropriate error message if:

- The API is unavailable.
- The request fails.
- The response is unsuccessful.
- No matching products are found.

### 8. User Interface

The application should have:

- A navigation bar.
- A search field.
- A category filter.
- A sorting option.
- A product grid.
- Product cards.
- A shopping cart section.

### Technical Requirements

Your application must demonstrate the use of:

- Fetch API.
- GET requests.
- Promises.
- Async and await.
- HTTP response handling.
- JSON.
- Arrays and objects.
- Array methods.
- DOM manipulation.
- Event listeners.
- Functions.
- Conditional statements.
- Error handling.

### Suggested Project Structure

```text
ecommerce-catalogue/
│
├── index.html
│
├── style.css
│
├── script.js
│
├── assets/
│   └── images/
│
└── README.md
```

### Assessment Criteria

| Evaluation Area | Weight |
|---|---:|
| API Integration | 20% |
| Product Display | 15% |
| Search and Filtering | 15% |
| Shopping Cart | 15% |
| DOM Manipulation | 10% |
| Error Handling | 10% |
| Code Organisation | 5% |
| User Interface | 10% |
| **Total** | **100%** |

### Submission Requirements

Submit:

1. A GitHub repository.
2. Complete source code.
3. A README.md file.
4. Screenshots of the application.
5. A description of the implemented features.
6. Instructions for running the application.

---

# 20. Key Takeaways

In this lesson, you learned that:

- APIs allow different software applications to communicate.
- Fetch API allows JavaScript to make HTTP requests.
- `fetch()` returns a Promise.
- GET retrieves information.
- POST submits information.
- PUT replaces a resource.
- PATCH partially updates a resource.
- DELETE requests the removal of a resource.
- JSON is a common format for exchanging information.
- `response.json()` reads and parses JSON response data.
- `response.ok` helps identify unsuccessful HTTP responses.
- `async` and `await` simplify asynchronous code.
- `try...catch` helps manage errors.
- Fetch API can be combined with DOM manipulation to create dynamic applications.
- API documentation is essential when integrating external services.
- API security and input validation are important in real-world applications.

---

# Congratulations!

You have completed the JavaScript Fundamentals lesson on Fetch API.

You can now make HTTP requests, retrieve external information, submit data to servers and display API responses in a webpage.

This is an important step towards building real-world frontend applications.

You are now ready to move beyond static webpages and develop applications that communicate with external services.

<p align="center">
  <strong>Keep building. Keep experimenting. Keep engineering.</strong>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:141e30,100:243b55&height=100&section=footer&text=END%20OF%20JAVASCRIPT%20FUNDAMENTALS&fontSize=18&fontColor=ffffff" width="100%">
</p>
