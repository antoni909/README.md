# ES6-Classes

## Repl: https://replit.com/@antoni909/ES6-Classes#vehicles-with-classes.js
## Sources: 
  - [MDN Inheritance and the prototype chain](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
  - [MDN this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)
  - [MDN Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

### MDN Inheritance and the prototype chain - "When it comes to inheritance, JavaScript only has one construct: objects. Each object has a private property which holds a link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. By definition, null has no prototype, and acts as the final link in this prototype chain." And also states: "When an inherited function is executed, the value of this points to the inheriting object, not to the prototype object where the function is an own property."

### MDN this - "A property of an execution context (global, function or eval) that, in non–strict mode, is always a reference to an object and in strict mode can be any value." And "In the global execution context (outside of any function), this refers to the global object whether in strict mode or not." While inside a function "nside a function, the value of this depends on how the function is called. [if the] code is not in strict mode, and because the value of this is not set by the call, this will default to the global object, which is window in a browser." Also noting that while in strict mode, "...if the value of this is not set when entering an execution context, it remains as undefined..."