## Title: Conditional Statements

### Lesson Title: Dictionary (Key–Value Data Structure)

---

### Quick Hook

What if you don’t want to search data by position… but by name?
That’s exactly what a dictionary helps you do — fast, clean, and powerful.

---

### Learning Objectives

By the end of this lesson, you will be able to

* Understand what a dictionary is
* Create dictionaries in multiple ways
* Access, add, update, and delete dictionary items
* Use common dictionary methods confidently
* Understand when and why dictionaries are useful

---

## Main Content

## What is a Dictionary?

A dictionary in Python stores data in **key–value pairs**.

Think of it like a real dictionary book:

* Word → Meaning
* Roll Number → Student Name
* Product ID → Price

Instead of using index numbers like lists, dictionaries use **keys** to access values.

---

## Real-Life Example

Imagine you are storing student marks.

Instead of writing:

* 0 → Rahul → 85
* 1 → Ananya → 92
* 2 → Ravi → 78

You can directly store:

* "Rahul" → 85
* "Ananya" → 92
* "Ravi" → 78

This is much cleaner.

Now, if you want Rahul’s marks, you don’t search through everything.
You directly use the key "Rahul".

That’s why dictionaries are **fast for searching**.

---

## How to Create a Dictionary

Dictionaries are created using curly braces `{}`.

Simple example:

* "apple" → 100
* "banana" → 40

Conceptually, it looks like:

```
{
  "apple": 100,
  "banana": 40
}
```

Here:

* "apple" is the key
* 100 is the value

---

## Accessing Values

If you want the price of apple:

You use the key.

Conceptually:

* Dictionary["apple"]

This directly gives you the value 100.

Notice something important:

* You don’t need to know the position
* You just need the key

---

## Adding New Data

You can also add new items.

Example:

* Add "mango" → 60

Just assign a new key with a value.

Dictionaries grow dynamically.

---

## Updating Values

Suppose the price of apple changes.

You can simply assign a new value to the same key.

The old value gets replaced.

---

## Deleting Data

You can remove items from a dictionary.

Example:

* Remove "banana"

There are specific methods for deletion, which we will practice in examples.

---

## Why Dictionary is Powerful

* Very fast searching
* No need to scan entire data
* Direct access using key
* Cleaner structure for structured data

If your program requires **frequent searching by identifier**, dictionary is the best choice.

---

## Dictionary Comprehension

Just like list comprehension, Python provides a short way to create dictionaries.

Example idea:

* Create a dictionary of numbers and their squares

Instead of writing multiple lines, you can generate it in one clean line.

This is called **dictionary comprehension**.

We will practice this step by step with examples.

---

## Common Dictionary Methods

Dictionaries come with built-in methods such as:

* Getting all keys
* Getting all values
* Getting key–value pairs
* Safely accessing values
* Removing items

We will explore each method with hands-on examples.

---

## Simple Practical Example

Let us take a small example.

Suppose we store country capitals.

* "India" → "New Delhi"
* "Japan" → "Tokyo"
* "France" → "Paris"

Now:

* Ask user for country name
* Print the capital

You see how clean and readable this becomes?

This is where dictionaries shine.

---

## Mini Checkpoint

Pause and think:

* What is stored in a dictionary — index or key?
* Can keys repeat?
* Why are dictionaries faster for searching?
* When would you choose a dictionary over a list?

---

## Recap

* Dictionary stores data as key–value pairs
* Keys are used to access values directly
* Searching is fast and efficient
* You can add, update, and delete items easily
* Dictionary comprehension provides a short creation method

---

## What’s Next

Next, we will practice real dictionary programs and challenges to make you fully comfortable using this powerful data type.
