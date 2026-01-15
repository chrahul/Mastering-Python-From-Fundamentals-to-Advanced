## Title: Conditional Statements

### Lesson Title: for loop and the range function

---

### Quick Hook

You already know how loops repeat work.
Now let us meet the loop that you will use the most in Python: the for loop.

---

### Learning Objectives

By the end of this lesson, you will be able to

* Explain what a for loop is and why it is widely used in Python
* Understand the range function and how it generates values
* Write for loops using range with start, stop, and step
* Use for loops with sequences like strings
* Read and trace for loop execution confidently

---

### Main Content

#### What is a for loop

A loop means repetition.
A for loop is used when you want to repeat an action for **each value in a sequence**.

In Python, the for loop is often called a *for-each loop* because

* It takes values one by one
* It works naturally with sequences

This makes it the most commonly used loop in Python programs.

---

#### Why we must learn range first

Before learning the for loop, we must understand the **range function**.
Why?
Because range is very commonly used with for loops to generate numbers.

Think of range as a **number generator**.

---

### Understanding the range function

The range function can take up to three values

* start value
* stop value
* step value

Important rules to remember

* start is optional, default is 0
* stop is mandatory
* step is optional, default is 1
* stop value is **never included**

---

#### Example 1: range with one value

If you write range(5)

What values are generated

* 0 1 2 3 4

Why not 5
Because range always stops **before** the stop value.

---

#### Example 2: range with start and stop

If you write range(1, 5)

Values generated

* 1 2 3 4

---

#### Example 3: range with different start

If you write range(6, 11)

Values generated

* 6 7 8 9 10

---

#### Example 4: range with step

If you write range(0, 10, 2)

Values generated

* 0 2 4 6 8

The step decides how much the value changes each time.

---

#### Using negative values in range

Range supports negative values too.

Example

* range(-5, -1) generates

  * -5 -4 -3 -2

---

#### Using negative step

Range can move backward as well.

Example

* range(10, 5, -1) generates

  * 10 9 8 7 6

---

### Now let us learn the for loop

#### Basic syntax of for loop

The structure looks like this

* for variable in sequence

  * statements

The variable takes **one value at a time** from the sequence.

---

#### Example 1: for loop with range

Imagine this logic

* Take numbers from 0 to 4
* Print each number

What happens conceptually

* range provides values one by one
* for loop picks each value
* statements inside the loop execute

Execution flow

* variable becomes 0, print it
* variable becomes 1, print it
* variable becomes 2, print it
* variable becomes 3, print it
* variable becomes 4, print it
* no more values, loop ends

The key idea

* range does **not** give all values at once
* values are produced one at a time

---

#### Example 2: for loop with a string

A string is also a sequence.

Think of a string as

* A collection of characters placed in order

When you write a for loop on a string

* The loop takes one character at a time

Conceptual flow

* first character is taken
* printed
* next character is taken
* printed
* continues until characters are finished

This makes for loop extremely powerful and simple.

---

### How for loop works internally

You can think of a for loop like this

* Ask the sequence for the next value
* If a value exists, execute the loop body
* If no value exists, exit the loop

---

### Visualizing the flow

Execution flow of for loop

* Start
* Is there a next value in the sequence

  * Yes: take the value and run loop body
  * No: exit loop
* Execute statements after the loop

This flow repeats automatically for each value.

---

### Why for loop feels different from other languages

In many languages, for loops are counter based.
In Python, for loops are **sequence based**.

Instead of thinking

* how many times to loop

You think

* what sequence do I want to loop over

This makes Python code simpler and more readable.

---

### Mini Checkpoint

Pause and think

* Does range include the stop value
* What happens if you do not provide start in range
* Can for loop work with strings
* Why is for loop called a for-each loop in Python

---

### Recap

* for loop repeats statements for each value in a sequence
* range generates numbers for looping
* start and step in range are optional
* stop value is never included
* for loop works naturally with strings and other sequences

---

### What’s Next

Next, we will practice **for loop challenges** and gradually combine for loop with conditions to solve real problems step by step.
