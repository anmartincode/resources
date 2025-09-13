# Programming Fundamentals Terminology Journal

A comprehensive guide to fundamental programming concepts with code snippets and examples.

## Table of Contents

1. [Data Types & Variables](#data-types--variables)
2. [Control Structures](#control-structures)
3. [Functions & Methods](#functions--methods)
4. [Object-Oriented Programming](#object-oriented-programming)
5. [Data Structures](#data-structures)
6. [Algorithms & Complexity](#algorithms--complexity)
7. [Error Handling & Debugging](#error-handling--debugging)
8. [Best Practices](#best-practices)

---

## Data Types & Variables

### Variable
A named storage location that holds a value that can be changed during program execution.

```python
# Python
name = "Alice"
age = 25
is_student = True

# JavaScript
let name = "Alice";
let age = 25;
let isStudent = true;

# Java
String name = "Alice";
int age = 25;
boolean isStudent = true;
```

### Data Types

#### Primitive Types
Basic data types built into the language.

```python
# Python (dynamically typed)
integer_num = 42
float_num = 3.14
boolean_val = True
string_val = "Hello World"
none_val = None

# JavaScript
let integerNum = 42;
let floatNum = 3.14;
let booleanVal = true;
let stringVal = "Hello World";
let nullVal = null;
let undefinedVal = undefined;

# Java (statically typed)
int integerNum = 42;
double floatNum = 3.14;
boolean booleanVal = true;
String stringVal = "Hello World";
```

#### Composite Types
Data types that can hold multiple values.

```python
# Python
# List (mutable, ordered)
fruits = ["apple", "banana", "orange"]
fruits.append("grape")

# Tuple (immutable, ordered)
coordinates = (10, 20)

# Dictionary (key-value pairs)
person = {"name": "Alice", "age": 25}

# Set (unique values)
unique_numbers = {1, 2, 3, 4, 5}
```

```javascript
// JavaScript
// Array
let fruits = ["apple", "banana", "orange"];
fruits.push("grape");

// Object
let person = {name: "Alice", age: 25};

// Set
let uniqueNumbers = new Set([1, 2, 3, 4, 5]);
```

### Constants
Variables whose values cannot be changed after initialization.

```python
# Python (convention: UPPER_CASE)
PI = 3.14159
MAX_CONNECTIONS = 100

# JavaScript
const PI = 3.14159;
const MAX_CONNECTIONS = 100;

# Java
final double PI = 3.14159;
final int MAX_CONNECTIONS = 100;
```

---

## Control Structures

### Conditional Statements
Control the flow of execution based on conditions.

#### If-Else Statements

```python
# Python
age = 18

if age >= 18:
    print("Adult")
elif age >= 13:
    print("Teenager")
else:
    print("Child")
```

```javascript
// JavaScript
let age = 18;

if (age >= 18) {
    console.log("Adult");
} else if (age >= 13) {
    console.log("Teenager");
} else {
    console.log("Child");
}
```

#### Switch Statements

```javascript
// JavaScript
let day = "Monday";

switch (day) {
    case "Monday":
        console.log("Start of work week");
        break;
    case "Friday":
        console.log("TGIF!");
        break;
    default:
        console.log("Regular day");
}
```

```java
// Java
String day = "Monday";

switch (day) {
    case "Monday":
        System.out.println("Start of work week");
        break;
    case "Friday":
        System.out.println("TGIF!");
        break;
    default:
        System.out.println("Regular day");
}
```

### Loops
Repeat code execution based on conditions.

#### For Loops

```python
# Python
# Range-based loop
for i in range(5):
    print(i)  # 0, 1, 2, 3, 4

# Iterate over collection
fruits = ["apple", "banana", "orange"]
for fruit in fruits:
    print(fruit)
```

```javascript
// JavaScript
// Traditional for loop
for (let i = 0; i < 5; i++) {
    console.log(i);  // 0, 1, 2, 3, 4
}

// For-of loop
let fruits = ["apple", "banana", "orange"];
for (let fruit of fruits) {
    console.log(fruit);
}
```

#### While Loops

```python
# Python
count = 0
while count < 5:
    print(count)
    count += 1
```

```javascript
// JavaScript
let count = 0;
while (count < 5) {
    console.log(count);
    count++;
}
```

#### Do-While Loops

```javascript
// JavaScript
let count = 0;
do {
    console.log(count);
    count++;
} while (count < 5);
```

---

## Functions & Methods

### Function
A reusable block of code that performs a specific task.

```python
# Python
def greet(name, age=25):
    """Function to greet a person with their name and age."""
    return f"Hello {name}, you are {age} years old!"

# Function call
message = greet("Alice")
print(message)  # Hello Alice, you are 25 years old!
```

```javascript
// JavaScript
function greet(name, age = 25) {
    return `Hello ${name}, you are ${age} years old!`;
}

// Arrow function
const greetArrow = (name, age = 25) => {
    return `Hello ${name}, you are ${age} years old!`;
};

// Function call
let message = greet("Alice");
console.log(message);
```

```java
// Java
public static String greet(String name, int age) {
    return "Hello " + name + ", you are " + age + " years old!";
}

// Method call
String message = greet("Alice", 25);
System.out.println(message);
```

### Method
A function that belongs to a class or object.

```python
# Python
class Calculator:
    def add(self, a, b):
        return a + b
    
    def multiply(self, a, b):
        return a * b

calc = Calculator()
result = calc.add(5, 3)  # 8
```

```javascript
// JavaScript
class Calculator {
    add(a, b) {
        return a + b;
    }
    
    multiply(a, b) {
        return a * b;
    }
}

let calc = new Calculator();
let result = calc.add(5, 3);  // 8
```

### Parameters vs Arguments
- **Parameter**: Variable in the function definition
- **Argument**: Actual value passed to the function

```python
# Python
def calculate_area(length, width):  # length, width are parameters
    return length * width

area = calculate_area(10, 5)  # 10, 5 are arguments
```

### Return Statement
Specifies the value that a function should return.

```python
# Python
def get_max(a, b):
    if a > b:
        return a
    else:
        return b

max_value = get_max(10, 20)  # Returns 20
```

---

## Object-Oriented Programming

### Class
A blueprint for creating objects that defines properties and methods.

```python
# Python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def introduce(self):
        return f"Hi, I'm {self.name} and I'm {self.age} years old."

# Create an instance
person = Person("Alice", 25)
print(person.introduce())
```

```javascript
// JavaScript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
    
    introduce() {
        return `Hi, I'm ${this.name} and I'm ${this.age} years old.`;
    }
}

// Create an instance
let person = new Person("Alice", 25);
console.log(person.introduce());
```

### Object
An instance of a class that contains data (attributes) and behavior (methods).

```python
# Python
class Car:
    def __init__(self, brand, model, year):
        self.brand = brand
        self.model = model
        self.year = year
        self.speed = 0
    
    def accelerate(self, increment):
        self.speed += increment
    
    def brake(self, decrement):
        self.speed = max(0, self.speed - decrement)

my_car = Car("Toyota", "Camry", 2023)
my_car.accelerate(20)
print(f"Speed: {my_car.speed}")  # Speed: 20
```

### Inheritance
A mechanism where a class inherits properties and methods from another class.

```python
# Python
class Animal:
    def __init__(self, name):
        self.name = name
    
    def speak(self):
        return "Some generic animal sound"

class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"

class Cat(Animal):
    def speak(self):
        return f"{self.name} says Meow!"

dog = Dog("Buddy")
cat = Cat("Whiskers")
print(dog.speak())  # Buddy says Woof!
print(cat.speak())  # Whiskers says Meow!
```

---

## Data Structures

### Array/List
An ordered collection of elements that can be accessed by index.

```python
# Python - List
numbers = [1, 2, 3, 4, 5]
numbers.append(6)        # Add to end
numbers.insert(0, 0)     # Insert at index
numbers.remove(3)        # Remove first occurrence
print(numbers[2])        # Access by index: 3
```

```javascript
// JavaScript - Array
let numbers = [1, 2, 3, 4, 5];
numbers.push(6);         // Add to end
numbers.unshift(0);      // Add to beginning
numbers.splice(2, 1);    // Remove at index 2
console.log(numbers[2]); // Access by index
```

### Stack
A Last-In-First-Out (LIFO) data structure.

```python
# Python - Using list as stack
stack = []
stack.append(1)  # Push
stack.append(2)  # Push
stack.append(3)  # Push
top = stack.pop()  # Pop: returns 3
print(stack)  # [1, 2]
```

```javascript
// JavaScript - Using array as stack
let stack = [];
stack.push(1);  // Push
stack.push(2);  // Push
stack.push(3);  // Push
let top = stack.pop();  // Pop: returns 3
console.log(stack);  // [1, 2]
```

### Queue
A First-In-First-Out (FIFO) data structure.

```python
# Python - Using collections.deque
from collections import deque

queue = deque()
queue.append(1)  # Enqueue
queue.append(2)  # Enqueue
queue.append(3)  # Enqueue
front = queue.popleft()  # Dequeue: returns 1
print(queue)  # deque([2, 3])
```

### Hash Table/Dictionary
A data structure that maps keys to values for fast lookup.

```python
# Python - Dictionary
scores = {"Alice": 95, "Bob": 87, "Charlie": 92}
scores["David"] = 88     # Add/Update
del scores["Bob"]        # Delete
print(scores["Alice"])   # Lookup: 95
```

```javascript
// JavaScript - Object/Map
let scores = {"Alice": 95, "Bob": 87, "Charlie": 92};
scores["David"] = 88;    // Add/Update
delete scores["Bob"];    // Delete
console.log(scores["Alice"]);  // Lookup: 95

// Using Map
let scoreMap = new Map();
scoreMap.set("Alice", 95);
scoreMap.set("Bob", 87);
console.log(scoreMap.get("Alice"));  // 95
```

---

## Algorithms & Complexity

### Algorithm
A step-by-step procedure for solving a problem.

```python
# Python - Linear Search Algorithm
def linear_search(arr, target):
    """Search for target in array, return index or -1 if not found."""
    for i, value in enumerate(arr):
        if value == target:
            return i
    return -1

numbers = [1, 3, 5, 7, 9, 11]
index = linear_search(numbers, 7)
print(f"Found at index: {index}")  # Found at index: 3
```

### Time Complexity
Describes how the runtime of an algorithm grows with input size.

```python
# Python - Examples of different time complexities

# O(1) - Constant time
def get_first_element(arr):
    return arr[0] if arr else None

# O(n) - Linear time
def find_max(arr):
    if not arr:
        return None
    max_val = arr[0]
    for num in arr[1:]:
        if num > max_val:
            max_val = num
    return max_val

# O(n²) - Quadratic time
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
    return arr

# O(log n) - Logarithmic time (Binary Search)
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    
    while left <= right:
        mid = (left + right) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1
```

### Space Complexity
Describes how much memory an algorithm uses relative to input size.

```python
# Python - Space complexity examples

# O(1) - Constant space
def swap_variables(a, b):
    a, b = b, a
    return a, b

# O(n) - Linear space
def create_copy(arr):
    return arr.copy()

# O(n²) - Quadratic space
def create_matrix(n):
    return [[0 for _ in range(n)] for _ in range(n)]
```

### Sorting Algorithms

#### Bubble Sort
```python
# Python - Bubble Sort (O(n²))
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        swapped = False
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
                swapped = True
        if not swapped:
            break
    return arr
```

#### Quick Sort
```python
# Python - Quick Sort (O(n log n) average)
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    
    return quick_sort(left) + middle + quick_sort(right)
```

---

## Error Handling & Debugging

### Exception
An event that occurs during program execution that disrupts normal flow.

```python
# Python - Exception handling
def divide_numbers(a, b):
    try:
        result = a / b
        return result
    except ZeroDivisionError:
        print("Error: Cannot divide by zero!")
        return None
    except TypeError:
        print("Error: Invalid input types!")
        return None
    finally:
        print("Division operation completed")

result = divide_numbers(10, 0)  # Error: Cannot divide by zero!
```

```javascript
// JavaScript - Exception handling
function divideNumbers(a, b) {
    try {
        if (typeof a !== 'number' || typeof b !== 'number') {
            throw new TypeError('Both arguments must be numbers');
        }
        if (b === 0) {
            throw new Error('Cannot divide by zero');
        }
        return a / b;
    } catch (error) {
        console.log('Error:', error.message);
        return null;
    } finally {
        console.log('Division operation completed');
    }
}

let result = divideNumbers(10, 0);  // Error: Cannot divide by zero
```

### Debugging
The process of finding and fixing errors in code.

```python
# Python - Debugging techniques

# 1. Print statements
def calculate_factorial(n):
    print(f"Calculating factorial of {n}")
    if n <= 1:
        print("Base case reached")
        return 1
    result = n * calculate_factorial(n - 1)
    print(f"Factorial of {n} is {result}")
    return result

# 2. Assert statements
def divide(a, b):
    assert b != 0, "Divisor cannot be zero"
    return a / b

# 3. Using debugger (pdb)
import pdb

def complex_function(data):
    pdb.set_trace()  # Breakpoint
    processed = []
    for item in data:
        if item > 0:
            processed.append(item * 2)
    return processed
```

### Logging
Recording information about program execution for debugging and monitoring.

```python
# Python - Logging
import logging

# Configure logging
logging.basicConfig(
    level=logging.INFO,
    format='%(asctime)s - %(levelname)s - %(message)s'
)

def process_data(data):
    logging.info(f"Processing {len(data)} items")
    
    try:
        result = []
        for item in data:
            if item < 0:
                logging.warning(f"Negative value found: {item}")
            result.append(item * 2)
        
        logging.info("Data processing completed successfully")
        return result
    except Exception as e:
        logging.error(f"Error processing data: {e}")
        raise

# Usage
data = [1, -2, 3, 4, -5]
processed = process_data(data)
```

---

## Best Practices

### Code Organization

#### Naming Conventions
```python
# Python - PEP 8 naming conventions
# Variables and functions: snake_case
user_name = "Alice"
def calculate_total_price():
    pass

# Constants: UPPER_CASE
MAX_CONNECTIONS = 100
API_BASE_URL = "https://api.example.com"

# Classes: PascalCase
class UserManager:
    pass

# Private attributes: leading underscore
class BankAccount:
    def __init__(self):
        self._balance = 0  # Protected
        self.__account_id = "123"  # Private
```

```javascript
// JavaScript - Common naming conventions
// Variables and functions: camelCase
let userName = "Alice";
function calculateTotalPrice() {
    // ...
}

// Constants: UPPER_CASE
const MAX_CONNECTIONS = 100;
const API_BASE_URL = "https://api.example.com";

// Classes: PascalCase
class UserManager {
    // ...
}
```

#### Comments and Documentation
```python
# Python - Docstrings and comments
def calculate_compound_interest(principal, rate, time, compound_frequency=12):
    """
    Calculate compound interest.
    
    Args:
        principal (float): Initial amount of money
        rate (float): Annual interest rate (as decimal)
        time (float): Time in years
        compound_frequency (int): Number of times interest is compounded per year
    
    Returns:
        float: Final amount after compound interest
    
    Example:
        >>> calculate_compound_interest(1000, 0.05, 2)
        1104.713067441311
    """
    # Formula: A = P(1 + r/n)^(nt)
    amount = principal * (1 + rate / compound_frequency) ** (compound_frequency * time)
    return amount
```

### Code Quality

#### DRY Principle (Don't Repeat Yourself)
```python
# Bad - Repetitive code
def calculate_area_rectangle(length, width):
    return length * width

def calculate_area_square(side):
    return side * side

# Good - DRY principle
def calculate_area(length, width=None):
    if width is None:
        width = length  # Square
    return length * width

# Usage
rectangle_area = calculate_area(5, 3)  # 15
square_area = calculate_area(4)        # 16
```

#### Single Responsibility Principle
```python
# Bad - Multiple responsibilities
class User:
    def __init__(self, name, email):
        self.name = name
        self.email = email
    
    def save_to_database(self):
        # Database logic
        pass
    
    def send_email(self, message):
        # Email logic
        pass
    
    def validate_email(self):
        # Validation logic
        pass

# Good - Single responsibility
class User:
    def __init__(self, name, email):
        self.name = name
        self.email = email

class UserRepository:
    def save(self, user):
        # Database logic
        pass

class EmailService:
    def send(self, to, message):
        # Email logic
        pass

class EmailValidator:
    def is_valid(self, email):
        # Validation logic
        pass
```

### Testing
```python
# Python - Unit testing with unittest
import unittest

def add_numbers(a, b):
    return a + b

class TestMathFunctions(unittest.TestCase):
    def test_add_positive_numbers(self):
        self.assertEqual(add_numbers(2, 3), 5)
    
    def test_add_negative_numbers(self):
        self.assertEqual(add_numbers(-2, -3), -5)
    
    def test_add_mixed_numbers(self):
        self.assertEqual(add_numbers(-2, 3), 1)

if __name__ == '__main__':
    unittest.main()
```

---

## Common Programming Patterns

### Recursion
A function calling itself to solve a problem.

```python
# Python - Recursive factorial
def factorial(n):
    # Base case
    if n <= 1:
        return 1
    # Recursive case
    return n * factorial(n - 1)

print(factorial(5))  # 120
```

### Iteration vs Recursion
```python
# Python - Iterative vs Recursive Fibonacci

# Iterative approach
def fibonacci_iterative(n):
    if n <= 1:
        return n
    
    a, b = 0, 1
    for _ in range(2, n + 1):
        a, b = b, a + b
    return b

# Recursive approach
def fibonacci_recursive(n):
    if n <= 1:
        return n
    return fibonacci_recursive(n - 1) + fibonacci_recursive(n - 2)

print(fibonacci_iterative(10))   # 55
print(fibonacci_recursive(10))   # 55 (but much slower for large n)
```

### Design Patterns

#### Singleton Pattern
```python
# Python - Singleton pattern
class DatabaseConnection:
    _instance = None
    
    def __new__(cls):
        if cls._instance is None:
            cls._instance = super().__new__(cls)
        return cls._instance
    
    def __init__(self):
        if not hasattr(self, 'initialized'):
            self.connection_string = "database://localhost"
            self.initialized = True

# Usage
db1 = DatabaseConnection()
db2 = DatabaseConnection()
print(db1 is db2)  # True - same instance
```

---

## Summary

This terminology journal covers the fundamental concepts every programmer should understand:

- **Data Types & Variables**: The building blocks of programs
- **Control Structures**: How to control program flow
- **Functions & Methods**: Reusable code blocks
- **Object-Oriented Programming**: Organizing code with classes and objects
- **Data Structures**: Efficient ways to store and organize data
- **Algorithms & Complexity**: Problem-solving approaches and performance analysis
- **Error Handling**: Managing and recovering from errors
- **Best Practices**: Writing clean, maintainable code

Mastering these fundamentals provides a solid foundation for learning any programming language and tackling complex software development challenges.

---

*Remember: Programming is a skill that improves with practice. Start with simple examples, gradually work on more complex problems, and always strive to write clean, readable code.*
