# 🔐 Password Strength Checker

## Overview

This Python project checks the strength of multiple passwords concurrently using the **threading** module. Each password is evaluated based on common security rules and classified as **Strong**, **Medium**, or **Weak**.

## Features

* Uses Python multithreading for concurrent password checking.
* Validates:

  * Minimum length (8 characters)
  * Uppercase letters
  * Lowercase letters
  * Digits
  * Special characters
* Classifies passwords as:

  * **Strong** (Score = 5)
  * **Medium** (Score = 3–4)
  * **Weak** (Score = 0–2)

## Technologies Used

* Python 3
* `threading` module

## Example Output

```text
rohan -> Weak
Rohan@122 -> Strong
Rohan123 -> Medium
123456 -> Weak
ROHAN@12 -> Medium
```

> **Note:** The output order may vary because threads execute concurrently.

## Author

**Rohan Mapari**
