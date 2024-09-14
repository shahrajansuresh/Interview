Certainly! Here’s a comprehensive list of over 200 JavaScript interview questions, ranging from basic to advanced, with answers included.

### Basic Questions

1. **What is JavaScript?**
   - **Answer:** JavaScript is a high-level, interpreted programming language primarily used to create dynamic and interactive effects on web pages. It is a core technology of the World Wide Web, alongside HTML and CSS.

2. **What are variables in JavaScript?**
   - **Answer:** Variables are containers for storing data values. In JavaScript, variables are declared using `var`, `let`, or `const`.

3. **What is the difference between `var`, `let`, and `const`?**
   - **Answer:** 
     - **`var`**: Function-scoped or globally-scoped, can be re-declared and updated.
     - **`let`**: Block-scoped, can be updated but not re-declared in the same scope.
     - **`const`**: Block-scoped, cannot be updated or re-declared, but objects and arrays declared with `const` can still be modified.

4. **What is a data type in JavaScript?**
   - **Answer:** Data types specify the kind of data a variable can hold. JavaScript has primitive types (string, number, boolean, null, undefined, symbol, bigint) and non-primitive types (object, array, function).

5. **What are the different data types in JavaScript?**
   - **Answer:** 
     - Primitive: `string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`.
     - Non-primitive: `object` (including arrays and functions).

6. **What is a function in JavaScript?**
   - **Answer:** A function is a block of code designed to perform a particular task. It is executed when it is invoked or called.

7. **How do you declare a function in JavaScript?**
   - **Answer:** Functions can be declared using function declarations, function expressions, or arrow functions:
     - **Function Declaration:**
       ```javascript
       function myFunction() {
         // code
       }
       ```
     - **Function Expression:**
       ```javascript
       const myFunction = function() {
         // code
       }
       ```
     - **Arrow Function:**
       ```javascript
       const myFunction = () => {
         // code
       }
       ```

8. **What is a callback function in JavaScript?**
   - **Answer:** A callback function is a function passed as an argument to another function, which is then executed inside that function.

9. **What is a promise in JavaScript?**
   - **Answer:** A promise is an object representing the eventual completion or failure of an asynchronous operation and its resulting value.

10. **What is async/await?**
    - **Answer:** `async/await` is a syntax for working with promises that allows writing asynchronous code in a more synchronous style. `async` functions always return a promise, and `await` pauses the execution of an `async` function until the promise is resolved.

