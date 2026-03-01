## Title: Dictionary Looping Methods

### Lesson Title: Looping Over and Accessing Dictionary Data

---

### Quick Hook

You already know how to create a dictionary.
Now the real question is — how do we **move through it**, access values safely, and work with all entries efficiently?

That’s exactly what we’ll learn in this lesson.

---

### Learning Objectives

By the end of this lesson, you will be able to:

* Loop through dictionary keys, values, and key–value pairs
* Use `.keys()`, `.values()`, and `.items()` correctly
* Understand the difference between index access and `.get()`
* Use `.setdefault()` and understand how it modifies a dictionary
* Choose the right method based on your requirement

---

## Main Content

Let’s start with a simple example dictionary.

```python
inventory = {
    101: "Pen",
    102: "Notebook",
    103: "Eraser",
    104: "Marker"
}
```

We will use this dictionary throughout the lesson.

---

# 1️ Basic Looping Using a for Loop

You already know this:

```python
for key in inventory:
    print(key)
```

This prints **only the keys**.

Because when you loop directly over a dictionary, Python automatically gives you keys.

If you want values too:

```python
for key in inventory:
    print(key, inventory[key])
```

Here:

* `key` gives the key
* `inventory[key]` gives the value

Simple and clear.

---

# 2️ Using .keys() Method

If you explicitly want keys:

```python
inventory.keys()
```

This returns a special object called `dict_keys`.

To actually see them clearly:

```python
for k in inventory.keys():
    print(k)
```

You will get:

```
101
102
103
104
```

 Important:
`inventory` and `inventory.keys()` behave almost the same in loops.

---

# 3️ Using .values() Method

If you only want values:

```python
for v in inventory.values():
    print(v)
```

Output:

```
Pen
Notebook
Eraser
Marker
```

Use this when:

* You don’t care about keys
* You only want stored values

---

# 4️ Using .items() Method

Now suppose you want both key and value together.

Use `.items()`.

```python
for k, v in inventory.items():
    print(k, v)
```

Here:

* `.items()` returns pairs
* `k, v` unpack those pairs

Output:

```
101 Pen
102 Notebook
103 Eraser
104 Marker
```

 Think of `.items()` as giving you ready-made key–value tuples.

---

## Summary So Far

| Method     | What It Gives   |
| ---------- | --------------- |
| dictionary | Keys            |
| .keys()    | Keys            |
| .values()  | Values          |
| .items()   | Key–Value pairs |

---

# 5️ Using .get() Method

Now let’s talk about accessing a single value.

Normal way:

```python
inventory[102]
```

Output:

```
Notebook
```

But what if the key does not exist?

```python
inventory[999]
```

This gives an error.

---

## Using get()

```python
inventory.get(999)
```

No error.
It returns `None`.

That’s safer.

---

## Providing a Default Value

You can also give an alternate value.

```python
inventory.get(999, "Item Not Found")
```

Now output will be:

```
Item Not Found
```

 Important Difference:

* `[]` → raises error if key missing
* `.get()` → returns `None` (or custom value)

Use `.get()` when you want safer access.

---

# 6️ Using .setdefault() Method

This one is slightly different.

Let’s try:

```python
inventory.setdefault(103)
```

Since key 103 exists, it returns:

```
Eraser
```

Now try with a missing key:

```python
inventory.setdefault(200)
```

Now something interesting happens.

* It inserts key 200
* Assigns value `None`

Check dictionary:

```python
print(inventory)
```

You will see:

```
200: None
```

So `.setdefault()` does two things:

* If key exists → returns value
* If key doesn’t exist → adds it

---

## Setting a Custom Default

```python
inventory.setdefault(300, "Pencil")
```

Now:

* Key 300 gets inserted
* Value becomes "Pencil"

This method actually modifies the dictionary.

That is the big difference from `.get()`.

---

# Difference Between get() and setdefault()

| Method       | Adds Missing Key? | Raises Error? |
| ------------ | ----------------- | ------------- |
| []           | ❌                 | ✅             |
| get()        | ❌                 | ❌             |
| setdefault() | ✅                 | ❌             |

---

## When to Use What?

* Use `[]` when you are sure the key exists
* Use `.get()` when you want safe access
* Use `.setdefault()` when you want to insert if missing

---

### Mini Checkpoint

Pause and think:

1. What happens when you loop directly over a dictionary?
2. What does `.items()` return?
3. What is the difference between `.get()` and `[]`?
4. Which method modifies the dictionary: `.get()` or `.setdefault()`?

---

### Recap

* Looping over dictionary gives keys by default
* `.keys()` → keys
* `.values()` → values
* `.items()` → key–value pairs
* `.get()` safely retrieves values
* `.setdefault()` inserts missing keys

---

### What’s Next

In the next lesson, we will learn how to **add, update, and delete entries** in a dictionary — which makes dictionary handling even more powerful.
