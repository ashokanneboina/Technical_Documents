# SOLID Principles in Object-Oriented Programming

SOLID is a set of five design principles that help developers build maintainable, scalable, and flexible software systems.

---

## S — Single Responsibility Principle (SRP)

**Definition:**  
A class should have only one reason to change.  
In other words, a class should have only one responsibility.

**Why?**
- Reduces complexity  
- Improves maintainability  
- Makes testing easier  

**Bad Example:**
```python
class Report:
    def generate(self):
        pass

    def save_to_file(self):
        pass
```
This class handles both report generation and file saving.

**Good Example:**
```python
class Report:
    def generate(self):
        pass

class ReportSaver:
    def save_to_file(self, report):
        pass
```

Now each class has one responsibility.

---

## O — Open/Closed Principle (OCP)

**Definition:**  
Software entities should be open for extension but closed for modification.

You should be able to add new functionality without modifying existing code.

**Bad Example:**
```python
class PaymentProcessor:
    def pay(self, method):
        if method == "credit":
            pass
        elif method == "paypal":
            pass
```

Every new method requires modifying the class.

**Good Example:**
```python
class Payment:
    def pay(self):
        pass

class CreditPayment(Payment):
    def pay(self):
        pass

class PayPalPayment(Payment):
    def pay(self):
        pass
```

Now new payment types can be added without changing existing code.

---

## L — Liskov Substitution Principle (LSP)

**Definition:**  
Subclasses must be replaceable with their base classes without altering correctness.

A child class should behave like its parent.

**Bad Example:**
```python
class Bird:
    def fly(self):
        pass

class Penguin(Bird):
    def fly(self):
        raise Exception("Penguins can't fly")
```

Penguin violates LSP because it cannot behave like a general Bird.

**Good Design:**
```python
class Bird:
    pass

class FlyingBird(Bird):
    def fly(self):
        pass

class Penguin(Bird):
    pass
```

---

## I — Interface Segregation Principle (ISP)

**Definition:**  
Clients should not be forced to depend on methods they do not use.

Prefer small, specific interfaces over large, general ones.

**Bad Example:**
```python
class Worker:
    def work(self):
        pass
    def eat(self):
        pass
```

A robot doesn’t need `eat()`.

**Good Example:**
```python
class Workable:
    def work(self):
        pass

class Eatable:
    def eat(self):
        pass
```

Classes implement only what they need.

---

## D — Dependency Inversion Principle (DIP)

**Definition:**  
High-level modules should not depend on low-level modules.  
Both should depend on abstractions.

**Bad Example:**
```python
class MySQLDatabase:
    def connect(self):
        pass

class App:
    def __init__(self):
        self.db = MySQLDatabase()
```

App depends directly on a concrete database.

**Good Example:**
```python
class Database:
    def connect(self):
        pass

class MySQLDatabase(Database):
    def connect(self):
        pass

class App:
    def __init__(self, db: Database):
        self.db = db
```

Now `App` depends on abstraction, not implementation.

---

# Summary Table

# SOLID Principles — Summary 

**SRP — Single Responsibility Principle**  
One class should have only one responsibility.  
A class should have only one reason to change.

**OCP — Open/Closed Principle**  
Software entities should be open for extension but closed for modification.  
You should add new functionality without changing existing code.

**LSP — Liskov Substitution Principle**  
Subclasses must be replaceable for their base classes without breaking the program.

**ISP — Interface Segregation Principle**  
Clients should not be forced to depend on methods they do not use.  
Prefer small, specific interfaces.

**DIP — Dependency Inversion Principle**  
High-level modules should depend on abstractions, not on concrete implementations.




