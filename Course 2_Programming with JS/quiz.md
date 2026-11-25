# 🚀 Programming with JavaScript
## Meta Full Stack Developer Professional Certificate

> **Author:** Upeka Rathnayaka
>
> **Course:** Programming with JavaScript
>
> **Goal:** Master JavaScript for real-world web development and technical interviews.
>
> "Learning to code is not about memorizing syntax. It's about learning how to solve problems."

---

# 📚 Table of Contents

- 🌱 Module 1 - Introduction to JavaScript
- 🧱 Module 2 - Building Blocks of a Program
- 🧠 Module 3 - Programming Paradigms
- 🧪 Module 4 - Testing
- 🎯 Final Revision
- 💼 JavaScript Interview Questions
- 🐞 Debugging Exercises
- 💻 Coding Challenges
- ⚡ JavaScript Cheat Sheet
- ⭐ Common Mistakes

---

# 🌱 MODULE 1
# Introduction to JavaScript

---

# 🎯 Learning Objectives

After completing this module, you should be able to:

✅ Explain what JavaScript is

✅ Understand why JavaScript is important

✅ Declare variables

✅ Identify JavaScript data types

✅ Use operators

✅ Write conditional statements

✅ Create loops

✅ Read simple JavaScript code

---

# 📖 Chapter 1
# What is JavaScript?

---

## ❓ Question 1

What is JavaScript?

### ✅ Answer

JavaScript is a high-level, interpreted programming language that makes websites interactive.

It allows developers to create dynamic web pages by responding to user actions, changing content, validating forms, fetching data from servers, creating animations, and much more.

Unlike HTML and CSS, JavaScript is a programming language capable of making decisions and performing calculations.

---

🧠 Remember

HTML builds the structure.

CSS designs the appearance.

JavaScript adds intelligence and interaction.

---

💡 Example

```javascript
console.log("Hello World");
```

Output

```
Hello World
```

---

🎯 Interview Tip

This is one of the most common interview questions.

Always mention:

- Interactive websites
- Programming language
- Frontend
- Backend (Node.js)

---

## ❓ Question 2

Who created JavaScript?

### ✅ Answer

JavaScript was created by Brendan Eich in 1995 while working at Netscape.

He developed the first version in only **10 days**.

Originally JavaScript was called

Mocha

then

LiveScript

before finally becoming

JavaScript.

---

💡 Fun Fact

Despite the name,

JavaScript

and

Java

are completely different programming languages.

---

## ❓ Question 3

Why is JavaScript so popular?

### ✅ Answer

JavaScript is popular because:

✔ Every modern web browser supports it.

✔ It is beginner-friendly.

✔ It powers millions of websites.

✔ It can be used for frontend development.

✔ It can be used for backend development.

✔ Large communities support it.

✔ Thousands of libraries and frameworks exist.

Examples

React

Vue

Angular

Node.js

Express

Next.js

---

## ❓ Question 4

What can JavaScript build?

### ✅ Answer

JavaScript can build

✔ Websites

✔ Mobile Apps

✔ Desktop Applications

✔ APIs

✔ Games

✔ Dashboards

✔ Real-time Chat Applications

✔ Streaming Platforms

✔ E-commerce Websites

✔ AI-powered Applications

---

🌍 Real Examples

Netflix

Facebook

Instagram

WhatsApp Web

Spotify

Google Maps

YouTube

Amazon

GitHub

---

## ❓ Question 5

What is the difference between HTML, CSS and JavaScript?

### ✅ Answer

| Technology | Purpose |
|------------|----------|
| HTML | Structure |
| CSS | Styling |
| JavaScript | Behaviour |

Think of a car.

HTML = Frame

CSS = Paint

JavaScript = Engine

Without JavaScript the page cannot respond to the user.

---

# 📖 Chapter 2
# Variables

---

## ❓ Question 6

What is a variable?

### ✅ Answer

A variable is a named container used to store information.

The stored value can later be used, changed or displayed.

Example

```javascript
let name = "Upeka";
```

Here

name

is the variable.

"Upeka"

is the stored value.

---

💡 Real World Analogy

Think of a variable as a labeled storage box.

The label tells you where to find the value.

---

## ❓ Question 7

Why do we use variables?

### ✅ Answer

Variables allow us to

Store information

Reuse information

Modify information

Perform calculations

Display information

Without variables every value would need to be written repeatedly.

