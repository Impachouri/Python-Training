# Advanced Python Assignment: Variables, Statements, and Expressions

## 1. Advanced Data Types and Type Conversion

### Challenge:

- Create a Python program that accepts user inputs of different types (integer, float, string, boolean) and dynamically stores them in a dictionary.
- Implement type-checking logic to ensure that inputs are stored as the correct data type.
- Write a function `convert_and_calculate` that converts all numeric values to floats and calculates their sum.

### prerequisite:

Dictionary, list comprehension

## 2. Complex Expressions and Order of Operations

### Challenge:

- Write a Python function `evaluate_expression` that accepts a string representing a mathematical expression and evaluates it.
- The function should handle parentheses, exponentiation, and mixed operators.
- Implement error handling to manage invalid expressions.

### prerequisite:

eval function

## 3. Dynamic Variable Management

### Challenge:

- Create a program where the user can dynamically create variables with names and values entered as inputs.
- Store these variables in a dictionary, and allow the user to update any variable by providing its name and a new value.

### prerequisite:

Dictionary

## 4. Advanced Function Calls and Nested Expressions

### Challenge:

- Implement a function `nested_function_call` that accepts a list of numbers and returns the result of `max(numbers) - min(numbers) + sum(numbers)`.
- Avoid using loops; rely solely on built-in functions and expressions.

## 5. Reassignment and Updating Variables

### Challenge:

- Create a simulation where a variable `balance` starts at 1000.
- Simulate daily transactions, updating the balance accordingly.
- Print the balance after each transaction.

### Example

balance = 1000
transactions = [100, -50, 200, -75]

## 6. Investigating Memory Allocation

### Challenge:

- Write a program that compares the memory addresses of variables before and after reassignment.
- Use the `id()` function to inspect the memory addresses.
