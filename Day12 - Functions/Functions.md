---
## 📘 11.1 Introduction to Functions

### 11.1.1 Topics:
- What is a function?
- Importance of functions
- Types of functions (built-in vs user-defined)
- Modularity and code reuse

### 11.1.2 Learning Objectives:
- Understand how functions enhance code structure and readability.
- Define and invoke functions.
- Differentiate between returning and printing in a function.
---

## 🧱 11.2 Function Definition

### Notes:

```python
def greet():
    print("Hello, world!")
```

- `def` keyword starts function definition.
- `greet()` is the function name.
- `()` encloses optional parameters.

### 🔍 Key Points:

- The body is indented.
- Function definitions do not execute until called.

---

## 🚀 11.3 Function Invocation

### Notes:

```python
greet()
```

- This executes the function body.
- A function can be called multiple times.

---

## 🎯 11.4 Function Parameters

### Notes:

```python
def greet(name):
    print("Hello", name)
greet("Alice")
```

- Parameters are placeholders for input.
- Arguments are actual values passed.

---

## 🎁 11.5 Returning a Value from a Function

### Notes:

```python
def add(x, y):
    return x + y
result = add(3, 4)
```

- `return` sends a value back to the caller.
- Use the result further in your code.

---

## 👩‍💻 11.6 Decoding a Function

### Practice:

Break down and explain:

```python
def mystery(a, b):
    c = a * b
    print("Sum is", a + b)
    return c
```

---

## 📏 11.7 Type Annotations

### Notes:

```python
def add(x: int, y: int) -> int:
    return x + y
```

- Helps with readability and debugging.
- Not enforced at runtime.

---

## 🧮 11.8 A Function That Accumulates

### Notes:

```python
def accumulate(numbers):
    total = 0
    for num in numbers:
        total += num
    return total
```

- Used in summation, averages, etc.

---

## 🎯 11.9 Variables and Parameters are Local

### Notes:

```python
def func(x):
    x = x + 1
    print(x)

x = 10
func(x)
print(x)  # Still 10
```

- Variables inside functions are local unless declared global.

---

## 🌍 11.10 Global Variables

### Notes:

```python
count = 0
def increment():
    global count
    count += 1
```

- Use `global` to modify global variables inside a function.

---

## 🔁 11.11 Functions Can Call Other Functions (Composition)

### Notes:

```python
def square(x):
    return x * x

def sum_of_squares(a, b):
    return square(a) + square(b)
```

- Break large problems into smaller, reusable parts.

---

## 🧭 11.12 Flow of Execution Summary

### Key Ideas:

- Python reads from top to bottom.
- Function body executes **only** when called.
- Each function call starts a new local scope.

---

## 👩‍💻 11.13 Print vs Return

### Notes:

- `print()` outputs to console, used for user-facing messages.
- `return` sends data back to the caller.

```python
def f():
    print("Hi")  # Side effect

def g():
    return "Hi"  # Pure function
```

---

## 🔄 11.14 Passing Mutable Objects

### Notes:

```python
def modify_list(lst):
    lst.append(10)

my_list = [1, 2]
modify_list(my_list)
print(my_list)  # [1, 2, 10]
```

- Mutable objects (lists, dicts) can be changed inside functions.

---

## 💥 11.15 Side Effects

### Notes:

- Any modification of external state (printing, modifying global or mutable objects) is a side effect.

---

# 📘 In-depth Assignments

---

## 🧠 Level 1 – Basic Understanding

> Focus: Syntax, simple usage, function calls, return values

1. **Create a function `welcome()` that prints "Welcome to Python!" and call it three times.**
2. **Write a function `square(n)` that takes a number `n` and returns its square.**
3. **Write a function `is_even(num)` that returns `True` if a number is even, else `False`.**
4. **Define a function `full_name(first, last)` that returns the full name as a string.**
5. **Create a function `circle_area(radius)` that returns the area of a circle using `πr²`. Use `pi = 3.14`.**

---

## ⚙️ Level 2 – Intermediate Skills

> Focus: Parameters, return, iteration, conditionals, type annotations

1. **Define a function `sum_even(numbers: list[int]) -> int` that returns the sum of all even numbers in a list.**
2. **Write a function `reverse_string(s: str) -> str` to return the reverse of a string.**
3. **Create a function `fibonacci(n: int) -> list[int]` that returns the first `n` Fibonacci numbers.**
4. **Write a function `count_vowels(sentence: str) -> int` that counts and returns the number of vowels.**
5. **Write a function `average_marks(marks: list[float]) -> float` that returns the average of marks.**

---

## 🔬 Level 3 – Advanced Practice

> Focus: Function composition, scope, mutation, edge cases, pure vs impure functions

1. **Create a function `analyze_text(text: str)` that returns:**

   - Number of words
   - Number of unique words
   - Frequency of each word

2. **Write a function `is_palindrome(s: str) -> bool` that checks if the input string is a palindrome. Ignore cases and spaces.**

3. **Implement `nested_sum(data: list) -> int` that takes a nested list of integers and returns the sum of all integers.**

   ```python
   nested_sum([[1, 2], [3, [4, 5]], 6])  # Output: 21
   ```

4. **Create a function `safe_divide(x: float, y: float) -> float` that handles divide-by-zero using try-except.**

5. **Simulate a digital clock with a function `time_increment(h: int, m: int) -> tuple[int, int]` that returns the time after 1 minute. Handle boundary cases (e.g., 23:59).**

---

## 💻 Real-world Problem Set: Function Design and Architecture

> Focus: Realistic situations, reusable function design, side effects, mutable arguments

### **Personal Expense Tracker**

1. Create the following functions:

   - `add_expense(expenses: list[float], amount: float) -> None`
   - `total_expense(expenses: list[float]) -> float`
   - `highest_expense(expenses: list[float]) -> float`
   - `average_expense(expenses: list[float]) -> float`
   - `expense_summary(expenses: list[float]) -> dict[str, float]`

2. Use `global` variable to maintain a transaction count across functions.

3. Add a function `print_report()` that **prints** the entire summary — this demonstrates **side effects vs return**.

4. Apply **function composition** to build `generate_report()` that internally calls the above functions.

---

## 🧠 Conceptual Questions (Code + Theory)

1. **What is the difference between returning a value and printing it? Illustrate with two functions.**
2. **Explain with code how passing a mutable object (like a list) affects the original outside the function.**
3. **Write a function where a global variable is modified and explain the risks involved.**
4. **Demonstrate function composition by creating a calculator that computes `sqrt(x² + y²)` using helper functions.**
5. **Create an example where misunderstanding local scope causes a logic bug. Fix it using correct scoping.**

---

## 🌐 Bonus: Mini Challenges

1. **Write a recursive function to compute factorial of a number.**
2. **Create a function that accepts variable number of arguments and returns their sum.**
3. **Build a mock `login()` function that checks a username and password from a predefined list of users.**
4. **Write a function `flatten_list(nested: list) -> list` that flattens a nested list of any depth.**
5. **Use function annotations and docstrings to fully document a `bmi(weight: float, height: float) -> float` calculator.**

---
