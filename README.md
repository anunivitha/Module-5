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
```
class Student:
    def _init_(self,a):
        self.a=a
    def get(self):
        self.a=input()
    def info(self):
        print("This is non parametrized constructor")
        print("Hello",self.a)
obj=Student()
obj.get()
obj.info()
```
## Output
<img width="712" alt="Screenshot 2025-06-01 at 1 33 51 PM" src="https://github.com/user-attachments/assets/8af870a3-f42f-45cf-8793-a5a1be4fef5b" />


## Result
   Thus the program that creates a **Student** class with a **default constructor** and a method to display a welcome message along with the student’s name provided by the user has been executed successfully

# Destructor in Python

This project demonstrates how to implement a *destructor* in Python using a simple class.

## 🚀 Overview

The program defines a class Demo with:

- A *constructor* __init__ that initializes an instance variable and prints a message.
- A *destructor* __del__ that prints a message when the object is destroyed.

## 🧠 Algorithm

1. Define a class named Demo.
2. Inside the class, define the __init__ method:
   - Initialize an instance variable status with the value "Alive".
   - Print the value of status.
3. Define the __del__ method:
   - Print a message indicating the object is being destroyed.
4. Outside the class:
   - Create an instance of the Demo class.
   - Delete the object using the del keyword.
## Program
```
class Demo:
    def __init__(self):
        print("Hello World!")

    def __del__(self):
        print("Hello from the __del__ method.")

# Create and delete the object
obj = Demo()
del obj
```
## 🧪 Output
<img width="708" alt="Screenshot 2025-06-01 at 1 33 57 PM" src="https://github.com/user-attachments/assets/e78edfba-9d28-497b-ab53-fefe7aa10fed" />


## Result

Thus the program demonstrates how to implement a *destructor* in Python using a simple class has been executed successfully.
   
# Hierarchical Inheritance in Python

This Python project demonstrates *Hierarchical Inheritance* using a base class Details and two derived classes Employee and Patient. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses *Hierarchical Inheritance* to input and display *Employee* and *Patient* details.

## 📘 Description

- *Base Class:* Details
  - Stores common attributes: name, age
  - Provides methods: getName(), getAge()

- *Derived Class 1:* Employee
  - Inherits from Details
  - Adds: employee_id, department
  - Method: getEmployeeDetails()

- *Derived Class 2:* Patient
  - Inherits from Details
  - Adds: patient_id, disease
  - Method: getPatientDetails()

## 🧠 Algorithm

1. Create base class Details with common attributes.
2. Create Employee class extending Details, adding employee-specific data.
3. Create Patient class extending Details, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
# hierarchical inheritance
```
class Details:
    def __init__(self):
        self.__id="<No Id>"
        self.__name="<No Name>"
        self.__gender="<No Gender>"
    def setData(self,id,name,gender):
        self.__id=id
        self.__name=name
        self.__gender=gender
    def showData(self):
        print("Id: ",self.__id)
        print("Name: ", self.__name)
        print("Gender: ", self.__gender)

class Employee(Details): #Inheritance
    def __init__(self):
        self.__company="<No Company>"
        self.__dept="<No Dept>"
    def setEmployee(self,id,name,gender,comp,dept):
        self.setData(id,name,gender)
        self.__company=comp
        self.__dept=dept
    def showEmployee(self):
        self.showData()
        print("Hospital: ", self.__company)
        print("Department: ", self.__dept)

class Patient(Details): #Inheritance
    def __init__(self):
        self.__hospital="<No Hospital>"
        self.__dept="<No Dept>"
    def setEmployee(self,id,name,gender,hos,dept):
        self.setData(id,name,gender)
        self.__hospital=hos
        self.__dept=dept
    def showEmployee(self):
        self.showData()
        print("Hospital: ", self.__hospital)
        print("Department: ", self.__dept)

id=int(input())
name=input()
gender=input()
comp=input()
dept=input()
id1=int(input())
nam=input()
gen=input()
hosp=input()
dep=input()

print("Doctor Object")
e=Employee()
e.setEmployee(id,name,gender,comp,dept)
e.showEmployee()
print("\nPatient Object")
d = Patient()
d.setEmployee(id1, nam, gen, hosp, dep)
d.showEmployee()
```
## Sample Output
<img width="706" alt="Screenshot 2025-06-01 at 1 34 04 PM" src="https://github.com/user-attachments/assets/82eb2184-607f-47a3-9cc2-9742b6939184" />


