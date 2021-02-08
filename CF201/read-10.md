# Reading-1

## If you wish to exit to the homepage click on the following link to head back to the [homepage](../README.md)

## Reading Assignment is as follows

    From the Duckett JS book:

    JavaScript book, Ch. 1, “Error Handling & Debugging”

## JS Chapter 1

Error Handling and Debugging 

1. Order of Execution - not necessarily linear or ‘ordered’
1. Execution Contexts - code can live in 1 places: 
      1. Global - lives in the script
      1. Function - lives inside a function
      1. Eval Code (hidden)
1. The Stack - the JS interpreter stacks new functions on top of current task, as a result new stack items create new execution context
1. When JS enters new Execution of Context there are 1 phases
    1. Prepare
        1. New scope created
        1. Creation of functions, args, vals 
        1. Hoisting of funcs/vars
        1. Var Object is created
    1. Execute
        1. Assign vals to vars
        1. Ref funcs + run code
        1. Execute statements
1. Scope - the current execution vars object + vars object for each parent execution context
1. Errors - if JS statement generates an error, it throws a pre-built exception code called exception-handling code
    1. Error-Objects
        1. Error - generic
        1. SyntaxError - incorrect syntax
        1. ReferenceError - ref a var not declared/within scope
        1. TypeError - coerced data type
        1. RangeError - out of range num
        1. URIError - incorrect use
        1. EvalError - funct used incorrectly
    1. Dealing with Errors - 1 ways
        1. Debug the Script - 
        1. Find another solution if can't debug
    1. Debugging Workflow where debugging = deduction
        1. Where is the problem?
        1. What is the problem?
1. Handling Exceptions
    1. Use code blocks for:
        1. try - specify code that might throw an exception
        1. catch - gives alternate set of code
            1. 1 parameter is the error object lets user know something has gone wrong
        1. finally - will run if try block succeed or failed
1. Throwing Errors - generate own errors before the interpreter runs into them, creating a new error object.
    1. Use the syntax:throw new Error( ‘message’ ) ;
1. Debugging Tips and Common Errors pg 484-485

## To exit to the homepage click on the following link to head back to the [homepage](../README.md)

## To return to the top of the page [click here](#Reading-1)