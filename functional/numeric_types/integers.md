## Integers in Python

**Integers** in Python are numerical data types representing whole numbers without decimal points. They can be both positive, negative, or zero.

**Key Characteristics:**

- **Arbitrary Precision:** Python integers can handle arbitrarily large numbers, unlike many other programming languages that have fixed-size integer types. This means you can work with extremely large or small numbers without worrying about overflow or underflow.
- **Immutability:** Integers are immutable, meaning their value cannot be changed after they are created. When you reassign an integer variable, you're essentially creating a new integer object.
- **Operations:** You can perform various mathematical operations on integers, including:
    - Addition (`+`)
    - Subtraction (`-`)
    - Multiplication (`*`)
    - Division (`/`)
    - Floor division (`//`)
    - Modulus (`%`)
    - Exponentiation (`**`)

**Example:**

```python
x = 10
y = -5
z = 0

# Arithmetic operations
result1 = x + y
result2 = x * y
result3 = x // y  # Floor division
result4 = x % y  # Modulus

print(result1)  # Output: 5
print(result2)  # Output: -50
print(result3)  # Output: -2
print(result4)  # Output: 0
```

## Integer Constructors and Bases

**Integer Constructors**

Python provides several ways to create integer objects:

1. **Direct Assignment:**
   - The most common method is to directly assign an integer value to a variable:

   ```python
   x = 10
   y = -5
   ```

2. **`int()` Function:**
   - You can use the `int()` function to convert other data types (such as strings, floats, or other integers) to integers:

   ```python
   x = int("10")  # Converts string to integer
   y = int(3.14)  # Converts float to integer (truncates decimal part)
   ```

**Integer Bases**

Python supports integers in various bases, including:

- **Decimal (base 10):** The default base for integers in Python.
- **Binary (base 2):** Use a prefix `0b` or `0B` to represent binary numbers.
- **Octal (base 8):** Use a prefix `0o` or `0O` to represent octal numbers.
- **Hexadecimal (base 16):** Use a prefix `0x` or `0X` to represent hexadecimal numbers.

**Examples:**

```python
# Decimal
x = 10

# Binary
y = 0b1010  # Equivalent to 10 in decimal
z = 0B1010  # Equivalent to 10 in decimal

# Octal
a = 0o12  # Equivalent to 10 in decimal
b = 0O12  # Equivalent to 10 in decimal

# Hexadecimal
c = 0xA  # Equivalent to 10 in decimal
d = 0XA  # Equivalent to 10 in decimal
```

**Converting Between Bases:**

You can use the built-in functions `bin()`, `oct()`, and `hex()` to convert integers to their binary, octal, or hexadecimal representations, respectively.

```python
x = 10
binary_string = bin(x)  # Output: '0b1010'
octal_string = oct(x)  # Output: '0o12'
hex_string = hex(x)  # Output: '0xa'
```

**Additional Notes:**

- When converting from other data types to integers, the `int()` function truncates the decimal part of floating-point numbers.
- You can specify the base when using the `int()` function to convert strings to integers. For example, `int("1010", 2)` converts the binary string "1010" to the decimal integer 10.

By understanding integer constructors and bases, you can effectively work with integers in Python and perform various numerical operations.

- Python also supports **long integers** for extremely large numbers. However, the distinction between integers and long integers has been removed in Python 3.
- You can convert other data types to integers using the `int()` function. For example, `int("10")` converts the string "10" to the integer 10.

**In Conclusion:**

Integers are a fundamental data type in Python, providing a versatile and efficient way to work with whole numbers. Understanding their characteristics and operations is essential for effective programming in Python.
