### Basic TypeScript Concepts

1. **What is TypeScript, and how does it differ from JavaScript?**
   - **Answer:** TypeScript is a statically typed superset of JavaScript that compiles to plain JavaScript. It introduces static types, interfaces, and other features that help with early error detection and improve code quality. Unlike JavaScript, TypeScript requires type annotations and provides compile-time type checking.

2. **How do you declare a variable with a specific type in TypeScript?**
   - **Answer:** You can declare a variable with a specific type using a type annotation. For example:
     ```typescript
     let age: number = 30;
     let name: string = 'John';
     ```

3. **What are TypeScript interfaces and how are they used?**
   - **Answer:** Interfaces in TypeScript define the shape of an object, including properties and methods. They are used to type-check object structures and ensure they adhere to a specific contract. For example:
     ```typescript
     interface Person {
       name: string;
       age: number;
     }

     const person: Person = {
       name: 'Alice',
       age: 25
     };
     ```

4. **Explain the concept of `any` type in TypeScript.**
   - **Answer:** The `any` type in TypeScript represents any value and effectively disables type checking for that variable. It is a way to opt-out of type safety and should be used sparingly. Example:
     ```typescript
     let data: any = 'Hello';
     data = 42;
     ```

5. **What is type inference in TypeScript?**
   - **Answer:** Type inference is the ability of TypeScript to automatically deduce the type of a variable based on its value, without explicit type annotations. For example:
     ```typescript
     let num = 5; // TypeScript infers 'num' as 'number'
     ```

6. **How do you define a function with typed parameters and return type?**
   - **Answer:** You can specify types for function parameters and return values. For example:
     ```typescript
     function greet(name: string): string {
       return `Hello, ${name}!`;
     }
     ```

7. **What are TypeScript tuples, and how are they different from arrays?**
   - **Answer:** Tuples are arrays with a fixed number of elements where each element can have a different type. Unlike arrays, which can have elements of any type, tuples have a defined length and type for each position. Example:
     ```typescript
     let person: [string, number] = ['John', 30];
     ```

8. **Explain the use of `enum` in TypeScript.**
   - **Answer:** Enums are a way to define a set of named constants. They can be used to represent a collection of related values. For example:
     ```typescript
     enum Color {
       Red,
       Green,
       Blue
     }

     let myColor: Color = Color.Green;
     ```

9. **What are TypeScript classes, and how do they differ from JavaScript classes?**
   - **Answer:** TypeScript classes are similar to JavaScript classes but with additional features like type annotations, access modifiers (public, private, protected), and interfaces. They provide a way to create objects with specific structures and behaviors.

10. **How do you implement inheritance in TypeScript?**
    - **Answer:** Inheritance in TypeScript is implemented using the `extends` keyword. A subclass inherits properties and methods from a superclass. Example:
      ```typescript
      class Animal {
        name: string;

        constructor(name: string) {
          this.name = name;
        }

        speak(): void {
          console.log(`${this.name} makes a noise.`);
        }
      }

      class Dog extends Animal {
        bark(): void {
          console.log(`${this.name} barks.`);
        }
      }

      const dog = new Dog('Rex');
      dog.speak(); // Rex makes a noise.
      dog.bark();  // Rex barks.
      ```

### Intermediate TypeScript Concepts

11. **What are generics in TypeScript, and why are they useful?**
    - **Answer:** Generics allow you to write flexible, reusable functions, classes, and interfaces that can work with any data type. They help maintain type safety while avoiding code duplication. Example:
      ```typescript
      function identity<T>(arg: T): T {
        return arg;
      }
      ```

12. **How do you use type assertions in TypeScript?**
    - **Answer:** Type assertions are used to tell TypeScript the specific type of a variable. You can use them when you have more information about the type than TypeScript can infer. Example:
      ```typescript
      let someValue: any = 'This is a string';
      let strLength: number = (someValue as string).length;
      ```

