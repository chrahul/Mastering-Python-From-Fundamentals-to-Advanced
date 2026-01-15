## Title: Conditional Statements

### Lesson Title: else with while loop

---

### Quick Hook

You already know how if else works.
Now let us look at a lesser known but powerful Python feature where else works with loops too.

---

### Learning Objectives

By the end of this lesson, you will be able to

* Understand what else with while loop means
* Explain when the else block of a loop executes
* Distinguish between normal loop completion and break based exit
* Read and reason about while else programs confidently
* Use while else intentionally instead of accidentally

---

### Main Content

#### Revisiting else with if

Let us quickly recall how else works with if.

* If the condition is true, the if block runs
* If the condition is false, the else block runs

This behavior is familiar and straightforward.

---

#### Can else be used with loops

Yes.
In Python, else can be used with

* if
* while
* for
* try

In this lesson, we will focus only on **else with while**.

---

#### Basic structure of while with else

A while loop normally looks like this

* Condition is checked
* Statements inside the loop run while the condition is true
* When the condition becomes false, the loop stops

Now Python allows an else block after the while loop.

Conceptually, it looks like this

* while condition

  * loop body
* else

  * statements

The else block belongs to the while loop, not to an if statement.

---

#### How while else actually works

Let us understand the execution flow step by step.

1. Python checks the while condition
2. If the condition is true, it enters the loop
3. The loop repeats as long as the condition remains true
4. When the condition becomes false

   * Python exits the loop
   * Then executes the else block

So far, this looks similar to if else.

But there is an important difference.

---

#### The real purpose of while else

The else block of a while loop executes **only if the loop ends normally**.

Normal ending means

* The loop stops because the condition became false

The else block does **not** execute if the loop stops because of a break statement.

This is the key idea.

---

#### Example 1: Loop completes normally

Think about this logic in plain English.

* Start counting from 1
* Keep counting while the value is less than or equal to 5
* When counting is complete, print a message

What happens conceptually

* Loop prints values from 1 to 5
* Condition becomes false
* else block runs
* Program continues

So the else block confirms that the loop finished all its iterations successfully.

---

#### Example 2: Loop exits using break

Now let us slightly change the situation.

* Start counting from 1
* Stop immediately when the value reaches 3

What happens

* Loop prints 1 and 2
* When value becomes 3, break executes
* Loop exits immediately
* else block is skipped
* Program continues after the loop

This tells us something important.

---

#### What else with while really means

You can think of while else like this

* else means the loop completed without interruption
* break means the loop was interrupted
* else does not run if break was used

This makes while else very useful when you want to

* Confirm successful completion
* Detect early exit
* Separate normal flow from interrupted flow

---

#### When should you use while else

Use while else when

* You want to run cleanup logic only after full loop completion
* You want to detect whether a search loop failed or succeeded
* You want cleaner logic without extra flags or variables

If the loop stops early using break, else is skipped automatically.

---

### Mini Checkpoint

Pause and answer these

* When does the else block of a while loop execute
* What happens to else if break is used
* Is else attached to if or while in this lesson
* Why might while else be better than using a flag variable

---

### Recap

* Python allows else with while loops
* else executes only when the loop ends normally
* break prevents the else block from running
* while else helps detect successful loop completion
* This feature simplifies certain program flows

---

### What’s Next

In the next lesson, we will practice more loop patterns and move toward **for loops**, where else works the same way but feels even more natural.