---

## ❓ Question 8

How do you declare a variable?

### ✅ Answer

There are three ways.

```javascript
var age = 25;

let city = "Riga";

const PI = 3.14159;
```

---

## ❓ Question 9

What is let?

### ✅ Answer

let creates a variable that can be reassigned later.

Example

```javascript
let score = 50;

score = 100;
```

Output

```
100
```

Use let whenever you expect the value to change.

---

## ❓ Question 10

What is const?

### ✅ Answer

const creates a variable whose reference cannot be reassigned.

Example

```javascript
const country = "Latvia";
```

This is allowed.

```javascript
const age = 20;
```

This is NOT allowed.

```javascript
age = 21;
```

Result

```
TypeError
```

---

🎯 Best Practice

Use

const

by default.

Use

let

only when the value changes.

Avoid

var

in modern JavaScript.

---

## ❓ Question 11

What is var?

### ✅ Answer

var is the old way of declaring variables.

It is function-scoped and allows redeclaration.

Example

```javascript
var x = 10;

var x = 20;

console.log(x);
```

Output

```
20
```

Today developers rarely use var because let and const are safer.

---

## ❓ Question 12

When should you use let instead of const?

### ✅ Answer

Use let whenever the value needs to change.

Example

```javascript
let lives = 3;

lives--;

console.log(lives);
```

Output

```
2
```

Since the value changes,

let

is appropriate.

---

# ⭐ Summary

✅ JavaScript makes websites interactive.

✅ HTML creates structure.

✅ CSS creates design.

✅ JavaScript creates behaviour.

✅ Variables store information.

✅ let allows reassignment.

✅ const prevents reassignment.

✅ var is considered outdated for most modern code.

---

# 🧠 Quick Revision Quiz

### 1. What is JavaScript?

Answer:

_____________________________________

---

### 2. Who created JavaScript?

Answer:

_____________________________________

---

### 3. Which keyword should be used by default?

Answer:

_____________________________________

---

### 4. Which keyword allows reassignment?

Answer:

_____________________________________

---

### 5. Which keyword is mostly avoided today?

Answer:

_____________________________________

---

---

# 📖 Chapter 3
# JavaScript Data Types

---

## 🎯 Learning Objectives

After this chapter you should be able to:

✅ Understand what data types are

✅ Identify primitive data types

✅ Identify reference data types

✅ Use the `typeof` operator

---

## ❓ Question 13

### What is a data type?

### ✅ Answer

A data type tells JavaScript what kind of information is being stored inside a variable.

Different data types are handled differently by JavaScript.

Examples include:

- Numbers
- Text
- True or False values
- Objects

Example

```javascript
let age = 26;
let name = "Upeka";
let student = true;
```

Each variable stores a different data type.

---

💡 Remember

Think of a data type as the "category" of your data.

---

## ❓ Question 14

### How many primitive data types are there?

### ✅ Answer

JavaScript has **7 primitive data types**.

1. String

2. Number

3. Boolean

4. Undefined

5. Null

6. Symbol

7. BigInt

Primitive values store a single value.

---

## ❓ Question 15

### What is a String?

### ✅ Answer

A string is a sequence of characters.

Strings can use:

```javascript
"Double Quotes"
```

```javascript
'Single Quotes'
```

```javascript
`Backticks`
```

Example

```javascript
let country = "Latvia";
```

---

Example

```javascript
let language = 'JavaScript';
```

---

## ❓ Question 16

### What is a Number?

### ✅ Answer

Numbers represent numeric values.

JavaScript uses one Number type for both integers and decimals.

Examples

```javascript
let age = 26;
```

```javascript
let price = 14.99;
```

```javascript
let temperature = -5;
```

---

## ❓ Question 17

### What is a Boolean?

### ✅ Answer

A Boolean stores only two possible values.

```
true
```

or

```
false
```

Example

```javascript
let loggedIn = true;
```

Example

```javascript
let isStudent = false;
```

---

💡 Real World Example

```javascript
let paymentCompleted = true;
```

```javascript
let emailVerified = false;
```

---

## ❓ Question 18

### What is Undefined?

### ✅ Answer

Undefined means

"A variable exists but has not been given a value."

Example

```javascript
let score;

console.log(score);
```

Output

```
undefined
```

---

Common Mistake ❌

Many beginners think

undefined

means zero.

It does NOT.

---

