**Docstrings:**

- **Purpose:** Docstrings are string literals placed at the beginning of functions, classes, and modules to provide documentation about their purpose, parameters, return values, and usage.
- **Best practices:**
    - Use triple quotes (`"""`) to enclose docstrings for multi-line descriptions.
    - Write clear and concise explanations.
    - Use consistent formatting and indentation.
    - Include information about parameters, return values, and potential exceptions.
- **Example:**

```python
def my_function(x, y):
    """Calculates the sum of two numbers.

    Args:
        x: The first number.
        y: The second number.

    Returns:
        The sum of x and y.
    """

    return x + y
```

**Annotations:**

- **Purpose:** Annotations are optional type hints added to function parameters and return values. They provide information about the expected data types, making code more readable and maintainable.
- **Syntax:**

```python
def my_function(x: int, y: float) -> float:
    """Calculates the sum of two numbers.

    Args:
        x: The first number (integer).
        y: The second number (float).

    Returns:
        The sum of x and y (float).
    """

    return x + y
```

- **Benefits:**
    - Improved code readability and understanding.
    - Enhanced static type checking with tools like `mypy`.
    - Better IDE support, such as auto-completion and type hints.

**Combining Docstrings and Annotations:**

You can combine docstrings and annotations to provide comprehensive documentation for your functions:

```python
def my_function(x: int, y: float) -> float:
    """Calculates the sum of two numbers.

    Args:
        x: The first number (integer).
        y: The second number (float).

    Returns:
        The sum of x and y (float).
    """

    return x + y
```

**Key Points:**

- Docstrings are essential for documenting your code.
- Annotations provide optional type hints.
- Combining docstrings and annotations can enhance code readability and maintainability.
- Use consistent formatting and style for both docstrings and annotations.

By effectively using docstrings and annotations, you can improve the quality and maintainability of your Python code.
