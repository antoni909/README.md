# Reading-04

## If you wish to exit to the homepage click on the following link to head back to the [homepage](../README.md)

## Reading Assignment is as follows

This layout chapter is BIG. Focus your attention on understanding the core concepts presented on pp.358-364, and look at the code samples on the website that accompanies the textbook. You will have another reading assignment on this chapter, so do not try to digest it all now.

This layout chapter is BIG. Focus your attention on understanding the core concepts presented on pp.358-364, and look at the code samples on the website that accompanies the textbook. You will have another reading assignment on this chapter, so do not try to digest it all now.

## Reading

From the Duckett HTML book:
Chapter 4: Ch.4 “Links” (pp.74-93)
Chapter 15: “Layout” (pp.358-404)

From the Duckett JS book:
Chapter 3 (first part): “Functions, Methods, and Objects” (pp.86-99 ONLY)

Article: “6 Reasons for Pair Programming”

## JavaScript Chapter 3: Functions, Methods and Objects

## Summary Type: Notes in Outline Form

### Functions let you contain a series of statements that have been grouped together to perform a specific task. 

1. Functions
-Call: when you invoke/call the function to perform its task
-Parameter: pieces of information passed to the function
-Return: is the answer you expect the funciton to give you, a response
-Declaring: use the following syntax: function functionName() {code block} to call the funtion: functionName();
-Arguments as Values vs Arguments as Variable
  - Args as Vals: you specify the value of the parameter of a function using arguments
  -Args as Vars: you dont have to specify the value when calling a function, you can use variables in their place
-Multiple Vals out of a Function
  - functions can return more than one value using an array
1. Function Expressions when a browswer expects to see an expression then it will treat it as an expression
  -Immediately Invoke Func Expressions
    -use the following syntax: 
    var name = (function() {code block}()); where the () after the code block is called the final parenthesis and it tells the interpretter to call the funtion immediately
    -the grouping order paranthesis, enase the entire code, ensure the interpretter treats it as a function expresssion
1. Variable Scope
  -Local Varibles: are function level or local vars useable only inside function
  -Global Variables: vars that can be used outsind/inside local/funtions
    -use more memory than local vars
    -naming conflicts arise vs none with local vars

## If you wish to exit to the homepage click on the following link to head back to the [homepage](../README.md)

## OR would you like to head to the top of the page?[top of page](#Reading-04)

## HTML Chapter 15: Layout

## Summary Type: Notes Outline Form

### The chapter explores the following topics:

- Find ways to position elements using NORMAL flow/RELATIVE positioning/ and floats

- how different screen sizes affect design process

- Difference between FIXED and LIQUID layouts

- GRIDS make page layout proffessional

### Concepts in Positioning Elements

1. Block level Elements start a new line
  -Parent/Containing Element is when block element sits INSIDE another block element then the outer element becomes the parent
  -<h1>,<p>,<ul>,<ol>
1. Inline level Elements flow in between surrounding txt
  -<img>,<b>,<i>
1. Controlling Position of Elements use position property in CSS to select from the following schemes
  1. Normal Flow
    -Default Behavior where Block Elemements appear in a new line
  1. Relative Position
    -This moves element from it normal spot to a select new position top,right,bottom,left
  1. Absolute Position
    -These Elements move as user scroll up/down screen
    - Box Offset properties: indicatre where box shoul be positioned
      -fixed poistioning
      -floating elements
1. CSS rule for ELements
  1. position:static & top/right/bottom/left: (pixels, percent, ems)
    - normal flow of elements
  1. position:relative  & top/right/bottom/left: (pixels, percent, ems)
    - moves element in relation to where it would have been in normal flow
  1. position:absolute  & top/right/bottom/left: (pixels, percent, ems) & width: (pixels, percent, ems)
    - box is taken out of normal flow and will not affect position of other elements
  1. position:fixed & top/right/bottom/left: (pixels, percent, ems) & width: 100% (pixels, percent, ems)
    - positions the element relative to the browswer window
  1. z-index: n;
    - property that allows you to select which element sits on top of overlapping elements
  1. float: (left,right, none); & width:n(pixels, percent, ems);
    - allows you to take an element in normal flow and place it as far L/R of CONTAINING element as possible
    - clear: left/right/both/none; 
      - allows you to say no element should touch L/R side of a box

1. Screen Resolution refers to the number of dots per inch
1. Page Size: designers try and create pages around 960-1k pixels wide
1. Fixed Width Layouts - do not change size as user inc/dec size of browswer window (use pixels)
  1. How to set-up basic fixed layout using div elements as containers
      - body element : fix width of page by 960 px, margin is auto
      - main boxes: margin of 10px, to create space between them
      - nav, feature, footer stretch to width of containing element same as body element 
      - Number of Columns have width of 300 px and use float left allowing them to sit sidebyside
1. Liquid Layouts - stretch and contract as useer inc/dec size of browser window (use percentage)
  1. How to set-up basic liquid layout using div elements as containers and ids to target specific tags
      - body element: width of page by 90% to leave rm in the  R/L sides of page
      - Columns have margin: 1%, width: 31.3% (devided by number of columns in the page/body element)
      - nav, feature, footer stretch to width of containing element same as body element and margin: 1% 
1. Layout Grids: How items are positioned on a page
  1. 960 Pixel Grid
      - 960 px wide and 12 column grid, each column has margin: 10px
      - example:
        960
        460 + 460
        300 + 300 + 300
        220 + 220 + 220 + 220
        140 + 140 + 140 + 140 + 140 + 140
1. Multiple Style sheets
  1. @import url (fake.com);
    - rule used to import css rules from another css page
  1. link 
    - HTML element used to import css rules from css page