11. **What are template literals in JavaScript?**
    - **Answer:** Template literals are string literals allowing embedded expressions. They are enclosed by backticks (`` ` ``) and can contain placeholders marked by the dollar sign and curly braces (`${expression}`).

12. **What is the difference between `==` and `===` in JavaScript?**
    - **Answer:** 
      - `==` (loose equality) compares values for equality after converting both values to the same type.
      - `===` (strict equality) compares values for equality without type conversion.

13. **What is the `typeof` operator used for in JavaScript?**
    - **Answer:** The `typeof` operator returns a string indicating the type of the unevaluated operand.

14. **What is an object in JavaScript?**
    - **Answer:** An object is a collection of key-value pairs where keys are strings (or Symbols) and values can be any data type. Objects are used to store collections of data and more complex entities.

15. **How do you create an object in JavaScript?**
    - **Answer:** Objects can be created using object literals, constructors, or `Object.create()`:
      - **Object Literal:**
        ```javascript
        const obj = { key: 'value' };
        ```
      - **Constructor:**
        ```javascript
        const obj = new Object();
        obj.key = 'value';
        ```
      - **Object.create():**
        ```javascript
        const obj = Object.create(null);
        obj.key = 'value';
        ```

16. **What is an array in JavaScript?**
    - **Answer:** An array is an ordered collection of items where each item can be accessed by its index. Arrays are objects with integer keys.

17. **How do you create an array in JavaScript?**
    - **Answer:** Arrays can be created using array literals or the `Array` constructor:
      - **Array Literal:**
        ```javascript
        const arr = [1, 2, 3];
        ```
      - **Array Constructor:**
        ```javascript
        const arr = new Array(1, 2, 3);
        ```

18. **What is a higher-order function in JavaScript?**
    - **Answer:** A higher-order function is a function that takes another function as an argument or returns a function as a result.

19. **What are arrow functions and how do they differ from traditional functions?**
    - **Answer:** Arrow functions provide a shorter syntax for writing functions and do not have their own `this`, `arguments`, `super`, or `new.target`. They are often used for short functions or callbacks.

20. **What is event delegation in JavaScript?**
    - **Answer:** Event delegation is a technique where a single event listener is attached to a parent element to handle events for multiple child elements. This improves performance and reduces memory usage.

### Intermediate Questions

21. **What is closure in JavaScript?**
    - **Answer:** A closure is a feature where an inner function retains access to the outer function’s variables even after the outer function has finished execution.

22. **What is the event loop in JavaScript?**
    - **Answer:** The event loop is a mechanism that allows JavaScript to perform non-blocking operations by using a single thread to handle asynchronous tasks. It continuously checks the message queue and executes pending tasks.

23. **What is the difference between synchronous and asynchronous code?**
    - **Answer:** Synchronous code is executed sequentially, blocking the execution of subsequent code until the current operation completes. Asynchronous code allows other code to run while waiting for a long-running task to complete.

24. **What is the `this` keyword in JavaScript?**
    - **Answer:** `this` refers to the object from which a function is called. Its value depends on the context in which it is used (global object, object method, constructor function, etc.).

25. **How do you bind `this` in JavaScript?**
    - **Answer:** You can bind `this` using methods like `.bind()`, `.call()`, or `.apply()`. `.bind()` creates a new function with a specified `this` value, while `.call()` and `.apply()` call a function with a specified `this` value immediately.

26. **What is the prototype chain in JavaScript?**
    - **Answer:** The prototype chain is a mechanism for inheritance in JavaScript. Objects inherit properties and methods from their prototype, and this chain continues up to `Object.prototype`.

27. **What is the `prototype` property of a constructor function?**
    - **Answer:** The `prototype` property is an object that is used to attach properties and methods that should be inherited by instances created by the constructor function.

28. **How do you handle errors in JavaScript?**
    - **Answer:** Errors can be handled using `try...catch` blocks. The `try` block contains code that may throw an error, and the `catch` block contains code to handle the error.

29. **What is the `arguments` object in JavaScript?**
    - **Answer:** The `arguments` object is an array-like object available within all non-arrow functions that contains the arguments passed to the function.

30. **What is the difference between `null` and `undefined` in JavaScript?**
    - **Answer:** 
      - `null` is an explicit value that indicates the absence of any object value.
      - `undefined` indicates that a variable has been declared but has not been assigned a value.

31. **What is an IIFE (Immediately Invoked Function Expression)?**
    - **Answer:** An IIFE is a function that is defined and executed immediately after its creation. It is used to create a local scope and avoid polluting the global scope.
      ```javascript
      (function() {
        // code
      })();
      ```

32. **What is a JavaScript module?**
    - **Answer:** A module is a reusable piece of code that encapsulates related functionality. JavaScript modules allow you to export and import code between different files or modules.

33. **How do you create and use a module in JavaScript?**
    - **Answer:** Use `export` to expose functions or variables from a module, and `import` to bring them into another module.
      - **Export:**
        ```javascript
        export const myFunction = () => { /* code */ };
        ```
      - **Import:**
        ```javascript
        import { myFunction } from './myModule';
        ```

34. **What is the `Object.create()` method in JavaScript?**


    - **Answer:** `Object.create()` creates a new object with the specified prototype object and properties. It allows you to set up inheritance and create objects with a custom prototype.

35. **What is the `bind()` method in JavaScript?**
    - **Answer:** `bind()` creates a new function that, when called, has its `this` keyword set to the provided value and allows you to preset arguments.

36. **What is the `call()` method in JavaScript?**
    - **Answer:** `call()` invokes a function with a specified `this` value and individual arguments provided directly.

37. **What is the `apply()` method in JavaScript?**
    - **Answer:** `apply()` invokes a function with a specified `this` value and arguments provided as an array (or array-like object).

38. **What is a JavaScript event?**
    - **Answer:** An event is an occurrence that the browser or JavaScript engine recognizes and responds to, such as user interactions (clicks, key presses) or browser actions (loading, resizing).

39. **What are event listeners in JavaScript?**
    - **Answer:** Event listeners are functions that are executed when a specified event occurs. They can be added to elements using methods like `addEventListener()`.

40. **How do you remove an event listener in JavaScript?**
    - **Answer:** Remove an event listener using the `removeEventListener()` method. The event listener must be removed using the same function reference that was used to add it.

### Advanced Questions

41. **What is functional programming in JavaScript?**
    - **Answer:** Functional programming is a paradigm where functions are first-class citizens, meaning they can be passed as arguments, returned from other functions, and assigned to variables. It emphasizes immutability, pure functions, and higher-order functions.

42. **What are pure functions?**
    - **Answer:** Pure functions are functions that produce the same output for the same input and have no side effects. They do not modify external state or rely on external variables.

43. **What are higher-order functions in JavaScript?**
    - **Answer:** Higher-order functions are functions that take other functions as arguments or return functions as their results.

44. **What is currying in JavaScript?**
    - **Answer:** Currying is a technique where a function returns another function, and each function takes a single argument. It allows for the creation of partially applied functions.

45. **What is memoization in JavaScript?**
    - **Answer:** Memoization is an optimization technique where function results are cached based on their input arguments to avoid redundant computations and improve performance.

46. **What are closures and how are they used in JavaScript?**
    - **Answer:** Closures are functions that retain access to their lexical scope even after their outer function has finished execution. They are used to create private variables and maintain state.

47. **What is the event delegation pattern?**
    - **Answer:** Event delegation is a technique where a single event listener is attached to a parent element to handle events for multiple child elements. This improves performance and simplifies event management.

48. **What is prototypal inheritance in JavaScript?**
    - **Answer:** Prototypal inheritance is a feature where objects can inherit properties and methods from other objects. Each object has a prototype, and the prototype chain determines the inheritance hierarchy.

49. **What is the `Object.defineProperty()` method used for?**
    - **Answer:** `Object.defineProperty()` is used to define new properties or modify existing properties on an object with specific descriptors, such as `enumerable`, `configurable`, and `writable`.

50. **What is the difference between `Object.keys()` and `Object.values()`?**
    - **Answer:** 
      - `Object.keys()` returns an array of the object's own enumerable property names.
      - `Object.values()` returns an array of the object's own enumerable property values.

51. **What are symbols in JavaScript and how are they used?**
    - **Answer:** Symbols are a primitive data type introduced in ES6. They are unique and immutable identifiers used to create unique property keys for objects, avoiding property name collisions.

52. **What is a generator function in JavaScript?**
    - **Answer:** A generator function is a function that can be paused and resumed, allowing you to produce a sequence of values over time. It is defined using the `function*` syntax and yields values with the `yield` keyword.

53. **What are `Set` and `Map` in JavaScript?**
    - **Answer:** 
      - **`Set`**: A collection of unique values, where each value can only appear once.
      - **`Map`**: A collection of key-value pairs where keys can be of any type, and values are stored in the order they were added.

54. **What is the `WeakMap` and `WeakSet` in JavaScript?**
    - **Answer:** 
      - **`WeakMap`**: A collection of key-value pairs where keys are objects and values are arbitrary values. Keys are weakly referenced, meaning they do not prevent garbage collection.
      - **`WeakSet`**: A collection of objects where each object can appear only once, and objects are weakly referenced.

55. **What is `Object.assign()` and how is it used?**
    - **Answer:** `Object.assign()` is used to copy the values of all enumerable properties from one or more source objects to a target object. It is commonly used for object merging and cloning.

56. **What are `async` functions and how do they work?**
    - **Answer:** `async` functions are functions that always return a promise. Inside an `async` function, you can use the `await` keyword to wait for promises to resolve, making asynchronous code easier to read and write.

57. **What is the difference between `await` and `then()` for handling promises?**
    - **Answer:** 
      - `await` pauses the execution of an `async` function until the promise is resolved or rejected.
      - `.then()` is a method on the promise object used to handle the resolution or rejection of the promise.

58. **What is the purpose of the `catch` block in JavaScript promises?**
    - **Answer:** The `catch` block is used to handle errors that occur during the execution of a promise. It catches any rejection or exception and allows for proper error handling.

59. **How do you implement a debounce function in JavaScript?**
    - **Answer:** A debounce function limits the rate at which a function can be executed. It delays the execution until a certain amount of time has passed since the last invocation.
      ```javascript
      function debounce(func, wait) {
        let timeout;
        return function(...args) {
          clearTimeout(timeout);
          timeout = setTimeout(() => func.apply(this, args), wait);
        };
      }
      ```

60. **What is a throttling function in JavaScript and how is it different from debouncing?**
    - **Answer:** Throttling ensures a function is executed at most once in a specified period, while debouncing delays the execution until a specified time has passed since the last invocation. Throttling is useful for rate-limiting operations like scrolling or resizing.

61. **What is the `Reflect` API in JavaScript?**
    - **Answer:** The `Reflect` API is a built-in object that provides methods for interceptable JavaScript operations, such as property access, function invocation, and object manipulation. It is used in custom behavior for objects and proxies.

62. **What is a Proxy object in JavaScript?**
    - **Answer:** A Proxy object allows you to create a handler for another object, intercepting and customizing fundamental operations (e.g., property access, assignment) on the target object.

63. **How do you implement a custom iterator in JavaScript?**
    - **Answer:** Implement a custom iterator by defining a `Symbol.iterator` method on an object, which returns an iterator object with a `next` method.
      ```javascript
      const myIterable = {
        [Symbol.iterator]() {
          let i = 0;
          return {
            next() {
              return i < 3 ? { value: i++, done: false } : { done: true };
            }
          };
        }
      };
      ```

64. **What are JavaScript decorators and how are they used?**
    - **Answer:** Decorators are a proposal for a syntax to modify or annotate classes and class members. They are applied as annotations before the class or method definition and can be used to add metadata or modify behavior.

65. **What is the purpose of the `Proxy` object and how do you use it?**
    - **Answer:** The `Proxy` object is used to define custom behavior for fundamental operations (e.g., property lookup, assignment) on an object. It allows for creating objects with custom behavior for operations like validation, property access, and more.
      ```javascript
      const handler = {
        get(target, prop, receiver) {
          console.log(`Getting ${prop}`);
          return Reflect.get(...arguments);
        }
      };
      const proxy = new Proxy({}, handler);
      proxy.name; // Logs: Getting name
      ```

66. **What are the new features introduced in ES6?**
    - **Answer:** ES6 (ECMAScript 2015) introduced several new features including:
      - Let and const
      - Arrow functions
      - Template literals
      - Classes
      - Destructuring assignment
      - Default parameters
      - Rest and spread operators
      - Promises
      - Modules (import/export)
      - Enhanced object literals
      - Symbols
      - Iterators and generators



67. **What are `WeakRef` and `FinalizationRegistry` in JavaScript?**
    - **Answer:** 
      - **`WeakRef`**: A weak reference to an object that does not prevent garbage collection. Useful for memory-sensitive operations.
      - **`FinalizationRegistry`**: Provides a way to register callbacks that will be invoked when objects are garbage collected.

68. **How does JavaScript handle memory management and garbage collection?**
    - **Answer:** JavaScript uses automatic garbage collection to manage memory. The garbage collector reclaims memory used by objects that are no longer reachable or referenced, using algorithms like mark-and-sweep.

69. **What are some common performance optimization techniques in JavaScript?**
    - **Answer:** Common techniques include:
      - Minimizing DOM manipulations and reflows
      - Debouncing and throttling events
      - Using efficient algorithms and data structures
      - Optimizing rendering and avoiding memory leaks
      - Leveraging web workers for off-main-thread tasks

70. **What are JavaScript’s asynchronous patterns?**
    - **Answer:** Asynchronous patterns include:
      - Callbacks
      - Promises
      - `async/await`
      - Observables (in libraries like RxJS)

71. **What is the `async` and `await` syntax used for?**
    - **Answer:** The `async` and `await` syntax is used for writing asynchronous code in a more synchronous style. `async` functions return a promise, and `await` pauses the execution until the promise is resolved.

72. **What is destructuring assignment in JavaScript?**
    - **Answer:** Destructuring assignment allows you to unpack values from arrays or properties from objects into distinct variables.
      ```javascript
      const [a, b] = [1, 2];
      const {x, y} = {x: 10, y: 20};
      ```

73. **What is the purpose of `Array.prototype.reduce()`?**
    - **Answer:** `reduce()` is used to apply a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.

74. **What is a `Map` and how does it differ from an `Object`?**
    - **Answer:** 
      - **`Map`**: A collection of key-value pairs where keys can be any data type and entries are ordered by insertion.
      - **`Object`**: A collection of key-value pairs where keys are strings or symbols, and properties are unordered.

75. **What is the `Set` object in JavaScript?**
    - **Answer:** `Set` is a collection of unique values. It allows values to be stored without duplication and provides methods to check for existence, add, and delete values.

76. **How do you handle asynchronous operations in JavaScript?**
    - **Answer:** Handle asynchronous operations using:
      - Callbacks
      - Promises
      - `async/await`

77. **What is a closure and how does it work in JavaScript?**
    - **Answer:** A closure is a function that retains access to its lexical scope even after its outer function has finished execution. It allows for encapsulation and data hiding.

78. **How does JavaScript handle scope and context?**
    - **Answer:** 
      - **Scope**: Determines the accessibility of variables and functions. JavaScript has global scope and function scope (and block scope with `let` and `const`).
      - **Context**: Refers to the `this` value inside a function, which is determined by how the function is called.

79. **What are `Object.entries()` and `Object.fromEntries()` methods?**
    - **Answer:** 
      - **`Object.entries()`**: Returns an array of a given object’s own enumerable string-keyed property [key, value] pairs.
      - **`Object.fromEntries()`**: Transforms a list of key-value pairs into an object.

80. **What is the `Reflect` API and how is it used in JavaScript?**
    - **Answer:** The `Reflect` API provides methods for interceptable JavaScript operations. It is used to perform operations like getting and setting properties, invoking functions, and handling prototypes.

81. **What are the benefits of using `let` and `const` over `var`?**
    - **Answer:** 
      - **`let`**: Provides block scope and prevents redeclaration in the same scope.
      - **`const`**: Also provides block scope and prevents reassignment of variables, although the values of objects and arrays can still be modified.

82. **How do you create a promise in JavaScript and what are its states?**
    - **Answer:** Create a promise using the `Promise` constructor, passing in a function with `resolve` and `reject` parameters. A promise can be in one of three states: pending, fulfilled, or rejected.
      ```javascript
      const myPromise = new Promise((resolve, reject) => {
        // asynchronous code
      });
      ```

83. **What is the `fetch` API and how is it used?**
    - **Answer:** The `fetch` API is used to make HTTP requests. It returns a promise that resolves to the `Response` object representing the response to the request.
      ```javascript
      fetch('https://api.example.com/data')
        .then(response => response.json())
        .then(data => console.log(data))
        .catch(error => console.error('Error:', error));
      ```

84. **What is the difference between `Object.freeze()` and `Object.seal()`?**
    - **Answer:** 
      - **`Object.freeze()`**: Prevents new properties from being added to an object and marks all existing properties as read-only.
      - **`Object.seal()`**: Prevents new properties from being added and marks all existing properties as non-configurable, but properties can still be modified.

85. **What is a `Symbol` in JavaScript and what are its uses?**
    - **Answer:** A `Symbol` is a unique and immutable primitive data type used primarily as property keys in objects to avoid name collisions.

86. **What are `Map` and `Set` objects and how do they differ?**
    - **Answer:** 
      - **`Map`**: A collection of key-value pairs where keys can be of any type and entries are ordered by insertion.
      - **`Set`**: A collection of unique values, where each value can only appear once and is stored in insertion order.

87. **What is a `WeakMap` and when would you use it?**
    - **Answer:** A `WeakMap` is a collection of key-value pairs where keys are objects and are weakly referenced. It is used for storing private data or metadata associated with objects without preventing garbage collection.

88. **What is a `WeakSet` and when would you use it?**
    - **Answer:** A `WeakSet` is a collection of objects where each object can appear only once and is weakly referenced. It is useful for storing objects without preventing garbage collection.

89. **What are `Array.prototype.map()` and `Array.prototype.filter()` used for?**
    - **Answer:** 
      - **`map()`**: Creates a new array populated with the results of calling a provided function on every element in the calling array.
      - **`filter()`**: Creates a new array with all elements that pass the test implemented by the provided function.

90. **What is the difference between `Array.prototype.forEach()` and `Array.prototype.map()`?**
    - **Answer:** 
      - **`forEach()`**: Executes a provided function once for each array element and does not return a new array.
      - **`map()`**: Executes a provided function once for each array element and returns a new array with the results.

91. **What is the `Promise.all()` method?**
    - **Answer:** `Promise.all()` takes an iterable of promises and, when all of the promises have resolved, returns a single promise that resolves with an array of the resolved values. If any promise is rejected, it returns a promise that is rejected with the reason from the first promise that was rejected.

92. **What is the `Promise.race()` method?**
    - **Answer:** `Promise.race()` returns a promise that resolves or rejects as soon as one of the promises in the iterable resolves or rejects, with the value or reason from that promise.

93. **What is the `Promise.allSettled()` method?**
    - **Answer:** `Promise.allSettled()` takes an iterable of promises and returns a promise that resolves after all of the given promises have either resolved or rejected, with an array of objects describing the outcome of each promise.

94. **What is a JavaScript generator function?**
    - **Answer:** A generator function is defined using the `function*` syntax and can yield multiple values over time. It allows iteration over sequences of values and can be paused and resumed.
      ```javascript
      function* myGenerator() {
        yield 1;
        yield 2;
        yield 3;
      }
      ```

95. **How do you use a generator function?**
    - **Answer:** Create an instance of a generator function and use its `next()` method to get values:
      ```javascript
      const gen = myGenerator();
      console.log(gen.next().value); // 1
      console.log(gen.next().value); // 2
      console.log(gen.next().value); // 3
      ```

96. **What is the `Symbol.iterator` property?**
    - **Answer:** `Symbol.iterator` is a well-known

 symbol that is used to define an iterator for an object, enabling the object to be iterable using constructs like `for...of` loops.

97. **How do you use `Array.prototype.reduce()` method?**
    - **Answer:** `reduce()` applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value. It can be used to perform operations like summing values, flattening arrays, or building objects.
      ```javascript
      const sum = [1, 2, 3].reduce((acc, val) => acc + val, 0);
      ```

98. **What is the purpose of the `Object.create()` method?**
    - **Answer:** `Object.create()` creates a new object with the specified prototype object and properties, allowing for inheritance and object creation with a custom prototype.

99. **What is the `Object.keys()` method?**
    - **Answer:** `Object.keys()` returns an array of a given object's own enumerable property names.

100. **What is the `Object.values()` method?**
    - **Answer:** `Object.values()` returns an array of a given object's own enumerable property values.
    
101. **What is the `Object.entries()` method used for?**
   - **Answer:** `Object.entries()` returns an array of a given object's own enumerable string-keyed property `[key, value]` pairs.

102. **What is the difference between `Object.assign()` and the spread operator (`{...obj}`)?**
   - **Answer:** 
     - **`Object.assign()`**: Copies properties from one or more source objects to a target object. It performs a shallow copy.
     - **Spread operator**: Also performs a shallow copy, but it can be used to create a new object by spreading properties of existing objects into it.

103. **What is the purpose of the `Array.prototype.find()` method?**
   - **Answer:** `find()` returns the first element in the array that satisfies the provided testing function. It returns `undefined` if no elements match.

104. **What is the difference between `Array.prototype.some()` and `Array.prototype.every()`?**
   - **Answer:** 
     - **`some()`**: Returns `true` if at least one element in the array satisfies the provided testing function.
     - **`every()`**: Returns `true` if all elements in the array satisfy the provided testing function.

105. **What are template literals in JavaScript?**
   - **Answer:** Template literals are string literals that allow embedded expressions. They are enclosed by backticks (`` ` ``) and support multi-line strings and variable interpolation using `${}`.
     ```javascript
     const name = 'World';
     const greeting = `Hello, ${name}!`;
     ```

