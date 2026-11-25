# 🐍 Programming in Python — Zero to Hero

> **Meta Full Stack Developer — Programming in Python**
>
> This is not a collection of boring lecture notes.
>
> This is my journey from:
>
> **"I know a little Python" → "I understand what Python is actually doing."**

---

# 🗺️ Welcome to Python Land

Imagine we've just arrived in a new country called **Python**.

Luckily, we've already spent some time in JavaScript Land, so programming isn't completely foreign.

We already understand that computers need instructions.

But Python has its own customs.

JavaScript might say:

```javascript
let name = "Upeka";

console.log("Hello " + name);
```

Python looks at the `let`, braces, semicolons and says:

> "Why are you carrying all that luggage?" 😭

```python
name = "Upeka"

print("Hello", name)
```

Welcome to Python.

Our journey has four major regions:

```text
🌱 Module 1
Getting Started with Python

        ↓

🧰 Module 2
Basic Programming with Python

        ↓

🧠 Module 3
Programming Paradigms

        ↓

🏗️ Module 4
Modules, Libraries & Testing
```

Throughout the journey we'll use:

> 🧠 **Genius Corner** — understand what's really happening  
> 🐍 **Python Under the Hood** — mental models  
> ⚠️ **Trap** — common mistakes  
> 🔄 **JS → Python** — connect Python to JavaScript  
> 🧪 **Try It** — experiments worth running  
> 🎯 **Checkpoint** — things I should be able to explain myself

---

# 🌱 MODULE 1 — GETTING STARTED WITH PYTHON

# Chapter 1 — What Is Programming Anyway?

A computer is incredibly powerful.

But there's a catch.

It's also incredibly literal.

Tell a human:

> "Make me coffee."

They automatically understand dozens of hidden steps.

A computer needs something more like:

```text
Find cup
↓
Put cup under machine
↓
Prepare coffee
↓
Pour coffee
↓
Stop
```

Programming is basically the art of taking a problem and breaking it into instructions precise enough for a computer to execute.

Those instructions together form a **program**.

---

# Chapter 2 — Meeting Python 🐍

Python is a:

> **high-level, general-purpose programming language**

Let's unpack that instead of memorizing it.

### High-level

Python hides many complicated hardware-level details.

We can write:

```python
print("Hello")
```

instead of worrying about CPU instructions and memory addresses.

### General-purpose

Python isn't designed for only one job.

It's used for:

- Web development
- Backend development
- Automation
- Scripting
- Data analysis
- Data science
- Machine learning
- Artificial intelligence
- Cybersecurity
- Testing
- Scientific computing
- General software development

Python was created by **Guido van Rossum** and first released in the early 1990s.

One of Python's biggest ideas is:

> Code should be readable.

Look at this:

```python
if hungry:
    eat()
```

Even if someone has never studied Python, they can probably guess what it means.

---

# Chapter 3 — How Does Python Actually Run?

Let's create:

```text
hello.py
```

Inside:

```python
print("Hello Python!")
```

Conceptually:

```text
Our Python code
      ↓
Python implementation
      ↓
Python processes the instructions
      ↓
Computer executes them
      ↓
Result
```

Python is commonly called an **interpreted language**.

But that's slightly simplified.

The most common Python implementation, **CPython**, first compiles Python source code into something called **bytecode**.

Then the Python Virtual Machine executes that bytecode.

Very roughly:

```text
Python source
     ↓
Bytecode
     ↓
Python Virtual Machine
     ↓
Execution
```

## 🧠 Genius Corner

"Compiled language" and "interpreted language" aren't always two perfectly separate boxes.

Languages can involve both ideas at different stages.

For now, the important thing is:

> We write Python. Python handles the ugly machinery underneath.

---

# Chapter 4 — Python Says Its First Words 🗣️

The traditional first program:

```python
print("Hello, world!")
```

`print()` basically tells Python:

> Show this value on the screen.

```python
print("I need coffee")
```

Result:

```text
I need coffee
```

We can print numbers too:

```python
print(42)
```

Or multiple values:

```python
name = "Upeka"

print("Hello", name)
```

---

# Chapter 5 — Comments: Messages to Future Me

Sometimes code needs explanation.

Python ignores comments:

```python
# Calculate final price
price = 20
```

Inline comments work too:

```python
tax = 0.21  # 21% tax
```

But don't do this:

```python
age = 27  # Set age to 27
```

The code already told us that. 😂

Comments are most useful for explaining:

> **WHY** something is being done.

---

# Chapter 6 — Variables: Giving Things Names 📦

Imagine working in a restaurant kitchen.

There are containers everywhere.

One contains:

```text
Salt
```

Another:

```text
Sugar
```

Another:

```text
Flour
```

Without labels, we'd have chaos.

Programs have the same problem.

We give values names:

```python
name = "Upeka"
age = 27
salary = 1500
```

A beginner explanation says:

> A variable is a container that stores data.

That's useful initially.

But here's the more accurate version.

## 🧠 Genius Corner — Variables Aren't Really Boxes

In Python, it's better to think:

> A variable is a **name referring to an object**.

Consider:

```python
x = 10
```

Think:

```text
x ─────→ 10
```

Now:

```python
y = x
```

We have:

```text
x ───┐
     ├──→ 10
y ───┘
```

Then:

```python
x = 20
```

Python doesn't magically change `y`.

Instead:

```text
x ─────→ 20

y ─────→ 10
```

So:

```python
print(y)
```

still gives:

```text
10
```

That little mental model becomes VERY important later when we learn about mutable objects.

---

