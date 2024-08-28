## Comparison Operators in Python

Comparison operators are used to compare values in Python. They return a Boolean value (True or False) based on the relationship between the operands.

**List of comparison operators:**

| Operator | Meaning | Example |
|---|---|---|
| `==` | Equal to | `x == y` |
| `!=` | Not equal to | `x != y` |
| `<` | Less than | `x < y` |
| `>` | Greater than | `x > y` |
| `<=` | Less than or equal to | `x <= y` |
| `>=` | Greater than or equal to | `x >= y` |

**Example:**

```python
x = 10
y = 5

if x > y:
    print("x is greater than y")
elif x == y:
    print("x is equal to y")
else:
    print("x is less than y")
```

**Important Notes:**

- When comparing floating-point numbers, be aware of potential rounding errors. Use a tolerance value to compare them approximately.
- You can chain comparison operators for more complex comparisons:

  ```python
  if 0 < x < 10:
      print("x is between 0 and 10")
  ```

- Comparison operators can be used with various data types, including numbers, strings, and lists. The comparison logic depends on the specific data type.
