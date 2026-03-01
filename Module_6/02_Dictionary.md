## Title: Conditional Statements

### Lesson Title: Dictionary – Key–Value Data Structure

---

### Quick Hook

What if instead of remembering positions, you could access data by name?
That’s exactly what a dictionary lets you do — fast lookup using keys.

---

### Learning Objectives

By the end of this lesson, you will be able to

* Understand what a dictionary is and how it differs from lists
* Create dictionaries with different types of keys and values
* Read, update, and insert data into a dictionary
* Traverse a dictionary using a loop
* Understand why keys must be immutable

---

## Main Content

## What is a Dictionary?

A dictionary is a data type that stores information in **key–value pairs**.

Unlike lists or tuples, where we use index positions (0, 1, 2…),
in a dictionary, we use **keys** to access values.

Think of it like this:

* Employee ID → Employee Name
* Product Code → Product Price
* Username → Password

The key is used to quickly find the value.

That’s why dictionary is often called an **associative data type** or similar to a **hash table**.

---

## How to Create a Dictionary

Dictionaries are created using **curly brackets `{}`**.

Important:

* Empty `{}` creates a dictionary, not a set.

### Simple Example

Let’s create a dictionary for a small store.

* Product ID → Product Name

Conceptually:

```python
products = {
    101: "Pen",
    102: "Notebook",
    103: "Eraser"
}
```

Each entry looks like:

* key : value

So here:

* 101 is the key
* "Pen" is the value

Each pair is called:

* Entry
* Item
* Key–Value Pair

All mean the same thing.

---

## Important Rules About Keys

* Keys must be **unique**
* Values can be duplicated
* Keys are used for searching
* Keys must be **immutable**

We will understand immutable part shortly.

---

## Reading Data from a Dictionary

To get a value, you use the key inside square brackets.

Example:

```python
products[101]
```

This gives:

* "Pen"

You give the key → you get the value.

---

### What if the Key Does Not Exist?

If you try:

```python
products[999]
```

You will get:

* KeyError

Because that key does not exist.

Dictionary does not ignore mistakes silently.
If key is missing, it raises an error.

---

## Updating an Existing Value

Suppose the product name for 102 needs correction.

You simply assign a new value:

```python
products[102] = "Spiral Notebook"
```

If the key already exists:

* The value gets replaced

Very simple.

---

## Adding a New Entry

If the key does not exist, assignment adds a new entry.

Example:

```python
products[104] = "Marker"
```

Now 104 is added to the dictionary.

So assignment works in two ways:

* If key exists → update
* If key does not exist → insert

---

## Traversing a Dictionary

Now let us see how to loop through a dictionary.

If you write:

```python
for item in products:
    print(item)
```

It prints only the keys.

Why?

Because by default, dictionary traversal gives keys.

---

### Getting Values While Traversing

Inside the loop, the variable contains the key.

So you can get value like this:

```python
for item in products:
    print(item, products[item])
```

This prints both:

* key
* value

---

## Can Keys and Values Be Any Type?

Yes… with some rules.

### Keys can be:

* Integer
* Float
* String
* Boolean
* Tuple

But NOT:

* List
* Set
* Dictionary

Why?

Because keys must be **immutable (hashable)**.

Lists are mutable, so they cannot be keys.

---

### Simple Example

Valid key:

```python
data = {
    (1, 2): "Coordinates"
}
```

Invalid key:

```python
data = {
    [1, 2]: "Coordinates"
}
```

This gives an error:

* TypeError: unhashable type: list

Remember:

Only immutable types can be keys.

---

## Values Can Be Anything

Values can be:

* Integer
* String
* List
* Tuple
* Set
* Dictionary

Example:

```python
student = {
    "name": "Amit",
    "marks": [80, 85, 90],
    "details": {"age": 20, "city": "Delhi"}
}
```

Here values include:

* String
* List
* Dictionary

No restriction on value type.

---

## Real-World Style Example

Let’s create a dictionary for exam scores.

* Roll Number → Student Name

```python
students = {
    1: "Neha",
    2: "Arjun",
    3: "Riya"
}
```

Now:

```python
students[2]
```

Returns:

* "Arjun"

You see how clean and readable this is?

No searching through a list.
Just direct access.

---

## Why Dictionary is Powerful

* Fast searching
* Clear structure
* Organized data storage
* Easy updates and insertions
* Extremely useful in real programs

In data science and real applications, dictionaries are used very frequently.

---

### Mini Checkpoint

Pause and think:

* What is stored in a dictionary — index or key?
* Can two keys be the same?
* Why can’t a list be used as a key?
* What happens if you access a key that does not exist?

---

### Recap

* Dictionary stores data as key–value pairs
* Keys are unique and must be immutable
* Values can be any type
* Assignment updates or inserts data
* Looping through dictionary gives keys by default

---

### What’s Next

Next, we will explore **dictionary methods and dictionary comprehension** to create and manipulate dictionaries more efficiently.