# Chapter 7 — Naming Variables

Good:

```python
customer_name = "Anna"
total_price = 25.50
```

Bad:

```python
x = "Anna"
a = 25.50
```

Unless `x` genuinely makes sense mathematically, descriptive names make code much easier to understand.

Python usually uses:

```text
snake_case
```

Example:

```python
first_name
restaurant_total
customer_order
```

---

# 🔄 JavaScript → Python

JavaScript:

```javascript
let age = 27;
const name = "Upeka";
```

Python:

```python
age = 27
name = "Upeka"
```

Python doesn't require:

```text
let
const
;
```

Minimalist queen. ✨

---

# Chapter 8 — Data Types: Every Value Has a Personality 🎭

Consider:

```python
name = "Upeka"
age = 27
height = 1.50
learning_python = True
nothing = None
```

Python sees several different types.

---

## Integer — `int`

Whole numbers:

```python
10
27
0
-100
```

Example:

```python
age = 27
```

---

## Float — `float`

Numbers with decimal components:

```python
3.14
1.50
-2.5
```

Example:

```python
temperature = 21.5
```

### ⚠️ Floating-Point Weirdness

Try:

```python
print(0.1 + 0.2)
```

You may see:

```text
0.30000000000000004
```

Python hasn't forgotten mathematics.

Computers represent many decimal fractions approximately using binary floating-point representation.

This becomes important when dealing with things such as money or numerical precision.

---

## String — `str`

Text:

```python
"Hello"
"Python"
"27"
```

Notice:

```python
27
```

and:

```python
"27"
```

are NOT the same thing.

One is:

```text
integer
```

The other:

```text
string
```

---

## Boolean — `bool`

Only two values:

```python
True
False
```

Notice the capital letters.

JavaScript:

```javascript
true;
false;
```

Python:

```python
True
False
```

Tiny difference.

Very annoying when forgotten. 😂

---

## None — `None`

Sometimes we intentionally represent:

> There is no value here.

Python uses:

```python
None
```

Example:

```python
result = None
```

`None` is NOT the same as:

```python
0
False
""
[]
```

---

# Chapter 9 — Asking Python "What Are You?"

We can inspect a value:

```python
age = 27

print(type(age))
```

Python:

```text
<class 'int'>
```

We can also check:

```python
isinstance(age, int)
```

Result:

```python
True
```

---

# Chapter 10 — Type Conversion

Sometimes we need to transform one type into another.

```python
int("27")
```

becomes:

```python
27
```

Other examples:

```python
float("3.5")

str(100)

bool(1)
```

But Python isn't a magician.

```python
int("pizza")
```

💥

```text
ValueError
```

There is no sensible integer representation of `"pizza"`.

---

# Chapter 11 — Strings Have Superpowers

```python
language = "Python"
```

Access characters:

```python
language[0]
```

Result:

```text
P
```

Last character:

```python
language[-1]
```

Result:

```text
n
```

Length:

```python
len(language)
```

Result:

```text
6
```

Methods:

```python
language.upper()
language.lower()
language.capitalize()
```

---

# Chapter 12 — String Slicing 🍰

Suppose:

```python
word = "Python"
```

```python
word[0:3]
```

Result:

```text
Pyt
```

General structure:

```text
sequence[start:stop:step]
```

Examples:

```python
word[:3]
word[3:]
word[::2]
```

Important:

> The `stop` position is NOT included.

---

# 🧠 Genius Corner — Strings Are Immutable

Try:

```python
word = "Python"

word[0] = "J"
```

💥

Python refuses.

Strings are:

> **immutable**

Meaning the string object cannot be modified character-by-character.

Operations usually create a new string instead.

Keep that word in your head:

```text
MUTABLE
vs
IMMUTABLE
```

It's about to become very important.

---

# Chapter 13 — F-Strings: Stop Gluing Strings Together

We could write:

```python
name = "Upeka"
age = 27

print("My name is " + name + " and I am " + str(age))
```

Works.

Looks annoying.

Instead:

```python
print(f"My name is {name} and I am {age}.")
```

Much cleaner.

---

# Chapter 14 — Python Talks Back

So far WE give Python information.

But what if Python needs information from the user?

Meet:

```python
input()
```

Example:

```python
name = input("What's your name? ")

print("Hello", name)
```

Now Python waits for the user.

---

# ⚠️ The `input()` Trap

Suppose:

```python
age = input("Age: ")
```

You type:

```text
27
```

Surely Python has the number `27`?

Nope.

Python has:

```python
"27"
```

`input()` returns a **string**.

So:

```python
age = int(input("Age: "))
```

Now:

```text
Keyboard
   ↓
input()
   ↓
"27"
   ↓
int()
   ↓
27
```

## 🧠 Genius Corner

Why doesn't Python automatically know?

Because:

```text
123
```

could mean:

- Age
- Product code
- Username
- House number
- Password fragment
- Actual number

Python doesn't assume.

**The programmer decides what the data means.**

---

# Chapter 15 — Python Gets a Calculator 🧮

Arithmetic operators:

```python
10 + 3
```

Addition.

```python
10 - 3
```

Subtraction.

```python
10 * 3
```

Multiplication.

```python
10 / 3
```

Division.

```python
10 // 3
```

Floor division.

```python
10 % 3
```

Remainder.

```python
10 ** 3
```

Exponentiation.

---

# Chapter 16 — Modulus Is More Useful Than It Looks

Want to know whether a number is even?

```python
number = 8

if number % 2 == 0:
    print("Even")
```

Because:

```text
8 ÷ 2
```

