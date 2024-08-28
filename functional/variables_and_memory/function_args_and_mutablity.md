**Function Arguments:**

* **Passing values:** When you call a function in Python, you can pass values to it as arguments. These arguments become variables within the function's scope.
* **Types of arguments:** There are three main types of arguments:
    - **Positional arguments:** These are passed in the order they are defined in the function's signature.
    - **Keyword arguments:** These are passed using keyword-value pairs, allowing you to specify the argument names explicitly.
    - **Default arguments:** These are assigned default values in the function's signature, so they are optional when calling the function.

**Mutability and Function Arguments:**

* **Mutable objects:** When you pass a mutable object (like a list or dictionary) as an argument to a function, the function can modify the object's contents. This is because the function receives a reference to the object, not a copy.
* **Immutable objects:** When you pass an immutable object (like a number, string, or tuple) as an argument to a function, the function cannot modify the object's value. Instead, it creates a new object with the modified value.

**Example:**

```python
def modify_list(my_list):
    my_list.append(4)

my_list = [1, 2, 3]
modify_list(my_list)
print(my_list)  # Output: [1, 2, 3, 4]

def modify_string(my_string):
    my_string = my_string + " world"

my_string = "hello"
modify_string(my_string)
print(my_string)  # Output: hello
```

In the first example, the `modify_list` function modifies the list passed as an argument. This is because lists are mutable. In the second example, the `modify_string` function creates a new string and assigns it to `my_string` within the function, but this doesn't affect the original `my_string` outside the function.

**Key Points:**

* When passing mutable objects to functions, be aware that the function can modify the original object.
* When passing immutable objects to functions, the function cannot modify the original object.
* Understanding the mutability of objects is crucial for writing correct and predictable Python code.
