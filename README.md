# 📊 Writing Test Assertions with Python's `unittest`

This project demonstrates how to write unit test assertions using Python's built-in `unittest` framework to validate a `Stack` data structure. The lab guides you through writing test cases for each of the Stack's core methods using Test-Driven Development (TDD).

---

## 📂 Repository Structure

```
duwjx-tdd_bdd_PracticeCode/
└── labs/
    └── 02_writing_test_assertions/
        ├── stack.py            # Stack class implementation
        ├── test_stack.py       # Unit tests for Stack methods
        └── requirements.txt    # Required Python packages
```

---

## 🛠️ Lab Setup

### ✅ Step 1: Clone the Repo

```bash
cd /home/project
git clone https://github.com/ibm-developer-skills-network/duwjx-tdd_bdd_PracticeCode.git
cd duwjx-tdd_bdd_PracticeCode/labs/02_writing_test_assertions/
```

### ✅ Step 2: Install Requirements

```bash
python3.8 -m pip install -r requirements.txt
```

---

## 🔪 Running Tests

Use the following commands to run tests:

```bash
nosetests         # Run all tests
nosetests --stop  # Stop on first failure
```

---

## 📌 Task-wise Implementation with Code Snippets

### ☑️ Task 1: Test `is_empty()`

#### 🔢 Objective

Test if the stack correctly reports empty and non-empty states.

#### 💻 Code

```python
def test_is_empty(self):
    self.assertTrue(self.stack.is_empty())
    self.stack.push(5)
    self.assertFalse(self.stack.is_empty())
```

---

### ☑️ Task 2: Test `peek()`

#### 🔢 Objective

Test that `peek()` returns the top item without removing it.

#### 💻 Code

```python
def test_peek(self):
    self.stack.push(3)
    self.stack.push(5)
    self.assertEqual(self.stack.peek(), 5)
```

---

### ☑️ Task 3: Test `pop()`

#### 🔢 Objective

Test that `pop()` removes and returns the top value.

#### 💻 Code

```python
def test_pop(self):
    self.stack.push(3)
    self.stack.push(5)
    self.assertEqual(self.stack.pop(), 5)
    self.assertEqual(self.stack.peek(), 3)
    self.stack.pop()
    self.assertTrue(self.stack.is_empty())
```

---

### ☑️ Task 4: Test `push()`

#### 🔢 Objective

Test that `push()` adds an item to the top of the stack.

#### 💻 Code

```python
def test_push(self):
    self.stack.push(3)
    self.assertEqual(self.stack.peek(), 3)
    self.stack.push(5)
    self.assertEqual(self.stack.peek(), 5)
```

---

## 🔄 Final Test Output

```bash
....
----------------------------------------------------------------------
Ran 4 tests in 0.001s

OK
```

---

## 🧵 Conclusion

By completing this lab, you learned how to:

* Write meaningful unit tests using Python's `unittest` module.
* Use assertions like `assertEqual()`, `assertTrue()`, and `assertFalse()`.
* Apply TDD methodology to build confidence in your code.

These practices ensure that your programs behave as expected and can catch bugs early in the development process.

---

## 📝 License

This lab is part of the [IBM Developer Skills Network](https://developer.ibm.com/)'s educational resources.

NAME- Souvik Mandal