leaves remainder:

```text
0
```

Modulus appears everywhere in programming.

---

# Chapter 17 — Comparison Operators

Python can ask questions:

```python
5 == 5
5 != 4
5 > 3
5 < 10
5 >= 5
5 <= 10
```

These produce:

```python
True
```

or:

```python
False
```

---

# Chapter 18 — Assignment Operators

Instead of:

```python
score = score + 5
```

we can write:

```python
score += 5
```

Also:

```python
score -= 5
score *= 2
score /= 2
```

---

# Chapter 19 — Logic 🧠

Suppose entry requires:

- Age ≥ 18
- ID

```python
age = 27
has_id = True

if age >= 18 and has_id:
    print("Welcome")
```

### `and`

Both must be true.

### `or`

At least one must be true.

### `not`

Reverses truthiness.

```python
is_raining = False

if not is_raining:
    print("Go outside")
```

---

# Chapter 20 — Membership Operators

```python
fruits = ["apple", "banana"]

"apple" in fruits
```

Result:

```python
True
```

Also:

```python
"mango" not in fruits
```

---

# Chapter 21 — Equality vs Identity 👀

This one separates memorizing Python from understanding Python.

```python
a = [1, 2]
b = [1, 2]
```

Then:

```python
a == b
```

asks:

> Do they contain equal values?

Result:

```python
True
```

But:

```python
a is b
```

asks:

> Are these literally the SAME object?

Result:

```python
False
```

So:

```text
== → equality

is → identity
```

Use:

```python
value is None
```

instead of:

```python
value == None
```

---

# Chapter 22 — Truthiness

Python can interpret many values as true or false.

Falsy examples:

```python
False
None
0
0.0
""
[]
{}
set()
```

Example:

```python
name = ""

if name:
    print("We have a name")
else:
    print("Name is empty")
```

---

# Chapter 23 — Python Starts Making Decisions 🚦

```python
age = 20

if age >= 18:
    print("Adult")
```

Two paths:

```python
if age >= 18:
    print("Adult")
else:
    print("Minor")
```

Several:

```python
score = 75

if score >= 90:
    print("Excellent")

elif score >= 70:
    print("Good")

else:
    print("Keep practicing")
```

---

# ⚠️ Indentation Is NOT Decoration

JavaScript:

```javascript
if (age >= 18) {
	console.log("Adult");
}
```

Python:

```python
if age >= 18:
    print("Adult")
```

Python uses indentation to understand structure.

So indentation is part of the language itself.

---

# Chapter 24 — Loops: Python Gets Tired of Repetition 🔁

Suppose we want:

```text
Hello
Hello
Hello
Hello
Hello
```

Please don't write:

```python
print("Hello")
print("Hello")
print("Hello")
print("Hello")
print("Hello")
```

Somewhere a programmer just screamed.

Use a loop.

---

# `for` Loop

```python
for number in range(5):
    print(number)
```

Result:

```text
0
1
2
3
4
```

Notice:

```python
range(5)
```

stops BEFORE `5`.

General form:

```python
range(start, stop, step)
```

---

# Loop Through Collections

```python
fruits = ["apple", "banana", "mango"]

for fruit in fruits:
    print(fruit)
```

Python visits each item.

Need the position too?

```python
for index, fruit in enumerate(fruits):
    print(index, fruit)
```

Need to pair sequences?

```python
names = ["Ana", "Ben"]
scores = [90, 82]

for name, score in zip(names, scores):
    print(name, score)
```

---

# `while` Loop

`while` means:

> Keep doing this while the condition remains true.

```python
energy = 3

while energy > 0:

    print("Working")

    energy -= 1
```

Conceptually:

```text
3 → work
2 → work
1 → work
0 → STOP
```

Forget:

```python
energy -= 1
```

and congratulations...

♾️ **Infinite loop.**

---

# Emergency Buttons 🚨

## `break`

> GET ME OUT.

```python
for number in range(10):

    if number == 5:
        break

    print(number)
```

## `continue`

> Skip this one.

```python
for number in range(5):

    if number == 2:
        continue

    print(number)
```

## `pass`

> Do absolutely nothing for now.

```python
if condition:
    pass
```

Useful as a placeholder.

---

# 🎯 MODULE 1 BOSS FIGHT

I should be able to explain:

- What Python is
- How Python code runs
- Variables as names bound to objects
- `int`, `float`, `str`, `bool`, `None`
- Type conversion
- String indexing and slicing
- Immutability
- Input/output
- Arithmetic operators
- Comparison operators
- Logical operators
- Membership
- Equality vs identity
- Truthiness
- `if / elif / else`
- `for`
- `while`
- `range()`
- `enumerate()`
- `zip()`
- `break`
- `continue`
- `pass`

If I can explain those **without reading their definitions**, Module 1 is actually in my brain.

---

# 🧰 MODULE 2 — THE PROGRAMMER'S TOOLBOX

Our programs work.

But they're about to get messy.

Imagine copying the same 20 lines every time we calculate a restaurant bill.

Absolutely not.

Time for functions.

---

# Chapter 25 — Functions

Define:

```python
def greet():
    print("Hello")
```

Call:

```python
greet()
```

A function doesn't execute merely because it was defined.

It waits until it's called.

---

# Parameters vs Arguments

```python
def greet(name):
    print(name)
```

`name` is the:

> parameter

Here:

```python
greet("Upeka")
```

`"Upeka"` is the:

> argument

---

# `return` — Give Me Something Back

```python
def add(a, b):
    return a + b
```

Then:

```python
result = add(5, 3)
```

