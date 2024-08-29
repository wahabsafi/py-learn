**Function Introspection:**

Function introspection refers to the ability to examine the properties and behavior of a function at runtime. It allows you to access information about a function's parameters, return type, docstring, and other attributes.

**Common Introspection Techniques:**

1. **`dir()` function:**
   - Returns a list of all attributes (including methods) of an object, including functions.
   - Can be used to inspect the attributes of a function object.

   ```python
   def my_function(x, y):
       return x + y

   print(dir(my_function))
   ```

2. **`help()` function:**
   - Provides a detailed description of an object, including its docstring and parameters.
   - Can be used to get information about a function.

   ```python
   help(my_function)
   ```

3. **`inspect` module:**
   - Offers a more extensive set of tools for introspection.
   - Provides functions to get the function's source code, arguments, return type, and more.

   ```python
   import inspect

   print(inspect.getsource(my_function))
   print(inspect.getargspec(my_function))
   ```

**Key Attributes of Functions:**

- **`__name__`:** The name of the function.
- **`__doc__`:** The function's docstring.
- **`__annotations__`:** A dictionary containing type hints for the function's parameters and return value (if present).
- **`__defaults__`:** A tuple containing the default values for optional parameters.
- **`__kwdefaults__`:** A dictionary containing the default values for keyword-only arguments.

**Example:**

```python
def my_function(x: int, y: float = 3.14) -> float:
    """Calculates the sum of two numbers.

    Args:
        x: The first number (integer).
        y: The second number (float).

    Returns:
        The sum of x and y (float).
    """

    return x + y

print(my_function.__name__)  # Output: my_function
print(my_function.__doc__)  # Output: Calculates the sum of two numbers. ...
print(my_function.__annotations__)  # Output: {'x': <class 'int'>, 'y': <class 'float'>, 'return': <class 'float'>}
```

**Use Cases for Function Introspection:**

- **Dynamic code generation:** Generating code based on the properties of functions.
- **Debugging and analysis:** Examining the behavior and structure of functions.
- **Metaprogramming:** Creating programs that manipulate or generate other programs.

By understanding function introspection, you can gain valuable insights into the structure and behavior of your Python code, enabling you to write more efficient, maintainable, and flexible programs.