## Result
    Thus the program that uses *Hierarchical Inheritance* to input and display *Employee* and *Patient* details hase been executed successfully

# Multilevel Inheritance Example in Python

This Python project demonstrates the concept of *Multilevel Inheritance* to collect and display the *name, **age, and **location* of a person.

## 🎯 Aim

To write a Python program that uses multilevel inheritance to get and display a person’s name, age, and location.

## 🧠 Algorithm

1. *Parent Class*  
   - __init__(name) initializes the name attribute.  
   - getName() returns the name.

2. *Child Class (inherits Parent)*  
   - __init__(name, age) initializes name using super() and adds age.  
   - getAge() returns the age.

3. *Grandchild Class (inherits Child)*  
   - __init__(name, age, location) initializes name and age using super() and adds location.  
   - getLocation() returns the location.

4. *Input & Output*  
   - Take user input for name, age, and location.  
   - Create an instance of Grandchild.  
   - Print all details using class methods.

## Program
```
class Parent:
   def __init__(self,name):
     self.name = name
   def getName(self):
     return self.name
class Child(Parent):
   def __init__(self,name,age):
     Parent.__init__(self,name)
     self.age = age
   def getAge(self):
     return self.age
class Grandchild(Child):
   def __init__(self,name,age,location):
     Child.__init__(self,name,age)
     self.location=location
   def getLocation(self):
     return self.location
name=input()
age=int(input())
loc=input()
gc = Grandchild(name,age,loc)
print(gc.getName(), gc.getAge(), gc.getLocation())
```

## Sample Output
<img width="707" alt="Screenshot 2025-06-01 at 1 34 11 PM" src="https://github.com/user-attachments/assets/7aee7357-967e-4c2f-b425-523239019830" />


## Result
     Thus the program that uses multilevel inheritance to get and display a person’s name, age, and location executed successfully.

# Arithmetic Operations Using Multiple Inheritance in Python

This Python program demonstrates *multiple inheritance* by performing basic arithmetic operations — Addition, Subtraction, and Division — using three classes.

## 🎯 Aim

To write a Python program to calculate *Add, Sub & Division* using *Multiple Inheritance*.

## 🧠 Algorithm

1. **Define Calculation1 class**
   - Contains Summation(a, b) method to return the sum of two numbers.
2. **Define Calculation2 class**
   - Contains Subtraction(a, b) method to return the difference of two numbers.
3. **Define Derived class**
   - Inherits from both Calculation1 and Calculation2.
   - Contains Division(a, b) method to return the division result.
4. *Input*
   - Prompt the user to enter two numbers.
5. *Process*
   - Create an object of the Derived class.
   - Call Summation, Subtraction, and Division methods.
6. *Output*
   - Display the results of the three operations.

## 💻 Program 
```
class Calculation1:  
    def Summation(self,a,b):  
        return a+b;  
class Calculation2:  
    def sub(self,a,b):  
        return a-b;  
class Derived(Calculation1,Calculation2):  
    def Mul(self,a,b):  
        return a*b;  
a=int(input())
b=int(input())
d = Derived()  
print(d.Summation(a,b))  
print(d.sub(a,b))  
print(d.Mul(a,b))
```
## Output Example
<img width="701" alt="Screenshot 2025-06-01 at 1 34 18 PM" src="https://github.com/user-attachments/assets/ffd171a4-e2a6-4721-b4d5-4e10fa57be97" />


## Result
     Thus the program demonstrates *multiple inheritance* by performing basic arithmetic operations — Addition, Subtraction, and Division — using three classes has been executed successfully.
