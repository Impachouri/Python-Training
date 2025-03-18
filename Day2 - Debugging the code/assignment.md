## Advanced Debugging Assignment

### 1. Error Classification

Identify the type of error in the following code snippets and fix them:

```python
for i in range(5)
    print(i)

x = 10 / 0

def calculate_area(radius):
    return 2 * 3.14 * radius
```

### 2. Debugging Complex Functions

Debug the following function and correct the mistakes:

```python
def process_data(data):
    total = 0
    for item in data:
        total += int(item)
    return total / len(data)

print(process_data(['10', '20', 'abc', '30']))
```

### 3. Advanced Debugging Challenge

You’re given a function that fails intermittently. Investigate the bug and fix it:

```python
import random

def unreliable_function():
    number = random.choice([0, 1, 2])
    return 10 / number

for i in range(10):
    print(unreliable_function())
```

### 4. Writing Debug-Friendly Code

Refactor the following function to improve readability and add error handling:

```python
def calculate_discount(price, discount):
    return price - (price * discount / 100)

print(calculate_discount(100, '10%'))
```

### 5. Rubber Duck Debugging

Explain the following code snippet step-by-step as if you’re teaching someone unfamiliar with coding:

```python
numbers = [1, 2, 3, 4, 5]
result = 1
for num in numbers:
    result *= num
print("Product:", result)
```

### 6. Advanced Challenge: Debug a Multi-threaded Program

Fix the race condition in the following code:

```python
import threading

counter = 0
def increment():
    global counter
    for _ in range(100000):
        counter += 1

threads = [threading.Thread(target=increment) for _ in range(2)]
for t in threads:
    t.start()
for t in threads:
    t.join()

print("Counter:", counter)  # Expected: 200000
```

### 7. Activity: Debug with Breakpoints

Learn to use breakpoints in your IDE (e.g., VSCode, PyCharm) to inspect variable states step-by-step.

**Steps:**

1. Open your IDE and load the following code:

```python
def divide(a, b):
    result = a / b
    return result

a = 10
b = 0
print(divide(a, b))
```

2. Set a breakpoint at the line where `result` is calculated.
3. Run the code in debug mode.
4. Inspect the values of `a` and `b` before the division.
5. Step through the code to observe the flow of execution.
6. Fix the division by zero error and re-run the code.

#### Learn More:

- [VSCode Debugging Guide](https://code.visualstudio.com/docs/editor/debugging)
- [PyCharm Debugger](https://www.jetbrains.com/help/pycharm/debugging-your-first-python-application.html)

### 8. Memory Leaks and Performance Debugging

Optimize the following code and fix potential memory leaks:

```python
import time

def inefficient_function():
    result = []
    for i in range(100000):
        result.append(i * 2)
    time.sleep(2)
    return result

print(len(inefficient_function()))
```

### 9. Unexpected None

Debug why the function returns `None`:

```python
def add(a, b):
    result = a + b
print(add(3, 4))
```

### 10. Silent Failures

Identify why the code doesn't raise an error:

```python
try:
    result = 10 / 0
except:
    pass
print("No error detected!")
```

---

## Submission Guidelines:

- Submit a Python file containing your solutions.
- Include comments explaining each fix.
- Add a README file summarizing the challenges you faced and how you solved them.

Happy Debugging! 🐞
