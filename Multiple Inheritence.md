# Arithmetic Operations Using Multiple Inheritance in Python

This Python program demonstrates **multiple inheritance** by performing basic arithmetic operations — Addition, Subtraction, and Division — using three classes.

## 🎯 Aim

To write a Python program to calculate **Add, Sub & Division** using **Multiple Inheritance**.

## 🧠 Algorithm

1. **Define `Calculation1` class**
   - Contains `Summation(a, b)` method to return the sum of two numbers.
2. **Define `Calculation2` class**
   - Contains `Subtraction(a, b)` method to return the difference of two numbers.
3. **Define `Derived` class**
   - Inherits from both `Calculation1` and `Calculation2`.
   - Contains `Division(a, b)` method to return the division result.
4. **Input**
   - Prompt the user to enter two numbers.
5. **Process**
   - Create an object of the `Derived` class.
   - Call `Summation`, `Subtraction`, and `Division` methods.
6. **Output**
   - Display the results of the three operations.

## 💻 Program 
```p
class Calculation1:
    def Summation(self, a, b):
        return a + b

class Calculation2:
    def Subtraction(self, a, b):
        return a - b

class Derived(Calculation1, Calculation2):
    def Division(self, a, b):
        if b == 0:
            return "Error! Division by zero."
        return a / b

try:
    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))

    calc = Derived()

    # Call methods from all three classes using the single 'calc' object
    print(f"\nResults:")
    print(f"Addition (from Calculation1): {calc.Summation(num1, num2)}")
    print(f"Subtraction (from Calculation2): {calc.Subtraction(num1, num2)}")
    print(f"Division (from Derived): {calc.Division(num1, num2)}")

except ValueError:
    print("Invalid input! Please enter numeric values.")
```
## Output Example
<img width="832" height="478" alt="image" src="https://github.com/user-attachments/assets/0278f1b1-ff52-4055-bd41-7c242238611a" />


## Result
The Python program was executed successfully, demonstrating multiple inheritance. The derived class accessed methods from both parent classes and performed addition, subtraction, and division correctly.

