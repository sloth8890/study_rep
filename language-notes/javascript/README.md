# JavaScript Cheat Sheet

## Scope
Understanding JavaScript scope is fundamental to writing effective and bug-free code. Here's a summary of the three main scopes in JavaScript:
1. Global Scope
    - Variables declared outside any function or block have a global scope.
    - They can be accessed from any part of the code, including within functions.
2. Local Scope
    - Variables declared inside a function have function scope.
    - Accessible only within the function where they are declared.
    - Variables with function scope are not visible outside the function.
3. Block Scope (`let` and `const` concepts)
    - Variables declared with `let` and `const` have block scope.
    - Limited to the block of code (enclosed by curly braces `{}`) where the variable is defined.
    - Provides more fine-grained control over variable visibility.

## Variable Declaration

In JavaScript, there are different ways to declare variables, each with its own scope and mutability characteristics. Let's discuss each of them using your provided code snippets:

1. `var`:
   - Variables declared with `var` have function scope or global scope, depending on where they are declared.
   - If declared within a function, they are scoped to that function.
   - If declared outside any function, they are global variables.
   - Variables declared with `var` can be redeclared and reassigned.
   
   ```js
   var global_greeting = "hey hi";

   function newFunction() {
       var hello = "hello";
   }
   
   console.log(global_greeting); // Output: hey hi
   console.log(hello); // Error: hello is not defined
   ```
   In this example, `global_greeting` is declared as a global variable using `var`, so it's accessible anywhere in the code. However, `hello` is declared within the `newFunction()` function using `var`, making it scoped to that function. Thus, it's not accessible outside the function.

2. `let`:
   - Variables declared with `let` have block scope, meaning they are limited to the block (enclosed by curly braces) where they are defined.
   - Variables declared with `let` can be reassigned but cannot be redeclared within the same scope.

   ```js
   let greeting = "hello";

   if (true) {
       let message = "world";
       console.log(greeting); // Output: hello
       console.log(message); // Output: world
   }
   
   console.log(greeting); // Output: hello
   console.log(message); // Error: message is not defined
   ```
   In this example, both `greeting` and `message` are declared using `let`. They have block scope, so they are accessible only within the block where they are defined.

3. `const`:
   - Variables declared with `const` also have block scope.
   - Variables declared with `const` must be initialized with a value, and this value cannot be changed once assigned.
   - Like variables declared with `let`, variables declared with `const` cannot be redeclared within the same scope.

   ```js
   const PI = 3.14;
   PI = 3; // Error: Assignment to constant variable.
   ```

   In this example, `PI` is declared as a constant with a value of `3.14`. Any attempt to reassign `PI` to a different value will result in an error because `PI` is declared with `const`, making it immutable.

These are the key differences between `var`, `let`, and `const` variable declarations in JavaScript. It's generally recommended to use `let` and `const` instead of `var` due to their more predictable scoping behavior and avoidance of common pitfalls associated with `var`.