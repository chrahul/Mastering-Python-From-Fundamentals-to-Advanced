## Title: Conditional Statements – If Else

### Quick Hook

Programs become powerful when they can **decide**.
This lesson teaches your program how to choose between two paths based on a condition.

---

### Learning Objectives

By the end of this lesson, you will be able to:

* Understand relational operators and how comparisons work
* Explain what a conditional statement is
* Write simple if else logic in Python
* Predict how a program flows based on conditions
* Visualize program execution using control flow thinking

---

### Main Content

### Relational Operators – Making Comparisons

Before a program can decide, it must **compare** values.

Relational operators are used to compare data and they always produce a **boolean result**.

That result is either true or false.

Common relational comparisons include:

* Less than
* Less than or equal to
* Greater than
* Greater than or equal to
* Equal to
* Not equal to

These operators compare two values and answer a simple question.

For example:

* Is three less than six
  Result is true

* Is three greater than six
  Result is false

This true or false result becomes the foundation for conditional statements.

---

### What Is a Conditional Statement

A conditional statement allows your program to execute code **only when a condition is satisfied**.

In simple words:

* If a condition is true, do one thing
* Otherwise, do something else

This is how programs start behaving intelligently.

---

### If Else – Basic Decision Making

<img width="4800" height="2700" alt="image" src="https://github.com/user-attachments/assets/39a3a72d-42b8-4bdc-ac8d-1df47d238e39" />


The most basic conditional structure has two parts:

* If block
* Else block

How it works:

* First, Python checks the condition
* If the condition is true

  * Statements inside the if block are executed
* If the condition is false

  * Statements inside the else block are executed

Only one block runs. Never both.

---

### Importance of Indentation

Python uses indentation to understand **which statements belong to which block**.

Statements under if must be indented
Statements under else must also be indented

Indentation is not optional in Python.
It defines logic.

---

### Example – Checking Positive or Negative

Let us understand this with a simple example.

Goal:
Check whether a number is positive or negative.

Logic:

* If the number is greater than or equal to zero

  * Print positive
* Otherwise

  * Print negative

Flow explanation:

* Python reads the number
* Condition is checked
* Based on true or false, one block runs
* Program ends

If the number is positive, the if block executes.
If the number is negative, the else block executes.

---

### Control Flow – How Programs Move

Normally, a program runs **top to bottom**, one statement after another.

This is called linear flow.

Conditional statements change this flow.

Instead of running everything:

* The program pauses
* Evaluates a condition
* Chooses one path
* Skips the other path

This movement of execution is called **control flow**.

---

### Visualizing Control Flow

Think of control flow like a road junction:

* Program starts
* Reaches a decision point
* One road is taken if condition is true
* Another road is taken if condition is false

Only one road is followed.

This way of thinking helps a lot when programs become bigger.

---

### Mini Checkpoint

Pause and think:

* What kind of result does a comparison produce
* Can both if and else blocks execute together
* Why is indentation critical in Python
* What happens when a condition is false

---

### Recap

* Relational operators compare values
* Comparisons always result in true or false
* If else allows decision making in programs
* Only one block executes based on the condition
* Control flow determines how a program runs

---

### What’s Next

In the next lesson, we will practice **real problems** using if else.
You will solve small challenges to strengthen your decision making logic.
