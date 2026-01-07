## Numeric Data Types — Integers and Floats

---

### Quick Hook

Numbers are at the heart of most programs—counts, prices, measurements, scores.
Before we move further, let’s understand **how Python stores and works with numbers**, starting with integers and floats.

---

### Learning Objectives

By the end of this lesson, you will be able to:

* Declare and use **integer** and **float** variables in Python
* Understand how Python handles **positive, negative, and large numbers**
* Know how **memory allocation** works for numeric data
* Understand why integers and floats are **immutable**
* Recognize and use **floating-point (scientific) notation**

---

## Main Content

### 1. Numeric Data Types in Python

You’ve already seen that **numeric types** are one category of Python data types.
This category includes:

* `int` (integer)
* `float`
* `bool`
* `complex`

In this lecture, we’ll focus on **int** and **float**.
The remaining numeric types will be covered next.

Keep your **Jupyter Notebook** ready—we’ll practice everything side by side.

---

## 2. Integer (`int`) Data Type

### a) Declaration and Initialization

Creating an integer in Python is straightforward:

```python
items = 120
```

* The value has **no decimal point**
* Python automatically understands it as an integer

No special keyword is needed.

---

### b) Positive and Negative Integers

Integers can be:

* Positive
* Negative
* Zero

Examples:

```python
profit = 450
loss = -90
```

Both are perfectly valid integers in Python.

---

### c) Size of Integers (Very Important)

One powerful feature of Python is this:

 **Integers have no fixed size limit**

Examples:

```python
small_num = 345
big_num = 98765432101234567890
```

Both are valid.

In many other languages (like C or Java), integers have size limits.
In Python, you can store **as many digits as your memory allows**.

---

### d) Memory Usage of Integers

Even though integers can grow very large, Python:

* Allocates memory dynamically
* Uses more memory as the number grows

We can check memory usage using the `sys` module:

```python
import sys
sys.getsizeof(items)
```

Smaller integers consume less memory, larger ones consume more.
You don’t need to memorize exact sizes—just understand that **size depends on value**.

---

### e) Immutability of Integers

Integers are **immutable**.

What does that mean?

It means:

* The value itself never changes in memory
* A **new value** is created when you reassign

Example:

```python
x = 110
x = 205
```

Behind the scenes:

* `110` remains unchanged
* `205` is stored at a new memory location
* `x` now points to the new value

You can verify this using the `id()` function:

```python
id(x)
```

Each reassignment gives a **different memory address**.

This is why integers are called immutable.

---

## 3. Float (`float`) Data Type

### a) Declaration and Initialization

Any numeric value **with a decimal point** becomes a float:

```python
rate = 18.75
discount = 0.05
```

Even if the decimal comes before the digits, it’s still valid.

---

### b) Floating-Point (Scientific) Representation

Python also supports **scientific notation**, often called floating-point representation.

Example:

```python
value = 2.5e3
```

This means:

```
2.5 × 10³ = 2500.0
```

Another example:

```python
ratio = 4.75e-2
```

Which means:

```
4.75 ÷ 100 = 0.0475
```

Here:

* The first part is called the **mantissa**
* The power of 10 is called the **exponent**

This representation follows IEEE standards and is widely used in computing.

---

### c) Positive and Negative Floats

Floats can also be positive or negative:

```python
height = 172.6
depth = -3.5
```

In scientific notation, both mantissa and exponent can be positive or negative.

Examples:

```python
a = -3.2e2
b = 6.1e-3
```

---

### d) Practice in Jupyter Notebook

You can try all these in your notebook:

```python
a = 29.75
b = -1.25
c = 2.5e2
d = -4.1e-3

print(a, b, c, d)
```

Notice:

* Python automatically treats them as floats
* Both lowercase `e` and uppercase `E` work

---

## Mini Checkpoint

Pause and think:

1. How does Python decide whether a number is `int` or `float`?
2. Can Python store very large integers?
3. What does immutability mean in the context of numbers?
4. What does `3.4e2` represent?

---

## Recap

* Numeric data types store single (scalar) values
* `int` stores whole numbers with unlimited size
* `float` stores decimal numbers
* Python allocates memory dynamically for numbers
* Integers and floats are **immutable**
* Scientific notation (`e` or `E`) represents powers of 10

---

## What’s Next

In the next lesson, we’ll continue with **numeric data types** and explore **Boolean and Complex numbers**, along with where and why they are used.
