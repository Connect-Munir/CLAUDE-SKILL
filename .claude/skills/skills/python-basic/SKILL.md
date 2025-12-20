---
name: python-basic
description: Learn and teach Python fundamentals including syntax, data types, control flow, functions, and object-oriented programming. Use when creating learning materials, tutorials, or explanations for Python beginners. Includes best practices and code examples.
---

# Python Basics

## Summary

The **Python Basics** skill provides comprehensive guidance for learning and teaching Python fundamentals. It covers essential concepts from variables and data types to functions and object-oriented programming, with clear explanations, practical examples, and best practices for Python development.

## Key Terms

- **Syntax**: Python's rules for writing valid code (indentation-based)
- **Data Types**: Built-in types like int, str, list, dict, tuple, set
- **Indentation**: Python uses whitespace to define code blocks (4 spaces standard)
- **Functions**: Reusable code blocks defined with `def` keyword
- **Objects & Classes**: Blueprint for creating objects with attributes and methods
- **Modules & Packages**: Code organization and reusability units

## When to Use This Skill

Use this skill when you need to:
- Create Python learning materials or tutorials
- Explain Python fundamentals to beginners
- Demonstrate Python best practices and conventions
- Build educational content about Python syntax and concepts
- Provide code examples and explanations
- Generate study materials or documentation
- Compare Python with other programming languages

## Understanding Python

Python is a high-level, interpreted programming language known for:
- **Readability** - Clean, intuitive syntax that reads like English
- **Simplicity** - Easy to learn for beginners
- **Versatility** - Used for web development, data science, automation, AI, and more
- **Large ecosystem** - Extensive libraries and frameworks
- **Community** - Active, supportive community with abundant resources

## Core Concepts

### 1. Variables & Data Types

**Variables** are containers for storing values. Python is **dynamically typed** (type determined at runtime).

**Basic Data Types**:
```python
# Integers and Floats
age = 25              # int
height = 5.9          # float
pi = 3.14159

# Strings (text)
name = "Alice"
message = 'Hello World'
multiline = """This is a
multiline string"""

# Booleans
is_student = True
is_working = False

# None (absence of value)
result = None
```

### 2. Collections (Data Structures)

Python provides several ways to organize data:

**List** - Ordered, mutable (changeable), allows duplicates:
```python
fruits = ["apple", "banana", "cherry"]
numbers = [1, 2, 3, 4, 5]
mixed = [1, "hello", 3.14, True]

# Access elements (0-indexed)
print(fruits[0])    # "apple"
print(fruits[-1])   # "cherry" (last element)

# Modify
fruits.append("orange")
fruits[0] = "avocado"
```

**Tuple** - Ordered, immutable (unchangeable), allows duplicates:
```python
coordinates = (10, 20)
colors = ("red", "green", "blue")

# Access (same as list)
print(coordinates[0])  # 10

# Cannot modify
coordinates[0] = 15    # Error!
```

**Dictionary** - Unordered, mutable, key-value pairs:
```python
person = {
    "name": "Bob",
    "age": 30,
    "city": "New York"
}

# Access by key
print(person["name"])  # "Bob"

# Modify
person["age"] = 31
person["job"] = "Developer"  # Add new key
```

**Set** - Unordered, mutable, no duplicates:
```python
colors = {"red", "green", "blue"}
numbers = {1, 2, 3, 2, 1}  # {1, 2, 3} - duplicates removed

colors.add("yellow")
colors.remove("red")
```

### 3. Operators

**Arithmetic Operators**:
```python
a = 10
b = 3

a + b  # 13 (addition)
a - b  # 7 (subtraction)
a * b  # 30 (multiplication)
a / b  # 3.333... (division)
a // b # 3 (floor division)
a % b  # 1 (modulo - remainder)
a ** b # 1000 (exponentiation)
```

**Comparison Operators**:
```python
5 == 5      # True (equal)
5 != 3      # True (not equal)
5 > 3       # True (greater than)
5 < 3       # False (less than)
5 >= 5      # True (greater or equal)
5 <= 3      # False (less or equal)
```

