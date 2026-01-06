## Rules for Naming Variables in Python

---

### Quick Hook

Variables are just names—but **bad names create confusion**.
In this lesson, we’ll learn the simple rules and smart guidelines that help you write **clean, readable Python code**.

---

### Learning Objectives

By the end of this lesson, you will be able to:

* Apply Python’s **rules** for valid variable names
* Follow practical **naming guidelines** for readability
* Identify **invalid variable names** and understand why they fail
* Recognize Python **keywords** and avoid using them
* Understand how **case sensitivity** affects variables

---

## Main Content

### 1. Why Do Variable Naming Rules Exist?

Variables are names given to data.
But Python (and every programming language) needs **some discipline** to understand those names.

So Python defines:

* **Strict rules** (breaking them causes errors)
* **Guidelines** (breaking them won’t cause errors, but leads to messy code)

Let’s go through both—one by one.

---

### 2. Guideline: Variable Names Should Be Meaningful

This is **not a strict rule**, but a very important habit.

#### Good Examples

```python
item_code = 402
unit_cost = 47.50
client_name = "Ravi"
```

From the names alone, you can guess what data is stored.

#### Poor Examples

```python
x = 402
y = 47.50
z = "Ravi"
```

These technically work—but they don’t explain anything.

 **Rule of thumb**:
A variable name should tell *what kind of data it holds*.

---

### 3. Rule: Allowed Characters in Variable Names

Python allows:

* Alphabets: `a–z`, `A–Z`
* Numbers: `0–9`
* Underscore: `_`

 Not allowed:

* Spaces
* Special characters like `@`, `#`, `-`, `$`

#### Valid Examples

```python
score1 = 88
employee_id = 1057
total_marks_2024 = 450
```

#### Invalid Examples

```python
user-name = "Amit"   #  hyphen not allowed
total cost = 500    #  space not allowed
amount$ = 300       #  special character
```

---

### 4. Rule: Variable Name Must Start Correctly

A variable name:

*  **Must start with a letter or underscore**
*  **Must not start with a number**

#### Valid

```python
city2 = "Pune"
_address = "MG Road"
```

#### Invalid

```python
3city = "Pune"   #  starts with a number
```

---

### 5. Rule: Variable Names Cannot Be Keywords

Python has **reserved words** called *keywords*.
These words have predefined meaning in the language.

Examples of Python keywords:

* `if`, `else`, `while`
* `True`, `False`
* `None`, `for`, `return`

You **cannot** use them as variable names.

#### Invalid Examples

```python
if = 10
False = "No"
```

Python will throw a **syntax error**.

You don’t need to memorize all keywords right now.
As you practice, you’ll naturally recognize them.

---

### 6. Rule: Python Is Case Sensitive

Python treats variable names with different letter cases as **different variables**.

#### Example

```python
rate = 12.5
Rate = 15.0
RATE = 18.0
```

All three are **separate variables**.

This also explains something interesting:

```python
false = 0
```

* `False` (capital F) is a keyword 
* `false` (small f) is a valid variable 

 **Important note**:
Although this is allowed, it’s **not recommended**.
Using keyword-like names—even with case changes—creates confusion.

---

### 7. Trying the Rules in Jupyter Notebook

Let’s quickly test some names.

#### Valid Examples

```python
value9 = 100
user_score = 78
```

 Executes without error

#### Invalid Examples

```python
9value = 100
```

 Syntax error (cannot start with a number)

```python
user score = 78
```

 Syntax error (space not allowed)

```python
True = "yes"
```

 Keyword usage error

Python immediately tells you when a rule is broken—**read the error messages carefully**.

---

## Mini Checkpoint

Quick self-check:

1. Can a variable name contain a space?
2. Can it start with a number?
3. Is `_total` a valid variable name?
4. Why is `False` invalid but `false` valid?

---

## Recap

* Variable names should be **meaningful** (guideline)
* Only letters, numbers, and underscore are allowed
* Names must start with a letter or underscore
* Keywords cannot be used as variable names
* Python is case sensitive
* Breaking rules causes syntax errors; breaking guidelines causes confusion

---

## What’s Next

In the next lesson, we’ll continue exploring **variables** and move into how Python handles **data internally**, setting the stage for deeper work with data types and operations.