106. **What is the purpose of `Array.prototype.slice()`?**
   - **Answer:** `slice()` returns a shallow copy of a portion of an array into a new array object, selected from start to end (end not included) without modifying the original array.

107. **What is the `Array.prototype.splice()` method used for?**
   - **Answer:** `splice()` changes the contents of an array by removing or replacing existing elements and/or adding new elements in place. It modifies the original array.

108. **What is the difference between `splice()` and `slice()`?**
   - **Answer:** 
     - **`splice()`**: Modifies the original array and can add or remove elements.
     - **`slice()`**: Returns a new array with selected elements from the original array, without modifying the original array.

109. **How does JavaScript's `this` keyword work in functions?**
   - **Answer:** `this` refers to the object that is executing the current function. Its value is determined by how the function is called (global object, object method, constructor, or `bind`, `call`, `apply`).

110. **What are arrow functions, and how do they differ from regular functions?**
    - **Answer:** Arrow functions are a shorthand syntax for writing functions. They do not have their own `this` context; instead, they inherit `this` from the surrounding lexical scope.
      ```javascript
      const add = (a, b) => a + b;
      ```

111. **What is a promise and how does it work?**
    - **Answer:** A promise is an object representing the eventual completion or failure of an asynchronous operation. It has three states: pending, fulfilled, and rejected. Promises have methods like `then()`, `catch()`, and `finally()` for handling results or errors.

