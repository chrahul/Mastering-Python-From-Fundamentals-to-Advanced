
### Title

Loop Control in a Real World Program

---

### Quick Hook

Imagine you are building a small system that keeps taking user input until the user decides to exit.
This is exactly how login screens, menus, and validation systems work in real applications.

---

### Learning Objectives

By the end of this lesson, you will be able to

* Understand how infinite loops are used intentionally
* Use break to safely exit a running loop
* Use continue to skip invalid inputs
* Connect loop control to real software behavior

---

### Main Content

#### Real World Scenario

Let us build a **simple ATM style PIN validation system**.

Rules of the system

* The user must enter a 4 digit PIN
* If the PIN is correct, access is granted
* If the PIN is wrong, the user is asked again
* If the user enters an invalid input, skip it and ask again

This is a perfect use case for

* While loop
* Break
* Continue


<img width="4800" height="2700" alt="image" src="https://github.com/user-attachments/assets/032f8ea0-6d4a-4ce3-b63b-bb109149cee2" />


---

#### Step 1: Why an Infinite Loop is Needed

We do not know in advance

* How many times the user will enter a wrong PIN
* When the correct PIN will be entered

So we use an infinite loop intentionally.

This mimics real systems like

* ATM machines
* Login screens
* Menu driven applications

---

#### Step 2: Program Logic Explained

* Keep asking for the PIN
* If input is not 4 digits, skip and ask again
* If PIN matches, exit the loop
* Otherwise, continue asking

---

#### Program Example

```python
correct_pin = 4321

while True:
    pin = input("Enter your PIN: ")

    if len(pin) != 4:
        print("PIN must be 4 digits")
        continue

    if int(pin) == correct_pin:
        print("Access granted")
        break

    print("Wrong PIN. Try again")
```

---

#### How This Program Works Step by Step

1. The loop starts and runs continuously
2. User enters a PIN
3. If the PIN length is not 4

   * Continue skips the rest of the loop
4. If the PIN is correct

   * Break exits the loop completely
5. If the PIN is wrong

   * Loop repeats and asks again

This is **controlled looping**, not a mistake.

---

#### Why This Is Real World

This exact pattern is used in

* Banking systems
* Login authentication
* Device unlock screens
* Interactive command line tools

Once students understand this example, loops stop being scary.

---

### Mini Checkpoint



* Why is while True used here
* What would happen without break
* Why continue is used instead of else
* What happens after break executes

---

### Recap

* Infinite loops can be intentional and useful
* Break is used to exit when the goal is achieved
* Continue is used to skip invalid input
* Real applications rely heavily on this pattern
* Loops become safe when control is planned

---

### What’s Next

Next, we will convert this idea into **menu driven programs** using loops.
This will prepare you for writing real command line applications and tools.

---

