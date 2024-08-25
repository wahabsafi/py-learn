Python provides several conditional statements to control the flow of your code based on different conditions. Here are the main ones:

**1. `if` Statement:**

- Executes a block of code if a condition is True.

```python
if condition:
    # Code to execute if condition is True
```

**2. `if-else` Statement:**

- Executes one block of code if a condition is True, and another block if it's False.

```python
if condition:
    # Code to execute if condition is True
else:
    # Code to execute if condition is False
```

**3. `if-elif-else` Statement:**

- Checks multiple conditions sequentially and executes the first one that is True. If none are True, the `else` block is executed.

```python
if condition1:
    # Code to execute if condition1 is True
elif condition2:
    # Code to execute if condition2 is True
else:
    # Code to execute if none of the conditions are True
```

**4. Nested `if` Statements:**

- You can nest `if` statements within other `if` statements to create more complex conditions.

```python
if condition1:
    if condition2:
        # Code to execute if both conditions are True
    else:
        # Code to execute if condition1 is True but condition2 is False
else:
    # Code to execute if condition1 is False
```

**Examples:**

```python
age = 25

if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")

x = 10

if x > 0:
    print("x is positive.")
elif x < 0:
    print("x is negative.")
else:
    print("x is zero.")

score = 85

if score >= 90:
    print("Grade A")
elif score >= 80:
    print("Grade B")
else:
    print("Grade C")
```

**Key points:**

- Conditions are evaluated to either True or False.
- The code block within the `if` statement is executed only if the condition is True.
- The `else` block is executed only if the `if` condition is False.
- You can use `elif` to check multiple conditions sequentially.
- Nested `if` statements allow for more complex decision-making.

By understanding and effectively using conditional statements, you can create dynamic and flexible Python programs that can adapt to different situations.