**Logical Operators**:
```python
x = True
y = False

x and y     # False (both must be True)
x or y      # True (at least one must be True)
not x       # False (inverts boolean)
```

**Assignment Operators**:
```python
x = 5       # Assign
x += 3      # x = x + 3 (x is now 8)
x -= 2      # x = x - 2
x *= 2      # x = x * 2
x /= 4      # x = x / 4
```

### 4. Control Flow

**If-Elif-Else**:
```python
age = 20

if age < 13:
    print("Child")
elif age < 18:
    print("Teen")
elif age < 65:
    print("Adult")
else:
    print("Senior")
```

**Loops - While**:
```python
count = 0
while count < 5:
    print(count)
    count += 1

# Output: 0, 1, 2, 3, 4
```

**Loops - For**:
```python
# Loop through a list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

# Loop with range
for i in range(5):      # 0, 1, 2, 3, 4
    print(i)

# Loop with index
for index, fruit in enumerate(fruits):
    print(f"{index}: {fruit}")
```

**Loop Control**:
```python
for i in range(10):
    if i == 3:
        continue    # Skip this iteration
    if i == 7:
        break       # Exit loop
    print(i)
```

### 5. Functions

**Function Definition**:
```python
# Basic function
def greet(name):
    """This function greets someone."""
    return f"Hello, {name}!"

greet("Alice")  # "Hello, Alice!"

# Default parameters
def introduce(name, age=25):
    return f"{name} is {age} years old"

introduce("Bob")           # Bob is 25 years old
introduce("Charlie", 30)   # Charlie is 30 years old

# Multiple return values
def get_coordinates():
    return 10, 20

x, y = get_coordinates()   # x=10, y=20

# *args (variable number of arguments)
def sum_numbers(*args):
    return sum(args)

sum_numbers(1, 2, 3, 4)    # 10

# **kwargs (keyword arguments)
def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Alice", age=25, city="NYC")
```

### 6. String Operations

**String Methods**:
```python
text = "  Hello World  "

# Case conversion
text.upper()            # "  HELLO WORLD  "
text.lower()            # "  hello world  "
text.capitalize()       # "  hello world  " (first char upper)
text.title()            # "  Hello World  " (first char of each word)

# Trimming and replacing
text.strip()            # "Hello World" (remove whitespace)
text.replace("World", "Python")  # "  Hello Python  "

# Searching and checking
text.find("World")      # 8 (position of substring)
text.count("l")         # 3 (count occurrences)
text.startswith("Hello")# False (because of spaces)
text.endswith("World")  # False (because of spaces)

# Splitting and joining
words = "apple,banana,cherry".split(",")  # ["apple", "banana", "cherry"]
",".join(words)         # "apple,banana,cherry"

# String formatting
name = "Alice"
age = 25
f"My name is {name} and I'm {age}"  # f-strings (preferred)
"My name is {} and I'm {}".format(name, age)  # format method
"My name is %s and I'm %d" % (name, age)  # % operator (older)
```

### 7. List Comprehensions

Concise way to create lists:
```python
# Traditional approach
squares = []
for i in range(5):
    squares.append(i ** 2)
# [0, 1, 4, 9, 16]

# List comprehension (more Pythonic)
squares = [i ** 2 for i in range(5)]

# With condition
even_squares = [i ** 2 for i in range(10) if i % 2 == 0]
# [0, 4, 16, 36, 64]

# With transformation
words = ["hello", "world"]
upper_words = [word.upper() for word in words]
# ["HELLO", "WORLD"]
```

### 8. Exception Handling

Handle errors gracefully:
```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero!")
except ValueError:
    print("Invalid value")
except Exception as e:
    print(f"An error occurred: {e}")
else:
    print("No error occurred")
finally:
    print("This always executes")
```

### 9. Object-Oriented Programming (OOP)

