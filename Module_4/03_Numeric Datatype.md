## Numeric Datatype

Boolean and Complex

---

### Quick Hook

So far, numbers looked simple. Whole numbers and decimals.
Now we step into two powerful ideas that quietly run most programs logic and advanced math.

---

### Learning Objectives

By the end of this lesson, you will be able to

* Declare and use Boolean values correctly in Python
* Understand how Boolean values behave internally
* Identify where Boolean values are used in programs
* Understand what complex numbers are and why Python supports them
* Create and inspect complex numbers using different methods

---

## Main Content

### 1. Recap of Numeric Datatypes

You already know that Python numeric datatypes include

* int
* float
* bool
* complex

In the previous lesson, we covered integer and float in detail.
In this lesson, we focus on the remaining two

* Boolean
* Complex

If you are new to programming, these may feel unfamiliar. Take it slow and practice along.

---

## 2. Boolean Datatype

### What is a Boolean

A Boolean represents a logical state

* True means yes
* False means no

Python provides Boolean values as built in constants.

---

### Declaration and Initialization

A Boolean variable is created like this

```python
flag = True
status = False
```

Important rules

* True must start with capital T
* False must start with capital F
* Lowercase true or false is invalid

Python treats lowercase versions as variable names, not Boolean values.

---

### Boolean and Numbers

Internally

* True behaves like the number one
* False behaves like the number zero

Example

```python
value = True
int(value)
```

Result is one

But remember

* One does not automatically become True
* Only True converts to one

---

### Where Boolean is Used

Boolean values appear naturally when you compare values.

Example idea

* Is one value greater than another
* Is two values equal

The result of any comparison is always Boolean

* True
* False

These results are later used in decision making logic like conditions.

You will study this in detail when we learn conditional statements.

---

### Practice in Jupyter Notebook

```python
x = True
y = False
print(x, y)
print(type(x))
print(int(x))
```

Try assigning lowercase true and observe the error message carefully.
Reading errors is part of learning programming.

---

## 3. Complex Datatype

### What is a Complex Number

Complex numbers come from mathematics.
They contain two parts

* Real part
* Imaginary part

In math, imaginary part is based on square root of minus one.

Python supports complex numbers directly.

---

### Complex Numbers in Python

Python represents complex numbers using j instead of i.

Reason

* i is commonly used as a loop variable in programs
* j avoids confusion

---

### Creating Complex Numbers

Direct form

```python
num1 = 6 + 4j
```

Using decimal values

```python
num2 = 2.75 + 1.25j
```

Using the complex function

```python
num3 = complex(5, 3)
```

Only real part

```python
num4 = complex(8)
```

Python automatically sets the imaginary part to zero.

---

### Checking the Type

```python
print(type(num1))
```

Result shows complex datatype.

---

### Where Complex Numbers Are Used

Complex numbers appear in

* Mathematical calculations
* Engineering problems
* Scientific computing
* Data analysis

You may not use them daily, but Python supports them fully when needed.

---

### Practice in Jupyter Notebook

```python
c = 7 + 2j
print(c)
print(type(c))

d = complex(4, 1.5)
print(d)
```

Try creating different combinations and observe the output.

---

## Mini Checkpoint

Think about these questions

* What values can a Boolean variable hold
* Why does Python require capital True and False
* What is the imaginary part in a complex number
* How does Python represent square root of minus one

---

## Recap

* Boolean datatype represents True or False
* Boolean values are used in comparisons and conditions
* True behaves like one and False behaves like zero internally
* Complex numbers contain real and imaginary parts
* Python uses j to represent the imaginary unit
* Complex numbers are fully supported in Python

---

## What’s Next

In the next lesson, we move from numeric values to collections and start exploring sequence datatypes like list and tuple.
