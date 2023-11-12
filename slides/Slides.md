---
marp: true
theme: custom-default
paginate: true
footer: 'imec'
---

# Unit testing in Python
## A guide by
### Koen Ongena

![bg right](https://images.unsplash.com/photo-1574169208507-84376144848b?q=80&w=2079&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

---

## Agenda

1. What is Unit Testing?
2. Benefits of Unit Testing
3. When to Apply Unit Testing
4. Getting Started with Unit Testing in Python
5. Keeping your tests maintainable

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

# Getting Started with Unit Testing in Python

## Step 3: Run Tests

Command-line Execution:
Use the test runner provided by the chosen framework.


`python -m unittest test_module.py`

---

# Getting Started with Unit Testing in Python

## IDE Integration:
  Most modern IDEs have built-in support for running tests.

---

# Keeping your tests maintainable

* AAA pattern (aka given/when/then)
* Keep the Arrange part lean and mean
* One Assert Per Test Method
* Avoid Test Interdependence
* Test Positive and Negative Scenarios

---
## AAA Pattern

__Arrange__:
    Set up the necessary preconditions and inputs.
__Act__:
    Perform the action or behavior being tested.
__Assert__:
    Verify that the expected outcomes are met.


<!-- If you find that the “arrange” part of your unit test becomes cumbersome, stop what you’re doing.  One of the most undercover powerful things about unit tests is that they provide excellent feedback on the design of your code — specifically its modularity.  If you find yourself laboring heavily to get a class and method setup so that you can test it, you have a design problem.

When you create setup heavy tests, you create brittle tests.  Tests carry a maintenance weight, just like production code.  You thus want to avoid unwieldy tests like the plague — they’ll break and make you and everyone else hate them.  So instead of going nuts on the setup, take a critical look at your design. -->

---

```
import unittest

class MyTestCase(unittest.TestCase):
    def test_example(self):
        # Arrange
        x = 1
        y = 2

        # Act
        result = sum(x, y)

        # Assert
        self.assertEqual(result, 3)

```

---

## Keep the Arrange part lean and mean

If the “arrange” part of your unit test becomes cumbersome,reconsider the design or the "unit" you are testing.

---
## One Assert Per Test Method

---
## Avoid Test Interdependence

---
## Test Positive and Negative Scenarios

---
<i class="fa-brands fa-github"></i> GitHub: https://github.com/koen-ongena-imec/unit-testing-python