112. **What is a "polyfill" in JavaScript?**
    - **Answer:** A polyfill is a piece of code (usually JavaScript) used to provide modern functionality on older browsers that do not natively support it.

113. **What is the `Object.preventExtensions()` method?**
    - **Answer:** `Object.preventExtensions()` prevents new properties from being added to an object. Existing properties can still be modified or deleted, but no new properties can be added.

114. **What is the `Object.seal()` method?**
    - **Answer:** `Object.seal()` prevents new properties from being added to an object and marks all existing properties as non-configurable. Existing properties can still be modified.

115. **What is `Object.freeze()` used for?**
    - **Answer:** `Object.freeze()` prevents modifications to existing properties and disallows the addition or removal of properties. It makes an object immutable.

116. **What is the `Array.prototype.concat()` method?**
    - **Answer:** `concat()` is used to merge two or more arrays into a single array. It does not change the existing arrays but returns a new array.

117. **How does the `Array.prototype.flat()` method work?**
    - **Answer:** `flat()` creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.

118. **What is the `Array.prototype.flatMap()` method?**
    - **Answer:** `flatMap()` first maps each element using a mapping function and then flattens the result into a new array.

119. **What are JavaScript's `new` and `constructor` keywords used for?**
    - **Answer:** 
      - **`new`**: Creates a new instance of an object type.
      - **`constructor`**: A special method for initializing new objects created by a class or function.

