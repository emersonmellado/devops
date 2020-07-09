OOP - Object Oriented Programming (Paradigm)

Try to mimic the real world into Classes (Objects) by using abstraction. 
The behaviour of a class is represented by attributes and actions are executed by methods.

- Classes (objects)
    - Polymorphism
    - Inheritance
- Members
    - Attributes (properties)
    - Methods
    - Messages
    - Local variables
    - Access Operators
    - Accessibility
    - Encapsulation
    - Interface
    
Syntax of a class:
class NAME:
    # attributes
    # methods
    # contructor
    
    Example:
        class Person:
            name = "John"
            age = 37
    
Write a few classes that could be used in a system for a school using basic OOP principles:
    
- First you understand the basic of the requirements
    -  You understand a bit of the domain that needs to be represented in classes.

  1         2         3 
Input -> Process -> Output

1. What are the inputs?
2. What are the processes required?
3. What is the expected output?

Person
    Students
    Instructors: wage
    Coordinator: wage
Programs
    Levels
        Lessons
            Exercises
Material
Administration 

class Person:
    name = "John"
    age = 37
    program = "DevOps course"
    role = "Student"
    
class Person:
    name = "Mary"
    age = 22
    program = "DevOps course"
    role = "Student"
    
class Person:
    name = "Jane"
    age = 34
    program = "DevOps course"
    role = "Coordinator"
    
class Person:
    name = "Bruce"
    age = 35
    program = "DevOps course"
    role = "Instructor"