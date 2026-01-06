## Dynamically Typed Languages in Python

---

### Quick Hook

One of the reasons Python feels so easy and flexible is this:
**you don’t have to worry about data types upfront.**
In this lesson, you’ll clearly see why Python is called a *dynamically typed* language.

---

### Learning Objectives

By the end of this lesson, you will be able to:

* Explain what **statically typed** and **dynamically typed** languages mean
* Compare Python with languages like C, C++, and Java
* Understand how Python decides a variable’s data type
* Observe how a variable’s type can change at runtime
* Use `type()` to check a variable’s data type in Python

---

## Main Content

### 1. Why Do We Talk About “Typing” in Programming?

When we say a language is *typed*, we are talking about:

> **How a language handles data types for variables**

Some languages want you to be very strict.
Others give you flexibility.

To understand Python properly, we must first look at **statically typed languages**.

---

### 2. What Are Statically Typed Languages?

Languages like:

* C
* C++
* Java

are known as **statically typed languages**.

In these languages:

* You must **declare the data type of a variable in advance**
* That data type **cannot change later**

#### Example (Conceptual – not Python):

You might say:

* “Create a variable called `count` that can store only integers”

Once that decision is made:

* `count` can **only** store integer values
* It cannot store decimals or text later

If you want a decimal value, you must create a **separate variable** with a float type.

So in statically typed languages:

* Data type is decided **before execution**
* Data type remains **fixed throughout the program**

That’s why they are called *static*.

---

### 3. What Is a Dynamically Typed Language?

Now comes Python 😊

Languages like:

* Python
* JavaScript

are called **dynamically typed languages**.

In these languages:

* You **do not declare the data type**
* Python decides the data type **based on the value you assign**
* The decision happens **at runtime**

---

### 4. How Python Handles Variables

Let’s look at how variable assignment works in Python.

Suppose you write:

```python
x = 42
```

* Python sees `42`
* `42` is an integer
* So `x` now refers to an integer object

Now later in the same program, you write:

```python
x = 3.14
```

* Python sees `3.14`
* That’s a floating-point value
* Now `x` refers to a float object

Later again:

```python
x = "Python"
```

* Now `x` refers to a string object

So the **same variable name** is reused, but the **data it refers to changes**.

That’s dynamic typing.

---

### 5. What’s Actually Changing?

This is important to understand conceptually.

In Python:

* A variable is a **reference**
* The reference can point to **different objects at different times**

So what changes is **not the variable itself**, but **what it refers to**.

Earlier:

* `x → integer object`

Later:

* `x → float object`

Later:

* `x → string object`

The old data that is no longer referenced becomes unused and will be cleaned up automatically (we’ll talk about this later).

---

### 6. Checking the Data Type Using `type()`

Python provides a built-in function called `type()`.

It tells you:

> What kind of object a variable is currently referring to

#### Example Walkthrough (in Jupyter Notebook):

```python
value = 100
type(value)
```

Output:

```text
<class 'int'>
```

Now change the value:

```python
value = 8.5
type(value)
```

Output:

```text
<class 'float'>
```

Change it again:

```python
value = "Learning Python"
type(value)
```

Output:

```text
<class 'str'>
```

And now try a collection:

```python
value = [2, 4, 6, 8]
type(value)
```

Output:

```text
<class 'list'>
```

So one variable name `value` held:

* an integer
* a float
* a string
* a list

All in the same program.

That’s the real power of dynamic typing.

---

### 7. Why Is Dynamic Typing Useful?

**Benefits for the programmer:**

* Less code to write
* No need to plan data types in advance
* Faster development
* Easier experimentation

This flexibility is one big reason why:

* Python is beginner-friendly
* Python is widely used in data science, automation, and scripting

---

## Mini Checkpoint

Quick check:

1. In statically typed languages, when is the data type decided?
2. In Python, how does a variable get its data type?
3. Can the same variable refer to different data types in Python?
4. What does the `type()` function do?

---

## Recap

* Statically typed languages require fixed data types
* Dynamically typed languages decide types at runtime
* Python is dynamically typed
* Variable names are references, not fixed containers
* `type()` helps inspect a variable’s current data type
* A variable’s type can change as values change

---

## What’s Next

In the next lesson, we’ll continue exploring **variables**, and then move deeper into **Python’s core data types**, starting with numeric types in more detail.
