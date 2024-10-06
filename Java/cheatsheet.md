# Java Cheatsheet

## Basics

- **Variables**: Used to store data values.
    ```java
    int variableName = value; // Integer variable
    String str = "Hello";     // String variable
    boolean isActive = true;  // Boolean variable
    ```

- **Data Types**:
  - `int`: Integer type (e.g., `42`).
  - `double`: Double precision floating-point type (e.g., `3.14`).
  - `char`: Single character (e.g., `'A'`).
  - `String`: Sequence of characters (e.g., `"Hello, World!"`).
  - `boolean`: Represents `true` or `false`.

- **Operators**:
  - Arithmetic: `+`, `-`, `*`, `/`, `%`
  - Relational: `==`, `!=`, `<`, `>`, `<=`, `>=`
  - Logical: `&&` (AND), `||` (OR), `!` (NOT)

- **Control Structures**:
  - **Conditional Statements**:
    ```java
    if (condition) {
        // code if condition is true
    } else {
        // code if condition is false
    }
    ```

  - **Switch Statement**:
    ```java
    switch (expression) {
        case value1:
            // code
            break;
        case value2:
            // code
            break;
        default:
            // default code
    }
    ```

  - **Loops**:
    - **For Loop**:
      ```java
      for (int i = 0; i < 10; i++) {
          // code to execute
      }
      ```
    - **While Loop**:
      ```java
      while (condition) {
          // code to execute
      }
      ```
    - **Do-While Loop**:
      ```java
      do {
          // code to execute
      } while (condition);
      ```

## Intermediate

- **Methods**: Blocks of code that perform a specific task.
    ```java
    public returnType methodName(parameterType parameter) {
        // code
        return value; // optional
    }
    ```

- **Arrays**: Used to store multiple values in a single variable.
    ```java
    int[] numbers = {1, 2, 3, 4, 5}; // Array declaration and initialization
    ```

- **Strings**: Immutable sequences of characters.
    ```java
    String text = "Hello";
    int length = text.length(); // Get length of the string
    String upper = text.toUpperCase(); // Convert to uppercase
    ```

- **Classes and Objects**: 
    - **Class Definition**:
      ```java
      class ClassName {
          // Attributes
          int attribute;

          // Method
          void methodName() {
              // code
          }
      }
      ```

    - **Creating an Object**:
      ```java
      ClassName obj = new ClassName(); // Create an instance
      obj.methodName(); // Call a method
      ```

## Advanced

- **Inheritance**: Mechanism to create a new class based on an existing class.
    ```java
    class ParentClass {
        // Parent class code
    }

    class ChildClass extends ParentClass {
        // Child class code
    }
    ```

- **Interfaces**: Define methods that a class must implement.
    ```java
    interface MyInterface {
        void method(); // No body
    }

    class MyClass implements MyInterface {
        public void method() {
            // Implementation
        }
    }
    ```

- **Abstract Classes**: Classes that cannot be instantiated and may contain abstract methods.
    ```java
    abstract class AbstractClass {
        abstract void abstractMethod(); // Abstract method
    }
    ```

- **Exception Handling**: Mechanism to handle runtime errors using `try...catch`.
    ```java
    try {
        // Code that may throw an exception
    } catch (ExceptionType e) {
        // Handling exception
    } finally {
        // Code that always executes
    }
    ```

- **Collections Framework**: Interfaces and classes for working with groups of objects.
    - **List**:
      ```java
      import java.util.ArrayList;

      ArrayList<String> list = new ArrayList<>();
      list.add("Element 1");
      list.add("Element 2");
      ```

    - **Map**:
      ```java
      import java.util.HashMap;

      HashMap<Integer, String> map = new HashMap<>();
      map.put(1, "Value 1");
      map.put(2, "Value 2");
      ```

- **Streams**: Used to process sequences of elements (available in Java 8 and above).
    ```java
    import java.util.stream.Stream;

    Stream<String> stream = Stream.of("A", "B", "C");
    stream.forEach(System.out::println); // Prints each element
    ```

- **Lambda Expressions**: A concise way to express instances of single-method interfaces (functional interfaces).
    ```java
    (parameters) -> expression; // e.g., (x, y) -> x + y
    ```

- **Multithreading**: Running multiple threads concurrently.
    ```java
    class MyThread extends Thread {
        public void run() {
            // Code to execute
        }

        public static void main(String[] args) {
            MyThread t1 = new MyThread();
            t1.start(); // Start the thread
        }
    }
    ```
