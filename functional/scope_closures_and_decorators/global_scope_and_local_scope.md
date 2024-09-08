**Global Scope:**

- **Encompasses the entire program:** Global scope refers to the outermost level of a Python program. Variables defined at this level are accessible from anywhere within the program.
- **Defined outside functions:** Global variables are typically defined outside of functions.
- **Modified from anywhere:** They can be modified from any part of the program, including within functions.

**Example:**

```python
global_variable = 10

def my_function():
    print(global_variable)  # Accesses the global variable

my_function()  # Output: 10
```

**Local Scope:**

- **Within functions:** Local scope refers to the scope within a function. Variables defined inside a function are only accessible within that function and its nested functions.
- **Created upon function call:** Local variables are created when a function is called and are destroyed when the function returns.

**Example:**

```python
def my_function():
    local_variable = 20
    print(local_variable)  # Accesses the local variable

my_function()  # Output: 20

# Trying to access the local variable outside the function will raise an error
# print(local_variable)  # Raises NameError: name 'local_variable' is not defined
```

**Key Points:**

- Variables defined outside functions have global scope.
- Variables defined within functions have local scope.
- Local variables take precedence over global variables with the same name within a function.
- To modify a global variable within a function, you need to use the `global` keyword.

**Example with `global` keyword:**

```python
global_variable = 10

def modify_global():
    global global_variable
    global_variable = 20

modify_global()
print(global_variable)  # Output: 20
```

**Additional Notes:**

- Nested functions can access variables from their enclosing functions (non-local scope).
- Python also supports the `nonlocal` keyword to modify variables from outer non-local scopes within nested functions.

By understanding global and local scope, you can write more organized and maintainable Python code.