13. **What are TypeScript modules and how do they work?**
    - **Answer:** TypeScript modules are files containing code that can be exported and imported between different files. They help organize code into separate, reusable pieces. Example:
      ```typescript
      // math.ts
      export function add(x: number, y: number): number {
        return x + y;
      }

      // app.ts
      import { add } from './math';
      console.log(add(2, 3));
      ```

14. **What are `interface` and `type` in TypeScript, and when would you use each?**
    - **Answer:** Both `interface` and `type` can be used to define types. `interface` is typically used for object shapes and can be extended or merged. `type` is more versatile and can define complex types like unions and intersections. Example:
      ```typescript
      interface Person {
        name: string;
        age: number;
      }

      type Address = {
        street: string;
        city: string;
      };

      type PersonWithAddress = Person & Address;
      ```

15. **Explain the concept of `union` types in TypeScript.**
    - **Answer:** Union types allow a variable to be one of several types. They are defined using the `|` symbol. Example:
      ```typescript
      let value: string | number;
      value = 'Hello';
      value = 42;
      ```

16. **What are `intersection` types in TypeScript?**
    - **Answer:** Intersection types combine multiple types into one. They are created using the `&` symbol and represent a type that has all the properties of the combined types. Example:
      ```typescript
      interface A {
        a: number;
      }

      interface B {
        b: string;
      }

      type C = A & B;

      let obj: C = {
        a: 1,
        b: 'Hello'
      };
      ```

17. **How do you use `type guards` to narrow down types in TypeScript?**
    - **Answer:** Type guards are techniques used to narrow the type of a variable within a conditional block. Examples include using `typeof`, `instanceof`, or custom type guard functions. Example:
      ```typescript
      function isString(value: any): value is string {
        return typeof value === 'string';
      }

      let value: any = 'Hello';

      if (isString(value)) {
        console.log(value.length); // TypeScript knows value is a string
      }
      ```

18. **What is the purpose of `readonly` in TypeScript?**
    - **Answer:** The `readonly` modifier ensures that properties of an object cannot be modified after initialization. It is useful for creating immutable data structures. Example:
      ```typescript
      interface Person {
        readonly name: string;
        age: number;
      }

      const person: Person = { name: 'Alice', age: 30 };
      // person.name = 'Bob'; // Error: Cannot assign to 'name' because it is a read-only property
      ```

19. **How do you handle default values for function parameters in TypeScript?**
    - **Answer:** Default values for function parameters are specified directly in the function signature. Example:
      ```typescript
      function greet(name: string = 'Guest'): string {
        return `Hello, ${name}!`;
      }
      ```

20. **What are `decorators` in TypeScript and how are they used?**
    - **Answer:** Decorators are special functions that can modify classes, methods, accessors, or properties. They are experimental and require enabling the `experimentalDecorators` compiler option. Example:
      ```typescript
      function log(target: any, propertyName: string | Symbol) {
        console.log(`Property ${String(propertyName)} is being accessed.`);
      }

      class MyClass {
        @log
        myProperty: string;
      }
      ```

### Advanced TypeScript Concepts

21. **What are `conditional types` in TypeScript, and how do they work?**
    - **Answer:** Conditional types provide a way to select one of two types based on a condition. They use the `T extends U ? X : Y` syntax. Example:
      ```typescript
      type TrueOrFalse<T> = T extends true ? 'Yes' : 'No';

      type Test1 = TrueOrFalse<true>;  // 'Yes'
      type Test2 = TrueOrFalse<false>; // 'No'
      ```

22. **How does TypeScript handle `type inference` for generics?**
    - **Answer:** TypeScript infers types for generics based on how they are

 used. If no type arguments are provided, TypeScript tries to infer the types from function usage or context. Example:
      ```typescript
      function identity<T>(arg: T): T {
        return arg;
      }

      let result = identity('Hello'); // TypeScript infers T as string
      ```

