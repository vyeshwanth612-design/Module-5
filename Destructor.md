# Destructor in Python

This project demonstrates how to implement a **destructor** in Python using a simple class.

## 🚀 Overview

The program defines a class `Demo` with:

- A **constructor** `__init__` that initializes an instance variable and prints a message.
- A **destructor** `__del__` that prints a message when the object is destroyed.

## 🧠 Algorithm

1. Define a class named `Demo`.
2. Inside the class, define the `__init__` method:
   - Initialize an instance variable `status` with the value `"Alive"`.
   - Print the value of `status`.
3. Define the `__del__` method:
   - Print a message indicating the object is being destroyed.
4. Outside the class:
   - Create an instance of the `Demo` class.
   - Delete the object using the `del` keyword.
## Program
```p
class Demo:
    def __init__(self):
        self.status = "Alive"
        print(f"Object Status: {self.status}")
        print("Constructor called: Object created.")

    def __del__(self):
        print("Destructor called: Object is being destroyed. Goodbye!")

print("--- Creating Object ---")
obj = Demo()

print("--- Deleting Object ---")
del obj

print("Program execution finished.")
```

## 🧪 Output
<img width="1907" height="538" alt="image" src="https://github.com/user-attachments/assets/592c10d0-b45d-4cf6-881a-7f0089646c1d" />


## Result