120. **What is the `Array.prototype.reduceRight()` method?**
    - **Answer:** `reduceRight()` is similar to `reduce()`, but it processes the array from right to left, starting from the last element.

121. **What is the purpose of `Object.getOwnPropertyDescriptor()`?**
    - **Answer:** `Object.getOwnPropertyDescriptor()` returns a property descriptor for a specific property of an object, providing details like value, writability, and enumerability.

122. **How do you handle exceptions in JavaScript?**
    - **Answer:** Exceptions are handled using `try`, `catch`, `finally`, and `throw`. The `catch` block catches exceptions thrown in the `try` block, and `finally` executes code after `try` and `catch`, regardless of the outcome.

123. **What is `setTimeout()` and how is it used?**
    - **Answer:** `setTimeout()` schedules a function to be executed after a specified delay (in milliseconds). It returns a timeout ID that can be used to cancel the timeout with `clearTimeout()`.

124. **What is `setInterval()` and how does it differ from `setTimeout()`?**
    - **Answer:** `setInterval()` schedules a function to be executed repeatedly at specified intervals. Unlike `setTimeout()`, which runs the function only once after a delay, `setInterval()` repeats the execution.

125. **What is `clearTimeout()` and `clearInterval()` used for?**
    - **Answer:** `clearTimeout()` and `clearInterval()` are used to cancel the timeout or interval set by `setTimeout()` and `setInterval()`, respectively.

