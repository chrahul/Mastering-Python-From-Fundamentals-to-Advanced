
## Example 1: Using `break`

### Real World Scenario: Exit a Menu

**Situation**
You are building a small menu system.
The program should keep running **until the user chooses Exit**.

---

### Program Example Using `break`

```python
while True:
    choice = input("Enter option (1 View, 2 Settings, 3 Exit): ")

    if choice == "3":
        print("Exiting application")
        break

    print("You selected option", choice)
```

---

### What Is Happening Here

* `while True` keeps the program running
* User keeps entering options
* When the user enters `3`

  * `break` immediately exits the loop
* Program stops cleanly

---

### Real World Mapping

This pattern is used in

* Application menus
* Command line tools
* Games exit option
* Admin consoles

**Key idea**
 `break` means **stop looping completely**

---

## Example 2: Using `continue`

### Real World Scenario: Skip Invalid Input

**Situation**
You are collecting ages from users.
If the age is invalid, skip it and ask again.

---

### Program Example Using `continue`

```python
while True:
    age = int(input("Enter your age (0 to exit): "))

    if age == 0:
        print("Thank you")
        break

    if age < 0:
        print("Invalid age. Try again")
        continue

    print("Your age is", age)
```

---

### What Is Happening Here

* Loop keeps running
* If age is negative

  * `continue` skips printing
  * Goes back to the start of the loop
* Valid age gets printed
* Entering `0` exits using `break`

---

### Real World Mapping

This pattern is used in

* Form validation
* User input checking
* Data cleaning pipelines
* Prompt validation in GenAI

**Key idea**
 `continue` means **skip this round, try again**

---

## Break vs Continue (One Line Difference)

* `break` → exit the loop
* `continue` → skip the current step, loop again

Students usually confuse these two.
Seeing them **side by side** fixes that permanently.

---

.
