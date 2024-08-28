**Complex Numbers in Python:**

Complex numbers in Python are represented using the `complex` class from the built-in `complex` module. They consist of a real part and an imaginary part.

**Creating Complex Numbers:**

You can create complex numbers in several ways:

- **Directly:**
  ```python
  complex_number = 3 + 4j
  ```
- **Using the `complex()` constructor:**
  ```python
  complex_number = complex(3, 4)
  ```

**Accessing Real and Imaginary Parts:**

You can access the real and imaginary parts of a complex number using the `real` and `imag` attributes:

```python
complex_number = 3 + 4j
real_part = complex_number.real  # 3
imaginary_part = complex_number.imag  # 4
```

**Arithmetic Operations:**

You can perform various arithmetic operations on complex numbers:

- **Addition:**
  ```python
  result = (3 + 4j) + (1 - 2j)  # 4 + 2j
  ```
- **Subtraction:**
  ```python
  result = (3 + 4j) - (1 - 2j)  # 2 + 6j
  ```
- **Multiplication:**
  ```python
  result = (3 + 4j) * (1 - 2j)  # 11 + 2j
  ```
- **Division:**
  ```python
  result = (3 + 4j) / (1 - 2j)  # -0.2 + 1.4j
  ```
- **Conjugate:**
  ```python
  result = (3 + 4j).conjugate()  # 3 - 4j
  ```
- **Magnitude (absolute value):**
  ```python
  result = abs(3 + 4j)  # 5.0
  ```

**Special Values:**

Python supports the following special complex numbers:

- `complex(0, 1)`: Represents the imaginary unit `i`.
- `complex(inf, 0)`: Represents positive infinity.
- `complex(-inf, 0)`: Represents negative infinity.
- `complex(nan, 0)`: Represents not a number (NaN).

**Additional Notes:**

- Complex numbers are immutable in Python, meaning their values cannot be changed after creation.
- You can use the `cmath` module for more advanced complex number operations, such as trigonometric functions and logarithms.

**Example:**

```python
complex_number1 = 3 + 4j
complex_number2 = 1 - 2j

result = complex_number1 * complex_number2
print(result)  # Output: (11+2j)
```

By understanding complex numbers in Python, you can effectively work with them in various mathematical and scientific applications.
