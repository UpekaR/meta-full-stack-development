# JavaScript, Node.js & NPM Notes

Learn JavaScript from beginner level to advanced concepts, including browser JavaScript, Node.js, NPM, and project-ready coding skills.

---

## Table of Contents

1. What is JavaScript?
2. JavaScript in Web Development
3. Running JavaScript
4. Variables
5. Data Types
6. Operators
7. Conditional Statements
8. Loops
9. Functions
10. Arrays
11. Objects
12. Strings
13. DOM Basics
14. Events
15. Error Handling
16. Modern JavaScript
17. Asynchronous JavaScript
18. JSON
19. Node.js
20. NPM
21. package.json
22. GitHub Notes
23. Mini Practice Tasks
24. Quick Revision

---

# 1. What is JavaScript?

JavaScript is a programming language used to make websites interactive and dynamic.

HTML creates the structure of a webpage.  
CSS controls the design and layout.  
JavaScript controls the behavior.

Example:

```javascript
console.log("Hello, JavaScript!");
```

Output:

```text
Hello, JavaScript!
```

JavaScript can be used for:

- Interactive websites
- Web applications
- Form validation
- Buttons and menus
- Games
- APIs
- Servers with Node.js
- React applications
- Full-stack development

---

# 2. JavaScript in Web Development

A simple way to remember the role of each language:

| Technology | Role |V
|---|---|
| HTML | Structure |
| CSS | Style |
| JavaScript | Behavior |

Example:

```html
<button onclick="alert('Hello!')">Click Me</button>
```

When the button is clicked, JavaScript runs and shows an alert.

---

# 3. Running JavaScript

JavaScript can run in different places.

## 3.1 In the Browser Console

Open browser developer tools:

```text
Right click → Inspect → Console
```

Then type:

```javascript
console.log("JavaScript is working!");
```

## 3.2 Inside HTML

```html
<!DOCTYPE html>
<html>
<head>
    <title>JavaScript Practice</title>
</head>
<body>
    <h1>Hello JavaScript</h1>

    <script>
        console.log("JavaScript inside HTML");
    </script>
</body>
</html>
```

## 3.3 External JavaScript File

HTML file:

```html
<script src="script.js"></script>
```

JavaScript file:

```javascript
console.log("External JavaScript file connected!");
```

## 3.4 With Node.js

Node.js allows JavaScript to run outside the browser.

```bash
node app.js
```

---

# 4. Variables

Variables are used to store data.

JavaScript has three main ways to declare variables:

```javascript
var oldWay = "Not recommended much now";
let changeableValue = "Can change";
const fixedValue = "Cannot change";
```

## 4.1 var

`var` is the old way of creating variables.

```javascript
var city = "Riga";
console.log(city);
```

## 4.2 let

`let` is used when the value can change.

```javascript
let age = 25;
age = 26;

console.log(age);
```

## 4.3 const

`const` is used when the value should stay the same.

```javascript
const birthYear = 1999;
console.log(birthYear);
```

## Simple Rule

| Keyword | Can Change? | Modern Use |
|---|---:|---|
| var | Yes | Avoid when possible |
| let | Yes | Use for changing values |
| const | No | Use by default |

---

# 5. Data Types

Data types describe what kind of value a variable stores.

## 5.1 String

A string is text.

```javascript
let name = "Upeka";
let course = "JavaScript";
```

## 5.2 Number

A number can be whole or decimal.

```javascript
let age = 25;
let price = 12.99;
```

## 5.3 Boolean

Boolean values are either `true` or `false`.

```javascript
let isStudent = true;
let isFinished = false;
```

## 5.4 Undefined

A variable is `undefined` when it has been declared but no value has been assigned.

```javascript
let job;
console.log(job);
```

## 5.5 Null

`null` means intentionally empty.

```javascript
let selectedItem = null;
```

## 5.6 Array

An array stores multiple values in one variable.

```javascript
let colors = ["Red", "Blue", "Green"];
```

## 5.7 Object

