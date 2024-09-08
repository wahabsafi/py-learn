**Non-Local Scope in Python**

Non-local scope refers to the scope of variables that are defined in an outer function but are accessible from nested functions. This is different from global scope, which applies to variables defined outside of any function.

**Using the `nonlocal` Keyword:**

To access and modify variables from an outer non-local scope within a nested function, you need to use the `nonlocal` keyword. This indicates that the variable should be treated as non-local, rather than a new local variable.

**Example:**

```python
def outer_function():
    x = 10

    def inner_function():
        nonlocal x
        x = 20

    inner_function()
    print(x)  # Output: 20

outer_function()
```

In this example:

- `x` is defined in the `outer_function` and is therefore non-local to the `inner_function`.
- The `nonlocal` keyword in `inner_function` indicates that the `x` being modified is the non-local variable, not a new local variable.
- The modified value of `x` is accessible in the `outer_function` after the `inner_function` is called.

**Key Points:**

- The `nonlocal` keyword is used to modify variables from outer non-local scopes within nested functions.
- Non-local scope is different from global scope.
- Using `nonlocal` can be helpful for creating closures and implementing certain design patterns.

**Additional Notes:**

- If a variable is not found in the local or global scope, Python searches for it in the enclosing scopes.
- The `nonlocal` keyword can be used to modify variables from multiple levels of nesting.

By understanding non-local scope and the `nonlocal` keyword, you can write more flexible and expressive Python code.
