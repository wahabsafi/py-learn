**`break` Statement:**

- **Purpose:** Terminates the execution of a loop (either a `for` loop or a `while` loop) immediately, even if the loop's condition is still true.
- **Usage:**

```python
while condition:
    # Code block
    if some_condition:
        break
```

- **Example:**

```python
numbers = [1, 2, 3, 4, 5]
for number in numbers:
    if number == 3:
        break
    print(number)
```

**`continue` Statement:**

- **Purpose:** Skips the remaining code in the current iteration of a loop and proceeds to the next iteration.
- **Usage:**

```python
while condition:
    # Code block
    if some_condition:
        continue
    # Remaining code
```

- **Example:**

```python
numbers = [1, 2, 3, 4, 5]
for number in numbers:
    if number % 2 == 0:
        continue
    print(number)
```

**`try` Statement:**

- **Purpose:** Handles potential exceptions (errors) that may occur during code execution.
- **Usage:**

```python
try:
    # Code that might raise an exception
except ExceptionType:
    # Code to handle the exception
else:
    # Code to execute if no exception occurred
finally:
    # Code to execute regardless of whether an exception occurred
```

- **Example:**

```python
try:
    number = int(input("Enter a number: "))
    result = 10 / number
    print("Result:", result)
except ZeroDivisionError:
    print("Error: Cannot divide by zero.")
else:
    print("Division successful.")
finally:
    print("This code always executes.")
```

**Key Points:**

- `break` immediately terminates the loop.
- `continue` skips the current iteration and proceeds to the next.
- `try`-`except` blocks are used to handle exceptions.
- The `else` block is executed if no exception occurs.
- The `finally` block is always executed, regardless of whether an exception occurred.
- You can use multiple `except` blocks to handle different types of exceptions.

By understanding and effectively using these statements, you can write more robust and error-tolerant Python code.
