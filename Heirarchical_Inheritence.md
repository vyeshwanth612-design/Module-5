# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
```p
class Details:
    def __init__(self):
        self.name = ""
        self.age = 0

    def getName(self):
        self.name = input("Enter Name: ")

    def getAge(self):
        self.age = int(input("Enter Age: "))

class Employee(Details):
    def __init__(self):
        super().__init__()
        self.employee_id = ""
        self.department = ""

    def getEmployeeDetails(self):
        self.getName()
        self.getAge()
        self.employee_id = input("Enter Employee ID: ")
        self.department = input("Enter Department: ")

    def displayEmployee(self):
        print(f"\n--- Employee Details ---")
        print(f"Name: {self.name}\nAge: {self.age}")
        print(f"ID: {self.employee_id}\nDept: {self.department}")

class Patient(Details):
    def __init__(self):
        super().__init__()
        self.patient_id = ""
        self.disease = ""

    def getPatientDetails(self):
        self.getName()
        self.getAge()
        self.patient_id = input("Enter Patient ID: ")
        self.disease = input("Enter Disease: ")

    def displayPatient(self):
        print(f"\n--- Patient Details ---")
        print(f"Name: {self.name}\nAge: {self.age}")
        print(f"ID: {self.patient_id}\nDisease: {self.disease}")

print("Registering Employee:")
emp = Employee()
emp.getEmployeeDetails()

print("\nRegistering Patient:")
pat = Patient()
pat.getPatientDetails()

emp.displayEmployee()
pat.displayPatient()
```
## Sample Output
<img width="817" height="395" alt="image" src="https://github.com/user-attachments/assets/2782074b-7586-48d9-b16d-e22542a6fd7d" />

## Result
The Python program was executed successfully, demonstrating hierarchical inheritance. The base class Details was inherited by both Employee and Patient classes, and the details were displayed correctly using their respective methods.


