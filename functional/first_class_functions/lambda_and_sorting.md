
**Sorting with Lambda Expressions:**

- **`sorted()` function:** The `sorted()` function is used to sort iterables (like lists, tuples, or strings) in ascending order.
- **`key` argument:** The `key` argument of `sorted()` takes a function that returns a key for each element to be compared during sorting.
- **Lambda as `key`:** Lambda expressions are commonly used as the `key` argument to define custom sorting criteria.

**Examples:**

**Sorting by a custom attribute:**

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

people = [Person("Alice", 30), Person("Bob", 25), Person("Charlie", 35)]

# Sort by age in ascending order
sorted_people = sorted(people, key=lambda person: person.age)
print(sorted_people)  # Output: [Person(name='Bob', age=25), Person(name='Alice', age=30), Person(name='Charlie', age=35)]
```

**Sorting by a calculated value:**

```python
numbers = [3, 1, 4, 1, 5, 9]

# Sort by the last digit of each number
sorted_numbers = sorted(numbers, key=lambda x: x % 10)
print(sorted_numbers)  # Output: [1, 1, 5, 9, 3, 4]
```

**Sorting in descending order:**

```python
sorted_numbers = sorted(numbers, key=lambda x: x % 10, reverse=True)
print(sorted_numbers)  # Output: [4, 3, 9, 5, 1, 1]
```

**Key points:**

- Lambda expressions provide a concise way to define functions for sorting.
- The `key` argument in `sorted()` allows you to customize the sorting criteria.
- You can use complex expressions within lambda functions to define custom sorting logic.
- The `reverse` argument in `sorted()` can be used to sort in descending order.

By effectively using lambda expressions with `sorted()`, you can sort lists based on various criteria, making your Python code more flexible and efficient.
