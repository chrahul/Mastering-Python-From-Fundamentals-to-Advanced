## Title: Dictionary Modification Methods

### Lesson Title: Adding, Updating, Copying, and Deleting Dictionary Entries

---

### Quick Hook

Creating a dictionary is just the beginning.
In real programs, we constantly add new data, update old data, remove entries, or duplicate structures.

In this lesson, we’ll learn the essential dictionary methods that help us do exactly that.

---

### Learning Objectives

By the end of this lesson, you will be able to:

* Use `.update()` to merge dictionaries
* Create a dictionary using `fromkeys()`
* Understand shallow copy using `.copy()`
* Remove entries using `.pop()`, `.popitem()`, and `.clear()`
* Choose the correct method depending on the situation

---

## Main Content

Let’s start with a fresh dictionary example.

```python
students = {
    1: "Arjun",
    2: "Meera",
    3: "Ravi",
    4: "Sneha"
}
```

We’ll use this dictionary throughout the lesson.

---

# 1️⃣ update() – Add or Merge Another Dictionary

Suppose we have new data:

```python
new_students = {
    5: "Karan"
}
```

Now we want to add this into `students`.

```python
students.update(new_students)
```

Now `students` becomes:

```python
{
    1: "Arjun",
    2: "Meera",
    3: "Ravi",
    4: "Sneha",
    5: "Karan"
}
```

### What does update() do?

* Takes another dictionary
* Adds its contents into the existing one
* If a key already exists, it overwrites the value

Think of `update()` as merging data.

---

# 2️⃣ fromkeys() – Create a Dictionary from Keys

Now suppose you only have keys:

```python
roll_numbers = [10, 20, 30, 40]
```

You want to create a dictionary using these as keys.

Use:

```python
dict.fromkeys(roll_numbers)
```

Output:

```python
{
    10: None,
    20: None,
    30: None,
    40: None
}
```

### Why None?

Because you only gave keys.
Python doesn’t know what values to assign.

---

## Setting a Default Value

You can give a default value:

```python
dict.fromkeys(roll_numbers, "Absent")
```

Now:

```python
{
    10: "Absent",
    20: "Absent",
    30: "Absent",
    40: "Absent"
}
```

Important:

* `fromkeys()` is called using the class name `dict`
* It creates a new dictionary

---

# 3️⃣ copy() – Create a Shallow Copy

Suppose we want a duplicate dictionary.

```python
students_copy = students.copy()
```

Now both dictionaries look the same.

But here is something important:

This is a **shallow copy**.

---

## What Does Shallow Copy Mean?

* A new dictionary object is created
* But it refers to the same internal values

Think of it like this:

* Two notebooks
* But both are copying the same printed text

If you change a value in `students_copy`, it does not affect `students`.

But internally, Python shares references for immutable objects.

For now, just remember:

`.copy()` creates a separate dictionary structure.

---

# 4️⃣ pop() – Remove a Specific Key

Suppose we want to remove key 2.

```python
students.pop(2)
```

This does two things:

* Removes key 2
* Returns its value

If key 2 had value "Meera", that value gets returned.

Now dictionary becomes:

```python
{
    1: "Arjun",
    3: "Ravi",
    4: "Sneha"
}
```

---

## What if Key Doesn’t Exist?

```python
students.pop(100)
```

This gives an error.

To avoid that:

```python
students.pop(100, "Not Found")
```

Now:

* No error
* Returns "Not Found"

---

# 5️⃣ popitem() – Remove the Last Inserted Item

```python
students.popitem()
```

This removes the most recently inserted entry.

It returns a tuple:

```python
(key, value)
```

After removal, the dictionary shrinks.

---

# 6️⃣ clear() – Remove Everything

If you want to empty the dictionary completely:

```python
students.clear()
```

Now:

```python
{}
```

Dictionary becomes empty.

---

# Quick Summary of Methods

| Method     | Purpose                     |
| ---------- | --------------------------- |
| update()   | Merge another dictionary    |
| fromkeys() | Create dictionary from keys |
| copy()     | Create shallow copy         |
| pop()      | Remove specific key         |
| popitem()  | Remove last inserted item   |
| clear()    | Remove all entries          |

---

# When Should You Use What?

* Use `update()` when combining data
* Use `fromkeys()` when keys exist but values are unknown
* Use `copy()` when duplicating data safely
* Use `pop()` when deleting specific entries
* Use `clear()` when resetting everything

---

### Mini Checkpoint

Think about these:

1. What happens if `update()` receives a key that already exists?
2. What value does `fromkeys()` assign by default?
3. Does `.copy()` create a deep copy?
4. Which method removes the last inserted item?

---

### Recap

* Dictionaries have built-in methods for modification
* `update()` merges dictionaries
* `fromkeys()` builds dictionary from a sequence
* `copy()` creates a shallow copy
* `pop()`, `popitem()`, and `clear()` remove entries

You now know how to fully manage dictionary data.

---

### What’s Next

Next, we’ll solve practical challenges using dictionaries so you can apply all these methods in real scenarios.