23. **What are `mapped types` in TypeScript, and how can you use them?**
    - **Answer:** Mapped types create new types by transforming properties of an existing type. They use the syntax `{ [P in K]: T }`. Example:
      ```typescript
      type Readonly<T> = {
        readonly [K in keyof T]: T[K];
      };

      interface Person {
        name: string;
        age: number;
      }

      type ReadonlyPerson = Readonly<Person>;
      ```

24. **How do you use `utility types` in TypeScript, and what are some common examples?**
    - **Answer:** Utility types provide built-in transformations for types. Examples include `Partial`, `Required`, `Pick`, and `Omit`. Example:
      ```typescript
      interface Person {
        name: string;
        age: number;
      }

      type PersonWithoutAge = Omit<Person, 'age'>;
      ```

25. **What is the `infer` keyword used for in TypeScript?**
    - **Answer:** The `infer` keyword is used within conditional types to infer a type variable. It allows you to capture and use types within a conditional type. Example:
      ```typescript
      type ReturnType<T> = T extends (...args: any[]) => infer R ? R : never;
      ```

26. **How do `namespace` and `module` differ in TypeScript?**
    - **Answer:** `namespace` is used for organizing code within a single file or project and is an older pattern. `module` (ES6 modules) is used for organizing code across different files and supports modern JavaScript module features.

27. **What are `type predicates` and how are they used in TypeScript?**
    - **Answer:** Type predicates are used in custom type guards to narrow down types within conditional blocks. They have the form `value is Type`. Example:
      ```typescript
      function isNumber(value: any): value is number {
        return typeof value === 'number';
      }
      ```

28. **How do you use `type inference` with `tuple` types in TypeScript?**
    - **Answer:** TypeScript can infer the types of tuple elements based on their initial values. Tuples with explicit types allow you to define a fixed-length array with specified types for each position. Example:
      ```typescript
      let tuple: [number, string] = [1, 'hello']; // TypeScript infers tuple as [number, string]
      ```

29. **What are `template literal types` in TypeScript?**
    - **Answer:** Template literal types allow you to create types using template string syntax. They enable the creation of complex string patterns and combinations. Example:
      ```typescript
      type Greeting = `Hello, ${string}`;
      let greet: Greeting = 'Hello, World'; // Valid
      ```

30. **How do `type aliases` differ from `interfaces` in TypeScript?**
    - **Answer:** Type aliases and interfaces can often be used interchangeably, but there are differences. Interfaces support declaration merging and are often used for object shapes. Type aliases can define any type, including primitives, unions, and intersections, and do not support declaration merging.

31. **What are `assertion functions` in TypeScript?**
    - **Answer:** Assertion functions are functions that narrow down types by asserting that a value is of a certain type. They return a type predicate to provide more accurate type information. Example:
      ```typescript
      function isString(value: any): value is string {
        return typeof value === 'string';
      }
      ```

32. **Explain the use of `keyof` operator in TypeScript.**
    - **Answer:** The `keyof` operator returns a union of all property names of a type. It is useful for creating types that are based on the keys of other types. Example:
      ```typescript
      interface Person {
        name: string;
        age: number;
      }

      type PersonKeys = keyof Person; // 'name' | 'age'
      ```

33. **How does `index signature` work in TypeScript?**
    - **Answer:** Index signatures allow you to define types for properties that are accessed using dynamic keys. They use the syntax `[key: KeyType]: ValueType`. Example:
      ```typescript
      interface StringMap {
        [key: string]: string;
      }

      let map: StringMap = {
        key1: 'value1',
        key2: 'value2'
      };
      ```

34. **What are `decorators` and how do you enable them in TypeScript?**
    - **Answer:** Decorators are special functions that can modify classes, methods, or properties. To use decorators in TypeScript, you need to enable the `experimentalDecorators` compiler option. Example:
      ```typescript
      @decorator
      class MyClass {}
      ```

35. **How does `type narrowing` work in TypeScript?**
    - **Answer:** Type narrowing involves using control flow analysis to narrow down the type of a variable based on conditions. TypeScript can refine types within conditional blocks, such as using `typeof`, `instanceof`, or custom type guards.
