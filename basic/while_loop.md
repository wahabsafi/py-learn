**While Loops in Python**

A while loop in Python is a control flow statement that repeatedly executes a block of code as long as a specified condition remains true. It's a useful tool for performing actions until a certain criteria is met.

**Basic Syntax:**

```python
while condition:
    # Code to be executed
```

- **Condition:** An expression that evaluates to either `True` or `False`.
- **Code to be executed:** A block of code that will be executed repeatedly as long as the condition is `True`.

**Example:**

```python
count = 0
while count < 5:
    print("Count:", count)
    count += 1
```

This code will print the numbers from 0 to 4, as the condition `count < 5` is true until `count` becomes 5.

**Infinite Loops:**

Be cautious of infinite loops. If the condition never becomes false, the loop will continue indefinitely. To avoid this, ensure that the condition eventually becomes false within the loop's body.

**Break and Continue Statements:**

- **`break`:** Terminates the loop immediately, even if the condition is still true.
- **`continue`:** Skips the remaining code in the current iteration and starts the next iteration.

```python
while True:
    number = int(input("Enter a number (0 to quit): "))
    if number == 0:
        break
    print("The square of", number, "is", number * number)
```

**Nested While Loops:**

You can have while loops within other while loops to create more complex control flow.

```python
i = 0
while i < 3:
    j = 0
    while j < 3:
        print(i, j)
        j += 1
    i += 1
```

**Key Points:**

- The `while` loop continues to execute as long as the condition is `True`.
- Be mindful of infinite loops.
- Use `break` to exit the loop prematurely.
- Use `continue` to skip the current iteration.
- Nested while loops can create complex control flow.

By understanding and effectively using while loops, you can write more flexible and powerful Python programs.
