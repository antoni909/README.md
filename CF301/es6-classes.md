# ES6-Classes

## Note-taking type: "create a map of the information", I decided to outline all the sources provided to me from the assignment and only focus on major/birds-eye view concepts

## Sources

[Repl for JS Classes vs Constructors and Prototypes](https://replit.com/@antoni909/ES6-Classes#vehicles-with-classes.js)
[YouTube - What the heck is the event loop anyway?,Philip Roberts,JSConf,EU
](https://www.youtube.com/watch?v=8aGhZQkoFbQ)
[YouTube - CodeFellows, Shred Talks](https://www.youtube.com/watch?v=9Yc5J3Ap9-4)
[MDN Inheritance and the prototype chain](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
[MDN this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)
[MDN Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

### MDN Inheritance and the prototype chain - "When it comes to inheritance, JavaScript only has one construct: objects. Each object has a private property which holds a link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. By definition, null has no prototype, and acts as the final link in this prototype chain." And also states: "When an inherited function is executed, the value of this points to the inheriting object, not to the prototype object where the function is an own property."

### MDN this - "A property of an execution context (global, function or eval) that, in non–strict mode, is always a reference to an object and in strict mode can be any value." And "In the global execution context (outside of any function), this refers to the global object whether in strict mode or not." While inside a function "nside a function, the value of this depends on how the function is called. [if the] code is not in strict mode, and because the value of this is not set by the call, this will default to the global object, which is window in a browser." Also noting that while in strict mode, "...if the value of this is not set when entering an execution context, it remains as undefined..."

### MDN Classes - per MDN the definition of Classes in js is "[that] Classes are in fact "special functions", and just as you can define function expressions and function declarations, the class syntax has two components: class expressions and class declarations." They are a bit different than functions because they are not subject to Hoisting, "An important difference between function declarations and class declarations is that function declarations are hoisted and class declarations are not." Also, something I learned is that Classes can be either declarations or expressions (much like functions) and that Class expressions can be named or unnamed
