**`for` Loops:**

- **Purpose:** Used to iterate over a sequence of elements (like lists, tuples, strings, or ranges).
- **Syntax:**

```python
for element in sequence:
    # Code to be executed
```

- **Elements:** The individual items in the sequence.
- **Sequence:** The collection of elements to iterate over.

**Examples:**

1. **Iterating over a list:**

```python
fruits = ["apple", "banana", "orange"]
for fruit in fruits:
    print(fruit)
```

2. **Iterating over a tuple:**

```python
numbers = (1, 2, 3, 4, 5)
for number in numbers:
    print(number * 2)
```

3. **Iterating over a string:**

```python
text = "hello world"
for char in text:
    print(char)
```

4. **Iterating over a range:**

```python
for i in range(5):
    print(i)
```

**`range()` Function:**

- Creates a sequence of numbers.
- Takes three arguments: `start` (default 0), `stop` (exclusive), and `step` (default 1).

```python
for i in range(2, 10, 2):
    print(i)
```

**Nested `for` Loops:**

- You can have `for` loops within other `for` loops to create more complex iterations.

```python
for i in range(3):
    for j in range(3):
        print(i, j)
```

**Key Points:**

- `for` loops are used to iterate over sequences.
- The `range()` function generates sequences of numbers.
- Nested `for` loops can be used for more complex iterations.
- The `break` and `continue` statements can be used to control the flow within `for` loops.

By understanding and effectively using `for` loops, you can write more concise and efficient Python code for various tasks.