Now:

```python
result
```

contains:

```text
8
```

---

# ⚠️ `print()` vs `return`

These are NOT equivalent:

```python
def add(a, b):
    print(a + b)
```

and:

```python
def add(a, b):
    return a + b
```

`print()`:

> displays something.

`return`:

> sends a value back to the caller.

Returned values can be:

- Stored
- Tested
- Passed elsewhere
- Transformed
- Reused

---

# Default Parameters

```python
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}"
```

Now:

```python
greet("Ana")
```

uses:

```text
Hello
```

But:

```python
greet("Ana", "Hi")
```

replaces it.

---

# Keyword Arguments

```python
greet(
    name="Ana",
    greeting="Good morning"
)
```

This can make calls more readable.

---

# 🧠 Genius Corner — Functions Are Abstraction

Functions aren't merely:

> "a way to avoid repeated code."

They allow us to hide complexity.

Imagine:

```python
total = calculate_total(order)
```

We don't need to think about every calculation every time.

We trust the abstraction:

```text
order
  ↓
calculate_total()
  ↓
total
```

That ability to hide unnecessary detail is one of the foundations of software engineering.

---

# Chapter 26 — Scope: Who Can See My Variable? 👀

```python
def make_coffee():

    size = "large"

    print(size)
```

`size` exists locally inside the function.

Outside:

```python
print(size)
```

💥

Python can't find it.

---

# LEGB Rule 🧠

Python looks for names roughly in this order:

```text
L → Local

E → Enclosing

G → Global

B → Built-in
```

Example built-in:

```python
print()
len()
sum()
```

---

# Chapter 27 — Lists 🛒

```python
fruits = [
    "apple",
    "banana",
    "mango"
]
```

Lists are:

```text
Ordered
Mutable
Indexable
Allow duplicates
```

Access:

```python
fruits[0]
```

Change:

```python
fruits[0] = "pear"
```

Add:

```python
fruits.append("orange")
```

Insert:

```python
fruits.insert(1, "kiwi")
```

Remove:

```python
fruits.remove("banana")
```

Pop:

```python
fruit = fruits.pop()
```

---

# Chapter 28 — List Comprehensions

Normal:

```python
squares = []

for number in range(5):
    squares.append(number ** 2)
```

Pythonic:

```python
squares = [
    number ** 2
    for number in range(5)
]
```

Condition:

```python
evens = [
    number
    for number in range(10)
    if number % 2 == 0
]
```

Beautiful when readable.

Terrifying when someone tries to fit an entire application inside one comprehension. 😂

---

# Chapter 29 — MUTABILITY 🧠

This concept is HUGE.

```python
a = [1, 2]

b = a
```

Memory model:

```text
a ───┐
     ├────→ [1, 2]
b ───┘
```

Now:

```python
b.append(3)
```

Result:

```text
a ───┐
     ├────→ [1, 2, 3]
b ───┘
```

So:

```python
print(a)
```

gives:

```text
[1, 2, 3]
```

Because we didn't copy the list.

We created another reference to the SAME object.

---

# Copying Lists

```python
b = a.copy()
```

or:

```python
b = a[:]
```

This creates a **shallow copy**.

Later, nested objects will make the shallow/deep-copy distinction important.

---

# Chapter 30 — Tuples 📦

```python
coordinates = (10, 20)
```

Tuples are:

```text
Ordered
Immutable
Allow duplicates
```

Unpack:

```python
x, y = coordinates
```

Python even lets us swap:

```python
a, b = b, a
```

One-item tuple:

```python
(5,)
```

Not:

```python
(5)
```

The comma matters.

---

# Chapter 31 — Sets 🎟️

```python
numbers = {1, 2, 3}
```

Sets contain unique values.

```python
{1, 1, 2, 2, 3}
```

becomes conceptually:

```text
1
2
3
```

Operations:

```python
a | b
```

Union.

```python
a & b
```

Intersection.

```python
a - b
```

Difference.

```python
a ^ b
```

Symmetric difference.

Empty set:

```python
set()
```

Because:

```python
{}
```

means empty dictionary.

---

# Chapter 32 — Dictionaries 🗄️

A dictionary stores:

```text
KEY → VALUE
```

Example:

```python
person = {
    "name": "Upeka",
    "age": 27,
    "city": "Riga"
}
```

Access:

```python
person["name"]
```

Safer lookup:

```python
person.get("country")
```

Fallback:

```python
person.get("country", "Unknown")
```

Add/change:

```python
person["language"] = "Python"
```

Iterate:

```python
for key, value in person.items():
    print(key, value)
```

---

# 🧠 Genius Corner — Hashability

Dictionary keys and set elements need to be:

> **hashable**

Common examples:

```python
"hello"
42
(1, 2)
```

A mutable list:

```python
[1, 2]
```

cannot normally be a dictionary key.

Why?

Because hash-based structures need a stable way to locate their keys.

If a key could change unpredictably after being stored, things would get messy very quickly.

---

# Choosing Data Structures

```text
Need ordered + changeable?

→ list


Need ordered but immutable?

→ tuple


Need unique values?

→ set


Need key → value relationships?

→ dictionary
```

---

# Chapter 33 — `*args`

Sometimes we don't know how many positional arguments will arrive.

```python
def add_all(*numbers):
    return sum(numbers)
```

Call:

```python
add_all(1, 2, 3, 4)
```

Inside the function:

```python
numbers
```

is a tuple.

---

# Chapter 34 — `**kwargs`

Unknown number of keyword arguments:

```python
def profile(**details):
    print(details)
```

