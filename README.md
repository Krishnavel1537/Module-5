# # Constructors in Python: Welcome Message with Student Name

## 🎯 Aim
To write a Python program that creates a **Student** class with a **default constructor** and a method to display a welcome message along with the student’s name provided by the user.

## 🧠 Algorithm
1. **Get user input**: Accept the student's name from the user.
2. **Define the class**: Create a class `Student` with a default constructor (`__init__`).
3. **Default Constructor**: In the constructor, assign the user input (student name) to an instance variable `self.a`.
4. **Display Message**: Define a method `show` that prints "This is non-parameterized constructor" and a welcome message with the student’s name.
5. **Execute the Program**: Instantiate the `Student` class and call the `show` method.

## 🧾 Program
# Step 1: Get user input
name = input("Enter the student's name: ")

# Step 2 & 3: Define the class with a default (non-parameterized) constructor
class Student:
    def __init__(self):
        # Assign user input to an instance variable
        self.a = name

    # Step 4: Method to display message
    def show(self):
        print("This is non-parameterized constructor")
        print(f"Welcome, {self.a}!")

# Step 5: Instantiate the class and call the method
s = Student()
s.show()



## Output<img width="1920" height="1080" alt="Screenshot (24)" src="https://github.com/user-attachments/assets/9dceb3d4-bc5d-4386-a318-2f9fdc43e511" />


## Resultthus , To write a Python program that creates a **Student** class with a **default constructor** and a method to display a welcome message along with the student’s name provided by the user.


# Destructor in Python

# Step 1: Define the class
class Demo:
    # Step 2: Constructor
    def __init__(self):
        self.status = "Alive"
        print(self.status)
    
    # Step 3: Destructor
    def __del__(self):
        print("The object is being destroyed.")

# Step 4: Create and delete the object
d = Demo()   # Constructor is called, prints "Alive"
del d       # Destructor is called, prints "The object is being destroyed."

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
# Step 1: Define the class
class Demo:
    # Step 2: Constructor
    def __init__(self):
        self.status = "Alive"
        print(self.status)
    
    # Step 3: Destructor
    def __del__(self):
        print("The object is being destroyed.")

# Step 4: Create and delete the object
d = Demo()   # Constructor is called, prints "Alive"
del d       # Destructor is called, prints "The object is being destroyed."

## 🧪 Output<img width="1920" height="1080" alt="Screenshot (25)" src="https://github.com/user-attachments/assets/01a9021a-d4e2-4c55-8361-7973b84d6dc3" />


## Result  Thus , hence proved


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
# Step 1: Base class
class Details:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def display_basic(self):
        print(f"Name: {self.name}")
        print(f"Age: {self.age}")

# Step 2: Employee class extending Details
class Employee(Details):
    def __init__(self, name, age, emp_id, dept):
        super().__init__(name, age)  # Initialize base class attributes
        self.emp_id = emp_id
        self.dept = dept
    
    def display_employee(self):
        self.display_basic()
        print(f"Employee ID: {self.emp_id}")
        print(f"Department: {self.dept}")

# Step 3: Patient class extending Details
class Patient(Details):
    def __init__(self, name, age, patient_id, disease):
        super().__init__(name, age)
        self.patient_id = patient_id
        self.disease = disease
    
    def display_patient(self):
        self.display_basic()
        print(f"Patient ID: {self.patient_id}")
        print(f"Disease: {self.disease}")

# Step 4: Get user input
print("Enter Employee Details:")
emp_name = input("Name: ")
emp_age = input("Age: ")
emp_id = input("Employee ID: ")
emp_dept = input("Department: ")

print("\nEnter Patient Details:")
pat_name = input("Name: ")
pat_age = input("Age: ")
pat_id = input("Patient ID: ")
pat_disease = input("Disease: ")

# Step 5: Create objects and display information
employee = Employee(emp_name, emp_age, emp_id, emp_dept)
patient = Patient(pat_name, pat_age, pat_id, pat_disease)

print("\n--- Employee Information ---")
employee.display_employee()

print("\n--- Patient Information ---")
patient.display_patient()


## Sample Output <img width="1920" height="1080" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/0ef31ac7-768c-4b51-832d-8dd27cc0dd81" />



# Multilevel Inheritance Example in Python

This Python project demonstrates the concept of **Multilevel Inheritance** to collect and display the **name**, **age**, and **location** of a person.

## 🎯 Aim

To write a Python program that uses multilevel inheritance to get and display a person’s name, age, and location.

## 🧠 Algorithm

1. **Parent Class**  
   - `__init__(name)` initializes the `name` attribute.  
   - `getName()` returns the `name`.

2. **Child Class (inherits Parent)**  
   - `__init__(name, age)` initializes `name` using `super()` and adds `age`.  
   - `getAge()` returns the `age`.

3. **Grandchild Class (inherits Child)**  
   - `__init__(name, age, location)` initializes `name` and `age` using `super()` and adds `location`.  
   - `getLocation()` returns the `location`.

4. **Input & Output**  
   - Take user input for name, age, and location.  
   - Create an instance of `Grandchild`.  
   - Print all details using class methods.

## Program
# Step 1: Parent Class
class Parent:
    def __init__(self, name):
        self.name = name
    
    def getName(self):
        return self.name

# Step 2: Child Class
class Child(Parent):
    def __init__(self, name, age):
        super().__init__(name)  # Initialize name in Parent
        self.age = age
    
    def getAge(self):
        return self.age

# Step 3: Grandchild Class
class Grandchild(Child):
    def __init__(self, name, age, location):
        super().__init__(name, age)  # Initialize name and age in Child
        self.location = location
    
    def getLocation(self):
        return self.location

# Step 4: Input & Output
name = input("Enter Name: ")
age = input("Enter Age: ")
location = input("Enter Location: ")

# Create instance of Grandchild
grandchild = Grandchild(name, age, location)

# Print details
print("\n--- Details ---")
print("Name:", grandchild.getName())
print("Age:", grandchild.getAge())
print("Location:", grandchild.getLocation())


## Sample Output  <img width="1920" height="1080" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/c35f549b-7142-461e-9a75-3d50872575a8" />


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

## 💻 Program # Step 1: Calculation1 class
class Calculation1:
    def Summation(self, a, b):
        return a + b

# Step 2: Calculation2 class
class Calculation2:
    def Subtraction(self, a, b):
        return a - b

# Step 3: Derived class inheriting both
class Derived(Calculation1, Calculation2):
    def Division(self, a, b):
        if b != 0:
            return a / b
        else:
            return "Division by zero not allowed"

# Step 4: Input
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

# Step 5: Create object and call methods
obj = Derived()
sum_result = obj.Summation(num1, num2)
sub_result = obj.Subtraction(num1, num2)
div_result = obj.Division(num1, num2)

# Step 6: Output
print("\n--- Results ---")
print(f"Sum: {sum_result}")
print(f"Subtraction: {sub_result}")
print(f"Division: {div_result}")

Add code here
## Output Example   ![Uploading Screenshot (28).png…]()

