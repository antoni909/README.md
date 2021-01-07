# **This page is a response to the reading assigned for Code102 course**

## **For this reading assignment we were instructed to focus our efforts and attention to the following pages**

**Duckett: JavaScript & jQuery:**
    - Comparison and logical operators: 150-151, 156, and 157
    - for and while loops: 170 - 173, and 176

## Comparison and logical operators: 150-151, 156, and 157

### **The ability to evaluate a situation hinges on the ability to use Boolean Values (resulting in True or False) by comparing one value to another using the following operators**

    1. ==  is equal to operator
    1. === is strictly equal to operator
    1. !=  is not equalt to operator
    1. !== is strictly not equal to operator
    1. >   greater than operator
    1. <   less than operator
    1. >=  greater than equal to operator
    1. <=  less than equal to operator

### Structure example: (a >= b) 

### Note: as long as an expression evaluates to into a single value an operand can be an expression (it is not limited to a single value or variable name)

## Logical Operator- allow you to compare the RESULTS of more than one comparison operator

### The following is an example from the book

    -   This contains 3 expressions: ((5<2) && (2>=3)))
    -                   Evaluates to:   F  &&    F   
    -                   Final Eval to:      F        since both sides arent True

### The following are the operators used in Logical Operators

    1. && is the Logical And operator (tests more than 1 condition)
            - if T && T then returns T
            - if T && F then returns F
            - if F && T then returns F
            - if F && F then returns F
    1. || is hte Logical Or operator (tests at least one condition)
            - if T || T then returns T
            - if T || F then returns T
            - if F || T then returns T
            - if F || F then returns F
    1. !  is the Logical Not operator (takes a single Boolean Value and inverts it)
            - if !T returns F
            - if !F returns T

## Loops and Loop Counters

### Loops check A condition and if the return is T then code block runs, the condition will run again and if the return is T then the code block runs again and repeats until it finds a condition that is F

### There are three types of loops

**For, While, and Do While Loops**
    - For Loop is used when you know the NUMBER of times you want to run a loop
    - While Loop is used when you do NOT KNOW the number of loops needed to run (The condition will continue to run as long as condition is T)
    - Do While Loop will always run statements inside curly braces at least once even if condition is false
