# C++ Cheatsheet

## Basics

- **Variables**: 
    ```cpp
    int variableName = value;  // Declaring an integer variable
    ```

- **Data Types**: 
  - `int`: Integer type (e.g., `42`).
  - `float`: Floating-point type (e.g., `3.14`).
  - `double`: Double precision floating-point type (e.g., `3.14159`).
  - `char`: Character type (e.g., `'a'`).
  - `string`: String type for text (requires `#include <string>`).
  - `bool`: Boolean type for true/false values.

- **Functions**: 
    ```cpp
    returnType functionName(parameters) {
        // Code to execute
    }
    ```

## Intermediate

- **Pointers**: Variables that store memory addresses of another variable.
    ```cpp
    int* ptr = &variable; // Pointer to an integer variable
    ```

- **Classes**: Blueprints for creating objects (instances).
    ```cpp
    class ClassName {
    public:
        void methodName() {
            // Code
        }
    };
    ```

- **Inheritance**: Mechanism for creating a new class from an existing class.
    ```cpp
    class Base {
    public:
        void baseMethod() {}
    };

    class Derived : public Base {
    public:
        void derivedMethod() {}
    };
    ```

- **Standard Template Library (STL)**: Library providing data structures and algorithms.
    - Example: Using vectors.
    ```cpp
    #include <vector>
    
    std::vector<int> vec;  // Declaring a vector
    vec.push_back(10);     // Adding an element
    ```

## Advanced

- **Templates**: Allow functions and classes to operate with generic types.
    ```cpp
    template <typename T>
    T add(T a, T b) {
        return a + b;
    }
    ```

- **Exception Handling**: Mechanism to handle runtime errors.
    ```cpp
    try {
        // Code that may throw an exception
    } catch (const std::exception& e) {
        std::cout << "Error: " << e.what() << std::endl;
    }
    ```

- **Lambda Expressions**: Anonymous functions for short snippets of code.
    ```cpp
    auto add = [](int a, int b) { return a + b; };
    ```

- **Smart Pointers**: Memory management features (e.g., `std::unique_ptr`, `std::shared_ptr`).
    ```cpp
    #include <memory>
    
    std::unique_ptr<int> ptr = std::make_unique<int>(5); // Unique pointer
    ```

- **Multithreading**: Running threads concurrently.
    ```cpp
    #include <thread>
    
    void threadFunction() {
        // Code for the thread
    }

    std::thread t(threadFunction);  // Create a thread
    t.join();                       // Wait for the thread to finish
    ```