## ❓ Question 19

### What is Null?

### ✅ Answer

Null means

"The value is intentionally empty."

Example

```javascript
let car = null;
```

You are deliberately saying

"There is no value."

---

Difference

Undefined

↓

No value assigned.

Null

↓

Empty value assigned intentionally.

---

## ❓ Question 20

### What is BigInt?

### ✅ Answer

BigInt stores very large integers that exceed the safe Number limit.

Example

```javascript
let population = 123456789012345678901234567890n;
```

Notice the

```
n
```

at the end.

---

## ❓ Question 21

### What is Symbol?

### ✅ Answer

A Symbol creates a unique value.

Symbols are mostly used when creating object properties that must never conflict with other properties.

Example

```javascript
const id = Symbol("id");
```

Most beginners won't use Symbol often.

---

## ❓ Question 22

### What are Reference Data Types?

### ✅ Answer

Reference types store collections of data.

Common reference types include

- Objects
- Arrays
- Functions

Unlike primitive values, reference values are stored by reference.

---

## ❓ Question 23

### What is an Object?

### ✅ Answer

An object stores related information using key-value pairs.

Example

```javascript
const student = {
    name: "Upeka",
    age: 26,
    country: "Sri Lanka"
};
```

Each property has

Key

↓

Value

---

## ❓ Question 24

### What is an Array?

### ✅ Answer

An array stores multiple values inside one variable.

Example

```javascript
const fruits = [
    "Apple",
    "Orange",
    "Banana"
];
```

Arrays use indexes.

The first element always starts at index

```
0
```

---

Example

```javascript
console.log(fruits[0]);
```

Output

```
Apple
```

---

## ❓ Question 25

### What is a Function?

### ✅ Answer

A function is a reusable block of code.

Example

```javascript
function greet() {
    console.log("Hello");
}

greet();
```

Output

```
Hello
```

---

# 📖 Chapter 4
# typeof Operator

---

## ❓ Question 26

### What does typeof do?

### ✅ Answer

The

```javascript
typeof
```

operator returns the data type of a value.

Example

```javascript
typeof "Hello";
```

Output

```
string
```

---

Example

```javascript
typeof 100;
```

Output

```
number
```

---

Example

```javascript
typeof true;
```

Output

```
boolean
```

---

Example

```javascript
typeof undefined;
```

Output

```
undefined
```

---

## ❓ Question 27

### What is the output?

```javascript
let age = 26;

console.log(typeof age);
```

### ✅ Answer

Output

```
number
```

---

## ❓ Question 28

### What is the output?

```javascript
let city = "Riga";

console.log(typeof city);
```

### ✅ Answer

Output

```
string
```

---

## ❓ Question 29

### What is the output?

```javascript
let isOnline = false;

console.log(typeof isOnline);
```

### ✅ Answer

Output

```
boolean
```

---

## ❓ Question 30

### What is the output?

```javascript
let score;

console.log(typeof score);
```

### ✅ Answer

Output

```
undefined
```

---

## ⚠ Common Interview Question

### What is the output?

```javascript
console.log(typeof null);
```

### ✅ Answer

Output

```
object
```

Although this looks strange, it is actually a long-standing bug in JavaScript that has been kept for backward compatibility.

---

# 📝 Quick Notes

✔ Primitive values store one value.

✔ Objects store collections of values.

✔ Arrays store ordered lists.

✔ Functions store reusable code.

✔ typeof returns the type of a value.

✔ undefined means "not assigned."

✔ null means "intentionally empty."

---

# 🎯 Practice Questions

Without running the code, predict the output.

### Question 1

```javascript
let language = "JavaScript";

console.log(typeof language);
```

Answer

____________________

---

### Question 2

```javascript
let number = 99;

console.log(typeof number);
```

Answer

____________________

---

### Question 3

```javascript
let active = true;

console.log(typeof active);
```

Answer

____________________

---

### Question 4

```javascript
let item = null;

console.log(typeof item);
```

Answer

____________________

---

### Question 5

```javascript
let score;

console.log(score);
```

Answer

____________________

---

# ⭐ Chapter Summary

✅ JavaScript has 7 primitive data types.

✅ Objects, Arrays, and Functions are reference types.

✅ Use `typeof` to check a value's type.

✅ `undefined` and `null` are different.

✅ `typeof null` returns `"object"` because of a historical JavaScript behavior.

---

---

