## Copying Sequences in Python

When working with sequences in Python, you may often need to create copies of existing sequences. There are two primary ways to do this:

### 1. **Shallow Copy**
* Creates a new sequence object but references the same underlying elements.
* Changes made to the original sequence will reflect in the copy.

**Using the `[:]` slice notation:**
```python
original_list = [1, 2, 3]
shallow_copy = original_list[:]
```

**Using the `copy()` method (for mutable sequences):**
```python
import copy

original_list = [1, 2, 3]
shallow_copy = copy.copy(original_list)
```

### 2. **Deep Copy**
* Creates a new sequence object and recursively copies all nested elements.
* Changes made to the original sequence or its nested elements will not affect the copy.

**Using the `deepcopy()` method:**
```python
import copy

original_list = [[1, 2], 3]
deep_copy = copy.deepcopy(original_list)
```

**When to Use Which:**

* **Shallow copy:** Use when you want to create a new sequence object without modifying the original sequence. However, be cautious of nested mutable elements.
* **Deep copy:** Use when you want to create a completely independent copy of the original sequence, including its nested elements. This is especially useful when dealing with nested mutable structures.

**Example:**

```python
original_list = [[1, 2], 3]

# Shallow copy
shallow_copy = original_list[:]
shallow_copy[0][0] = 5
print(original_list)  # Output: [[5, 2], 3]

# Deep copy
deep_copy = copy.deepcopy(original_list)
deep_copy[0][0] = 5
print(original_list)  # Output: [[1, 2], 3]
```

In this example, the shallow copy modifies the original list because it references the same nested list. The deep copy, on the other hand, creates a completely independent copy, so changes to the deep copy do not affect the original.

By understanding the difference between shallow and deep copies, you can effectively manipulate sequences in Python while maintaining data integrity.
