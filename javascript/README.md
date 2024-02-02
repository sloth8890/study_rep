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