# 📖 Chapter 5
# JavaScript Operators

---

# 🎯 Learning Objectives

After this chapter you should be able to

✅ Understand operators

✅ Perform arithmetic calculations

✅ Compare values

✅ Use logical operators

✅ Understand assignment operators

✅ Understand operator precedence

---

## ❓ Question 31

### What is an operator?

### ✅ Answer

An operator is a symbol that performs an operation on one or more values.

Example

```javascript
5 + 3
```

The

```
+
```

operator adds two numbers.

---

## ❓ Question 32

### What are Arithmetic Operators?

### ✅ Answer

Arithmetic operators perform mathematical calculations.

| Operator | Meaning |
|----------|---------|
| + | Addition |
| - | Subtraction |
| * | Multiplication |
| / | Division |
| % | Modulus (Remainder) |
| ** | Exponent |

---

## ❓ Question 33

### Addition (+)

### ✅ Answer

Adds two values.

Example

```javascript
let result = 10 + 5;

console.log(result);
```

Output

```
15
```

---

## ❓ Question 34

### Subtraction (-)

### ✅ Answer

Subtracts one value from another.

Example

```javascript
20 - 5
```

Output

```
15
```

---

## ❓ Question 35

### Multiplication (*)

### ✅ Answer

Multiplies values.

Example

```javascript
8 * 6
```

Output

```
48
```

---

## ❓ Question 36

### Division (/)

### ✅ Answer

Divides one number by another.

Example

```javascript
20 / 5
```

Output

```
4
```

---

## ❓ Question 37

### Modulus (%)

### ✅ Answer

Returns the remainder after division.

Example

```javascript
10 % 3
```

Output

```
1
```

---

💡 Interview Tip

Modulus is commonly used for checking even and odd numbers.

Example

```javascript
10 % 2
```

Output

```
0
```

This means 10 is even.

---

## ❓ Question 38

### Exponent (**)

### ✅ Answer

Raises a number to a power.

Example

```javascript
2 ** 4
```

Output

```
16
```

---

# 📖 Chapter 6
# Assignment Operators

---

## ❓ Question 39

### What is an assignment operator?

### ✅ Answer

Assignment operators assign values to variables.

Basic assignment

```javascript
let age = 26;
```

The

```
=
```

stores the value inside the variable.

---

## ❓ Question 40

### What does += do?

### ✅ Answer

It adds a value and stores the result.

Example

```javascript
let score = 10;

score += 5;

console.log(score);
```

Output

```
15
```

Equivalent to

```javascript
score = score + 5;
```

---

## ❓ Question 41

### What does -= do?

### ✅ Answer

Subtracts and stores.

Example

```javascript
let money = 100;

money -= 25;

console.log(money);
```

Output

```
75
```

---

## ❓ Question 42

### What does *= do?

### ✅ Answer

Multiplies and stores.

Example

```javascript
let number = 5;

number *= 4;

console.log(number);
```

Output

```
20
```

---

## ❓ Question 43

### What does /= do?

### ✅ Answer

Divides and stores.

Example

```javascript
let total = 30;

total /= 5;

console.log(total);
```

Output

```
6
```

---

# 📖 Chapter 7
# Comparison Operators

---

## ❓ Question 44

### Why do we use comparison operators?

### ✅ Answer

Comparison operators compare two values.

They always return

```
true
```

or

```
false
```

---

## ❓ Question 45

### Equal (==)

### ✅ Answer

Compares only the values.

JavaScript converts data types if necessary.

Example

```javascript
5 == "5"
```

Output

```
true
```

---

⚠ Common Mistake

Beginners often think

```
==
```

checks types.

It does NOT.

---

## ❓ Question 46

### Strict Equal (===)

### ✅ Answer

Compares both

✔ Value

✔ Data Type

Example

```javascript
5 === "5"
```

Output

```
false
```

Because

Number

is different from

String.

---

🎯 Best Practice

Always use

```
===
```

unless you have a specific reason not to.

---

## ❓ Question 47

### Not Equal (!=)

### ✅ Answer

Checks if two values are different.

Example

```javascript
10 != 5
```

Output

```
true
```

---

## ❓ Question 48

### Strict Not Equal (!==)

### ✅ Answer

Checks value and type.

Example

```javascript
10 !== "10"
```

Output

```
true
```

---

## ❓ Question 49

### Greater Than (>)

### ✅ Answer

