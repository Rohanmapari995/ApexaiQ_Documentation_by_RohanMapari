# Python Coding Standards (PEP 8)

## Overview

Python Coding Standards are a set of guidelines that help developers write **clean, readable, and maintainable** code. The official Python style guide is **PEP 8 (Python Enhancement Proposal 8)**.

---

## 1. Indentation

- Use **4 spaces** for each indentation level.
- Avoid using tabs.

```python
if x > 0:
    print("Positive")
```

---

## 2. Line Length

- Keep code lines within **79 characters**.
- Limit comments and docstrings to **72 characters**.

```python
message = (
    "This is a long string split across multiple lines."
)
```

---

## 3. Blank Lines

- Use **2 blank lines** between top-level functions and classes.
- Use **1 blank line** between methods inside a class.

```python
def add(a, b):
    return a + b


def subtract(a, b):
    return a - b
```

---

## 4. Naming Conventions

| Element | Convention | Example |
|---------|------------|---------|
| Variable | `snake_case` | `student_name` |
| Function | `snake_case` | `calculate_area()` |
| Class | `PascalCase` | `StudentRecord` |
| Constant | `UPPER_CASE` | `MAX_SIZE` |
| Module | `lowercase` | `math_utils.py` |
| Package | `lowercase` | `mypackage` |

---

## 5. Imports

Organize imports in the following order:

1. Standard library
2. Third-party libraries
3. Local modules

```python
import os
import sys

import numpy as np

from myproject import helper
```

---

## 6. Whitespace

Use spaces around operators and after commas.

```python
# Good
x = a + b
numbers = [1, 2, 3]

# Bad
x=a+b
```

---

## 7. Comments

Write comments that explain **why**, not **what**.

```python
# Increase timeout because the server responds slowly.
timeout = 30
```

---

## 8. Docstrings

Use docstrings to describe modules, classes, and functions.

```python
def square(x):
    """Return the square of a number."""
    return x * x
```

---

## 9. String Quotes

Be consistent when using single or double quotes.

```python
name = "Rohan"
city = 'Pune'
```

---

## 10. Boolean Comparisons

```python
# Good
if is_valid:

# Bad
if is_valid == True:
```

---

## 11. Checking for None

```python
# Good
if value is None:

# Bad
if value == None:
```

---

## 12. Exception Handling

Catch specific exceptions instead of using a generic `except`.

```python
try:
    number = int(input())
except ValueError:
    print("Invalid input")
```

---

## 13. List Comprehensions

Use list comprehensions for simple transformations.

```python
squares = [x * x for x in range(10)]
```

---

## 14. Constants

Define constants using uppercase names.

```python
PI = 3.14159
MAX_USERS = 100
```

---

## 15. Avoid Global Variables

Prefer passing values through functions.

```python
def greet(name):
    return f"Hello, {name}"
```

---

## 16. Use Meaningful Names

```python
# Good
student_marks = 85

# Bad
x = 85
```

---

## 17. Main Function

Use the following structure to define the program entry point.

```python
def main():
    print("Program Started")

if __name__ == "__main__":
    main()
```

---

## 18. Type Hints

Use type hints to improve readability and editor support.

```python
def add(a: int, b: int) -> int:
    return a + b
```

---

## 19. Avoid Magic Numbers

Use named constants instead of hardcoded values.

```python
MAX_RETRIES = 3

for _ in range(MAX_RETRIES):
    pass
```

---

## 20. The Zen of Python

View Python's guiding principles by running:

```python
import this
```

Some key principles include:

- Readability counts.
- Simple is better than complex.
- Explicit is better than implicit.
- Errors should never pass silently.
- There should be one obvious way to do it.

---

## Example

### Bad Code

```python
def calc(a,b):
 if(a>10):
  print("Large")
 return a+b
```

### Good Code

```python
def calculate_sum(a: int, b: int) -> int:
    """Return the sum of two integers."""

    if a > 10:
        print("Large number")

    return a + b
```

---

## Summary

- Use **4-space indentation**.
- Follow **snake_case** for variables and functions.
- Use **PascalCase** for class names.
- Keep lines within **79 characters**.
- Write meaningful variable names.
- Use comments and docstrings where appropriate.
- Handle exceptions specifically.
- Use type hints whenever possible.
- Follow **PEP 8** to write clean, consistent, and maintainable Python code.

---

## References

- **PEP 8 – Style Guide for Python Code**
- **The Zen of Python (`import this`)**
- **Python Official Documentation**