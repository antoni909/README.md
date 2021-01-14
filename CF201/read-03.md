# Reading 03

## If you wish to exit to the homepage click on the following link to head back to the [homepage](../README.md)

## Reading Assignment is as follows

Create a new markdown file in your reading notes repository
Add a link to this new file under the table of contents for this course
Then ACP your master branch to create a rendered web page on GitHub pages
Copy the rendered content and paste it into the discussion

## Reading

From the Duckett HTML book:

Chapter 3: “Lists” (pp.62-73)
Chapter 13: “Boxes” (pp.300-329)
From the Duckett JS book:

Review from Reading 02 - Chapter 2: “Basic JavaScript Instructions” (pp.70-73)

Chapter 4: “Decisions and Loops” from switch statements on (pp.162-182)

## JavaScript Chapter 04: Decisions and Loops

## Summary Type: Notes in Outline Form

### This js chapter focuses on how code can take different paths and will run different code based on the circumstances/situation. Evaluations, Decisions, and Loops help you design and control the flow of code based on the users interaction with the web page. Basic data workflow: 

  1. Evaluations - analyze values in scripts to determine expected results
  2. Decisions - Using results of evaluations, decide which path script should follow
  3. Loops - allows you to perform the same set of steps repeatedly  

### Switch Statements will evaluate its expression (a valid unit of code that resolves to a value, from MDN) matching the value of the expression to a case and runnint the code therein or the default case if there is no match, by convention the default is the last case

### Syntax [retrieved Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch).Note that break statements are not required and are optional if preceded by a return statement

switch (expression) {
  case value1:
    //Statements executed when the
    //result of expression matches value1
    [break;]
  case value2:
    //Statements executed when the
    //result of expression matches value2
    [break;]
  ...
  case valueN:
    //Statements executed when the
    //result of expression matches valueN
    [break;]
  [default:
    //Statements executed when none of
    //the values match the value of the expression
    [break;]]
}

### Switch Statements vs If...Else Statements

- Switch Statements: You have a default code that runs if their is no match found. When match is found, code runs then break statement runs to stop rest of switch code from running, providing better performance than multiple if statements.
- If...Else Statements: No need for else statement, with a series of if...else all are run even if there is a match. Performs more slowly than switch statement.

### Value Types in JavaScript

- Type Coercion is when JavaScript converts data types to complete an operation instead of producing an error. How JavaScript type coercion affects values:

  - Weak Typing is used by JavaScript because data values for data types are allowed to change
  - As a result, to check whether data and value types match use strict operators such as: ===, !==, ==, !=
  - The following are data types and their purpose:

    |Data Type  |Purpose              |
    |   :---:   |   :---:             |
    |string     |text                 |
    |number     |number / (NaN)       |
    |boolean    |true/false           |
    |null       |empty value          |
    |undefined  |var declare w/ no val|

  - NaN is a val that is counted as a number when a number is expected but not returned, ex: 'five'/5 returns NaN
  - Truth/Falsy Values: EVERY value in JS can be treated as if it were T/F. 
    - Falsy Values are treated as if False or the number 0.

    |Value      |Description              |
    |   :---:   |          :---:          |
    |false      |boolean false val        |
    |0          |number 0                 |
    |''         |empty string             |
    |1/'5'      |NaN                      |
    |var x;     |var declared w/ no val   |

    - Truthy Values are everything not considered falsy, can also be treated as the number 1.
    - Logic Operators are process left to right and stop as soon as they have a result, however the return a value that stopped the processing and the value was treated as truthy/falsy eventhough it was not a Boolean.

### Loops are used to check a condition if the condition returns true it will run another loop/iteration until it loops false. There are 3 types of loops

- For
  - used for running code a SPECIFIC number of times, the condition is the counter that tells the loop how many times it should run
  - Syntax

    for (initialization; condition; update){
      code block;
    }

    - initialization is a var that is created and set to 0 (or your pref) and acts as the counter and is only created the first time the loop is run
    - condition lets the counter know how many times to run until the condition is met
    - update allows you to ammend each iteration

- While
  - used when you do NOT know the number of times to loop, the condition can be something other than a counter and will run as long as the condition is true
- Do While
  - same as the while loop except that it will always run the code block at least once even if it evals to false

## Do you want to exit to the homepage? click on the following link to head back to the [homepage](../README.md)

## OR do you want to return to the top section? [top of page](#blank)

## HTML Chapter 03: Lists

## Summary Type:  Notes in Outline Form

### There are 3 types of lists: ordered, unordered, and definition lists. Ordered lists use numbers and unordered lists use bullets. You can also create nested lists inside li elements. Definition lists are hierarchically structured as follows

<dl>
  <dt>
    <dd></dd>
  </dt>
</dl>

### dl is definitions list and contains dt (definition term) and dd (definitnion)

