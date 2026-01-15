## Title: Conditional Statements

### Lesson Title: Nested Loops

---

### Quick Hook

What if one loop is not enough to solve your problem?
Nested loops help you repeat logic *inside* another repetition, just like working row by row in a table.

---

### Learning Objectives

By the end of this lesson, you will be able to

* Understand what a nested loop really means
* Write one loop inside another loop correctly
* Predict how outer and inner loops execute
* Use nested loops with a clear, real world style example
* Recognize when nested loops are the right tool

---

### Main Content

## What is a Nested Loop

A nested loop simply means

* A loop written **inside another loop**

You can nest

* A for loop inside a for loop
* A while loop inside a while loop

In this lesson, we will focus on **nested for loops**, because they are easier to read and widely used.

---

## A Simple Real World Analogy

Imagine a **cinema hall**.

* The hall has multiple rows
* Each row has multiple seats

If you want to check **every seat**, how would you do it?

You would

* Go row by row
* Inside each row, check every seat

This is exactly how nested loops work.

---

## A Simple Single Loop Example

First, let us look at a **single loop**.

Example idea

* Print floor numbers in a building

Concept

* Floors: 1 to 3

Simple logic

* Loop runs once for each floor

This loop prints

* Floor 1
* Floor 2
* Floor 3

This is a **single loop**, no nesting yet.

---

## Introducing a Nested Loop

Now let us extend the idea.

New requirement

* Each floor has **rooms**
* Rooms are numbered from 1 to 2

So now the task becomes

* For each floor
* Print all room numbers

This is where **nested loops** are needed.

---

## How the Nested Loop Is Structured

* **Outer loop** → controls floors
* **Inner loop** → controls rooms

Think of it like this

* Outer loop decides *which floor* you are on
* Inner loop walks through *all rooms on that floor*

---

## Simple Nested Loop Example

Let us imagine the logic in words

* For each floor from 1 to 3

  * For each room from 1 to 2

    * Print floor and room number

This will generate combinations like

* Floor 1 Room 1
* Floor 1 Room 2
* Floor 2 Room 1
* Floor 2 Room 2
* Floor 3 Room 1
* Floor 3 Room 2

---

## Step by Step Execution

Let us trace it slowly.

### Step 1

Outer loop starts

* Floor = 1

Inner loop starts

* Room = 1 → print Floor 1 Room 1
* Room = 2 → print Floor 1 Room 2

Inner loop finishes

---

### Step 2

Outer loop moves to next value

* Floor = 2

Inner loop starts again from the beginning

* Room = 1 → print Floor 2 Room 1
* Room = 2 → print Floor 2 Room 2

Inner loop finishes

---

### Step 3

Outer loop moves again

* Floor = 3

Inner loop runs again

* Room = 1 → print Floor 3 Room 1
* Room = 2 → print Floor 3 Room 2

Inner loop finishes
Outer loop finishes

---

## Key Observation

* The **inner loop always completes fully**
* Only after that does the **outer loop move forward**
* Inner loop restarts fresh for every outer loop value

---

## Why Nested Loops Are Useful

Nested loops are commonly used when working with

* Tables
* Grids
* Seating arrangements
* Timetables
* Two dimensional data

Anywhere you see **rows and columns**, nested loops are a natural fit.

---

## Another Simple Example: Daily Schedule

Imagine

* Days: Monday to Wednesday
* Tasks per day: Task 1 and Task 2

Logic

* For each day

  * Print all tasks

This again needs

* Outer loop for days
* Inner loop for tasks

Same concept, different problem.

---

## Can We Nest More Loops

Yes.

* Two loops → two dimensional problems
* Three loops → three dimensional problems

But remember

* More nesting means more complexity
* Always keep your logic clear and readable

---

### Mini Checkpoint

Pause and think

* Which loop runs more times, outer or inner
* Does the inner loop restart for every outer loop value
* Can you think of one real life example with rows and columns

---

### Recap

* A nested loop is a loop inside another loop
* Outer loop controls the big step
* Inner loop handles repeated small steps
* Inner loop always finishes before outer loop moves ahead
* Nested loops are ideal for structured data

---

### What’s Next

Next, we will practice **nested loop challenges**, including pattern printing and logic building to strengthen your understanding.