An object stores related data using key-value pairs.

```javascript
let student = {
    name: "Upeka",
    age: 25,
    country: "Sri Lanka"
};
```

---

# 6. Operators

Operators are symbols used to perform actions.

## 6.1 Arithmetic Operators

```javascript
let a = 10;
let b = 3;

console.log(a + b); // Addition
console.log(a - b); // Subtraction
console.log(a * b); // Multiplication
console.log(a / b); // Division
console.log(a % b); // Remainder
```

## 6.2 Assignment Operators

```javascript
let score = 10;

score += 5;  // score = score + 5
score -= 2;  // score = score - 2
score *= 3;  // score = score * 3
score /= 2;  // score = score / 2
```

## 6.3 Comparison Operators

```javascript
console.log(5 > 3);
console.log(5 < 3);
console.log(5 >= 5);
console.log(5 <= 4);
console.log(5 == "5");
console.log(5 === "5");
```

Important difference:

```text
==  checks only value
=== checks value and data type
```

Example:

```javascript
console.log(5 == "5");  // true
console.log(5 === "5"); // false
```

## 6.4 Logical Operators

```javascript
&&  // AND
||  // OR
!   // NOT
```

Example:

```javascript
let age = 20;
let hasID = true;

if (age >= 18 && hasID) {
    console.log("Allowed");
}
```

Meaning:

| Operator | Meaning | Example |
|---|---|---|
| `&&` | AND | Both conditions must be true |
| `||` | OR | At least one condition must be true |
| `!` | NOT | Reverses true/false |

---

# 7. Conditional Statements

Conditional statements allow the program to make decisions.

## 7.1 if Statement

```javascript
let age = 18;

if (age >= 18) {
    console.log("You are an adult.");
}
```

## 7.2 if...else Statement

```javascript
let marks = 45;

if (marks >= 50) {
    console.log("Pass");
} else {
    console.log("Fail");
}
```

## 7.3 else if Statement

```javascript
let marks = 75;

if (marks >= 90) {
    console.log("Grade A");
} else if (marks >= 75) {
    console.log("Grade B");
} else if (marks >= 50) {
    console.log("Grade C");
} else {
    console.log("Fail");
}
```

## 7.4 switch Statement

A `switch` statement is useful when checking many possible values.

```javascript
let day = "Monday";

switch (day) {
    case "Monday":
        console.log("Start of the week");
        break;

    case "Friday":
        console.log("Almost weekend");
        break;

    default:
        console.log("Normal day");
}
```

---

# 8. Loops

Loops repeat code.

## 8.1 for Loop

Used when we know how many times we want to repeat.

```javascript
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```

## 8.2 while Loop

Used when repetition depends on a condition.

```javascript
let count = 1;

while (count <= 5) {
    console.log(count);
    count++;
}
```

## 8.3 do...while Loop

Runs the code at least once before checking the condition.

```javascript
let number = 1;

do {
    console.log(number);
    number++;
} while (number <= 5);
```

## 8.4 Looping Through an Array

```javascript
let languages = ["HTML", "CSS", "JavaScript"];

for (let i = 0; i < languages.length; i++) {
    console.log(languages[i]);
}
```

---

# 9. Functions

Functions are reusable blocks of code.

## 9.1 Basic Function

```javascript
function greet() {
    console.log("Hello!");
}

greet();
```

## 9.2 Function with Parameters

```javascript
function greetUser(name) {
    console.log("Hello " + name);
}

greetUser("Upeka");
```

## 9.3 Function with Return Value

```javascript
function add(a, b) {
    return a + b;
}

let result = add(5, 3);
console.log(result);
```

## 9.4 Arrow Function

Arrow functions are a modern way to write functions.

```javascript
const greet = () => {
    console.log("Hello from arrow function!");
};

greet();
```

Short version:

```javascript
const multiply = (a, b) => a * b;

console.log(multiply(4, 5));
```

---

# 10. Arrays

Arrays store multiple values.

```javascript
let fruits = ["Apple", "Banana", "Mango"];
```

