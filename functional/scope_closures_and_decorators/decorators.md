## Decorators in Python

**Decorators** in Python are a powerful mechanism for modifying the behavior of functions or classes without directly altering their source code. They provide a way to add additional functionality to existing code in a modular and reusable manner.

**Basic Syntax:**

```python
def decorator_function(func):
    def wrapper(*args, **kwargs):
        # Perform additional actions before or after the function call
        result = func(*args, **kwargs)
        # Perform additional actions
        return result
    return wrapper

@decorator_function
def my_function(x, y):
    return x + y
```

**How Decorators Work:**

1. **Decorator Function:** The `decorator_function` takes another function as an argument and returns a new function.
2. **Wrapper Function:** The `wrapper` function inside the decorator acts as a wrapper around the original function. It can perform additional actions before or after the original function is called.
3. **Return Value:** The `wrapper` function returns the result of the original function.
4. **`@` Syntax:** The `@decorator_function` syntax is a syntactic sugar for applying the decorator to the `my_function`.

**Common Use Cases:**

- **Logging:**
  ```python
  def log_calls(func):
      def wrapper(*args, **kwargs):
          print(f"Calling {func.__name__}")
          result = func(*args, **kwargs)
          print(f"Result: {result}")
          return result
      return wrapper

  @log_calls
  def my_function(x, y):
      return x + y
  ```
- **Timing:**
  ```python
  import time

  def timeit(func):
      def wrapper(*args, **kwargs):
          start_time = time.time()
          result = func(*args, **kwargs)
          end_time = time.time()
          print(f"Time elapsed: {end_time - start_time} seconds")
          return result
      return wrapper

  @timeit
  def my_function(x, y):
      # ...
  ```
- **Caching:**
  ```python
  def cache(func):
      cache_dict = {}
      def wrapper(*args, **kwargs):
          key = (args, kwargs)
          if key in cache_dict:
              return cache_dict[key]
          result = func(*args, **kwargs)
          cache_dict[key] = result
          return result
      return wrapper

  @cache
  def fibonacci(n):
      # ...
  ```

**Key Points:**

- Decorators provide a modular and reusable way to modify the behavior of functions.
- Decorators can be chained to apply multiple modifications to a function.
- Decorators can be used for various purposes, such as logging, timing, caching, and more.

By understanding decorators, you can write more efficient, maintainable, and reusable Python code.
