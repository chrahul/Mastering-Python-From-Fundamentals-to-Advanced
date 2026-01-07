## Python Data Types — An Overview

---

### Quick Hook

Before you write powerful programs, you need to understand **what kind of data Python can store and work with**.
Python offers a rich set of data types—and that’s one big reason it’s so flexible and popular.

---

### Learning Objectives

By the end of this lesson, you will be able to:

* Identify the **major categories of data types** in Python
* Understand the difference between **scalar** and **collection** data types
* Recognize which data types are **mutable** and which are **immutable**
* Understand concepts like **indexing, uniqueness, and key–value pairs**
* Get a clear mental map of Python’s data type ecosystem

---

## Main Content

### 1. Why Data Types Matter

Every program works with data:

* numbers
* text
* collections of values
* mappings between values

Python provides **built-in data types** to handle all these scenarios efficiently.

Compared to languages like C++ or Java, Python has:

* more built-in data types
* simpler syntax
* greater flexibility

Let’s look at **all Python data types at a high level**, grouped into categories.

---

### 2. Categories of Python Data Types

Python data types can be broadly grouped as:

1. **Numeric Types**
2. **Sequence Types**
3. **Set Type**
4. **Dictionary Type**

We’ll now walk through each category with simple examples and ideas.

---

## 3. Numeric Data Types (Single Values)

Numeric types store **one value at a time** (scalar values).

### a) Integer (`int`)

* Whole numbers
* No decimal point

Example:

```python
count = 42
```

Here, `count` holds an integer value.

---

### b) Float (`float`)

* Numbers with a decimal point

Example:

```python
temperature = 36.6
```

Even though it’s numeric, the decimal makes it a float.

---

### c) Boolean (`bool`)

* Logical values: `True` or `False`

Example:

```python
is_active = True
```

Booleans are mainly used in:

* conditions
* decision-making
* comparisons

You’ll see them heavily in `if` statements later.

---

### d) Complex (`complex`)

* Numbers with **real** and **imaginary** parts

Example:

```python
z = 4 + 7j
```

Here:

* `4` is the real part
* `7j` is the imaginary part

Python supports complex numbers natively, which is useful in scientific and mathematical applications.

If this feels unfamiliar—don’t worry. We’ll revisit it later.

---

## 4. Sequence Data Types (Ordered Collections)

Sequence types store **multiple values together** and support:

* indexing
* ordered access

### a) List (`list`)

* Collection of values
* Ordered
* **Mutable** (can be changed)

Example:

```python
scores = [78, 85, 92, 88]
```

Key properties:

* Index starts from `0`
* Values can be modified, added, or removed
* Can store mixed data types

Visualization idea:

* `scores` refers to a group of values stored sequentially in memory

---

### b) Tuple (`tuple`)

* Collection of values
* Ordered
* **Immutable** (cannot be changed)

Example:

```python
dimensions = (1920, 1080)
```

Looks similar to a list, but:

* Uses parentheses `()`
* Once created, it is **locked**
* No adding, removing, or modifying elements

Tuple = **read-only list**

---

### c) String (`str`)

* Sequence of characters
* Ordered
* **Immutable**

Example:

```python
city = "Mumbai"
```

Important points:

* Can use single or double quotes
* Each character has an index
* You cannot modify individual characters

Strings behave like sequences, just specialized for text.

---

## 5. Set Data Type (`set`)

A set is a **collection of unique values**.

Key features:

* No duplicate values
* No indexing
* Unordered
* Mutable (can add/remove elements)

Example:

```python
unique_ids = {101, 203, 305, 101}
```

Result internally:

```text
{101, 203, 305}
```

Duplicates are automatically removed.

Important notes:

* You cannot access elements by index
* Order is not guaranteed
* You can add or remove values

---

## 6. Dictionary Data Type (`dict`)

A dictionary stores data as **key–value pairs**.

Key features:

* Keys must be unique
* Values can change
* Ordered (in modern Python)
* Mutable

Example:

```python
student = {
    "name": "Anita",
    "roll": 12,
    "grade": "A"
}
```

How it works:

* Keys act like labels
* Values store actual data
* You access data using keys, not indices

This type is extremely useful for structured data.

---

## 7. Quick Comparison Snapshot

| Category    | Stores Multiple? | Ordered | Mutable |
| ----------- | ---------------- | ------- | ------- |
| int / float | NO                | NO       | NO       |
| bool        | NO                | NO       | NO       |
| complex     | NO                | NO       | NO       |
| list        |YES               | YES       | YES       |
| tuple       | YES                | YES       | NO       |
| string      | YES                | YES     | NO       |
| set         | YES                | NO       |YES       |
| dictionary  | YES                | YES       | YES       |

---

## Mini Checkpoint

Test your understanding:

1. Which data types can store multiple values?
2. Which sequence types support indexing?
3. Can a set contain duplicate elements?
4. What is the main difference between a list and a tuple?

---

## Recap

* Python has a rich set of built-in data types
* Numeric types store single values
* Sequence types store ordered collections
* Lists are mutable; tuples and strings are immutable
* Sets store unique, unordered values
* Dictionaries store key–value pairs
* Each data type serves a specific purpose

---

## What’s Next

In the next lessons, we’ll **deep dive into each data type**, starting with **numeric data types**, and learn how to use them effectively in real Python programs.