Call:

```python
profile(
    name="Upeka",
    city="Riga"
)
```

Inside:

```python
details
```

is a dictionary.

`args` and `kwargs` are conventions.

The important pieces are:

```text
*
**
```

---

# Chapter 35 — Errors 💥

Errors are not Python insulting us.

They're Python giving us evidence.

Three useful categories:

### Syntax Error

Python can't understand the structure.

### Runtime Exception

Python starts running, then something goes wrong.

Example:

```python
10 / 0
```

```text
ZeroDivisionError
```

### Logical Error

The program runs...

but the answer is wrong.

```python
def area(width, height):
    return width + height
```

Perfectly valid Python.

Terrible rectangle maths. 😂

---

# Chapter 36 — Exception Handling

```python
try:

    number = int(input("Number: "))

except ValueError:

    print("Please enter a number")
```

More complete:

```python
try:

    number = int(input("Number: "))
    result = 100 / number

except ValueError:

    print("Invalid number")

except ZeroDivisionError:

    print("Cannot divide by zero")

else:

    print(result)

finally:

    print("Finished")
```

Mental model:

```text
try
↓
attempt risky code


except
↓
handle failure


else
↓
runs if no exception


finally
↓
runs regardless
```

---

# Raising Errors

We can deliberately say:

> This value is unacceptable.

```python
def set_age(age):

    if age < 0:
        raise ValueError(
            "Age cannot be negative"
        )
```

---

# Chapter 37 — Files 📁

Variables disappear when the program ends.

Files allow information to persist.

Basic:

```python
file = open(
    "notes.txt",
    "r"
)

content = file.read()

file.close()
```

Better:

```python
with open(
    "notes.txt",
    "r",
    encoding="utf-8"
) as file:

    content = file.read()
```

The `with` statement uses a **context manager** and helps ensure the file is closed correctly.

---

# File Modes

| Mode | Meaning           |
| ---- | ----------------- |
| `r`  | Read              |
| `w`  | Write / overwrite |
| `a`  | Append            |
| `x`  | Create            |
| `b`  | Binary            |
| `t`  | Text              |

⚠️ Be careful with:

```python
"w"
```

It can truncate an existing file.

Tiny letter.

Potentially catastrophic afternoon. 😭

---

# 🧠 MODULE 3 — PROGRAMMING PARADIGMS

A programming paradigm is basically:

> A style of thinking about and structuring programs.

Python supports several.

Our three kingdoms are:

```text
Procedural

Functional

Object-Oriented
```

---

# Chapter 38 — Procedural Programming 👣

Procedural programming thinks:

> What steps should happen?

Like cooking pasta:

```text
Boil water
↓
Add pasta
↓
Wait
↓
Drain
↓
Add sauce
↓
Serve
```

Code:

```python
def calculate_total(prices):

    total = 0

    for price in prices:
        total += price

    return total
```

Simple.

Direct.

Very useful.

---

# Chapter 39 — Algorithms 🧠

An algorithm is:

> A finite sequence of steps for solving a problem.

Suppose:

```python
numbers = [5, 2, 9, 7]
```

We need to find:

```text
7
```

One approach:

```python
for number in numbers:

    if number == 7:
        print("Found")
        break
```

This is a form of:

> Linear search.

But computer scientists don't only ask:

> Does it work?

They also ask:

> What happens when our list contains 10 million items?

Welcome to...

---

# Chapter 40 — Big-O 📈

Big-O describes how resource requirements grow as the input grows.

Common complexities:

```text
O(1)
Constant

O(log n)
Logarithmic

O(n)
Linear

O(n log n)
Linearithmic

O(n²)
Quadratic

O(2^n)
Exponential

O(n!)
Factorial
```

---

# O(1)

```python
first = numbers[0]
```

Whether there are:

```text
10 items
```

or:

```text
10,000,000 items
```

we directly access one position.

---

# O(n)

```python
for item in items:
    print(item)
```

More items means proportionally more iterations.

---

# O(n²)

```python
for a in items:

    for b in items:

        print(a, b)
```

Nested full loops.

Things get expensive quickly.

---

# O(log n)

Binary search is the classic example.

Instead of checking everything:

```text
1000 possibilities
↓
500
↓
250
↓
125
↓
...
```

we repeatedly reduce the search space.

---

# 🧠 Big-O Does NOT Mean Exact Runtime

Big-O does NOT tell us:

```text
"This function takes exactly 2 seconds."
```

It describes:

> How resource use grows as input size grows.

Actual speed also depends on:

- Hardware
- Implementation
- Constants
- Input
- Environment

We can also analyze:

```text
Time complexity

Space complexity
```

---

# Chapter 41 — Functional Programming 🧪

Functional programming places functions at the center.

One important idea:

> Pure functions.

```python
def add(a, b):
    return a + b
```

Given:

```text
2 and 3
```

it consistently produces:

```text
5
```

without changing unrelated external state.

Pure functions are often easier to:

- Test
- Understand
- Predict
- Reuse

---

# Functions Are Objects 🤯

In Python:

```python
def greet(name):
    return f"Hello {name}"
```

We can do:

```python
say_hello = greet
```

Then:

```python
say_hello("Upeka")
```

Functions can be:

- Assigned
- Passed
- Returned

They are:

> **first-class objects**

---

# `map()`

Transform items:

```python
numbers = [1, 2, 3]

squares = map(
    lambda n: n ** 2,
    numbers
)
```

---

# `filter()`

Keep matching items:

```python
evens = filter(
    lambda n: n % 2 == 0,
    numbers
)
```

