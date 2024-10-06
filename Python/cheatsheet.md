# Python Cheatsheet

## Basics

- **Variables**: 
    ```python
    variable_name = value  # Assigns a value to a variable
    ```

- **Data Types**:
  - `int`: Integer type for whole numbers (e.g., `5`).
  - `float`: Floating-point type for decimal numbers (e.g., `3.14`).
  - `str`: String type for textual data (e.g., `"Hello"`).
  - `list`: Ordered and mutable collection of items (e.g., `[1, 2, 3]`).
  - `tuple`: Ordered and immutable collection (e.g., `(1, 2, 3)`).
  - `dict`: Unordered collection of key-value pairs (e.g., `{"key": "value"}`).
  - `set`: Unordered collection of unique items (e.g., `{1, 2, 3}`).

- **Functions**: 
    ```python
    def function_name(parameters):
        # Code to execute
        return result  # Optional return statement
    ```

## Intermediate

- **List Comprehensions**: Concise way to create lists.
    ```python
    squares = [x**2 for x in range(10)]  # Creates a list of squares from 0 to 9
    ```

- **Lambda Functions**: Small anonymous functions defined with the `lambda` keyword.
    ```python
    add = lambda x, y: x + y
    result = add(5, 3)  # result is 8
    ```

- **File Handling**: Reading from and writing to files.
    ```python
    with open('file.txt', 'r') as file:  # Opens file for reading
        content = file.read()  # Reads file content
    ```

- **Error Handling**: Using `try...except` to catch exceptions.
    ```python
    try:
        # Code that may cause an exception
    except ExceptionType as e:
        print(f'Error occurred: {e}')
    ```

## Advanced

- **Decorators**: A way to modify the behavior of a function.
    ```python
    def my_decorator(func):
        def wrapper():
            print("Before the function call.")
            func()
            print("After the function call.")
        return wrapper

    @my_decorator
    def say_hello():
        print("Hello!")
    ```

- **Generators**: Functions that return an iterable set of values, one at a time, using `yield`.
    ```python
    def my_generator():
        yield 1
        yield 2
        yield 3

    for value in my_generator():
        print(value)  # Outputs 1, 2, 3
    ```

- **Context Managers**: Manages resources, ensuring proper acquisition and release.
    ```python
    class MyContextManager:
        def __enter__(self):
            # Setup code
            return self

        def __exit__(self, exc_type, exc_value, traceback):
            # Cleanup code
            pass

    with MyContextManager() as manager:
        # Code that uses the manager
    ```

- **Regular Expressions**: Used for searching and manipulating strings.
    ```python
    import re

    pattern = r'\d+'  # Matches one or more digits
    result = re.findall(pattern, 'There are 2 apples and 5 bananas.')  # ['2', '5']
    ```

- **Multithreading**: Running multiple threads (smaller units of a process) simultaneously.
    ```python
    import threading

    def print_numbers():
        for i in range(5):
            print(i)

    thread = threading.Thread(target=print_numbers)
    thread.start()  # Starts the thread
    thread.join()   # Waits for the thread to finish
    ```

