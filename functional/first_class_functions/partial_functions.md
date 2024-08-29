**Partial Functions:**

- **Creating new functions:** Partial functions are created by fixing some of the arguments of an existing function. This creates a new function with fewer parameters.
- **`functools.partial()`:** The `functools.partial()` function is used to create partial functions.
- **Syntax:** `functools.partial(func, *args, **kwargs)`

**Example:**

```python
from functools import partial

def greet(name, age):
    print("Hello, " + name + "! You are " + str(age) + " years old.")

greet_30 = partial(greet, age=30)
greet_30("Alice")  # Output: Hello, Alice! You are 30 years old.
```

In this example, `greet_30` is a partial function created by fixing the `age` argument to 30. When `greet_30` is called, only the `name` argument needs to be provided.

**Key Points:**

- Partial functions are created using the `functools.partial()` function.
- You can fix any number of arguments of an existing function.
- Partial functions can be used to create more concise and reusable code.
- Partial functions can be combined with other functional programming techniques like lambda expressions and decorators.

**Additional Examples:**

- **Creating a function that always adds 10:**

```python
add_10 = partial(lambda x, y: x + y, 10)
result = add_10(5)  # Output: 15
```

- **Creating a function that always prints a specific message:**

```python
print_message = partial(print, "Hello, world!")
print_message()  # Output: Hello, world!
```

**Use Cases:**

- **Creating reusable functions:** Partial functions can be used to create reusable functions with specific default arguments.
- **Simplifying function calls:** By fixing some arguments, partial functions can make function calls more concise.
- **Implementing design patterns:** Partial functions can be used to implement design patterns like the Strategy pattern.


## Real-World Examples of Partial Functions


### 1. **Creating Reusable Functions with Default Arguments:**

- **Logging:**
  ```python
  import logging

  def log_message(level, message):
      logging.log(level, message)

  log_info = partial(log_message, logging.INFO)
  log_info("This is an info message")  # Logs the message at the INFO level
  ```

- **Database Queries:**
  ```python
  def execute_query(connection, query, params=None):
      cursor = connection.cursor()
      cursor.execute(query, params)
      return cursor.fetchall()

  execute_query_with_params = partial(execute_query, connection, "SELECT * FROM users WHERE name = %s")
  result = execute_query_with_params("Alice")
  ```

### 2. **Currying:**

- **Creating new functions with fixed arguments:**
  ```python
  def add(x, y):
      return x + y

  add_10 = partial(add, 10)
  result = add_10(5)  # 15
  ```

### 3. **Simplifying Function Calls:**

- **Reducing boilerplate:**
  ```python
  def create_user(name, email, password):
      # ... create user ...

  create_user_with_password = partial(create_user, password="secret")
  create_user_with_password("Alice", "alice@example.com")
  ```

### 4. **Implementing Design Patterns:**

- **Strategy Pattern:**
  ```python
  def strategy1(x):
      return x**2

  def strategy2(x):
      return x + 10

  def apply_strategy(strategy, x):
      return strategy(x)

  apply_strategy_1 = partial(apply_strategy, strategy1)
  apply_strategy_2 = partial(apply_strategy, strategy2)
  ```

### 5. **Customizing Library Functions:**

- **Modifying built-in functions:**
  ```python
  from functools import partial
  from math import pow

  pow_2 = partial(pow, exp=2)
  result = pow_2(5)  # 25
  ```

These are just a few examples of how partial functions can be used in real-world applications.
By understanding partial functions, you can write more flexible, reusable, and efficient Python code.
