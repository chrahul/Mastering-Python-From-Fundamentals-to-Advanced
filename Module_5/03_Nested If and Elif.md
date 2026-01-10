## Title: Conditional Statements

### Lesson Title: Nested If and Elif

---

### Quick Hook

Real life decisions rarely stop at just two choices.
This lesson teaches your program how to handle **multiple conditions** in a clean and logical way.

---

### Learning Objectives

By the end of this lesson, you will be able to:

* Explain what nested if statements mean
* Write if and else inside another if or else block
* Understand what elif is and why it exists
* Replace nested logic with cleaner elif structures
* Use an if elif ladder to handle multiple conditions

---

### Main Content

### Quick Revision – If Else Basics

You already know how a basic conditional statement works:

* A condition is checked
* If the condition is true, the if block runs
* Otherwise, the else block runs

This entire structure is called a conditional statement.

Now the question is
Can we place another conditional statement **inside** this structure?

Yes, and that is where nesting begins.

---

### What Does Nested If Mean

Nested means **one thing inside another**.

In conditional statements, nesting means:

* Writing an if else inside another if block
* Writing an if else inside an else block

Both are allowed in Python.

So you can have:

* If inside if
* If inside else

You can even nest multiple levels if required.

This technique is used when a decision depends on a previous decision.

---

### Example – Temperature Classification Using Nested If

Let us understand nesting with a simple and realistic example.

Task
Check room temperature and classify it as:

* Normal
* Cold
* Hot

Logic we want:

* If temperature is exactly twenty five

  * Print normal
* Else

  * If temperature is less than twenty five

    * Print cold
  * Else

    * Print hot

Here is what is happening:

* First condition checks for normal temperature
* If that fails, we move to the else block
* Inside else, we again check another condition
* Based on that, one more decision is made

This is a perfect example of **nested if**.

---

### Why Nested If Is Useful

Nested if helps when:

* One decision depends on another
* You want fine control over logic
* Conditions are not independent

However, too much nesting can make code harder to read.

That is where elif comes in.

---

### Introducing Elif – Cleaner Decision Making

Elif is short for else if.

Instead of writing:

* Else

  * If condition

Python allows you to combine them as:

* Elif condition

This makes the code:

* Shorter
* Cleaner
* Easier to understand

The logic remains exactly the same.

---

### Same Example Using Elif

Now let us rewrite the temperature logic using elif.

Decision flow:

* If temperature equals twenty five

  * Print normal
* Elif temperature is less than twenty five

  * Print cold
* Else

  * Print hot

This version is easier to read and avoids deep nesting.

---

### Elif Ladder – Handling Multiple Conditions

When a program needs to check many conditions one by one, we use an **elif ladder**.

Structure looks like this:

* If condition one
* Elif condition two
* Elif condition three
* Elif condition four
* Else

How it works:

* Python checks conditions from top to bottom
* The first true condition executes
* All remaining conditions are skipped
* If none are true, else runs

This pattern is extremely common in real programs.

---

### When to Use Nested If vs Elif

Use nested if when:

* One decision depends on another
* Conditions are hierarchical

Use elif ladder when:

* You are checking multiple independent conditions
* Only one condition should match

---

### Mini Checkpoint

Think about these:

* Can an if exist inside an else block
* What problem does elif solve
* Will Python check all elif conditions once one is true
* Which is more readable for multiple conditions

---

### Recap

* Nested if means placing one conditional inside another
* Nesting is useful but can reduce readability
* Elif combines else and if into one statement
* Elif ladder handles multiple conditions cleanly
* Python executes only the first true condition

---

### What’s Next

In the next lesson, we will **solve practical challenges** using nested if and elif.
This will help you gain confidence and write better decision logic.
