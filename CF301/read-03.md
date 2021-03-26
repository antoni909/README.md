# Read-03-Notes

## Readings Assigned

React Docs - Lifting State Up
React Docs - lists and keys
React Tutorial through ‘Declaring a Winner’
The Spread Operator

## React Docs - Lifting State Up

[React Docs - Lifting State Up](https://reactjs.org/docs/lifting-state-up.html)

- How do different components share the same data?
  - Their shared state must be lifted to their closest common ancestor
  - Use the concept of top-down data flow
    - State is added locally to the component that requires it, then if another component also needs it, state gets lifted to closest common ancestor

## [React Docs - lists and keys](https://reactjs.org/docs/lists-and-keys.html)

- How do you transform lists in JavaScript
- Can use the map() method for arrays and use it to create an array of JSX elements

  - e.g.

    \const numbers=[1, 2, 3, 4, 5];

    \const listItems=numbers.map((number)=>&lt;li>{number}&lt;/li>);

- The entire list (the new array) is placed inside a parent element
  - &lt;ul>{listItems}&lt;/ul>
- Basic Lists are rendered inside a component
- [In-Depth Explanation on keys](<[https://reactjs.org/docs/reconciliation.html#recursing-on-children](https://reactjs.org/docs/reconciliation.html#recursing-on-children)>)
- What is key?
  - A key should be provided for list items
  - Special string Attribute that needs to be included for lists of elements
- Keys, help react identify items that have:
  - Changed
  - Added
  - Removed
- Ultimately, they are given to EACH element in the array to give them a stable identity
- How do you create a key?
  - Use a string that UNIQUELY identifies each list item
  - Can use the ids from your data
  - Last resort would be to use the arrays index, when no stable ids
    - The reason is because the data in the array could change position
    - [In-Depth-Explanation](<[https://medium.com/@robinpokorny/index-as-a-key-is-an-anti-pattern-e0349aece318](https://medium.com/@robinpokorny/index-as-a-key-is-an-anti-pattern-e0349aece318)>)
    - The key should be specified inside the array,
  - Keys do not need to be globally unique, but must be unique amongst siblings
- Embedded Expressions in JSX allow you to embed expressions using curly brace
  - Rule of Thumb on Use and Abuse : what is best for readability

[React Tutorial through ‘Declaring a Winner’](https://reactjs.org/tutorial/tutorial.html)

- [React Docs Tutorial and Basics](<[https://reactjs.org/tutorial/tutorial.html](https://reactjs.org/tutorial/tutorial.html)>)


## [The Spread Operator](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

- Quick syntax for
  - adding items to Arrays/Objects
  - Combining Arrays/Objects
  - Spreading an arr out in a Functions Args
- What is it?
  - (...)
  - It spreads the array into separate arguments
  - Used for:
    - Copying an arr
    - Combining an arr
    - Math funcs
    - Arr as args
      - Passess in the elements of the array into a function
    - Adding item to a list
    - Adding states to react
    - Combining objects
  - A copied array, using the spread operator, would mean that changes to the Original array would not affect the new/copied array
  - Deeply nested values will still be linked together, however.
    - Spread only makes Shallow Copy not a Deep Copy

[back to top](#Read-03-Notes)
[back to table of contents](/README.md)