Checks whether one value is larger.

Example

```javascript
10 > 3
```

Output

```
true
```

---

## ❓ Question 50

### Less Than (<)

### ✅ Answer

Checks whether one value is smaller.

Example

```javascript
3 < 8
```

Output

```
true
```

---

## ❓ Question 51

### Greater Than or Equal (>=)

### ✅ Answer

Returns true if the left value is greater than OR equal.

Example

```javascript
18 >= 18
```

Output

```
true
```

---

## ❓ Question 52

### Less Than or Equal (<=)

### ✅ Answer

Returns true if the left value is less than OR equal.

Example

```javascript
15 <= 20
```

Output

```
true
```

---

# 📖 Chapter 8
# Logical Operators

---

## ❓ Question 53

### What are logical operators?

### ✅ Answer

Logical operators combine multiple conditions.

The three logical operators are

```
&&
||
!
```

---

## ❓ Question 54

### AND (&&)

### ✅ Answer

Returns true only if BOTH conditions are true.

Example

```javascript
let age = 22;

console.log(age > 18 && age < 30);
```

Output

```
true
```

---

## ❓ Question 55

### OR (||)

### ✅ Answer

Returns true if at least ONE condition is true.

Example

```javascript
console.log(false || true);
```

Output

```
true
```

---

## ❓ Question 56

### NOT (!)

### ✅ Answer

Reverses a Boolean value.

Example

```javascript
let loggedIn = true;

console.log(!loggedIn);
```

Output

```
false
```

---

# 📖 Chapter 9
# Operator Precedence

---

## ❓ Question 57

### What is operator precedence?

### ✅ Answer

Operator precedence determines the order in which operations are performed.

Example

```javascript
2 + 3 * 4
```

Output

```
14
```

Multiplication happens before addition.

---

Example

```javascript
(2 + 3) * 4
```

Output

```
20
```

Parentheses are evaluated first.

---

💡 Easy Way to Remember

1. Parentheses

2. Exponents

3. Multiplication & Division

4. Addition & Subtraction

---

# 🎯 Predict the Output

## Question 1

```javascript
console.log(12 % 5);
```

### ✅ Answer

```
2
```

---

## Question 2

```javascript
console.log(5 == "5");
```

### ✅ Answer

```
true
```

---

## Question 3

```javascript
console.log(5 === "5");
```

### ✅ Answer

```
false
```

---

## Question 4

```javascript
console.log(true && false);
```

### ✅ Answer

```
false
```

---

## Question 5

```javascript
console.log(true || false);
```

### ✅ Answer

```
true
```

---

## Question 6

```javascript
console.log(!(5 > 2));
```

### ✅ Answer

```
false
```

---

## Question 7

```javascript
console.log(10 + 5 * 2);
```

### ✅ Answer

```
20
```

---

## Question 8

```javascript
console.log((10 + 5) * 2);
```

### ✅ Answer

```
30
```

---

# ⭐ Chapter Summary

✅ Operators perform actions on values.

✅ Arithmetic operators perform calculations.

✅ Assignment operators update variables.

✅ Comparison operators return Boolean values.

✅ Logical operators combine conditions.

✅ `===` is preferred over `==`.

✅ Parentheses have the highest precedence.

---
---

# 📖 Chapter 10
# Decision Making in JavaScript

> "Programs become intelligent when they can make decisions."

---

# 🎯 Learning Objectives

After this chapter you should be able to

✅ Make decisions using conditions

✅ Understand Boolean expressions

✅ Use if statements

✅ Use else statements

✅ Use else if

✅ Use nested if statements

---

# 🤔 Why do we need conditions?

Imagine you're creating a login page.

If the password is correct

➡ Login

Otherwise

➡ Show an error.

Without conditions, programs couldn't make decisions.

---

## ❓ Question 58

### What is an if statement?

### ✅ Answer

An **if statement** executes code only when a condition is true.

Syntax

```javascript
if (condition) {
    // code
}
```

Example

```javascript
let age = 20;

if(age >= 18){
    console.log("Adult");
}
```

Output

```
Adult
```

---

## ❓ Question 59

### What happens if the condition is false?

### ✅ Answer

JavaScript skips the code inside the if block.

Example

```javascript
let age = 15;

if(age >= 18){
    console.log("Adult");
}

console.log("Finished");
```

Output

```
Finished
```

---

## ❓ Question 60

