# Python Interview Questions & Answers

Questions based on the GeeksforGeeks "Python Interview Questions" page
(https://www.geeksforgeeks.org/python/python-interview-questions/). Answers are original explanations.

---

## Basic Python Interview Questions (Q1–Q23)

### 1. Is Python a compiled language or an interpreted language?
Both, in stages. CPython first compiles source (`.py`) into bytecode (`.pyc`), then the Python Virtual Machine interprets that bytecode at runtime. Because the compile step is automatic and invisible, Python is usually called interpreted. Some implementations (e.g. PyPy) add a JIT compiler that turns hot code into machine code.

### 2. What is a dynamically typed language?
A language where types belong to values, not variables, and are checked at runtime. You don't declare types; a name can hold an `int` now and a `str` later.
```python
x = 10      # int
x = "ten"   # now a str — perfectly legal
```
Statically typed languages (C, Java) fix the type at compile time.

### 3. Is indentation required in Python?
Yes. Indentation defines code blocks (function bodies, loops, `if` branches) instead of braces. Inconsistent indentation raises `IndentationError`. PEP 8 recommends 4 spaces.

### 4. What are the built-in data types in Python?
- **Numeric:** `int`, `float`, `complex`
- **Boolean:** `bool`
- **Sequence:** `str`, `list`, `tuple`, `range`
- **Set:** `set`, `frozenset`
- **Mapping:** `dict`
- **Binary:** `bytes`, `bytearray`, `memoryview`
- **None type:** `NoneType`

### 5. What is the difference between a mutable and an immutable data type?
Mutable objects can be changed in place after creation (`list`, `dict`, `set`, `bytearray`). Immutable objects cannot; any "change" creates a new object (`int`, `float`, `str`, `tuple`, `frozenset`, `bytes`). Only immutable (hashable) objects can be dict keys or set members.

### 6. What is variable scope in Python?
Scope is the region where a name is visible. Python resolves names with the **LEGB** rule:
- **L**ocal — inside the current function
- **E**nclosing — inside outer (enclosing) functions
- **G**lobal — module level
- **B**uilt-in — names like `len`, `print`

Use `global` or `nonlocal` to assign to names in outer scopes.

### 7. How do you floor and ceil a number in Python?
```python
import math
math.floor(3.7)   # 3  (largest integer <= x)
math.ceil(3.2)    # 4  (smallest integer >= x)
math.floor(-3.7)  # -4
```

### 8. What is the difference between `/` and `//` in Python?
`/` is true division and always returns a `float`. `//` is floor division: it rounds down toward negative infinity.
```python
7 / 2    # 3.5
7 // 2   # 3
-7 // 2  # -4
```

### 9. What is the difference between a `for` loop and a `while` loop?
`for` iterates over an iterable (list, range, string, etc.), so it's used when you know what you're looping over. `while` repeats as long as a condition stays true, so it's used when the number of iterations isn't known in advance.
```python
for i in range(3): print(i)

n = 3
while n > 0:
    n -= 1
```

### 10. Can we pass a function as an argument in Python?
Yes. Functions are first-class objects, so they can be passed, returned and stored in variables. Functions that take or return other functions are called higher-order functions.
```python
def apply(f, x):
    return f(x)

apply(abs, -5)  # 5
```

### 11. What is `pass` in Python?
A no-op statement used as a placeholder where syntax requires a statement but you don't want to run anything yet.
```python
def todo():
    pass

class Empty:
    pass
```

### 12. What are `break`, `continue` and `pass` in Python?
- `break` — exits the nearest enclosing loop immediately.
- `continue` — skips the rest of the current iteration and moves to the next.
- `pass` — does nothing.
```python
for i in range(10):
    if i == 2: continue   # skip 2
    if i == 5: break      # stop at 5
    print(i)              # 0 1 3 4
```

### 13. Are arguments passed by value or by reference in Python?
Neither exactly — Python uses **pass by object reference** (call by sharing). The function receives a reference to the same object. Mutating a mutable object (e.g. `list.append`) is visible to the caller; rebinding the parameter (`x = ...`) is not.
```python
def f(lst, n):
    lst.append(1)  # visible outside
    n += 1         # not visible outside

a, b = [], 0
f(a, b)
print(a, b)  # [1] 0
```

### 14. What is a lambda function?
An anonymous, single-expression function. Useful for short callbacks.
```python
square = lambda x: x * x
sorted(["bb", "a", "ccc"], key=lambda s: len(s))  # ['a', 'bb', 'ccc']
```

### 15. How is a dictionary different from a list?
A list is an ordered sequence accessed by integer index. A dict maps unique, hashable keys to values and is accessed by key. Dict lookup is O(1) on average; searching a list for a value is O(n). Since Python 3.7, dicts preserve insertion order.

### 16. What is list comprehension? Give an example.
A concise way to build a list from an iterable, optionally with a filter.
```python
squares = [x ** 2 for x in range(5)]          # [0, 1, 4, 9, 16]
evens   = [x for x in range(10) if x % 2 == 0]
```

### 17. What are `*args` and `**kwargs`?
`*args` collects extra positional arguments into a tuple; `**kwargs` collects extra keyword arguments into a dict.
```python
def f(*args, **kwargs):
    print(args, kwargs)

f(1, 2, a=3)  # (1, 2) {'a': 3}
```
The same symbols unpack sequences/dicts at call sites: `f(*my_list, **my_dict)`.

### 18. What is the difference between a set and a dictionary?
A set stores unique, hashable values with no associated data (`{1, 2, 3}`). A dict stores key–value pairs (`{"a": 1}`). Note `{}` creates an empty dict; use `set()` for an empty set. Sets support math operations like union (`|`) and intersection (`&`).

### 19. How can you concatenate two lists in Python?
```python
a, b = [1, 2], [3, 4]
c = a + b        # new list [1, 2, 3, 4]
a.extend(b)      # modifies a in place
d = [*a, *b]     # unpacking
```

### 20. What is a docstring in Python?
A string literal placed as the first statement of a module, class or function to document it. It's stored in `__doc__` and shown by `help()`.
```python
def add(a, b):
    """Return the sum of a and b."""
    return a + b

print(add.__doc__)
```

### 21. How is exception handling done in Python?
With `try` / `except` / `else` / `finally`:
```python
try:
    result = 10 / 0
except ZeroDivisionError as e:
    print("Error:", e)
else:
    print("Runs only if no exception")
finally:
    print("Always runs (cleanup)")
```
You raise exceptions with `raise`.

### 22. What is the difference between Python arrays and lists?
`array.array` (from the `array` module) stores elements of a single numeric type compactly, which saves memory. A list can hold any mix of object types and is built in. For heavy numeric work, NumPy arrays are the usual choice.
```python
from array import array
arr = array('i', [1, 2, 3])   # ints only
lst = [1, "two", 3.0]         # anything
```

### 23. What are modules and packages in Python?
A **module** is a single `.py` file containing code you can import. A **package** is a directory of modules (traditionally with an `__init__.py`) that organizes related modules under one namespace.
```python
import math                 # module
from os import path         # submodule of a package
```

---

## Intermediate Python Interview Questions (Q24–Q41)

### 24. What is the difference between `xrange` and `range`?
In Python 2, `range()` built a full list in memory while `xrange()` produced values lazily. Python 3 removed `xrange`; its `range()` behaves like the old `xrange` — a lazy, memory-efficient sequence object.

### 25. What is dictionary comprehension? Give an example.
Like list comprehension, but builds a dict.
```python
keys = ["a", "b", "c"]
vals = [1, 2, 3]
d = {k: v for k, v in zip(keys, vals)}     # {'a': 1, 'b': 2, 'c': 3}
squares = {x: x * x for x in range(4)}
```

### 26. Is tuple comprehension possible in Python?
No. Parentheses around a comprehension create a **generator expression**, not a tuple. To get a tuple, pass the generator to `tuple()`:
```python
gen = (x * 2 for x in range(3))       # generator
tup = tuple(x * 2 for x in range(3))  # (0, 2, 4)
```

### 27. Differentiate between a list and a tuple.
| List | Tuple |
|---|---|
| Mutable | Immutable |
| `[1, 2]` | `(1, 2)` |
| More memory, more methods | Less memory, slightly faster |
| Not hashable | Hashable (if contents are), usable as dict keys |
| For collections that change | For fixed records |

### 28. What is the difference between a shallow copy and a deep copy?
A shallow copy creates a new outer container but shares the nested objects. A deep copy recursively copies everything, so the copy is fully independent.
```python
import copy
a = [[1, 2], [3]]
s = copy.copy(a)
d = copy.deepcopy(a)
a[0].append(99)
print(s[0])  # [1, 2, 99]  — shared
print(d[0])  # [1, 2]      — independent
```

### 29. Which sorting technique is used by `sort()` and `sorted()`?
**Timsort** — a hybrid of merge sort and insertion sort. It is stable, runs in O(n log n) worst case, and is very fast on partially ordered real-world data. (Since Python 3.11 it uses the Powersort merge policy, a refinement of Timsort.) `list.sort()` sorts in place; `sorted()` returns a new list from any iterable.

### 30. What are decorators?
A decorator is a callable that takes a function and returns a new function that wraps or extends it, without changing the original's code. Applied with `@` syntax. Common uses: logging, timing, caching, access control.
```python
import functools

def log(func):
    @functools.wraps(func)
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__}")
        return func(*args, **kwargs)
    return wrapper

@log
def greet(name):
    return f"Hi {name}"
```

### 31. How do you debug a Python program?
- **`pdb`** / `breakpoint()` — interactive debugger: step (`n`, `s`), continue (`c`), print (`p var`).
- **`logging`** — leveled messages (DEBUG, INFO, WARNING, ERROR, CRITICAL) instead of prints.
- **IDE debuggers** (VS Code, PyCharm) with breakpoints and variable inspection.
- **`assert`**, tracebacks, and unit tests to localize bugs.
```python
x = 5
breakpoint()   # drops into pdb here
```

### 32. What are iterators in Python?
An iterator is an object that implements `__iter__()` (returns itself) and `__next__()` (returns the next value or raises `StopIteration`). `for` loops use this protocol under the hood. `iter()` gets an iterator from an iterable; `next()` advances it.
```python
it = iter([1, 2, 3])
next(it)  # 1
next(it)  # 2
```

### 33. What are generators in Python?
Functions that use `yield` to produce values lazily, one at a time. Each `yield` pauses the function and saves its state; the next call resumes from there. They automatically implement the iterator protocol and are memory efficient for large or infinite sequences.
```python
def count_up(n):
    i = 0
    while i < n:
        yield i
        i += 1

list(count_up(3))  # [0, 1, 2]
```

### 34. Does Python support multiple inheritance?
Yes. A class can inherit from several base classes. Python resolves attribute lookup using the **Method Resolution Order (MRO)**, computed with the C3 linearization algorithm; view it with `ClassName.__mro__`. `super()` follows the MRO.
```python
class A: pass
class B: pass
class C(A, B): pass
print(C.__mro__)
```

### 35. What is polymorphism in Python?
The ability of different types to respond to the same interface. In Python it shows up as method overriding in subclasses, operator overloading (e.g. `+` on ints vs strings), and duck typing ("if it has the method, it works").
```python
class Dog:
    def speak(self): return "Woof"
class Cat:
    def speak(self): return "Meow"

for a in (Dog(), Cat()):
    print(a.speak())
```

### 36. Define encapsulation in Python.
Bundling data and the methods that operate on it inside a class, and restricting direct access to internal state. Python relies on convention: `_name` means internal, `__name` triggers name mangling. Controlled access is often done with `@property`.
```python
class Account:
    def __init__(self):
        self.__balance = 0
    @property
    def balance(self):
        return self.__balance
```

### 37. How do you do data abstraction in Python?
By exposing only essential behavior and hiding implementation details, typically with **abstract base classes** from the `abc` module. A class with an `@abstractmethod` can't be instantiated until subclasses implement it.
```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self): ...

class Square(Shape):
    def __init__(self, s): self.s = s
    def area(self): return self.s ** 2
```

### 38. How is memory management done in Python?
CPython manages memory automatically in a private heap. Key mechanisms:
- **Reference counting** — an object is freed as soon as its reference count reaches zero.
- **Cyclic garbage collector** (`gc` module) — finds and frees reference cycles that refcounting can't.
- **pymalloc** — a specialized allocator for small objects.
- Caching/interning of small ints and some strings.

### 39. How do you delete a file using Python?
```python
import os
os.remove("file.txt")          # delete a file

from pathlib import Path
Path("file.txt").unlink()      # same, pathlib style

os.rmdir("empty_dir")          # delete an empty directory
import shutil
shutil.rmtree("some_dir")      # delete a directory tree
```

### 40. What is slicing in Python?
Extracting part of a sequence (`str`, `list`, `tuple`) with `seq[start:stop:step]`. `start` is inclusive, `stop` exclusive; negative indices count from the end. Slicing returns a new object.
```python
s = "Python"
s[1:4]   # 'yth'
s[:2]    # 'Py'
s[::-1]  # 'nohtyP'
```

### 41. What is a namespace in Python?
A mapping from names to objects (essentially a dict). Separate namespaces prevent name clashes. Types:
- **Built-in** — created when the interpreter starts (`print`, `len`).
- **Global** — one per module.
- **Local** — created for each function call.
- **Enclosing** — for nested functions.

Scope (Q6) determines which namespace a name lookup uses.

---

## Advanced Python Interview Questions (Q42–Q54)

### 42. What is PIP?
pip is Python's standard package installer. It downloads and installs packages from PyPI (the Python Package Index) and manages them.
```bash
pip install requests
pip install -r requirements.txt
pip list
pip uninstall requests
```

### 43. What is the `zip()` function?
`zip()` takes several iterables and returns an iterator of tuples, pairing items by position. It stops at the shortest input (use `strict=True` in 3.10+ to require equal lengths).
```python
names = ["a", "b"]
ages = [1, 2]
list(zip(names, ages))  # [('a', 1), ('b', 2)]
```

### 44. What are pickling and unpickling?
Pickling serializes a Python object into a byte stream (`pickle.dump` / `pickle.dumps`); unpickling reconstructs the object from bytes (`pickle.load` / `pickle.loads`). Used for saving objects to disk or sending them between processes. Never unpickle data from untrusted sources — it can execute arbitrary code.
```python
import pickle
with open("data.pkl", "wb") as f:
    pickle.dump({"a": 1}, f)
with open("data.pkl", "rb") as f:
    data = pickle.load(f)
```

### 45. What is the difference between `@classmethod`, `@staticmethod` and instance methods?
- **Instance method** — takes `self`; works with a specific object's data.
- **Class method** — takes `cls`; works with the class itself (common for alternative constructors).
- **Static method** — takes neither; a plain function namespaced inside the class.
```python
class Date:
    def __init__(self, y): self.y = y
    def show(self): return self.y                  # instance
    @classmethod
    def from_str(cls, s): return cls(int(s))       # class
    @staticmethod
    def is_leap(y): return y % 4 == 0 and (y % 100 != 0 or y % 400 == 0)  # static
```

### 46. What is `__init__()` in Python, and what role does `self` play in it?
`__init__()` is the initializer called automatically after a new object is created; it sets up the object's attributes. (The object itself is created by `__new__()`.) `self` refers to the instance being initialized and must be the first parameter of instance methods, giving access to the object's attributes and methods.
```python
class Person:
    def __init__(self, name):
        self.name = name

p = Person("Ana")
```

### 47. Write code to display the current time.
```python
from datetime import datetime
print("Current time:", datetime.now().strftime("%H:%M:%S"))

# or with the time module
import time
print(time.strftime("%H:%M:%S", time.localtime()))
```

### 48. What are access specifiers in Python?
Python has no enforced access modifiers; it uses naming conventions:
- **Public:** `name` — accessible anywhere (default).
- **Protected:** `_name` — by convention, internal to the class and its subclasses.
- **Private:** `__name` — name-mangled to `_ClassName__name`, making accidental outside access harder.

### 49. What are unit tests in Python?
Tests that verify the smallest units of code (functions, methods) in isolation. Python ships with `unittest`; `pytest` is a popular third-party alternative.
```python
import unittest

def add(a, b): return a + b

class TestAdd(unittest.TestCase):
    def test_add(self):
        self.assertEqual(add(2, 3), 5)

if __name__ == "__main__":
    unittest.main()
```

### 50. What is the Python Global Interpreter Lock (GIL)?
A mutex in CPython that allows only one thread to execute Python bytecode at a time. It simplifies memory management but prevents threads from running CPU-bound Python code in parallel. Threads still help for I/O-bound work (the GIL is released while waiting on I/O). For CPU-bound parallelism, use `multiprocessing` or `concurrent.futures.ProcessPoolExecutor`. Since Python 3.13, an experimental free-threaded (no-GIL) build is available.

### 51. What are function annotations in Python?
Optional metadata attached to parameters and return values, most commonly used for type hints. Python stores them in `__annotations__` but doesn't enforce them; tools like mypy and IDEs use them.
```python
def greet(name: str, times: int = 1) -> str:
    return name * times

greet.__annotations__
```

### 52. What are exception groups in Python?
Introduced in Python 3.11, `ExceptionGroup` bundles several unrelated exceptions so they can be raised together (useful in concurrent code, e.g. `asyncio.TaskGroup`). They're handled with `except*`, where each clause handles matching exceptions from the group.
```python
try:
    raise ExceptionGroup("errors", [ValueError("bad"), TypeError("wrong")])
except* ValueError as eg:
    print("value errors:", eg.exceptions)
except* TypeError as eg:
    print("type errors:", eg.exceptions)
```

### 53. What is the Python switch statement?
Python 3.10 added **structural pattern matching** with `match` / `case`. `_` is the wildcard default case. It can also match on structure (sequences, dicts, class attributes), not just values.
```python
def http_status(code):
    match code:
        case 200:
            return "OK"
        case 404:
            return "Not Found"
        case 500 | 503:
            return "Server error"
        case _:
            return "Unknown"
```
Before 3.10, the common substitutes were `if`/`elif` chains or dict lookups.

### 54. What is the walrus operator?
The assignment expression `:=` (Python 3.8+). It assigns a value and returns it within an expression, avoiding repeated computation.
```python
data = [1, 2, 3, 4]
while (n := len(data)) > 0:
    print(data.pop(), "remaining:", n - 1)

if (m := len("hello")) > 3:
    print(m)
```