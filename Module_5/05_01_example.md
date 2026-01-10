

## Real Program Example: ATM Cash Withdrawal Attempts

### Problem Statement

Imagine an ATM machine.

Rules:

* A user has **3 attempts** to enter the correct PIN
* If the PIN is correct → access is granted
* If the PIN is wrong → try again
* After 3 wrong attempts → card is blocked

<img width="4800" height="2700" alt="image" src="https://github.com/user-attachments/assets/4cda0bbd-9e82-4abf-8f42-6e44c7e1259a" />


---

## Why a Loop Is Needed Here

We do **not know in advance**:

* On which attempt the user will enter the correct PIN

But we **do know**:

* Maximum attempts allowed = 3

So we repeat the same steps:

1. Ask for PIN
2. Check if correct
3. Stop if correct or attempts exhausted

This is exactly where a **while loop** fits.

---

## Step-by-Step Thinking (Before Code)

Let us think like a human first.

* Start with attempts = 3
* While attempts are greater than 0:

  * Ask user to enter PIN
  * If PIN is correct → success, stop
  * Else → reduce attempts by 1
* If attempts become 0 → block card

This thinking becomes code.

---

## Python Program Using While Loop

```python
correct_pin = 4321
attempts = 3

while attempts > 0:
    entered_pin = int(input("Enter your ATM PIN: "))

    if entered_pin == correct_pin:
        print("Access granted. Welcome!")
        break
    else:
        attempts = attempts - 1
        print("Wrong PIN. Attempts left:", attempts)

if attempts == 0:
    print("Card blocked. Too many wrong attempts.")
```

---

## How the Loop Actually Executes

Let us **trace it like the computer**.

### Initial State

* attempts = 3

---

### First Attempt

* Condition checked → attempts > 0 → True
* User enters PIN
* If correct → loop stops
* If wrong → attempts becomes 2

---

### Second Attempt

* Condition checked → attempts > 0 → True
* User enters PIN
* If wrong → attempts becomes 1

---

### Third Attempt

* Condition checked → attempts > 0 → True
* User enters PIN
* If wrong → attempts becomes 0

---

### Loop Stops

* Condition checked → attempts > 0 → False
* Loop exits
* Program prints card blocked message

---

## Why This Is a Perfect Loop Example

This program shows:

* **Real-world repetition**
* **Condition-controlled execution**
* **Counter usage**
* **Loop termination**
* **Decision making inside loop**

Exactly what loops are meant for.

---

## Key Learning from This Example

* The **while condition controls repetition**
* The **counter controls how long it runs**
* The loop stops automatically when condition becomes false
* The program flow changes based on user input

---

## Mental Model to Remember

Think of a loop like this:

> "Keep doing this **while** something is true"

ATM example:

> "Keep asking for PIN **while** attempts are left"

---

## Mini Practice for Student

Ask students to modify this program:

* Change attempts to 5
* Add a message when only 1 attempt is left
* Remove break and see what happens

---