Python often uses comprehensions instead:

```python
squares = [
    n ** 2
    for n in numbers
]
```

---

# Lambda Functions

Tiny anonymous functions:

```python
lambda x: x ** 2
```

Equivalent idea:

```python
def square(x):
    return x ** 2
```

Lambdas are great when tiny.

If your lambda looks like ancient Sanskrit...

use `def`. 😂

---

# Chapter 42 — Recursion 🪞

Recursion happens when a function calls itself.

Factorial:

```text
5!

5 × 4 × 3 × 2 × 1
```

Python:

```python
def factorial(n):

    if n <= 1:
        return 1

    return n * factorial(n - 1)
```

The crucial part:

```python
if n <= 1:
```

is the:

> **base case**

Without a stopping condition, recursion continues until Python's recursion limit is reached.

---

# Chapter 43 — OOP 🏙️

Object-Oriented Programming organizes programs around:

> Objects.

Suppose we have customers.

Instead of:

```python
customer1_name = "Ana"
customer1_points = 20

customer2_name = "Ben"
customer2_points = 10
```

we describe:

> What IS a customer?

---

# Classes

```python
class Customer:
    pass
```

A class is a blueprint/type definition.

An object created from it is an:

> **instance**

```python
customer1 = Customer()
customer2 = Customer()
```

---

# Chapter 44 — `__init__`

```python
class Customer:

    def __init__(
        self,
        name,
        points
    ):

        self.name = name
        self.points = points
```

Create:

```python
customer = Customer(
    "Ana",
    20
)
```

---

# `self`

```python
self.name
```

`self` refers to:

> the current instance.

When:

```python
customer.greet()
```

Python provides the instance to the method.

---

# Methods

```python
class Customer:

    def __init__(self, name):
        self.name = name

    def greet(self):
        return f"Hello, I'm {self.name}"
```

---

# Chapter 45 — The Four Pillars of OOP 🏛️

```text
Encapsulation
Abstraction
Inheritance
Polymorphism
```

These are worth understanding, not merely memorizing.

---

# 1. Encapsulation 🔒

Keep related data and behavior together and control interaction with internal state.

```python
class BankAccount:

    def __init__(self):
        self._balance = 0

    def deposit(self, amount):

        if amount > 0:
            self._balance += amount
```

Python commonly uses:

```python
_name
```

to communicate:

> Internal implementation detail.

---

# 2. Abstraction 🎛️

Hide unnecessary complexity.

We call:

```python
account.deposit(100)
```

We don't need to know every internal step.

Like driving a car:

```text
Steering wheel
Brake
Accelerator
```

We don't manually control the engine's combustion process.

---

# 3. Inheritance 🌳

```python
class Animal:

    def speak(self):
        return "Sound"


class Dog(Animal):

    def speak(self):
        return "Woof"
```

`Dog` inherits from:

```text
Animal
```

---

# `super()`

```python
class Developer(Employee):

    def __init__(
        self,
        name,
        language
    ):

        super().__init__(name)

        self.language = language
```

---

# 4. Polymorphism 🎭

Different objects respond to the same interface differently.

```python
dog.speak()
cat.speak()
```

Same:

```text
speak()
```

Different behavior.

Python also commonly embraces:

> **Duck typing**

If something behaves like the object we need, its exact type may not matter.

---

# Chapter 46 — Abstract Classes

Sometimes a parent class should say:

> Every child MUST provide this behavior.

```python
from abc import (
    ABC,
    abstractmethod
)


class Shape(ABC):

    @abstractmethod
    def area(self):
        pass
```

Then:

```python
class Rectangle(Shape):

    def area(self):
        return (
            self.width
            * self.height
        )
```

---

# Chapter 47 — MRO 🧬

Python allows multiple inheritance.

```python
class C(A, B):
    pass
```

But if both parents have the same method...

who gets asked first?

Python needs rules.

That's:

> **Method Resolution Order**

Inspect:

```python
C.mro()
```

---

# 🧠 Genius Corner — `super()`

Beginner explanation:

> `super()` calls the parent.

Better explanation:

> `super()` continues method lookup according to Python's MRO.

That distinction becomes important with multiple inheritance.

---

# Chapter 48 — Dunder Methods ✨

You've already seen:

```python
__init__
```

These double-underscore methods connect objects to Python's behavior.

Examples:

```text
__init__
__str__
__repr__
__len__
__eq__
__add__
```

Example:

```python
class Book:

    def __init__(self, title):
        self.title = title

    def __str__(self):
        return self.title
```

Now:

```python
print(book)
```

can use:

```python
__str__()
```

---

# 🏗️ MODULE 4 — MODULES, PACKAGES, LIBRARIES & TOOLS

We now know how to build things.

But should we build EVERYTHING ourselves?

Absolutely not. 😭

Programmers reuse code.

---

# Chapter 49 — Modules

Suppose:

```text
calculator.py
```

contains:

```python
def add(a, b):
    return a + b
```

Another file:

```python
import calculator
```

Then:

```python
calculator.add(2, 3)
```

Specific import:

```python
from calculator import add
```

Alias:

```python
import calculator as calc
```

---

# Standard Library

Python already ships with many modules.

```python
import math
import random
import datetime
import json
import pathlib
```

Example:

```python
import math

math.sqrt(25)
```

Before installing something, it's worth asking:

> Does Python already have this?

---

# Chapter 50 — `__name__ == "__main__"`

This strange-looking thing:

```python
if __name__ == "__main__":
```

actually solves an important problem.

When a Python file runs directly:

