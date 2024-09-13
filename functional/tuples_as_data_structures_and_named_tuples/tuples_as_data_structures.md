## Tuples in Python: Immutable Sequences

**Tuples** are ordered, immutable sequences of elements in Python. This means that once a tuple is created, its elements cannot be changed. They are often used to represent groups of related data.

### Creating Tuples
Tuples are created using parentheses `()`. Elements within the parentheses are separated by commas.

```python
# Creating a tuple
my_tuple = (1, 2, 3, "hello", True)
```

### Accessing Elements
Elements in a tuple can be accessed using their index, starting from 0.

```python
# Accessing elements by index
first_element = my_tuple[0]  # 1
second_element = my_tuple[1]  # 2
```

### Slicing Tuples
You can extract a subset of elements from a tuple using slicing.

```python
# Slicing a tuple
sub_tuple = my_tuple[1:3]  # (2, 3)
```

### Immutability
Tuples are immutable, meaning you cannot modify their elements directly. Attempting to do so will raise an error.

```python
my_tuple[0] = 4  # This will raise a TypeError
```

### Common Use Cases
Tuples are often used for:

* **Representing fixed-length sequences:** For example, coordinates, dates, or RGB color values.
* **Returning multiple values from a function:** Functions can return tuples to return multiple values.
* **Using as keys in dictionaries:** Tuples can be used as keys in dictionaries because they are hashable (due to their immutability).

**Example:**

```python
# Representing a point in 2D space
point = (3, 5)

# Returning multiple values from a function
def divide(x, y):
    return x / y, x % y

result = divide(10, 3)
print(result)  # Output: (3, 1)
```

**In summary,** tuples provide a convenient and efficient way to represent ordered, immutable sequences of elements in Python. Their immutability makes them suitable for use in various scenarios where the data needs to remain unchanged.