126. **What is the `with` statement in JavaScript and why should it be avoided?**
    - **Answer:** The `with` statement extends the scope chain for a statement, making it harder to understand and debug. It is considered bad practice and is deprecated in strict mode.

127. **What is the `delete` operator used for?**
    - **Answer:** The `delete` operator removes a property from an object. It returns `true` if the property was successfully deleted, or `false` if the property could not be deleted.

128. **What are the differences between `null` and `undefined` in JavaScript?**
    - **Answer:** 
      - **`null`**: Represents an intentional absence of any object value.
      - **`undefined`**: Indicates that a variable has been declared but not assigned a value.

129. **What is the `typeof` operator used for?**
    - **Answer:** `typeof` returns a string indicating the type of the unevaluated operand, such as `"number"`, `"string"`, `"boolean"`, `"object"`, `"undefined"`, or `"function"`.

130. **What is the `instanceof` operator in JavaScript?**
    - **Answer:** `instanceof` tests whether an object is an instance of a specific constructor function or class, checking the prototype chain.

131. **What is the difference between `==` and `===` in JavaScript?**
    - **Answer:** 
      - **`==`**: Equality operator that performs type coercion before comparison.
      - **`===`**: Strict equality operator that compares both value and type without type coercion.

132. **What are JavaScript’s "truthy" and "falsy" values?**
    - **Answer:** "Truthy" values are values that are considered true in a Boolean context, while "falsy" values are considered false. Common falsy values include `0`, `""`, `null`, `undefined`, `NaN`, and `false`.

133. **What is the `eval()` function and why should it be avoided?**
    - **Answer:** `eval()` executes a string of JavaScript code. It should be avoided due to security risks and performance issues as it can execute arbitrary code.

134. **What is a “callback” function in JavaScript?**
    - **Answer:** A callback function is a function passed as an argument to another function and is executed after some operation has been completed.

135. **What is the `Function.prototype.bind()` method used for?**
    - **Answer:** `bind()` creates a new function that, when called, has its `this` keyword set to the provided value and can have preset arguments.

136

. **How do you handle errors in asynchronous code?**
    - **Answer:** Errors in asynchronous code can be handled using:
      - `try/catch` blocks with `async/await`
      - `.catch()` method with Promises
      - Error handling in callback functions

137. **What is the `import` and `export` syntax in JavaScript modules?**
    - **Answer:** 
      - **`import`**: Used to import functions, objects, or primitives from other modules.
      - **`export`**: Used to expose functions, objects, or primitives from a module so they can be imported into other modules.
      ```javascript
      // Export
      export const myFunction = () => {};
      
      // Import
      import { myFunction } from './myModule';
      ```

138. **What are JavaScript modules and how do they work?**
    - **Answer:** JavaScript modules allow for the organization and encapsulation of code. Modules can export variables, functions, or classes, and other modules can import these exports.

139. **What is `require` in Node.js and how does it differ from `import`?**
    - **Answer:** `require` is used in Node.js for importing modules, while `import` is used in ECMAScript modules. `require` is synchronous and is a part of CommonJS, whereas `import` is asynchronous and part of ES6 modules.

140. **What is the `prototype` chain in JavaScript?**
    - **Answer:** The prototype chain is a mechanism for object inheritance in JavaScript. Objects inherit properties and methods from their prototype, forming a chain of prototypes up to `Object.prototype`.

141. **What is the difference between `Object.create(null)` and `{}`?**
    - **Answer:** 
      - **`Object.create(null)`**: Creates an object with no prototype, meaning it does not inherit any properties from `Object.prototype`.
      - **`{}`**: Creates an object with `Object.prototype` as its prototype, inheriting properties and methods from it.

142. **What is the `Reflect` object in JavaScript?**
    - **Answer:** `Reflect` is a built-in object that provides methods for interceptable JavaScript operations, such as getting and setting properties, invoking functions, and handling prototypes.

143. **What is `Proxy` in JavaScript and how is it used?**
    - **Answer:** `Proxy` is an object that wraps another object or function and intercepts operations such as property access, assignment, and function calls. It allows for custom behavior for fundamental operations.

144. **What are JavaScript iterators and iterables?**
    - **Answer:** 
      - **Iterator**: An object that defines a `next()` method returning an object with `value` and `done` properties.
      - **Iterable**: An object that defines a `Symbol.iterator` method returning an iterator.

145. **What is `Promise.allSettled()` and how is it used?**
    - **Answer:** `Promise.allSettled()` returns a promise that resolves after all of the given promises have either resolved or rejected, with an array of objects describing the outcome of each promise.

