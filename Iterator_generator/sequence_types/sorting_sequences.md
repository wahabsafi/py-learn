### Sorting Sequences in Python

Python provides built-in functionality to **sort sequences** such as **lists**, and you can even sort custom sequences by implementing certain methods. Sorting is essential when working with ordered data, and Python gives you flexible ways to do this.

#### Key Python tools for sorting:
- **`sorted()` function**: Returns a **new sorted list** from any iterable.
- **`list.sort()` method**: **Sorts the list in place**, modifying the original list.
- Custom sorting: Using **custom keys** and **reverse sorting**.
- **Custom sequences**: By implementing sorting logic in custom sequence classes.

---

### 1. **Using `sorted()` Function**

The `sorted()` function is a general-purpose tool that works on any iterable, including **lists**, **tuples**, **sets**, and even custom sequences (as long as they can be compared).

- **Syntax**: `sorted(iterable, key=None, reverse=False)`

- **Parameters**:
  - **`iterable`**: The sequence to be sorted.
  - **`key`**: A function that serves as a key for sorting.
  - **`reverse`**: If `True`, the list is sorted in descending order.

#### Example: Sorting a List

```python
my_list = [3, 1, 4, 1, 5, 9]
sorted_list = sorted(my_list)
print(sorted_list)  # Output: [1, 1, 3, 4, 5, 9]
```

#### Example: Sorting with `reverse=True`

```python
my_list = [3, 1, 4, 1, 5, 9]
sorted_list = sorted(my_list, reverse=True)
print(sorted_list)  # Output: [9, 5, 4, 3, 1, 1]
```

---

### 2. **Using `list.sort()` Method**

The `list.sort()` method **modifies the list in place**, meaning that the original list is rearranged. This method does not return anything (`None` is returned).

- **Syntax**: `list.sort(key=None, reverse=False)`

#### Example: In-Place Sorting

```python
my_list = [3, 1, 4, 1, 5, 9]
my_list.sort()
print(my_list)  # Output: [1, 1, 3, 4, 5, 9]
```

This modifies `my_list` directly, rather than creating a new list.

#### Example: In-Place Sorting in Descending Order

```python
my_list = [3, 1, 4, 1, 5, 9]
my_list.sort(reverse=True)
print(my_list)  # Output: [9, 5, 4, 3, 1, 1]
```

---

### 3. **Custom Sorting with `key` Parameter**

The `key` parameter allows you to specify a function that extracts a value to be used for sorting. This is helpful when sorting by a specific attribute or a more complex condition.

#### Example: Sorting Strings by Length

```python
words = ['apple', 'banana', 'kiwi', 'grape']
sorted_words = sorted(words, key=len)
print(sorted_words)  # Output: ['kiwi', 'grape', 'apple', 'banana']
```

Here, the list is sorted by the length of each word (using `len` as the key function).

#### Example: Sorting Complex Objects (Tuples) by a Specific Element

```python
# List of tuples (name, age)
people = [('Alice', 30), ('Bob', 25), ('Charlie', 35)]

# Sort by the second element (age)
sorted_people = sorted(people, key=lambda person: person[1])
print(sorted_people)  # Output: [('Bob', 25), ('Alice', 30), ('Charlie', 35)]
```

In this example, we use a `lambda` function to extract the second element (age) of each tuple for sorting.

---

### 4. **Custom Sequences and Sorting**

If you create a custom sequence class, you can enable sorting by either implementing comparison methods (`__lt__`, `__gt__`, etc.) or providing a `key` function when calling `sorted()` or `list.sort()`.

#### Example: Custom Sequence with Sorting Support

Let’s create a custom class that stores data and sorts it based on specific criteria, such as the sum of elements.

```python
class MySequence:
    def __init__(self, data):
        self.data = list(data)

    # Enable sorting by sum of elements
    def __lt__(self, other):
        return sum(self.data) < sum(other.data)

    def __repr__(self):
        return f"MySequence({self.data})"

# Example usage
seq1 = MySequence([1, 2, 3])
seq2 = MySequence([4, 5])
seq3 = MySequence([2, 2, 2])

my_sequences = [seq1, seq2, seq3]
sorted_sequences = sorted(my_sequences)
print(sorted_sequences)  # Output: [MySequence([2, 2, 2]), MySequence([1, 2, 3]), MySequence([4, 5])]
```

#### Explanation:
- **`__lt__(self, other)`**: This method defines what it means for one sequence to be "less than" another. Here, sequences are compared based on the sum of their elements.
- **`sorted()`**: Uses the `__lt__` method to sort the custom sequences.

---

### 5. **Sorting in Custom Sequences Using `key` Parameter**

You can also use the `key` parameter with custom sequences if you prefer not to implement comparison methods like `__lt__`. For example, sorting custom sequences based on the **length** of their data.

#### Example:

```python
class MySequence:
    def __init__(self, data):
        self.data = list(data)

    def __repr__(self):
        return f"MySequence({self.data})"

# Example usage
seq1 = MySequence([1, 2, 3])
seq2 = MySequence([4, 5])
seq3 = MySequence([2, 2])

my_sequences = [seq1, seq2, seq3]

# Sort by the length of the internal data
sorted_sequences = sorted(my_sequences, key=lambda seq: len(seq.data))
print(sorted_sequences)  # Output: [MySequence([2, 2]), MySequence([4, 5]), MySequence([1, 2, 3])]
```

#### Explanation:
- **`key=lambda seq: len(seq.data)`**: This extracts the length of each sequence’s data for sorting. The sequences are sorted by the number of elements they contain.

---

### 6. **Sorting in Reverse Order**

Both `sorted()` and `list.sort()` allow sorting in reverse order by passing `reverse=True`. This can be combined with a custom key for more flexible sorting.

#### Example: Sorting in Reverse by Length

```python
words = ['apple', 'banana', 'kiwi', 'grape']
sorted_words = sorted(words, key=len, reverse=True)
print(sorted_words)  # Output: ['banana', 'apple', 'grape', 'kiwi']
```

Here, the list of words is sorted by length, but in descending order.

---

### 7. **Sort Stability**

Python’s sorting is **stable**, meaning that when multiple records have the same key, their original order is preserved. This can be useful when performing **multi-level sorting**.

#### Example: Sorting by Two Criteria

```python
people = [('Alice', 30), ('Bob', 25), ('Charlie', 25), ('Dave', 30)]

# Sort by age, then by name
sorted_people = sorted(people, key=lambda person: (person[1], person[0]))
print(sorted_people)
# Output: [('Bob', 25), ('Charlie', 25), ('Alice', 30), ('Dave', 30)]
```

Here, we first sort by age, and then by name when ages are the same. The sorting is stable, so the order of people with the same age remains consistent based on the second sorting criterion (name).

---

### Summary:

- **`sorted()`**: Returns a new sorted list from any iterable.
- **`list.sort()`**: Sorts the list in place.
- Both methods support custom sorting using the `key` parameter and reverse sorting with `reverse=True`.
- Sorting can be applied to **custom sequences** by implementing comparison methods (e.g., `__lt__`) or by using the `key` parameter.
- Python’s sorting algorithm is **stable**, which is useful for multi-level sorting.