### What is an else statement?

### ✅ Answer

The else block runs when the if condition is false.

Example

```javascript
let age = 15;

if(age >= 18){
    console.log("Adult");
}
else{
    console.log("Minor");
}
```

Output

```
Minor
```

---

## ❓ Question 61

### What is else if?

### ✅ Answer

Use **else if** when checking multiple conditions.

Example

```javascript
let marks = 82;

if(marks >= 90){
    console.log("A");
}
else if(marks >= 75){
    console.log("B");
}
else{
    console.log("C");
}
```

Output

```
B
```

---

💡 Best Practice

Write the most specific condition first.

---

## ❓ Question 62

### Can an if statement exist without else?

### ✅ Answer

Yes.

Example

```javascript
let raining = true;

if(raining){
    console.log("Take an umbrella");
}
```

Output

```
Take an umbrella
```

---

## ❓ Question 63

### What are nested if statements?

### ✅ Answer

A nested if is an if statement inside another if statement.

Example

```javascript
let loggedIn = true;
let admin = true;

if(loggedIn){

    if(admin){
        console.log("Admin Panel");
    }

}
```

Output

```
Admin Panel
```

---

# 📖 Chapter 11
# Truthy and Falsy Values

---

## ❓ Question 64

### What are Truthy values?

### ✅ Answer

Truthy values become

```
true
```

when evaluated inside a condition.

Examples

```javascript
1
```

```javascript
"Hello"
```

```javascript
[]
```

```javascript
{}
```

---

## ❓ Question 65

### What are Falsy values?

### ✅ Answer

There are only a few falsy values.

```
false

0

-0

0n

""

null

undefined

NaN
```

Example

```javascript
if(0){
    console.log("Hello");
}
```

Nothing prints because

```
0
```

is falsy.

---

🎯 Interview Tip

You should memorize every falsy value.

Many interviews ask this question.

---

# 📖 Chapter 12
# switch Statement

---

## ❓ Question 66

### What is a switch statement?

### ✅ Answer

A switch statement is another way of making decisions.

It is useful when comparing one value against many possible values.

Syntax

```javascript
switch(value){

    case value1:
        break;

    case value2:
        break;

    default:
}
```

---

## ❓ Question 67

### Example of switch

```javascript
let day = 2;

switch(day){

case 1:
    console.log("Monday");
    break;

case 2:
    console.log("Tuesday");
    break;

default:
    console.log("Unknown");

}
```

Output

```
Tuesday
```

---

## ❓ Question 68

### Why is break important?

### ✅ Answer

Without break,

JavaScript continues executing the next case.

Example

```javascript
let day = 1;

switch(day){

case 1:
    console.log("Monday");

case 2:
    console.log("Tuesday");

}
```

Output

```
Monday

Tuesday
```

---

With break

```javascript
case 1:
    console.log("Monday");
    break;
```

Output

```
Monday
```

---

# 📖 Chapter 13
# Loops

---

> Computers are good at repeating tasks.

Instead of writing the same code 100 times,

we use loops.

---

## ❓ Question 69

### What is a loop?

### ✅ Answer

A loop repeats code until a condition becomes false.

JavaScript has

- for

- while

- do...while

- for...of

- for...in

---

## ❓ Question 70

### What is a for loop?

### ✅ Answer

A for loop repeats code a specific number of times.

Syntax

```javascript
for(initialization;
condition;
increment){

}
```

Example

```javascript
for(let i = 1; i <= 5; i++){

    console.log(i);

}
```

Output

```
1

2

3

4

5
```

---

## ❓ Question 71

### What are the three parts of a for loop?

### ✅ Answer

Initialization

Runs once.

Condition

Checked before every iteration.

Increment

Runs after every iteration.

---

## ❓ Question 72

### What is an infinite loop?

### ✅ Answer

An infinite loop never stops.

Example

```javascript
while(true){

}
```

Avoid infinite loops because they freeze programs.

---

## ❓ Question 73

### What is a while loop?

### ✅ Answer

A while loop repeats while a condition is true.

Example

```javascript
let i = 1;

while(i <= 5){

    console.log(i);

    i++;

}
```

Output

```
1

2

3

4

5
```

---

## ❓ Question 74

### When should you use a while loop?

### ✅ Answer

Use a while loop when you don't know beforehand how many times the loop should run.

Example

Reading user input until they type `"exit"`.

