## Variables in Python

---

### Quick Hook

In the last lesson, we learned that every program has **data** and **operations**.
Now the big question is: *where does that data live inside a program?*
That’s exactly what **variables** are for.

---

### Learning Objectives

By the end of this lesson, you will be able to:

* Explain what a **variable** is (in plain language)
* Understand **declaration** and **initialization** in Python
* Visualize how variables relate to **memory**
* Identify basic data types stored in variables: **int, float, string**
* Use **multiple assignment** and understand `id()` with shared values

---

## Main Content

### 1. What Are Variables?

If you remember from the previous lecture, a program has two major parts:

* **Data**
* **Instructions (operations)** performed on that data

Now, where do we store that data?

We store it using **variables**.

A **variable** is simply:

> A name given to data, so we can use that name to access the data in our program.

Let’s connect it to the examples you already saw.

#### Example: Area of Rectangle

* `length = 15` → here `length` is the variable name, and `15` is the data
* `breadth = 5` → `breadth` is the variable name, and `5` is the data
* `area = length * breadth` → `area` is also a variable that stores the result

So variables are basically **names** we use inside the program to work with data.

#### Example: Bill Calculation

* `prices` is the name given to a list of values (not just one value)
* `quantity` is another list of values
* `total` stores the final answer

So data can be:

* A **single value** (scalar)
* A **list of values** (vector)

---

### 2. Declaration and Initialization

Now let’s learn two important terms:

#### Declaration

When you introduce a variable name in your program:

* Example: `length`

You are saying:

> “I want a variable called length.”

#### Initialization

When you assign a value to that variable:

* Example: `length = 15`

You are saying:

> “Store 15 inside the variable length.”

In Python, **declaration and initialization happen together**.

---

### 3. `=` is Assignment, Not “Equal To”

This is an important point.

When you write:

`length = 15`

You are **not saying**:

> length is equal to 15

You are saying:

> Assign the value 15 to the variable length

So `=` in programming is called the **assignment operator**.

---

### 4. Variables and Memory (How to Visualize It)

<img width="2304" height="1728" alt="image" src="https://github.com/user-attachments/assets/d4fbc649-ea6f-45cb-b409-118271119e9c" />


Your program runs in **RAM (main memory)**.
So the data stored in variables also occupies memory.

When you do:

`length = 15`

Python allocates memory to store the value `15`, and `length` becomes the name that refers to that data.

You can visualize variables in two ways:

#### Visual 1: Variable as “name of the memory location”

* Memory has a location storing `15`
* That location is referred to as `length`

#### Visual 2 (Better for Python): Variable as a “reference”

* Data lives somewhere in memory
* The variable points to it like a reference

In Python, I want you to think like this:

> A variable is a **reference** to data stored in memory.

So `length` is not the data itself —
it is a reference to where that data exists.

---

### 5. Basic Types of Data Stored in Variables

Let’s now see different types of data you can assign.

#### Integer (int)

A number without a decimal point:

* `length = 15`

#### Float (float)

A number with a decimal point:

* `price = 12.75`

#### String (str)

Text written inside quotes:

* `name = 'John'`

At this stage, these three are enough.
There are more data types in Python, and we will learn them slowly.

---

### 6. Multiple Assignment in Python

Python allows you to declare and initialize multiple variables in one line.

Example:

* `name, price, qty = 'Soap', 12.75, 5`

Here:

* `name` gets `'Soap'`
* `price` gets `12.75`
* `qty` gets `5`

Important rule:

> Variables get values in the same order.

This is very useful when values are related, like:

* product name
* product price
* product quantity

---

### 7. Assigning the Same Value to Multiple Variables

You can also initialize multiple variables with the same value:

* `a, b, c = 1, 1, 1`

or

* `a = b = c = 1`

Now here’s an interesting thing about Python:

If the value is the same, Python may not allocate memory three times.
Instead, all variables can point to the **same memory location**.

So internally, it can look like:

* `a` refers to value `1`
* `b` refers to the same `1`
* `c` also refers to the same `1`

---

### 8. Practicing in Jupyter Notebook (Hands-On)

Now let’s practice the same concepts quickly.

#### Example 1: Simple variable

* Declare and initialize:

  * `length = 15`
* Print it:

  * `print(length)`
* Output will be:

  * `15`

#### Example 2: List stored in a variable

* `prices = [ ... ]`
* `print(prices)`
* You’ll see the list printed

#### Example 3: Multiple assignment

* `name, price, qty = 'Soap', 12.75, 5`
* `print(name, price, qty)`
* Output will show all values

---

### 9. Checking Memory Reference Using `id()`

To confirm whether `a`, `b`, and `c` refer to the same location, we can print their IDs.

* `id(a)`
* `id(b)`
* `id(c)`

If the IDs are the same, it means:

> all variables are referring to the same memory location.

So when we initialize multiple variables with the same value, Python can optimize memory usage.

---

### 10. Your Turn

Now it’s your turn:

* Try all these examples on your machine
* Don’t just READ them
* Get comfortable with variable creation and printing

This practice will make the next topics much easier.

---

## Mini Checkpoint

Quick questions for you:

1. What is a variable in Python?
2. In Python, do we declare first and initialize later—or both together?
3. What does `=` mean in programming?
4. If `id(a) == id(b)`, what does that indicate?

---

## Recap

* Variables are **names/references** used to access data
* Python does declaration + initialization together
* `=` is an assignment operator
* Variables refer to data stored in memory
* Basic types: int, float, string
* Python supports multiple assignment
* `id()` helps check whether variables refer to the same object

---

## What’s Next

In the next lecture, we’ll continue with **more concepts related to variables**, and then slowly move deeper into **data types** in Python.
