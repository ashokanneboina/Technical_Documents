# 1. OOP Basics (Object-Oriented Programming)

Object-Oriented Programming organizes code using **classes and objects**.  
It helps structure large programs, improve reusability, and model real-world entities.

---

## A. Defining a Class

```python
class MyClass:
```
Defines a class named `MyClass`.  
A class is a blueprint for creating objects.

Example:
```python
class Person:
    pass
```

---

## B. Creating an Object (Instance)

```python
obj = MyClass()
```
Creates an object (instance) of the class.

Example:
```python
p = Person()
```

Each object has its own data.

---

## C. Constructor Method

```python
__init__(self)
```
The constructor method.  
Automatically runs when an object is created.  
Used to initialize attributes.

Example:
```python
class Person:
    def __init__(self, name):
        self.name = name
```

- `self` refers to the current object.
- Attributes are stored using `self.attribute_name`.

---

## D. Instance Methods

Methods are functions defined inside a class.

```python
def method(self):
```
Defines a method that operates on object data.

Example:
```python
class Person:
    def greet(self):
        print("Hello")
```

Called using:
```python
p.greet()
```

---

## E. __str()__ Method

```
__str__(self)
```
Defines the readable string representation of an object.  
Called when using `print(object)`.

Example:
```python
class Person:
    def __str__(self):
        return "Person object"
```

---

## F. __repr()__ Method

```python
__repr__(self)
```
Defines official string representation (mainly for debugging).  
Used in interactive console.

---

## G. Inheritance

Allows one class to inherit properties and methods from another.

```python
class Child(Parent):
```
Creates a subclass that inherits from `Parent`.

Example:
```python
class Student(Person):
    pass
```

---

## H. super()

```python
super()
```
Calls methods from the parent class.

Example:
```python
class Student(Person):
    def __init__(self, name, roll):
        super().__init__(name)
        self.roll = roll
```

Used to reuse parent constructor or methods.

---

## I. Encapsulation

Encapsulation restricts direct access to certain attributes.

```python
self._protected
self.__private
```

- `_variable` → protected (convention).
- `__variable` → private (name mangling).

---

## J. Class Variables

Variables shared across all objects.

```python
class MyClass:
    class_variable = 10
```

Accessed using:
```python
MyClass.class_variable
```

---

## K. Static Method

```python
@staticmethod
```
Method that does not depend on object or class.

Example:
```python
class Math:
    @staticmethod
    def add(a, b):
        return a + b
```

---

## L. Class Method

```python
@classmethod
```
Method that works with the class itself.

Example:
```python
class MyClass:
    @classmethod
    def create(cls):
        return cls()
```

---

## Core OOP Principles

# Four Pillars of Object-Oriented Programming (OOP)

## 1. Encapsulation
**Definition:**  
Encapsulation is the process of binding data (variables) and methods (functions) together inside a class and restricting direct access to some components.

**Purpose:**
- Protect data from unauthorized access
- Prevent accidental modification
- Improve maintainability

**Access Levels in Python:**
- Public → `self.name`
- Protected (convention) → `self._name`
- Private (name mangling) → `self.__name`

**Example:**
```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance
```

---

## 2. Abstraction
**Definition:**  
Abstraction hides internal implementation details and exposes only essential functionality.

**Purpose:**
- Reduce complexity
- Improve readability
- Separate interface from implementation

**Example using Abstract Base Class:**
```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass
```

---

## 3. Inheritance
**Definition:**  
Inheritance allows one class (child) to reuse properties and methods of another class (parent).

**Purpose:**
- Code reuse
- Logical hierarchy
- Reduced redundancy

**Example:**
```python
class Animal:
    def speak(self):
        return "Animal sound"

class Dog(Animal):
    def speak(self):
        return "Bark"
```

---

## 4. Polymorphism
**Definition:**  
Polymorphism allows the same method name to behave differently for different objects.

**Purpose:**
- Flexibility
- Interchangeable components
- Dynamic behavior

**Example:**
```python
class Dog:
    def sound(self):
        return "Bark"

class Cat:
    def sound(self):
        return "Meow"

def make_sound(animal):
    print(animal.sound())

make_sound(Dog())
make_sound(Cat())
```


---

## Simple Complete Example

```python
class Person:
    def __init__(self, name):
        self.name = name

    def greet(self):
        return f"Hello {self.name}"

class Student(Person):
    def __init__(self, name, roll):
        super().__init__(name)
        self.roll = roll
```