---

## ❓ Question 75

### What is a do...while loop?

### ✅ Answer

A do...while loop always executes at least once.

Example

```javascript
let i = 10;

do{

    console.log(i);

}while(i < 5);
```

Output

```
10
```

Although the condition is false,

the code executes once.

---

# 🎯 Predict the Output

### Question 1

```javascript
let age = 30;

if(age > 18){

console.log("Adult");

}
```

### ✅ Answer

```
Adult
```

---

### Question 2

```javascript
let marks = 40;

if(marks >= 50){

console.log("Pass");

}
else{

console.log("Fail");

}
```

### ✅ Answer

```
Fail
```

---

### Question 3

```javascript
for(let i=0;i<3;i++){

console.log(i);

}
```

### ✅ Answer

```
0

1

2
```

---

### Question 4

```javascript
let i = 1;

while(i<=3){

console.log(i);

i++;

}
```

### ✅ Answer

```
1

2

3
```

---

### Question 5

```javascript
console.log(Boolean(""));
```

### ✅ Answer

```
false
```

---

# 💼 Interview Questions

### Why use switch instead of multiple if statements?

**Answer**

Use `switch` when comparing one variable against many fixed values. It makes the code cleaner and easier to read.

---

### Which loop is used most often?

**Answer**

The `for` loop is the most commonly used loop because it's concise and works well when the number of iterations is known.

---

### What's the difference between while and do...while?

**Answer**

- `while` checks the condition before running the loop.
- `do...while` runs the code once before checking the condition.

---

# ⭐ Chapter Summary

✅ Use `if` for simple decisions.

✅ Use `else` when you need an alternative.

✅ Use `else if` for multiple conditions.

✅ `switch` is useful for many fixed options.

✅ `for` loops are best when you know the number of iterations.

✅ `while` loops are best when the number of iterations is unknown.

✅ `do...while` always executes at least once.

---

---

# 📖 Chapter 14
# Functions

> "Functions are reusable blocks of code that perform a specific task."

---

# 🎯 Learning Objectives

After completing this chapter you should be able to

✅ Explain what a function is

✅ Create functions

✅ Call functions

✅ Understand parameters

✅ Understand arguments

✅ Return values

✅ Understand function expressions

✅ Understand arrow functions

---

# 🤔 Why do we use functions?

Imagine you need to greet 100 users.

Without functions

```javascript
console.log("Hello John");
console.log("Hello Mary");
console.log("Hello Alex");
console.log("Hello Sarah");
```

Now imagine doing this 100 times...

Instead, we create one function.

```javascript
function greet(name){
    console.log("Hello " + name);
}

greet("John");
greet("Mary");
greet("Alex");
```

Much cleaner!

---

## ❓ Question 76

### What is a function?

### ✅ Answer

A function is a reusable block of code that performs a specific task.

Instead of writing the same code repeatedly, you write it once and call it whenever needed.

---

💡 Real World Example

Think of a coffee machine.

You press one button.

The machine performs many steps.

Functions work the same way.

---

## ❓ Question 77

### How do you declare a function?

### ✅ Answer

Syntax

```javascript
function functionName(){

}
```

Example

```javascript
function greet(){

    console.log("Hello");

}
```

---

## ❓ Question 78

### How do you call a function?

### ✅ Answer

Declaring a function does NOT execute it.

You must call it.

Example

```javascript
function greet(){

    console.log("Hello");

}

greet();
```

Output

```
Hello
```

---

## ❓ Question 79

### What happens if you never call a function?

### ✅ Answer

Nothing happens.

JavaScript stores the function in memory but never executes it.

---

## ❓ Question 80

### What are parameters?

### ✅ Answer

Parameters are variables listed inside the function definition.

Example

```javascript
function greet(name){

    console.log(name);

}
```

Here

```
name
```

is the parameter.

---

## ❓ Question 81

### What are arguments?

### ✅ Answer

Arguments are the actual values passed into the function.

Example

```javascript
function greet(name){

    console.log(name);

}

greet("Upeka");
```

Parameter

```
name
```

Argument

```
"Upeka"
```

---

🎯 Easy Memory Trick

Parameter

↓

Placeholder

Argument

↓

Actual value

---

## ❓ Question 82

### Can a function have multiple parameters?

### ✅ Answer

Yes.

Example

```javascript
function introduce(name, age){

    console.log(name);

    console.log(age);

}

introduce("Upeka",26);
```

