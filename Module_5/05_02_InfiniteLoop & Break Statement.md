### Title

Conditional Statements and Loop Control

---

### Quick Hook

So far, your loops have started and stopped nicely.
But what happens when a loop never stops, or when you want to exit early, or skip certain steps?
This lesson answers those exact questions.

---

### Learning Objectives

By the end of this lesson, you will be able to

* Understand what an infinite loop is and why it happens
* Identify common mistakes that cause loops to run forever
* Use the break statement to exit a loop safely
* Use the continue statement to skip specific iterations
* Write safer and more controlled while loops

---

### Main Content

#### Revisiting the While Loop

You already know how a while loop works.

* It repeats a block of code
* It keeps running as long as the condition is true
* It stops when the condition becomes false

This makes while loops powerful, but also risky if not written carefully.

---

#### Infinite Loop

An infinite loop is a loop that never stops running.

Why does this happen

* The condition is always true
* The variable used in the condition is never updated
* The stopping condition is written incorrectly

Example of an intentional infinite loop

* Using true directly as the condition
* The loop will never become false

This kind of loop keeps repeating forever unless you forcefully stop the program.

Why this matters

* Infinite loops can freeze programs
* They consume CPU and memory
* They usually happen by mistake, not on purpose

So the real lesson here is
Always make sure the condition can eventually become false.

---

#### Common Causes of Accidental Infinite Loops

1. Wrong condition
   If the condition is logically incorrect, the loop may never end

2. Missing update
   If the variable used in the condition is not modified inside the loop, the loop cannot stop

3. Comparison mistake
   Using equality where a range or limit is expected can cause endless repetition

Good practice

* Check your condition carefully
* Ensure the loop variable changes every iteration

---

#### Break Statement

Sometimes you want to stop a loop immediately, even if the condition is still true.
This is where break is useful.

What break does

* Instantly exits the loop
* Control moves to the first statement after the loop

How break is usually used

* Inside an if condition
* Triggered when a specific situation occurs

Example use cases

* User enters a correct password
* Required value is found
* Error condition is detected

Once break runs, the loop ends immediately.

---

#### Continue Statement

The continue statement does not stop the loop.
Instead, it skips the remaining statements for the current iteration.

What continue does

* Skips the rest of the loop body
* Jumps back to the condition check
* Continues with the next iteration

Think of it as
Skip this round, move to the next one.

---

#### Realistic Example for Continue

Imagine a loop that prints numbers from one to ten.
Now add a rule

* Do not print numbers divisible by three

Using continue

* When a number is divisible by three, skip printing
* Continue with the next number

This allows you to filter values without stopping the loop.

---

#### Key Difference Between Break and Continue

Break

* Ends the loop completely

Continue

* Skips the current iteration
* Loop continues running

Knowing when to use each makes your loops clean and efficient.

---

### Mini Checkpoint

Try answering these mentally

* What makes a loop infinite
* Why updating the loop variable is important
* What happens immediately after break executes
* What continue skips and what it does not

---

### Recap

* Infinite loops happen when conditions never become false
* Most infinite loops are caused by logic mistakes
* Break exits the loop instantly
* Continue skips the current iteration only
* Careful conditions make loops safe and predictable

---

### What’s Next

In the next lesson, we will practice these concepts through hands on challenges.
You will learn to spot infinite loops quickly and control loop behavior with confidence.