```python
__name__
```

is:

```text
"__main__"
```

So:

```python
def main():
    print("Running")


if __name__ == "__main__":
    main()
```

means:

> Run `main()` only when this file is executed directly.

If another file imports it, that application entry point doesn't automatically run.

---

# Chapter 51 — Packages

As projects grow:

```text
restaurant/
│
├── __init__.py
├── menu.py
├── orders.py
└── payments.py
```

Useful mental model:

```text
Module
↓
Reusable Python code unit/file


Package
↓
Organizes modules/subpackages


Library
↓
Broader reusable collection
```

---

# Chapter 52 — `pip`

Third-party packages can be installed using:

```bash
python -m pip install pytest
```

Using:

```bash
python -m pip
```

helps ensure we're using `pip` associated with the Python interpreter we selected.

---

# Chapter 53 — Virtual Environments 🚪

Imagine:

```text
Project A needs Package v1

Project B needs Package v2
```

Uh-oh.

Virtual environments isolate dependencies.

Create:

```bash
python -m venv .venv
```

Conceptually:

```text
Project A
↓
Environment A
↓
Dependencies A


Project B
↓
Environment B
↓
Dependencies B
```

No dependency soup. 🍲

---

# Chapter 54 — Python for Data, ML & AI 🤖

Python's ecosystem is one reason it's so powerful.

### NumPy

Numerical computing.

```python
import numpy as np
```

### pandas

Tabular data analysis.

```python
import pandas as pd
```

### Matplotlib

Visualization.

```python
import matplotlib.pyplot as plt
```

### scikit-learn

Machine learning.

```python
from sklearn.ensemble import IsolationForest
```

## 🧠 Genius Corner

Knowing Python does NOT mean memorizing every library.

Good developers know:

```text
Language fundamentals
+
Problem solving
+
Documentation
+
Relevant libraries
```

---

# Chapter 55 — Testing 🧪

Suppose:

```python
def add(a, b):
    return a + b
```

We expect:

```python
add(2, 3)
```

to produce:

```text
5
```

A test can express that expectation:

```python
def test_add():
    assert add(2, 3) == 5
```

Tests help us:

- Catch regressions
- Document expected behavior
- Refactor safely
- Increase confidence
- Design cleaner components

Tests do NOT magically prove that a complex application contains zero bugs.

---

# Types of Testing

### Unit Testing

Test a small unit:

```text
function
method
class
```

### Integration Testing

Test components working together.

### System / End-to-End Testing

Test larger workflows.

### Regression Testing

Make sure previously working behavior still works after changes.

---

# Chapter 56 — PyTest

Install:

```bash
python -m pip install pytest
```

Project:

```text
project/
│
├── calculator.py
└── test_calculator.py
```

Test:

```python
from calculator import add


def test_add():

    assert add(2, 3) == 5
```

Run:

```bash
pytest
```

---

# Testing Exceptions

```python
import pytest


def test_zero():

    with pytest.raises(ValueError):

        divide(10, 0)
```

---

# Fixtures

Reusable test setup:

```python
import pytest


@pytest.fixture
def sample_numbers():

    return [1, 2, 3]


def test_length(sample_numbers):

    assert len(sample_numbers) == 3
```

---

# Chapter 57 — TDD 🚦

Test-Driven Development changes the order.

Instead of:

```text
Write code
↓
Maybe test later
```

we do:

```text
🔴 RED
Write failing test

↓

🟢 GREEN
Write minimum code to pass

↓

🔧 REFACTOR
Improve code

↓

Repeat
```

---

# Example

First:

```python
def test_discount():

    assert (
        calculate_discount(
            100,
            10
        )
        == 90
    )
```

It fails.

Good.

We've defined expected behavior.

Now:

```python
def calculate_discount(
    price,
    percent
):

    return (
        price
        - price * percent / 100
    )
```

Test passes.

Then refactor safely.

---

# 🧠 Genius Corner — TDD

TDD isn't simply:

> Write tests.

It's:

> Use tests as part of the design process.

That's a much deeper idea.

---

# 🎁 BONUS — THINGS THAT MAKE PYTHON REALLY CLICK

These go slightly beyond the basic course but connect everything together.

---

# Iterables vs Iterators

A list is iterable:

```python
numbers = [1, 2, 3]
```

Create iterator:

```python
iterator = iter(numbers)
```

Then:

```python
next(iterator)
```

returns the next value.

A `for` loop essentially consumes an iterator until there are no items left.

---

# Generators

Generators produce values lazily.

```python
def countdown(n):

    while n > 0:

        yield n

        n -= 1
```

Then:

```python
for number in countdown(3):
    print(number)
```

A generator doesn't necessarily create every result in memory at once.

---

# Type Hints

```python
def add(
    a: int,
    b: int
) -> int:

    return a + b
```

Python remains dynamically typed.

Type hints communicate intent and help tools analyze code.

---

# Docstrings

```python
def calculate_total(prices):
    """
    Return the sum of all prices.
    """

    return sum(prices)
```

Docstrings document functions, classes and modules.

---

# PEP 8

Common Python style conventions:

```text
snake_case
→ variables/functions

PascalCase
→ classes

UPPER_CASE
→ constants by convention

4 spaces
→ indentation
```

Readable code is not decoration.

It's part of good engineering.

---

# 🏛️ THE PYTHON TRAP MUSEUM

## Trap 1 — Mutable Default Arguments

Danger:

```python
def add_item(
    item,
    items=[]
):

    items.append(item)

    return items
```

That default list can persist between calls.

Safer:

```python
def add_item(
    item,
    items=None
):

    if items is None:
        items = []

    items.append(item)

    return items
```

---

# Trap 2 — Assignment Doesn't Copy

```python
b = a
```

doesn't necessarily mean:

> Make a new object.

It may simply mean:

> Make another name refer to the same object.

---

# Trap 3 — `sort()` vs `sorted()`

```python
numbers.sort()
```

changes the list in place and returns:

```python
None
```

Whereas:

```python
new_numbers = sorted(numbers)
```

returns a new sorted list.

---

# Trap 4 — Shadowing Built-Ins

Don't casually do:

```python
list = [1, 2]

str = "hello"
```

Now you've hidden Python's built-in names:

```python
list
str
```

inside that scope.

---

# Trap 5 — Read the Traceback!

When Python crashes, don't just stare at the red text in betrayal. 😭

Look for:

```text
Exception type
↓
Message
↓
File
↓
Line number
↓
Call stack
```

Errors are clues.

---

# 🔄 JAVASCRIPT → PYTHON CHEAT BRIDGE

| Concept               | JavaScript         | Python         |
| --------------------- | ------------------ | -------------- | --- | ---- |
| Variable              | `let x = 10`       | `x = 10`       |
| Output                | `console.log()`    | `print()`      |
| Boolean               | `true / false`     | `True / False` |
| Null-ish value        | `null / undefined` | `None`         |
| AND                   | `&&`               | `and`          |
| OR                    | `                  |                | `   | `or` |
| NOT                   | `!`                | `not`          |
| Blocks                | `{ }`              | indentation    |
| Function              | `function()`       | `def`          |
| Array-like collection | Array              | List           |
| Key/value structure   | Object / Map       | Dictionary     |
| Current instance      | `this`             | `self`         |
| Exception             | `try/catch`        | `try/except`   |
| Interpolation         | Template literal   | f-string       |

But remember:

> JavaScript is a bridge to Python—not a translator.

The languages have different object models, scoping behavior, idioms and ecosystems.

---

# 🧪 ZERO → HERO PROJECT ROADMAP

Reading gives familiarity.

**Building gives skill.**

### Project 1 — Tip Calculator

Learn:

```text
input
types
conversion
math
f-strings
```

### Project 2 — Number Detective

Learn:

```text
conditions
boolean logic
modulus
```

### Project 3 — Restaurant Bill Calculator

Learn:

```text
functions
loops
lists
dictionaries
validation
```

### Project 4 — Word Counter

Learn:

```text
strings
files
dictionaries
loops
```

### Project 5 — Expense Tracker

Learn:

```text
functions
collections
exceptions
files
```

### Project 6 — OOP Restaurant System

Build:

```text
MenuItem

Customer

Order

Restaurant
```

### Project 7 — Tested Application

Use:

```text
PyTest
unit tests
edge cases
exception tests
fixtures
```

### Project 8 — TDD Feature

Build strictly:

```text
RED
↓
GREEN
↓
REFACTOR
```

---

# 👑 FINAL BOSS QUESTIONS

If I can explain these without Googling the definition, I'm actually learning Python.

1. Why are variables better understood as names bound to objects?
2. What is mutable vs immutable?
3. Why can changing `b` sometimes appear to change `a`?
4. What's shallow copying?
5. Why does `input()` return a string?
6. What's `==` vs `is`?
7. Why are dictionary keys hashable?
8. What's `print()` vs `return`?
9. Parameter vs argument?
10. What is LEGB?
11. List vs tuple vs set vs dictionary?
12. `*args` vs `**kwargs`?
13. Syntax error vs runtime exception vs logical error?
14. Why use `with` for files?
15. What does Big-O actually tell me?
16. Time complexity vs space complexity?
17. What makes a function pure?
18. Why are functions first-class objects?
19. `map()` vs `filter()`?
20. Why does recursion need a base case?
21. Class vs instance?
22. What exactly is `self`?
23. Encapsulation vs abstraction?
24. Inheritance vs polymorphism?
25. What is duck typing?
26. Why do abstract classes exist?
27. What problem does MRO solve?
28. What does `super()` actually do?
29. Module vs package vs library?
30. Why use a virtual environment?
31. What problem does testing solve?
32. Unit vs integration vs system testing?
33. What is a PyTest fixture?
34. What is Red → Green → Refactor?
35. Why can readable boring code be better than clever code?

---

# 📓 THINGS I KEEP FORGETTING

```text
input() returns str

range() excludes the stop value

True / False / None use capitals

= assigns

== compares equality

is compares identity

list / dict / set are mutable

tuple / str / int are immutable

dict keys and set elements must be hashable

return sends a value back

print displays a value

indentation defines blocks

"w" can overwrite a file

with helps manage resources safely

recursion needs a base case

self refers to the current instance by convention

super() follows the MRO

tests are executable expectations
```

---

# 🚀 THE REAL ZERO → HERO PATH

Finishing a Python course doesn't magically make someone a Python master.

It gives us the vocabulary.

Real skill begins when we can do this:

```text
Understand the problem
        ↓
Break it into smaller problems
        ↓
Choose suitable data structures
        ↓
Design functions/classes
        ↓
Write code
        ↓
Test
        ↓
Read errors
        ↓
Debug
        ↓
Refactor
        ↓
Explain WHY the solution works
```

The goal isn't:

> "I memorized Python."

The goal is:

> **"I understand programming well enough that when I meet something I don't know, I can reason about it, experiment, read the documentation, and figure it out."**

That's where **zero → hero** actually begins. 🐍👑
