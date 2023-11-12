---
marp: true
theme: custom-default
footer: 'https://github.com/koen-ongena-imec/unit-testing-python'
---

# Unit testing in Python
## A beginners guide

![bg right](https://images.unsplash.com/photo-1426927308491-6380b6a9936f?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

---

## Agenda

1. What is Unit Testing?
2. Benefits of Unit Testing
3. When to Apply Unit Testing
4. Getting Started with Unit Testing in Python

---

## What is Unit Testing?

- **Definition:** The process of testing individual units or components of a software application.
- **Unit:** The smallest testable part of an application, typically a function or method.

---

## Benefits of Unit Testing

1. **Early Detection of Bugs:**
   - Identifying issues at the development stage.
2. **Code Quality Assurance:**
   - Ensuring code is modular and maintainable.
3. **Facilitates Refactoring:**
   - Confidence to make changes without fear of breaking existing functionality.
4. **Documentation:**
   - Acts as executable documentation for your code.

---

## When to Apply Unit Testing

- **Before Integration Testing:**
  - Test individual components in isolation.
- **After Code Changes:**
  - Confirm existing functionality is unaffected.
- **Throughout Development:**
  - Continuous testing ensures ongoing code quality.

---

# Getting Started with Unit Testing in Python

## Step 1: Choose a Testing Framework

- **Popular Frameworks:**
  - `unittest` (built-in), `pytest`, `nose2`, etc.

---
# Getting Started with Unit Testing in Python

## Step 2: Write Test Cases

- **Anatomy of a Test Case:**
  - Define a test class.
  - Write test methods with assertions.

```python
import unittest

class MyTestCase(unittest.TestCase):
    def test_example(self):
        self.assertEqual(1 + 1, 2)
```

---
<i class="fa-brands fa-github"></i> GitHub: https://github.com/koen-ongena-imec/
