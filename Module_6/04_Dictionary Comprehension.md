## Title: Dictionary Comprehension

### Lesson Title: Creating Dictionaries Using Comprehension

---

### Quick Hook

You already know how to create dictionaries in different ways.
Now let’s make it cleaner and smarter using dictionary comprehension.

This will help you write powerful code in fewer lines.

---

### Learning Objectives

By the end of this lesson, you will be able to

* Understand what dictionary comprehension is
* Create a dictionary from iterable pairs using comprehension
* Use `zip()` inside dictionary comprehension
* Use `enumerate()` inside dictionary comprehension
* Recognize when comprehension makes your code cleaner

---

## Main Content

## What is Dictionary Comprehension?

Dictionary comprehension is a short and elegant way to create dictionaries.

Just like:

* List comprehension creates lists
* Set comprehension creates sets

Dictionary comprehension creates dictionaries using:

* Curly brackets `{}`
* A `for` loop inside
* A `key : value` expression

Basic structure:

```python
{key_expression : value_expression for item in iterable}
```

That’s the idea.

---

## Method 1: Using Iterable Pairs

Let’s take a fresh example.

Suppose we have product data stored as pairs:

```python
data = [
    (501, "Keyboard"),
    (502, "Mouse"),
    (503, "Monitor")
]
```

Each tuple contains:

* First element → key
* Second element → value

Now we can create a dictionary using comprehension.

```python
products = {k: v for (k, v) in data}
```

Let’s understand this clearly:

* `(k, v)` extracts the pair
* `k` becomes key
* `v` becomes value
* `{k: v}` creates dictionary entries

Result:

```python
{
    501: "Keyboard",
    502: "Mouse",
    503: "Monitor"
}
```

Clean and readable.

---

## Important Concept

When the iterable contains pairs like:

```python
( key , value )
```

You can unpack them directly in the `for` loop:

```python
for k, v in data
```

This is called tuple unpacking.

---

## Method 2: Using zip() with Dictionary Comprehension

Now imagine you have two separate lists.

```python
ids = [11, 12, 13]
courses = ["Python", "Java", "C++"]
```

You want:

* 11 → Python
* 12 → Java
* 13 → C++

First, `zip()` pairs them.

Inside comprehension:

```python
course_map = {k: v for k, v in zip(ids, courses)}
```

Let’s break it down:

* `zip(ids, courses)` creates pairs
* `k, v` unpacks them
* `{k: v}` forms the dictionary

Result:

```python
{
    11: "Python",
    12: "Java",
    13: "C++"
}
```

Very clean.

---

### What if Lists Are Unequal?

If:

```python
ids = [11, 12, 13, 14]
courses = ["Python", "Java", "C++"]
```

`zip()` ignores the extra element.

So only matching pairs are used.

---

## Method 3: Using enumerate() in Dictionary Comprehension

Now suppose you only have values:

```python
cities = ["Delhi", "Mumbai", "Chennai"]
```

But you want numeric keys.

Use `enumerate()`.

Basic example:

```python
city_map = {i: city for i, city in enumerate(cities)}
```

Output:

```python
{
    0: "Delhi",
    1: "Mumbai",
    2: "Chennai"
}
```

---

## Starting from a Custom Number

By default, `enumerate()` starts from 0.

But you can change it:

```python
city_map = {i: city for i, city in enumerate(cities, start=1)}
```

Now output becomes:

```python
{
    1: "Delhi",
    2: "Mumbai",
    3: "Chennai"
}
```

This is very useful when:

* You want auto-generated keys
* You want index-based mapping

---

## Why Use Dictionary Comprehension?

Compare these two approaches:

### Normal way:

```python
result = {}
for k, v in data:
    result[k] = v
```

### Comprehension way:

```python
result = {k: v for k, v in data}
```

Same result.
Less code.
Cleaner logic.

---

## When Should You Use It?

Use dictionary comprehension when:

* You are transforming data
* You are generating mappings
* You want compact code
* You are filtering or modifying values

It is widely used in real-world Python programs.

---

### Mini Checkpoint

Pause and think:

* What must be written inside `{}` in dictionary comprehension?
* What does `for k, v in zip(...)` actually unpack?
* What is the default start value of `enumerate()`?
* When would comprehension be better than a normal loop?

---

### Recap

* Dictionary comprehension creates dictionaries in a compact way
* Structure is `{key: value for ...}`
* It works with iterable pairs
* It works with `zip()`
* It works with `enumerate()`

---

### What’s Next

Next, we will apply dictionary comprehension in practical challenges and also combine it with conditions to make it even more powerful.