Output

```
Upeka

26
```

---

## ❓ Question 83

### What is a return statement?

### ✅ Answer

The return statement sends a value back to where the function was called.

Example

```javascript
function add(a,b){

    return a+b;

}

let result = add(5,3);

console.log(result);
```

Output

```
8
```

---

💡 Important

`return`

immediately stops the function.

Example

```javascript
function test(){

    return "Hello";

    console.log("World");

}

console.log(test());
```

Output

```
Hello
```

"World" never prints.

---

## ❓ Question 84

### What happens if a function has no return statement?

### ✅ Answer

Every JavaScript function returns something.

If no return statement exists,

JavaScript returns

```
undefined
```

Example

```javascript
function hello(){

    console.log("Hi");

}

console.log(hello());
```

Output

```
Hi

undefined
```

---

## ❓ Question 85

### What is the difference between console.log() and return?

### ✅ Answer

`console.log()`

Displays information.

`return`

Sends information back.

Example

```javascript
function add(a,b){

    return a+b;

}

console.log(add(4,5));
```

Output

```
9
```

---

## ❓ Question 86

### What is a function expression?

### ✅ Answer

A function can be stored inside a variable.

Example

```javascript
const greet = function(){

    console.log("Hello");

};

greet();
```

Output

```
Hello
```

---

## ❓ Question 87

### What is an anonymous function?

### ✅ Answer

An anonymous function is a function without a name.

Example

```javascript
const greet = function(){

    console.log("Hello");

};
```

The function itself has no name.

---

## ❓ Question 88

### What is an arrow function?

### ✅ Answer

Arrow functions provide a shorter syntax for writing functions.

Example

```javascript
const greet = () => {

    console.log("Hello");

};
```

---

Example

```javascript
const square = number => number * number;
```

Output

```javascript
console.log(square(5));
```

```
25
```

---

💡 Why use arrow functions?

✔ Less code

✔ Easier to read

✔ Widely used in React

---

## ❓ Question 89

### Can arrow functions return values?

### ✅ Answer

Yes.

Example

```javascript
const multiply = (a,b)=>{

    return a*b;

};

console.log(multiply(4,5));
```

Output

```
20
```

---

## ❓ Question 90

### What is function scope?

### ✅ Answer

Variables declared inside a function only exist inside that function.

Example

```javascript
function test(){

    let age = 20;

}

console.log(age);
```

Output

```
ReferenceError
```

The variable

```
age
```

cannot be accessed outside the function.

---

# 💻 Predict the Output

---

### Question 1

```javascript
function greet(){

console.log("Hello");

}

greet();
```

### ✅ Answer

```
Hello
```

---

### Question 2

```javascript
function add(a,b){

return a+b;

}

console.log(add(2,8));
```

### ✅ Answer

```
10
```

---

### Question 3

```javascript
function square(x){

return x*x;

}

console.log(square(4));
```

### ✅ Answer

```
16
```

---

### Question 4

```javascript
const hello = ()=>{

return "Hi";

};

console.log(hello());
```

### ✅ Answer

```
Hi
```

---

### Question 5

```javascript
function test(){

console.log("JavaScript");

}

console.log(test());
```

### ✅ Answer

```
JavaScript

undefined
```

---

# 💼 Interview Questions

## What is the difference between parameters and arguments?

### ✅ Answer

Parameters are variables defined in the function declaration.

Arguments are the actual values passed when calling the function.

---

## Why do we use return instead of console.log()?

### ✅ Answer

`return` allows the value to be reused later in the program.

`console.log()` only displays the value on the screen.

---

## When should you use an arrow function?

### ✅ Answer

Arrow functions are ideal for short functions, callbacks, and modern JavaScript applications such as React.

---

## ⭐ Chapter Summary

✅ Functions help eliminate repeated code.

✅ Functions must be called to execute.

✅ Parameters receive values.

✅ Arguments supply values.

✅ `return` sends a value back.

✅ Every function returns something.

✅ Arrow functions provide a concise syntax.

✅ Variables inside functions are local to that function.

---

# 🧠 Memory Checklist

Before moving on, make sure you can answer these without looking:

☐ What is a function?

☐ What is the difference between a parameter and an argument?

☐ What does `return` do?

☐ What happens if there is no `return` statement?

☐ What is an arrow function?

☐ What is function scope?

---

