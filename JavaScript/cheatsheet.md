# JavaScript Cheatsheet

## Basics

- **Variables**: Used to store data values.
  - `let variableName = value;` (Block-scoped variable)
  - `const constantName = value;` (Block-scoped constant, cannot be reassigned)
  - `var variableName = value;` (Function-scoped variable, can be re-declared)

- **Data Types**:
  - `string`: Represents text (e.g., `"Hello, World!"`).
  - `number`: Represents numeric values (e.g., `42`, `3.14`).
  - `boolean`: Represents logical values (`true` or `false`).
  - `null`: Represents an intentional absence of value.
  - `undefined`: Indicates a variable has been declared but not assigned.
  - `symbol`: Unique and immutable value.
  - `object`: Complex data structure for collections of data.

- **Functions**: Blocks of code designed to perform a particular task.
  - Regular function:
    ```javascript
    function functionName(parameters) {
        // code to be executed
    }
    ```
  - Arrow function (shorter syntax):
    ```javascript
    const functionName = (parameters) => {
        // code to be executed
    };
    ```

## Intermediate

- **Array Methods**: Powerful built-in methods for manipulating arrays.
  - **map**: Transforms each element in the array and returns a new array.
    ```javascript
    const doubled = array.map(element => element * 2);
    ```
  - **filter**: Creates a new array with all elements that pass the test implemented by the provided function.
    ```javascript
    const filteredArray = array.filter(element => element > 10);
    ```
  - **reduce**: Executes a reducer function on each element of the array, resulting in a single output value.
    ```javascript
    const total = array.reduce((accumulator, current) => accumulator + current, 0);
    ```

- **Promises**: Used for asynchronous operations, representing a value that may be available now, or in the future, or never.
  - Creating a Promise:
    ```javascript
    const promise = new Promise((resolve, reject) => {
        // asynchronous operation
        if (successful) {
            resolve(value); // Resolve promise with a value
        } else {
            reject(error); // Reject promise with an error
        }
    });
    ```

- **Template Literals**: For multi-line strings and string interpolation.
    ```javascript
    const name = "John";
    const greeting = `Hello, ${name}!`; // "Hello, John!"
    ```

## Advanced

- **Async/Await**: A way to work with promises that makes asynchronous code look synchronous.
    ```javascript
    async function fetchData() {
        try {
            const response = await fetch('url');
            const data = await response.json();
            return data;
        } catch (error) {
            console.error('Error fetching data:', error);
        }
    }
    ```

- **Closures**: Functions that have access to the parent scope, even after the parent function has closed.
    ```javascript
    function outerFunction() {
        let outerVariable = 'I am from outer scope';
        return function innerFunction() {
            console.log(outerVariable);
        };
    }
    const closureFunction = outerFunction();
    closureFunction(); // Outputs: I am from outer scope
    ```

- **Modules**: A way to separate your code into manageable pieces.
    - **Exporting**:
      ```javascript
      export const myFunction = () => { /* code */ };
      ```
    - **Importing**:
      ```javascript
      import { myFunction } from './myModule.js';
      ```

- **Error Handling**: Using `try...catch` to handle exceptions gracefully.
    ```javascript
    try {
        // Code that may throw an error
    } catch (error) {
        console.error('Error occurred:', error);
    }
    ```

- **Event Handling**: Responding to user interactions.
    ```javascript
    document.getElementById('button').addEventListener('click', function() {
        alert('Button clicked!');
    });
    ```

