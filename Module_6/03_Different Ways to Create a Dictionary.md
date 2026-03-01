

### Lesson Title: Different Ways to Create a Dictionary

---

### Quick Hook

You already know how to create a dictionary using curly brackets.
But what if your data comes in a different format — like two lists or a list of pairs?

In this lesson, we’ll learn smarter ways to create dictionaries.

---

### Learning Objectives

By the end of this lesson, you will be able to

* Create a dictionary using multiple methods
* Build a dictionary from iterable pairs
* Use the `zip()` function to combine keys and values
* Use the `enumerate()` function to auto-generate keys
* Understand when each method is useful

---

## Main Content

## Quick Recap: What is a Dictionary?

A dictionary is a collection of **key–value pairs**.

Example:

```python
profile = {
    "name": "Kiran",
    "age": 25,
    "city": "Hyderabad"
}
```

* "name" is the key
* "Kiran" is the value

Now let’s see different ways to create dictionaries beyond this direct method.

---

# Method 1: Direct Creation Using Curly Brackets

This is the simplest and most common way.

### Example

```python
employee = {
    1: "Manager",
    2: "Developer",
    3: "Designer"
}
```

This method is clear and straightforward.

But what if your data is not already in key–value form?

---

# Method 2: Creating Dictionary from Iterable Pairs

Suppose you already have data stored like this:

A list of pairs.

### Example

```python
data = [
    (101, "Laptop"),
    (102, "Tablet"),
    (103, "Mobile")
]
```

Here:

* Each tuple is a pair
* First element → key
* Second element → value

This is called **iterable pairs**.

Now we can convert this into a dictionary using the `dict()` function.

```python
products = dict(data)
```

Now `products` becomes:

```python
{
    101: "Laptop",
    102: "Tablet",
    103: "Mobile"
}
```

### Important Idea

`dict()` accepts an iterable where each element contains two items:

* key
* value

It does not care whether it is:

* list of tuples
* list of lists
* tuple of tuples

As long as each element has exactly two values.

---

## Simple Variation

Instead of tuples, you could write:

```python
data = [
    [201, "Math"],
    [202, "Science"]
]
```

Still works with:

```python
subjects = dict(data)
```

---

# Method 3: Using zip() Function

Now imagine this situation:

You have two separate lists:

```python
ids = [1, 2, 3]
names = ["Anil", "Sneha", "Rohit"]
```

One list has keys.
Another list has values.

Now how do we combine them?

That’s where `zip()` comes in.

---

## What Does zip() Do?

Think of a zipper in a jacket.

It joins:

* One element from first list
* One element from second list

Example:

```python
pairs = zip(ids, names)
```

Internally, it creates pairs like:

* (1, "Anil")
* (2, "Sneha")
* (3, "Rohit")

Now we pass this to `dict()`:

```python
students = dict(zip(ids, names))
```

And we get:

```python
{
    1: "Anil",
    2: "Sneha",
    3: "Rohit"
}
```

---

### What if One List Is Longer?

If one list has extra values:

```python
ids = [1, 2, 3, 4]
names = ["Anil", "Sneha", "Rohit"]
```

`zip()` will ignore the extra item.

It only pairs matching positions.

---

# Method 4: Using enumerate()

Now imagine this scenario:

You have only values.

```python
colors = ["Red", "Green", "Blue"]
```

You want automatic numeric keys.

That’s where `enumerate()` helps.

---

## What Does enumerate() Do?

It adds a number to each element.

By default, numbering starts from 0.

Example:

```python
dict(enumerate(colors))
```

Result:

```python
{
    0: "Red",
    1: "Green",
    2: "Blue"
}
```

---

## Starting from a Different Number

You can change starting value:

```python
dict(enumerate(colors, start=1))
```

Now output becomes:

```python
{
    1: "Red",
    2: "Green",
    3: "Blue"
}
```

Very clean and useful when:

* You want index-based keys
* You don’t want to manually write them

---

# Summary of All Methods

We learned four ways:

1. Direct curly bracket method
2. Using iterable pairs
3. Using zip()
4. Using enumerate()

In all cases, the final step is often:

```python
dict(...)
```

Which converts iterable pairs into a dictionary.

---

# When to Use Which Method?

* Data already in key–value format → use curly brackets
* Data in paired structure → use dict(iterable)
* Keys and values in separate lists → use zip()
* Only values available → use enumerate()

In real projects, data may come in any format.
You must know how to convert it into a dictionary.

---

### Mini Checkpoint

Pause and think:

* What does `dict()` expect as input?
* What happens if zip() gets lists of unequal length?
* What is the default starting index of enumerate()?
* When would you use enumerate() instead of zip()?

---

### Recap

* Dictionary can be created in multiple ways
* `dict()` converts iterable pairs into dictionary
* `zip()` combines two lists into pairs
* `enumerate()` generates numeric keys automatically
* Choose the method based on how your data is structured

---

### What’s Next

Next, we will learn **dictionary comprehension**, which allows us to create dictionaries in a short and elegant way.
