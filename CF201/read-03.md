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

### There are 3 types of lists: ordered, unordered, and definition lists. Ordered lists use numbers and unordered lists use bullets. You can also create nested lists inside li elements. Definition lists are hierarchically structured

### dl is definitions list and contains dt (definition term) and dd (definitnion)

## HTML Chapter 13: Boxes

## Summary-Type:  Notes in Outline Form

## This chapters covers the following topics on how to set properties that affect/control the appearence of 'html boxes'

- Control the dimensions of boxes
- Create borders around boxes
- Set margins and padding for boxes
- Show/hide boxes

## Border, Margin and Padding

1. Border will seperate the edge of one box from another
  1. border-width (values: thin, medium, thick) cannot use percentages only pixels and is used to control the width of the border
  1. border-top-width,border-right-width, border-bottom-width,border-left-width can all be condensed respectively into border-width property above, appearing in clockwise order
  1. border-style (values: solid, dotted, dashed, double, groove, ridge, inset, outset, hidden/none,)
  1. border-color (values: rgb, hex codes, css color name)
    - note that there is border-top-color, border-right-color, border-bottom-color, border-left-color and can be summarized by four values in the border-color property in clockwise(top,right,bottom,left)order.Example:  border-color: red green blue indigo;
  1. border: width style color;  is a shorthand border property

- Margins sit outside the border, creates a gap between the border of adjacent boxes
  1. margin (values: pixel, percentage, ems)
    - Note: if width is specified for a box, margin is added onto the width of the box
    - Shorthand: margin: margin-top margin-right margin-bottom margin-left;

- Padding is the space between the content and the border, increases the readability of the content.
  1. padding (values: pixel, percentage, ems) allows you to specify how much space appears between content of element and border.
    - Note: if width is specified for a box, padding is added onto the width of the box
    - Note: padding is NOT inherited to child elemnts and must be specified for every element
    - Shorthand: padding: padding-top padding-right padding-bottom padding-left;

## Chapter Outline

1. Box Dimensions
  1. Pixels: most popular, allows you to accurately control size
  1. Percentage: box size relative to size of browser window or the box its in
  1. ems: box size is based on the size of text within it. Used with percentage for measurements to create designs that are flexible accross devices with diff sized screens
1. Limiting Width
  1. Min-Width: properties that specify the smallest size a box can be displayed when browswer window is NARROW
  1. Max-Width: properties that specify the largest size a box can be displayed when browswer window is WIDE
1. Limiting Height
  1. min-height : set min height limit of text inside box
  1. max-height : set max height of text inside box
1. Overflowing Content
  1. overflow : tells browswer what to do if content contained in box is larger then the box
    1. hidden - hides extran content that does not fit in the box
    1. scroll - adds a scrollbar to see missing content
1. Centering content
  1. To center a box on the page/element it is in
    1. set left-margin: auto; and right-margin: auto;
    1. set width for the box (or it will take up the width of the page/element it is in)
    1. set text-align: center;
1. Change Inline/Block
  1. display is used to turn inline to block and vice versa, also to hide an element from page
    1. values
      1. inline; cause block level to ACT like inline
      1. block; cause inline element to ACT like block
      1. inline-block; cause block level element to FLOW like inline element and retain its block-level features
      1. none; hides an element from the page
  1. visibility (values: hidden, visible) allows you to hide boxes from users but leaves its placeholder space where it would have been
1. CSS3 
  1. border-image (values: stretch repeat round) applies an image to the border of any box
  1. box-shadow allows you to add a drop-shadow on the box 
  1. border-radius allows you to create round corners on any box

## Do you want to exit to the homepage? click on the following link to head back to the [homepage](../README.md)

## OR do you want to return to the top section? [top of page](#blank)