Array index starts from `0`.

```javascript
console.log(fruits[0]); // Apple
console.log(fruits[1]); // Banana
```

## 10.1 Common Array Methods

```javascript
let fruits = ["Apple", "Banana"];

fruits.push("Mango");      // Adds to end
fruits.pop();              // Removes from end
fruits.unshift("Orange");  // Adds to beginning
fruits.shift();            // Removes from beginning

console.log(fruits);
```

## 10.2 Useful Array Methods

| Method | Meaning |
|---|---|
| `push()` | Add item to end |
| `pop()` | Remove item from end |
| `unshift()` | Add item to beginning |
| `shift()` | Remove item from beginning |
| `includes()` | Check if item exists |
| `indexOf()` | Find item position |
| `length` | Get number of items |

Example:

```javascript
let colors = ["Red", "Blue", "Green"];

console.log(colors.includes("Blue"));
console.log(colors.indexOf("Green"));
console.log(colors.length);
```

---

# 11. Objects

Objects store related information using key-value pairs.

```javascript
let student = {
    name: "Upeka",
    age: 25,
    course: "Meta Web Development",
    country: "Sri Lanka"
};
```

## 11.1 Access Object Values

```javascript
console.log(student.name);
console.log(student["course"]);
```

## 11.2 Update Object Values

```javascript
student.age = 26;
console.log(student.age);
```

## 11.3 Add New Property

```javascript
student.goal = "Become a software developer";
console.log(student);
```

## 11.4 Array of Objects

This is common in real projects.

```javascript
let students = [
    {
        name: "Upeka",
        course: "JavaScript"
    },
    {
        name: "Anna",
        course: "React"
    }
];

console.log(students[0].name);
```

---

# 12. Strings

Strings are text values.

```javascript
let message = "JavaScript is powerful";
```

## 12.1 String Properties and Methods

```javascript
let text = "Hello JavaScript";

console.log(text.length);
console.log(text.toUpperCase());
console.log(text.toLowerCase());
console.log(text.includes("JavaScript"));
console.log(text.replace("Hello", "Hi"));
```

## 12.2 Template Literals

Template literals use backticks.

```javascript
let name = "Upeka";
let course = "JavaScript";

console.log(`My name is ${name} and I am learning ${course}.`);
```

Template literals are cleaner than using `+`.

Old way:

```javascript
console.log("My name is " + name + " and I am learning " + course);
```

Modern way:

```javascript
console.log(`My name is ${name} and I am learning ${course}`);
```

---

# 13. DOM Basics

DOM means Document Object Model.

The DOM allows JavaScript to access and change HTML elements.

## 13.1 Select an Element

```javascript
let title = document.querySelector("h1");
```

## 13.2 Change Text

```javascript
title.textContent = "New Heading";
```

## 13.3 Change Style

```javascript
title.style.color = "blue";
```

## 13.4 Select by ID

HTML:

```html
<h1 id="main-title">Hello</h1>
```

JavaScript:

```javascript
let heading = document.querySelector("#main-title");
heading.textContent = "Updated Title";
```

## 13.5 Select by Class

HTML:

```html
<p class="message">Welcome</p>
```

JavaScript:

```javascript
let message = document.querySelector(".message");
message.textContent = "Welcome to JavaScript!";
```

---

# 14. Events

Events happen when users interact with a webpage.

Common events:

| Event | Meaning |
|---|---|
| `click` | User clicks something |
| `mouseover` | Mouse goes over an element |
| `keydown` | User presses a key |
| `submit` | Form is submitted |
| `change` | Input value changes |

Example:

```html
<button id="btn">Click Me</button>
```

```javascript
let button = document.querySelector("#btn");

button.addEventListener("click", () => {
    alert("Button clicked!");
});
```

---

# 15. Error Handling

Errors can happen when code runs.

JavaScript uses `try...catch` to handle errors safely.

```javascript
try {
    let result = riskyFunction();
    console.log(result);
} catch (error) {
    console.log("Something went wrong.");
    console.log(error);
}
```