146. **How does the `for...in` loop differ from the `for...of` loop?**
    - **Answer:** 
      - **`for...in`**: Iterates over enumerable properties of an object, including inherited properties.
      - **`for...of`**: Iterates over iterable objects like arrays, strings, or collections, and does not include inherited properties.

147. **What are the benefits of using `const` over `let` and `var`?**
    - **Answer:** 
      - **`const`**: Ensures that the variable’s reference cannot be reassigned. It enforces immutability of the binding, though the object’s content can still be modified.
      - **`let` and `var`**: Do not provide this level of protection.

148. **What is the `Array.prototype.sort()` method?**
    - **Answer:** `sort()` sorts the elements of an array in place and returns the array. The sort order can be customized using a compare function.

149. **How do you define a class in JavaScript, and what is the purpose?**
    - **Answer:** Classes are defined using the `class` keyword and are syntactic sugar over JavaScript’s existing prototype-based inheritance. They provide a clearer, more intuitive syntax for creating objects and handling inheritance.
      ```javascript
      class Person {
        constructor(name) {
          this.name = name;
        }
        
        greet() {
          console.log(`Hello, ${this.name}!`);
        }
      }
      ```

150. **What are getter and setter methods in JavaScript classes?**
    - **Answer:** Getters and setters are methods that get or set the value of an object's property. They allow you to define custom behavior for property access and modification.
      ```javascript
      class Person {
        constructor(name) {
          this._name = name;
        }
        
        get name() {
          return this._name;
        }
        
        set name(value) {
          this._name = value;
        }
      }
      ```

151. **What is the purpose of the `super` keyword in JavaScript classes?**
    - **Answer:** `super` is used to call methods or constructors from a parent class. It allows for inheriting and extending functionalities from a base class.
      ```javascript
      class Animal {
        constructor(name) {
          this.name = name;
        }
      }
      
      class Dog extends Animal {
        constructor(name, breed) {
          super(name);
          this.breed = breed;
        }
      }
      ```

152. **What is the `new.target` pseudo-property in JavaScript?**
    - **Answer:** `new.target` is a pseudo-property that refers to the constructor function that was invoked with the `new` keyword. It can be used to determine if a class or function was called with `new`.

153. **What is the `this` context in JavaScript, and how can it be changed?**
    - **Answer:** The `this` context refers to the object that is executing the current function. It can be changed using `bind()`, `call()`, or `apply()` methods, or with arrow functions, which inherit `this` from their lexical scope.

154. **What are "immediately invoked function expressions" (IIFE)?**
    - **Answer:** An IIFE is a function expression that is executed immediately after its creation. It is often used to create a new scope to avoid polluting the global namespace.
      ```javascript
      (function() {
        console.log('I am an IIFE');
      })();
      ```

155. **What is the `globalThis` object in JavaScript?**
    - **Answer:** `globalThis` is a standard object that provides a way to access the global object across different environments (like browsers and Node.js) without needing to check for the global object explicitly.

156. **What is event delegation in JavaScript?**
    - **Answer:** Event delegation involves attaching a single event listener to a parent element to manage events for its child elements. This is done by leveraging event bubbling and can be more efficient than adding listeners to each child element individually.

157. **What is the purpose of `Object.assign()`?**
    - **Answer:** `Object.assign()` copies the values of all enumerable properties from one or more source objects to a target object, which is then returned. It is commonly used for merging objects or creating shallow copies.

158. **What are `try`, `catch`, `finally`, and `throw` used for in error handling?**
    - **Answer:** 
      - **`try`**: Block of code to be tested for errors.
      - **`catch`**: Block of code that handles the error if one occurs in the `try` block.
      - **`finally`**: Block of code that runs after `try` and `catch`, regardless of whether an error occurred.
      - **`throw`**: Used to explicitly throw an error.

159. **What is the `Array.prototype.includes()` method?**
    - **Answer:** `includes()` determines whether an array contains a certain element, returning `true` if it does, and `false` otherwise.

160. **What is the `Array.prototype.indexOf()` method?**
    - **Answer:** `indexOf()` returns the first index at which a given element can be found in the array, or `-1` if it is not present.

161. **What are JavaScript's data types?**
    - **Answer:** JavaScript has primitive data types (`undefined`, `null`, `boolean`, `number`, `bigint`, `string`, `symbol`) and object data types (`Object`, `Array`, `Function`, `Date`, etc.).

162. **What is a "prototype" in JavaScript?**
    - **Answer:** The prototype is an object from which other objects inherit properties and methods. Each JavaScript object has a prototype object from which it can inherit methods and properties.

163. **What is the `Object.getPrototypeOf()` method?**
    - **Answer:** `Object.getPrototypeOf()` returns the prototype (i.e., the internal `[[Prototype]]`) of the specified object.

164. **What is `Object.setPrototypeOf()` used for?**
    - **Answer:** `Object.setPrototypeOf()` sets the prototype (i.e., the internal `[[Prototype]]`) of a specified object.

165. **What is the `Symbol` data type and how is it used?**
    - **Answer:** `Symbol` is a unique and immutable primitive data type

 used as an identifier for object properties. Each symbol value is unique and can be used to avoid property name collisions.
      ```javascript
      const mySymbol = Symbol('description');
      ```

166. **What is the `Object.defineProperty()` method?**
    - **Answer:** `Object.defineProperty()` defines a new property or modifies an existing property on an object, allowing you to control its behavior and attributes like enumerability, writability, and configurability.

167. **What is the `Array.prototype.fill()` method used for?**
    - **Answer:** `fill()` changes all elements in an array to a specified value, from a start index to an end index, and returns the modified array.

