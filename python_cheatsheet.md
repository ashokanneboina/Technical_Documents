# Python Cheat Sheet 


---
# 1. Basic Syntax and Data Types

```python
x = 10
```
Assigns value 10 to variable x.

```python
a, b = 1, 2
```
Assigns multiple variables in one line.

```python
a, b = b, a
```
Swaps values without a temporary variable.

```python
print("Hello")
```
Displays output to the console.

```python
input("Enter: ")
```
Takes user input as a string.

```python
type(x)
```
Returns the datatype of x.

```python
isinstance(x, int)
```
Checks whether x is of type int.

---

## Python Data Types Map

Below is a simple visual map of Python built-in data types and their categories.

![Python Data Types Map](images/![alt text](https://intellipaat.com/blog/wp-content/uploads/2025/03/Screenshot-2025-03-27-122831.png)


---

# 2. Control Statements

Control statements allow your program to make decisions and execute different blocks of code depending on conditions.

---

```python
if condition:
```
Starts a conditional block.  
The code inside runs **only if the condition evaluates to True**.  
The condition must result in a Boolean value (`True` or `False`).

Example:
```python
if x > 10:
    print("Greater than 10")
```

---

```python
elif condition:
```
Stands for “else if”.  
Used to check **another condition** if the previous `if` (or `elif`) condition was False.  
You can use multiple `elif` blocks.

Example:
```python
elif x == 10:
    print("Exactly 10")
```

---

```python
else:
```
Final fallback block.  
Runs **only if all previous conditions are False**.  
It does not take a condition.

Example:
```python
else:
    print("Less than 10")
```

---

## Full Structure Example

```python
if x > 10:
    print("Greater")
elif x == 10:
    print(10)
```
----


# 3. Loops

Loops are used to repeat a block of code multiple times.  
In Python, the main loop types are:

- `for` loop  
- `while` loop  
- Nested loops (loop inside another loop)

---

# A. For Loop

Used when you want to iterate over a sequence (list, string, range, etc.).

```python
for i in range(5):
```
Runs 5 times, from 0 to 4.

Example:
```python
for i in range(5):
    print(i)
```

You can also loop directly over elements:

```python
for item in [10, 20, 30]:
```
Iterates over each element in the list.

Example:
```python
for item in [10, 20, 30]:
    print(item)
```

Use `range(start, stop, step)` for controlled iteration:

```python
for i in range(1, 10, 2):
```
Starts at 1, ends before 10, increments by 2.

---

# B. While Loop

Used when the number of iterations is not fixed.  
The loop runs as long as the condition remains True.

```python
while condition:
```

Example:
```python
x = 5
while x > 0:
    print(x)
    x -= 1
```

Important:
- The condition must eventually become False.
- Otherwise, it creates an infinite loop.

---

# C. Nested Loops

A loop inside another loop.

Example:
```python
for i in range(3):
    for j in range(2):
        print(i, j)
```

How it works:
- The outer loop runs first.
- For each outer loop iteration, the inner loop runs completely.

If outer runs 3 times and inner runs 2 times, total executions = 3 × 2 = 6.

---

# Quick Summary

- Use `for` when iterating over sequences.
- Use `while` when looping based on a condition.
- Use nested loops when working with grids, matrices, or combinations.


---

# 4. Strings (Immutable)

```python
s.lower()
```
Converts string to lowercase.

```python
s.upper()
```
Converts string to uppercase.

```python
s.title()
```
Capitalizes first letter of each word.

```python
s.capitalize()
```
Capitalizes only first character.

```python
s.swapcase()
```
Swaps uppercase to lowercase and vice versa.

```python
s.strip()
```
Removes whitespace from both ends.

```python
s.lstrip()
```
Removes whitespace from left side.

```python
s.rstrip()
```
Removes whitespace from right side.

```python
s.replace("old", "new")
```
Replaces substring with new value.

```python
s.find("a")
```
Returns index of first occurrence or -1.

```python
s.index("a")
```
Returns index but raises error if not found.

```python
s.count("a")
```
Counts occurrences of substring.

```python
s.split()
```
Splits string into list.

```python
"-".join(list)
```
Joins list elements into string.

```python
s.startswith("H")
```
Checks if string starts with substring.

```python
s.endswith("d")
```
Checks if string ends with substring.

```python
s.isalpha()
```
Returns True if only letters.

```python
s.isdigit()
```
Returns True if only digits.

```python
s.isalnum()
```
Returns True if alphanumeric.

```python
f"{name}"
```
Formats string using variables.

---

# 5. Lists (Mutable)

```python
lst.append(x)
```
Adds element at end.

```python
lst.extend([1,2])
```
Adds multiple elements.

```python
lst.insert(index, value)
```
Inserts value at specific index.

```python
lst.remove(value)
```
Removes first occurrence of value.

```python
lst.pop()
```
Removes and returns last element.

```python
lst.pop(index)
```
Removes element at index.

```python
lst.clear()
```
Removes all elements.

```python
lst.index(value)
```
Returns index of value.

```python
lst.count(value)
```
Counts occurrences.

```python
lst.sort()
```
Sorts list ascending.

```python
lst.sort(reverse=True)
```
Sorts descending.

```python
lst.reverse()
```
Reverses list order.

```python
lst.copy()
```
Creates shallow copy.

```python
lst[1:4]
```
Returns sliced portion.

```python
lst[::-1]
```
Returns reversed copy.

---

# 6. Tuples (Immutable)

```python
t.count(value)
```
Counts occurrences.

```python
t.index(value)
```
Returns index of value.

---

# 7. Sets (Unique Elements)

```python
s.add(value)
```
Adds element.

```python
s.update(iterable)
```
Adds multiple elements.

```python
s.remove(value)
```
Removes element (error if absent).

```python
s.discard(value)
```
Removes safely (no error).

```python
s.pop()
```
Removes random element.

```python
s.clear()
```
Empties set.

```python
a.union(b)
```
Returns combined elements.

```python
a.intersection(b)
```
Returns common elements.

```python
a.difference(b)
```
Returns elements in a not in b.

```python
a.symmetric_difference(b)
```
Returns non-common elements.

```python
a.issubset(b)
```
Checks if a is inside b.

```python
a.issuperset(b)
```
Checks if a contains b.

```python
a.isdisjoint(b)
```
Checks if no common elements.

---

# 8. Dictionaries (Key-Value)

```python
d["key"]
```
Accesses value by key.

```python
d.get("key")
```
Safely gets value.

```python
d.get("key", default)
```
Returns default if key missing.

```python
d["key"] = value
```
Adds or updates key.

```python
d.update(dict)
```
Updates multiple keys.

```python
d.setdefault(key, value)
```
Adds key if not exists.

```python
d.pop(key)
```
Removes key and returns value.

```python
d.popitem()
```
Removes last inserted pair.

```python
d.clear()
```
Removes all items.

```python
d.keys()
```
Returns all keys.

```python
d.values()
```
Returns all values.

```python
d.items()
```
Returns key-value pairs.

```python
dict.fromkeys(keys, value)
```
Creates dictionary with same value.

---

# 9. Functions

Functions are reusable blocks of code designed to perform a specific task.  
They improve modularity, readability, and reusability.

---

## A. Defining a Function

```python
def func():
```
Defines a function named `func`.  
The code inside the indented block belongs to the function.

Example:
```python
def greet():
    print("Hello")
```

The function will not run until it is called.

---

## B. Calling a Function

```python
greet()
```
Executes the function.

---

## C. Parameters and Arguments

Parameters are variables inside the function definition.  
Arguments are values passed when calling the function.

```python
def add(a, b):
```
Defines a function with two parameters.

```python
add(5, 3)
```
Passes 5 and 3 as arguments.

---

## D. Return Statement

```python
return value
```
Sends a result back to the caller and exits the function.

Example:
```python
def add(a, b):
    return a + b
```

Without `return`, the function returns `None`.

---

## E. Default Parameters

Allows parameters to have default values.

```python
def greet(name="Guest"):
```
If no argument is passed, `"Guest"` is used.

Example:
```python
greet()
greet("Ashok")
```

---

## F. Keyword Arguments

Allows passing arguments using parameter names.

```python
add(a=5, b=3)
```
Order does not matter when using keywords.

---

## G. Variable-Length Arguments

Used when the number of arguments is unknown.

### *args (Non-keyword arguments)

```python
def func(*args):
```
Collects multiple positional arguments into a tuple.

Example:
```python
def total(*nums):
    return sum(nums)
```

---

### **kwargs (Keyword arguments)

```python
def func(**kwargs):
```
Collects multiple keyword arguments into a dictionary.

Example:
```python
def print_data(**data):
    print(data)
```

---

## H. Lambda Functions

Small anonymous functions defined in one line.

```python
lambda x: x * x
```
Takes x and returns x squared.

Example:
```python
square = lambda x: x * x
```

Commonly used with:
- `map()`
- `filter()`
- `sorted()`

---

## I. Multiple Return Values

Functions can return multiple values as a tuple.

```python
def func():
    return 1, 2
```

Example:
```python
a, b = func()
```

---

## J. Recursive Functions

A function calling itself.

```python
def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n - 1)
```

Used for problems that can be broken into smaller similar subproblems.

---

## K. Scope of Variables

### Local Variable
Defined inside a function; accessible only inside it.

### Global Variable
Defined outside functions; accessible everywhere.

```python
x = 10

def func():
    global x
```

`global` allows modification of a global variable inside a function.

---

## L. Docstrings

Used to document a function.

```python
def add(a, b):
    """
    Returns the sum of two numbers.
    """
    return a + b
```

Access using:
```python
help(add)
```




---

# 10. Built-in Functions

```python
len(obj)
```
Returns length.

```python
sum(iterable)
```
Returns sum of elements.

```python
min(iterable)
```
Returns smallest value.

```python
max(iterable)
```
Returns largest value.

```python
sorted(iterable)
```
Returns sorted copy.

```python
range(n)
```
Generates sequence of numbers.

```python
zip(a,b)
```
Combines iterables.

```python
map(func, iterable)
```
Applies function to each element.

```python
filter(func, iterable)
```
Filters elements based on condition.

```python
all(iterable)
```
Returns True if all elements True.

```python
any(iterable)
```
Returns True if any element True.

---

# 11. Exception Handling

Exception handling allows your program to deal with runtime errors gracefully instead of crashing.  
It helps you control what happens when something unexpected occurs.

---

## A. try Block

```python
try:
```
Used to wrap code that might cause an error.  
If an exception occurs inside this block, Python immediately stops normal execution and looks for a matching `except` block.

Example:
```python
try:
    x = 10 / 0
```

---

## B. except Block

```python
except ErrorType:
```
Catches and handles a specific type of exception.  
If the raised error matches the specified type, this block executes.

Example:
```python
except ZeroDivisionError:
    print("Cannot divide by zero")
```

You can also capture the error object:

```python
except ZeroDivisionError as e:
    print(e)
```

---

## C. Multiple except Blocks

You can handle different errors separately.

```python
try:
    value = int(input("Enter number: "))
except ValueError:
    print("Invalid number")
except TypeError:
    print("Type error occurred")
```

---

## D. Generic except

```python
except Exception:
```
Catches all exceptions.  
Useful as a fallback, but should not replace specific exception handling.

Example:
```python
except Exception as e:
    print("Something went wrong:", e)
```

---

## E. else Block

```python
else:
```
Runs only if no exception occurs in the `try` block.

Example:
```python
try:
    x = 10 / 2
except ZeroDivisionError:
    print("Error")
else:
    print("Success")
```

---

## F. finally Block

```python
finally:
```
Always executes, whether an exception occurred or not.  
Commonly used for cleanup operations like closing files or releasing resources.

Example:
```python
finally:
    print("Execution finished")
```

---

## G. Raising Exceptions

```python
raise Exception("Error message")
```
Manually triggers an exception.  
Used when you want to enforce rules or validate inputs.

Example:
```python
def divide(a, b):
    if b == 0:
        raise ValueError("Denominator cannot be zero")
    return a / b
```

---

## H. Custom Exceptions

You can create your own exception classes.

```python
class CustomError(Exception):
    pass
```

Example:
```python
raise CustomError("Custom issue occurred")
```

---

## Common Built-in Exceptions

- `ZeroDivisionError` — Division by zero
- `ValueError` — Invalid value
- `TypeError` — Wrong data type
- `IndexError` — Invalid index
- `KeyError` — Missing dictionary key
- `FileNotFoundError` — File does not exist

---

## Full Structure Example

```python
try:
    x = int(input("Enter number: "))
    result = 10 / x
except ValueError:
    print("Invalid input")
except ZeroDivisionError:
    print("Cannot divide by zero")
else:
    print("Result:", result)
finally:
    print("Done")
```






---

# 12. OOP Basics (Object-Oriented Programming)

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

1. Encapsulation — Binding data and methods together.
2. Abstraction — Hiding implementation details.
3. Inheritance — Reusing code from parent classes.
4. Polymorphism — Same method behaving differently.

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



---

# 13. File Handling

File handling allows you to read from and write to files stored on your system.  
It is commonly used for storing data, logs, configuration files, and reports.

---

## A. Opening a File

```python
open("file.txt", "r")
```
Opens the file in **read mode**.  
The file must already exist. You can only read from it.

```python
open("file.txt", "w")
```
Opens the file in **write mode**.  
If the file exists, its content is erased. If it does not exist, Python creates it.

```python
open("file.txt", "a")
```
Opens the file in **append mode**.  
Adds new data to the end without deleting existing content.

```python
open("file.txt", "x")
```
Creates a new file.  
Raises an error if the file already exists.

---

## B. Reading from a File

```python
f.read()
```
Reads the entire file content as a single string.

```python
f.readline()
```
Reads one line at a time.

```python
f.readlines()
```
Reads all lines and returns them as a list.

Example:

```python
f = open("file.txt", "r")
content = f.read()
f.close()
```

---

## C. Writing to a File

```python
f.write(data)
```
Writes a string to the file. Returns the number of characters written.

```python
f.writelines(list_of_strings)
```
Writes multiple strings to the file.

Example:

```python
f = open("file.txt", "w")
f.write("Hello")
f.close()
```

---

## D. Closing a File

```python
f.close()
```
Closes the file and releases system resources.  
Always close files after use to avoid memory leaks.

---

## E. Using with Statement 

```python
with open("file.txt", "r") as f:
    content = f.read()
```

The `with` statement:
- Automatically closes the file after execution.
- Is safer and cleaner.
- Is the recommended approach.

---

## F. File Modes Summary

- `"r"` → Read
- `"w"` → Write (overwrites)
- `"a"` → Append
- `"x"` → Create new file
- `"b"` → Binary mode (e.g., `"rb"`, `"wb"`)
- `"t"` → Text mode (default)

---

## G. Example: Read and Write

```python
with open("input.txt", "r") as f:
    data = f.read()

with open("output.txt", "w") as f:
    f.write(data)
```

---
# 14. Iterators and Generators

Iterators and generators are used to handle data one item at a time instead of loading everything into memory.  
They are especially useful for large datasets and efficient looping.

---

## A. Iterators

An **iterator** is an object that allows sequential access to elements.

It follows the iterator protocol:
- `__iter__()` → returns the iterator object
- `__next__()` → returns the next item

### Creating an Iterator

```python
lst = [1, 2, 3]
it = iter(lst)
```
`iter()` converts an iterable (like list) into an iterator.

```python
next(it)
```
Returns the next element.  
Raises `StopIteration` when elements are finished.

Example:

```python
it = iter([1, 2, 3])
print(next(it))  # 1
print(next(it))  # 2
```

### Custom Iterator

```python
class Counter:
    def __init__(self, max):
        self.max = max
        self.current = 0

    def __iter__(self):
        return self

    def __next__(self):
        if self.current < self.max:
            self.current += 1
            return self.current
        else:
            raise StopIteration
```

---

## B. Generators

A **generator** is a simpler way to create iterators using `yield`.

Instead of returning all values at once, it produces values one at a time.

### Generator Function

```python
def gen():
    yield 1
    yield 2
    yield 3
```

Calling it:

```python
g = gen()
next(g)
```

`yield` pauses the function and remembers its state.

---

### Generator Expression

Similar to list comprehension but memory efficient.

```python
g = (x*x for x in range(5))
```

Unlike list comprehension, it does not store all values in memory.

---

## Key Differences

- Iterator → Created using `iter()` and `next()`
- Generator → Created using `yield`
- Generators are easier to write
- Generators are memory efficient
- Both produce values lazily (one at a time)

---

## When to Use

Use iterators and generators when:
- Working with large files
- Processing streams of data
- Handling infinite sequences
- Optimizing memory usage

They are important for writing efficient and scalable Python programs.

---- 

# Decorators

A **decorator** is a function that modifies the behavior of another function without changing its original code.

In simple terms:
- A decorator takes a function as input.
- It wraps that function inside another function.
- It returns the modified version of that function.

---

## Basic Structure

A decorator has three main parts:

1. A function that accepts another function.
2. A wrapper function inside it.
3. Returning the wrapper.

---

## Example

```python
def my_decorator(func):
    def wrapper():
        print("Before function runs")
        func()
        print("After function runs")
    return wrapper


@my_decorator
def greet():
    print("Hello")

greet()
```

---

## What Happens Here

- `my_decorator` receives `greet` as an argument.
- It defines a new function called `wrapper`.
- The `wrapper` adds extra behavior before and after calling `greet`.
- The decorator returns the `wrapper` function.
- The `@my_decorator` line replaces `greet` with the wrapped version.

This line:

```python
@my_decorator
```

Is equivalent to:

```python
greet = my_decorator(greet)
```

So when `greet()` is called, it actually runs the `wrapper` function.