Why this matters:

```text
Without error handling: the program may crash.
With error handling: the program can respond safely.
```

---

# 16. Modern JavaScript

Modern JavaScript includes features that make code cleaner and easier to write.

## 16.1 Spread Operator

The spread operator expands or copies arrays and objects.

```javascript
let numbers = [1, 2, 3];
let newNumbers = [...numbers, 4, 5];

console.log(newNumbers);
```

Output:

```text
[1, 2, 3, 4, 5]
```

## 16.2 Rest Operator

The rest operator collects many values into one array.

```javascript
function addNumbers(...numbers) {
    console.log(numbers);
}

addNumbers(1, 2, 3, 4);
```

Output:

```text
[1, 2, 3, 4]
```

## 16.3 Destructuring

Destructuring extracts values from arrays or objects.

Object example:

```javascript
let user = {
    name: "Upeka",
    age: 25
};

let { name, age } = user;

console.log(name);
console.log(age);
```

Array example:

```javascript
let colors = ["Red", "Blue", "Green"];

let [firstColor, secondColor] = colors;

console.log(firstColor);
console.log(secondColor);
```

---

# 17. Asynchronous JavaScript

JavaScript usually runs line by line.

Asynchronous JavaScript allows code to wait for tasks like:

- API requests
- Loading data
- Timers
- Database responses

## 17.1 setTimeout

```javascript
setTimeout(() => {
    console.log("This message appears after 2 seconds");
}, 2000);
```

## 17.2 Promises

A Promise represents a future result.

```javascript
let promise = new Promise((resolve, reject) => {
    let success = true;

    if (success) {
        resolve("Task completed");
    } else {
        reject("Task failed");
    }
});

promise
    .then((message) => {
        console.log(message);
    })
    .catch((error) => {
        console.log(error);
    });
```

## 17.3 async and await

`async` and `await` make asynchronous code easier to read.

```javascript
async function getData() {
    let response = await fetch("https://api.example.com/data");
    let data = await response.json();

    console.log(data);
}
```

---

# 18. JSON

JSON means JavaScript Object Notation.

It is used to store and exchange data.

Example JavaScript object:

```javascript
let user = {
    name: "Upeka",
    age: 25
};
```

Convert object to JSON string:

```javascript
let jsonData = JSON.stringify(user);
console.log(jsonData);
```

Convert JSON string back to object:

```javascript
let objectData = JSON.parse(jsonData);
console.log(objectData);
```

JSON is commonly used when working with APIs.

---

# 19. Node.js

Node.js allows JavaScript to run outside the browser.

With Node.js, JavaScript can be used for:

- Back-end development
- APIs
- Servers
- File handling
- Automation
- Command-line tools

## 19.1 Check Node.js Version

```bash
node -v
```

## 19.2 Run JavaScript with Node.js

Create a file:

```text
app.js
```

Add:

```javascript
console.log("Hello from Node.js");
```

Run:

```bash
node app.js
```

---

# 20. NPM

NPM means Node Package Manager.

It is used to install and manage JavaScript packages.

## 20.1 Check NPM Version

```bash
npm -v
```

## 20.2 Create a New Node Project

```bash
npm init
```

Quick version:

```bash
npm init -y
```

This creates:

```text
package.json
```

## 20.3 Install a Package

```bash
npm install package-name
```

Example:

```bash
npm install express
```

This creates:

```text
node_modules/
package-lock.json
```

---

# 21. package.json

`package.json` stores project information, scripts, and dependencies.

Example:

```json
{
  "name": "my-js-project",
  "version": "1.0.0",
  "main": "app.js",
  "scripts": {
    "start": "node app.js"
  }
}
```

Run the start script:

```bash
npm start
```

## Important Files

| File/Folder | Meaning |
|---|---|
| `package.json` | Project information and dependencies |
| `package-lock.json` | Exact package versions |
| `node_modules/` | Installed packages |
| `.gitignore` | Files/folders Git should ignore |