**Classes and Objects**:
```python
class Dog:
    """A class representing a dog."""

    # Class variable (shared by all instances)
    species = "Canis familiaris"

    # Constructor
    def __init__(self, name, age):
        self.name = name      # Instance variable
        self.age = age

    # Instance method
    def bark(self):
        return f"{self.name} says Woof!"

    def get_age(self):
        return f"{self.name} is {self.age} years old"

    # Special method
    def __str__(self):
        return f"Dog(name={self.name}, age={self.age})"

# Create objects
dog1 = Dog("Buddy", 3)
dog2 = Dog("Max", 5)

print(dog1.bark())          # "Buddy says Woof!"
print(dog1.get_age())       # "Buddy is 3 years old"
print(str(dog1))            # "Dog(name=Buddy, age=3)"
```

**Inheritance**:
```python
class Animal:
    def __init__(self, name):
        self.name = name

    def make_sound(self):
        pass

class Cat(Animal):
    def make_sound(self):
        return f"{self.name} says Meow!"

class Dog(Animal):
    def make_sound(self):
        return f"{self.name} says Woof!"

cat = Cat("Whiskers")
dog = Dog("Rex")

print(cat.make_sound())     # "Whiskers says Meow!"
print(dog.make_sound())     # "Rex says Woof!"
```

### 10. Modules & Packages

Use built-in and external modules:
```python
# Import entire module
import math
print(math.pi)        # 3.14159...
print(math.sqrt(16))  # 4.0

# Import specific function
from math import sqrt, pi
print(sqrt(25))       # 5.0

# Import with alias
import numpy as np
import pandas as pd

# Create your own module
# my_utils.py
def add(a, b):
    return a + b

# Use in another file
from my_utils import add
add(5, 3)  # 8
```

## Best Practices

✓ **Use meaningful variable names** - `user_age` not `ua`
✓ **Follow PEP 8** - Python's style guide for consistent code
✓ **Use 4 spaces for indentation** - Never mix tabs and spaces
✓ **Write docstrings** - Describe what functions do
✓ **Use type hints** - Specify input and return types
✓ **Keep functions focused** - One responsibility per function
✓ **Use list comprehensions** - More Pythonic than loops
✓ **Handle exceptions properly** - Don't use bare except clauses
✓ **Use f-strings** - Modern string formatting (Python 3.6+)
✓ **Avoid global variables** - Use function parameters instead

## Common Pitfalls to Avoid

✗ **Mutable default arguments**:
```python
# Bad
def add_item(item, list=[]):
    list.append(item)
    return list

# Good
def add_item(item, list=None):
    if list is None:
        list = []
    list.append(item)
    return list
```

✗ **Comparing with `is` instead of `==`**:
```python
# Wrong
if x is 5:      # Uses identity, not equality
    pass

# Correct
if x == 5:      # Compares values
    pass
```

✗ **Not closing files**:
```python
# Bad
file = open("data.txt")
data = file.read()

# Good
with open("data.txt") as file:
    data = file.read()
    # File automatically closes
```

## Useful Built-in Functions

| Function | Description |
|----------|-------------|
| `print()` | Display output |
| `input()` | Get user input |
| `len()` | Get length |
| `range()` | Create sequence of numbers |
| `type()` | Get data type |
| `isinstance()` | Check if object is instance of class |
| `int()`, `str()`, `float()` | Type conversion |
| `sum()`, `min()`, `max()` | Aggregate functions |
| `sorted()`, `reversed()` | Sort/reverse sequences |
| `enumerate()` | Get index and value in loop |
| `zip()` | Combine multiple sequences |
| `map()`, `filter()` | Functional programming |

## Questions for You

- **What's your experience level** with programming before learning Python?
- **What do you want to build** with Python—web apps, data analysis, automation, AI?
- **How much time** can you dedicate to learning Python fundamentals?
- **Are you working with Python 2 or Python 3?** (Always use Python 3—it's the modern standard)
- **What's your main challenge** in learning Python—syntax, concepts, or applying them?
