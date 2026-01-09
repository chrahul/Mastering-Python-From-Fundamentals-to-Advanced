## Literals in Python

---

### Quick Hook

So far you have been assigning values to variables without thinking much about where those values come from.
In this lesson, we name that idea properly and make it very clear.

---

### Learning Objectives

By the end of this lesson, you will be able to

* Explain what a literal is in simple terms
* Identify literals inside a Python program
* Use integer and float literals correctly
* Improve number readability using underscores
* Recognize Boolean, complex, and string literals

---

## Main Content

### 1. What Are Literals

Let us start with something familiar.

```python
a = 12
b = 7
```

Here

* a and b are variables
* 12 and 7 are the actual values written directly in the program

Now look at this

```python
c = a + b
```

Here

* c gets a value
* but that value is the result of a calculation

Now look at this

```python
name = input()
```

Here

* name gets a value
* but that value comes from the keyboard

So ask yourself one simple question
Which values are written directly inside the program

The answer is

* 12
* 7

These direct values written in the program are called literals.

So in simple words
Literals are fixed values written directly in the code.

They are also called constants.

---

## 2. Integer Literals

An integer literal is a whole number written directly in the program.

Example

```python
count = 45
```

Here

* 45 is an integer literal

### Improving Readability with Underscores

When numbers become large, they are hard to read.

Instead of writing

```python
population = 10000000
```

You can write

```python
population = 10_000_000
```

Important points

* Underscore is only for readability
* Python treats both values as the same number
* Underscore must be between digits only

Invalid examples

```python
num = _123
num = 123_
```

These cause errors.

Underscores do not change the value.
They only help humans read the number easily.

---

## 3. Float Literals

Float literals are numbers with a decimal point.

Examples

```python
price = 8.75
rating = 4.0
```

Even if the decimal part is zero, it is still a float.

### Scientific or Floating Representation

You can also write float literals using exponent notation.

```python
distance = 1.2e3
ratio = 5.6E-2
```

Python automatically converts these to decimal values.

### Using Underscores in Float Literals

Underscores can also be used in float literals.

```python
amount = 12_345.67
```

But this is invalid

```python
amount = _12.34
```

Underscore must stay between digits only.

---

## 4. Boolean Literals

Boolean literals represent logical values.

There are only two Boolean literals in Python

* True
* False

Examples

```python
is_active = True
is_logged_in = False
```

Rules to remember

* True and False must start with capital letters
* lowercase true or false is invalid

Also remember

* True behaves like the number one
* False behaves like the number zero

But

* one is not a Boolean
* zero is not a Boolean

They are integers.

---

## 5. Complex Literals

Complex literals represent numbers with real and imaginary parts.

In Python, imaginary part uses j.

Examples

```python
z1 = 3 + 4j
z2 = 1.5 + 2.5j
```

Both parts can be integers or floats.

Underscores are allowed here as well.

```python
z3 = 10_000 + 5_000j
```

These values are written directly in the program, so they are complex literals.

---

## 6. String Literals

String literals represent text data.

Strings can be written using

* single quotes
* double quotes
* triple quotes

Examples

```python
city = 'Paris'
country = "France"
message = '''Welcome'''
```

All three create string literals.

If you mix quotes, the inner quotes become part of the string.

Example

```python
text = 'Hello "World"'
```

Here

* the double quotes are part of the string value

Strings are one of the most commonly used literals in Python.

---

## Mini Checkpoint

Take a moment and think

* Which part of a = 10 is the literal
* Why underscores do not change numeric values
* How many Boolean literals exist in Python
* What makes a value a literal

---

## Recap

* Literals are fixed values written directly in code
* Integer literals can use underscores for readability
* Float literals support decimal and exponent form
* Boolean literals are only True and False
* Complex literals use j for imaginary part
* String literals store text using quotes

---

## What’s Next

In the next lesson, we will connect literals and variables with type conversion and understand how Python changes data from one form to another.