Usually do not upload `node_modules` to GitHub.

Add this to `.gitignore`:

```text
node_modules/
.env
```

---

# 22. Express.js Basic Server

Express is a Node.js framework used to build servers and APIs.

Install Express:

```bash
npm install express
```

Create `app.js`:

```javascript
const express = require("express");

const app = express();

app.get("/", (req, res) => {
    res.send("Hello from Express!");
});

app.listen(3000, () => {
    console.log("Server running on port 3000");
});
```

Run:

```bash
node app.js
```

Open in browser:

```text
http://localhost:3000
```

---

# 23. GitHub Notes for JavaScript Projects

Good files to upload:

```text
README.md
notes.md
index.html
style.css
script.js
app.js
package.json
package-lock.json
```

Usually avoid uploading:

```text
node_modules/
.env
```

Useful Git commands:

```bash
git status
git add .
git commit -m "Update JavaScript notes"
git push
```

---

# 24. Mini Practice Tasks

## Task 1: Variables

Create variables for:

- name
- age
- country
- course

Print them using `console.log()`.

Example:

```javascript
let name = "Upeka";
let age = 25;
let country = "Sri Lanka";
let course = "JavaScript";

console.log(name);
console.log(age);
console.log(country);
console.log(course);
```

## Task 2: Function

Create a function that adds two numbers.

```javascript
function add(a, b) {
    return a + b;
}

console.log(add(10, 5));
```

## Task 3: Array

Create an array of programming languages and print each one.

```javascript
let languages = ["HTML", "CSS", "JavaScript", "React"];

for (let i = 0; i < languages.length; i++) {
    console.log(languages[i]);
}
```

## Task 4: Object

Create an object about yourself.

```javascript
let student = {
    name: "Upeka",
    country: "Sri Lanka",
    course: "Meta Web Development",
    goal: "Become a software developer"
};

console.log(student);
```

## Task 5: DOM

Create a button that changes a heading.

HTML:

```html
<h1 id="title">Old Title</h1>
<button id="btn">Change Title</button>
```

JavaScript:

```javascript
let button = document.querySelector("#btn");
let title = document.querySelector("#title");

button.addEventListener("click", () => {
    title.textContent = "New Title";
});
```

## Task 6: Node.js

Create `app.js`.

```javascript
console.log("Learning JavaScript with Node.js");
```

Run:

```bash
node app.js
```

## Task 7: NPM

Create a Node.js project.

```bash
npm init -y
```

Then check if `package.json` was created.

---

# 25. Quick Revision

JavaScript makes websites interactive.  
Variables store data.  
Data types describe values.  
Operators perform actions.  
Conditionals make decisions.  
Loops repeat code.  
Functions make code reusable.  
Arrays store lists.  
Objects store related data.  
DOM connects JavaScript with HTML.  
Events respond to user actions.  
JSON is used for data exchange.  
Node.js runs JavaScript outside the browser.  
NPM manages JavaScript packages.

---

# 26. My Learning Goal

By completing this JavaScript course, I want to build a strong foundation in programming, understand how websites become interactive, learn how JavaScript works in the browser and in Node.js, and prepare myself for React, back-end development, and full-stack projects.

---

# 27. Status Tracker

| Topic | Status |
|---|---|
| JavaScript Basics | 🔄 |
| Variables & Data Types | 🔄 |
| Operators | 🔄 |
| Conditions | ⏳ |
| Loops | ⏳ |
| Functions | ⏳ |
| Arrays | ⏳ |
| Objects | ⏳ |
| DOM | ⏳ |
| Events | ⏳ |
| Modern JavaScript | ⏳ |
| Async JavaScript | ⏳ |
| Node.js | ⏳ |
| NPM | ⏳ |
| Mini Projects | ⏳ |

---

# Final Note

JavaScript is not just a language for small website effects. It is one of the main languages of modern web development. With JavaScript, Node.js, NPM, and React, I can build real full-stack applications and create a strong portfolio for IT jobs.