# Read-10

## In-Memory Storage

[Understanding the JavaScript Call Stack](https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4)

[JavaScript error messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

[JavaScript errors reference on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)

## Notes are based/paraphrased from the reading:

[The JavaScript Call Stack - What It Is and Why It's Necessary](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)

Primary Uses:
    1. Call Stack is used for Funciton Invocation(Call)
      - call stack is synchronous because function execution is completed one-at-a-time, top-to-bottom
    What is it?
      - it is a data structure that uses Last in First out principle to temporarily store /manage function invocation(call)
    LIFO
     - This means that the last funciton that gets pushed into the call stack is the first to be popped out
    Temporarily Store
     - When invoked, the function/params/vars are pushed into the call stack to form STACK FRAME
     - Serves as a temporary memory location
     - Memory is cleared when function returns/popped out of stack
    Manage Function Invocation(call)
     - Maintains a record of the position of each stack frame
     - It knows the function that will execute/removed from stack

Asynchronous JS - There are three parts:
    1. Callback Function - acted upon during execution after the call back funciton has been push to the stack by even loop
    2. Event Loop
    3. Task Queue

### [to the top](#-Read-10)

### [back to the home page](/README.md)

## JavaScript error messages

Types of Error Messages

  Reference Error
    caused by:
      - use a var that is not yet declared
      - using const/let hoisted like var/function by there is a time (Temporal Dead Zone) between hoisting and being declared where they cannot be accessed,

    - To fix: declare the varibale before any declaration is made
  Syntax Error
    caused by:
      - cannot be parsed in terms of syntax
    solved by: fix the syntax mistake
  Range Error
    caused by: giving an invalid length
    solved by: ... not mutating vars and making them constants instead
  Type Error
    caused by: when trying to access/use data types that are incompatible
    solved by: make sure it exists before trying to access

Debugging
  ...stick to console.log(), it is the easiest and simplest way to debug errors

### [top of page](#-Read-10)

### [home page](/README.md)