168. **What is the `Array.prototype.sort()` method and how can it be used?**
    - **Answer:** `sort()` sorts the elements of an array in place and returns the array. By default, it sorts elements as strings. A compare function can be provided to sort elements according to a custom order.

169. **What is the `Array.prototype.reverse()` method?**
    - **Answer:** `reverse()` reverses the elements of an array in place and returns the array.

170. **What is the `Array.prototype.findIndex()` method?**
    - **Answer:** `findIndex()` returns the index of the first element in the array that satisfies the provided testing function, or `-1` if no element satisfies the function.

171. **What is the `Array.prototype.from()` method?**
    - **Answer:** `Array.from()` creates a new array instance from an array-like or iterable object.

172. **What is `Object.getOwnPropertyNames()` used for?**
    - **Answer:** `Object.getOwnPropertyNames()` returns an array of all properties (including non-enumerable properties) found directly on the specified object.

173. **How do `call` and `apply` methods differ from `bind`?**
    - **Answer:** 
      - **`call()`**: Invokes a function with a specified `this` value and arguments provided individually.
      - **`apply()`**: Similar to `call()`, but arguments are provided as an array.
      - **`bind()`**: Creates a new function that, when called, has its `this` keyword set to the provided value and can have preset arguments.

174. **What is the `Object.is()` method?**
    - **Answer:** `Object.is()` determines whether two values are the same value. It is similar to the strict equality operator (`===`), but handles some edge cases differently (e.g., `NaN` is considered equal to `NaN`).

175. **What is the `Object.entries()` method and how is it used?**
    - **Answer:** `Object.entries()` returns an array of a given object's own enumerable string-keyed property `[key, value]` pairs, which can be used for iteration or transformation.

176. **How does the `Array.prototype.some()` method work?**
    - **Answer:** `some()` tests whether at least one element in the array passes the provided test function and returns `true` if it does, otherwise `false`.

177. **What is the purpose of the `Array.prototype.every()` method?**
    - **Answer:** `every()` tests whether all elements in the array pass the provided test function and returns `true` if they do, otherwise `false`.

178. **What is the `Array.prototype.concat()` method?**
    - **Answer:** `concat()` merges two or more arrays into a new array and does not change the original arrays.

179. **What is the `Array.prototype.join()` method?**
    - **Answer:** `join()` joins all elements of an array into a single string, with elements separated by a specified separator.

180. **What is the `Array.prototype.shift()` method?**
    - **Answer:** `shift()` removes the first element from an array and returns that removed element, changing the length of the array.

181. **What is the `Array.prototype.unshift()` method?**
    - **Answer:** `unshift()` adds one or more elements to the beginning of an array and returns the new length of the array.

182. **What is the `Array.prototype.pop()` method?**
    - **Answer:** `pop()` removes the last element from an array and returns that removed element, changing the length of the array.

183. **What is the `Array.prototype.push()` method?**
    - **Answer:** `push()` adds one or more elements to the end of an array and returns the new length of the array.

184. **What is the `String.prototype.trim()` method?**
    - **Answer:** `trim()` removes whitespace from both ends of a string and returns the new string.

185. **What is the `String.prototype.toLowerCase()` method?**
    - **Answer:** `toLowerCase()` returns a new string with all characters converted to lowercase.

186. **What is the `String.prototype.toUpperCase()` method?**
    - **Answer:** `toUpperCase()` returns a new string with all characters converted to uppercase.

187. **What is the `String.prototype.includes()` method?**
    - **Answer:** `includes()` determines whether a string contains another string, returning `true` if it does, and `false` otherwise.

188. **What is the `String.prototype.indexOf()` method?**
    - **Answer:** `indexOf()` returns the first index at which a given substring can be found in the string, or `-1` if it is not present.

189. **What is the `String.prototype.replace()` method?**
    - **Answer:** `replace()` returns a new string with some or all matches of a pattern replaced by a replacement string or function.

190. **What is the `String.prototype.split()` method?**
    - **Answer:** `split()` splits a string into an array of substrings based on a specified delimiter.

191. **What is the `String.prototype.charAt()` method?**
    - **Answer:** `charAt()` returns the character at a specified index in a string.

192. **What is the `String.prototype.slice()` method?**
    - **Answer:** `slice()` extracts a section of a string and returns it as a new string, without modifying the original string.

193. **What is the `String.prototype.substr()` method?**
    - **Answer:** `substr()` returns a portion of a string specified by a starting index and length.

194. **What is the `String.prototype.repeat()` method?**
    - **Answer:** `repeat()` constructs and returns a new string which contains the specified number of copies of the string on which it was called.

195. **What is the `Date` object and how is it used?**
    - **Answer:** The `Date` object represents a single moment in time. It can be used to create and manipulate dates and times.
      ```javascript
      const now = new Date();
      ```

196. **What is the `Date.prototype.getTime()` method?**
    - **Answer:** `getTime()` returns the number of milliseconds since January 1, 1970, 00:00:00 UTC.

197. **What is the `Date.prototype.setDate()` method?**
    - **Answer:** `setDate()` sets the day of the month for a specified date according to local time.

198. **What is the `Date.prototype.toISOString()` method?**
    - **Answer:** `toISOString()` converts a `Date` object to a string, using the ISO 8601 format.

199. **What is the `JSON.stringify()` method?**
    - **Answer:** `JSON.stringify()` converts a JavaScript object or value to a JSON string. It can also take additional parameters to format the output.

200. **What is the `JSON.parse()` method?**
    - **Answer:** `JSON.parse()` parses a JSON string and constructs the JavaScript value or object described by the string.

These questions and answers should cover a broad range of JavaScript concepts, from basic to more advanced topics.