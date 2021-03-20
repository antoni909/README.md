# Readings

## Introduction to React and Components

## [Back to Home](/README.md)

## Resources Used
[React Tutorial through ‘Passing Data Through Props’](https://reactjs.org/tutorial/tutorial.html)
[React Docs - hello world](https://reactjs.org/docs/hello-world.html)
[React Docs - introducing JSX](https://reactjs.org/docs/introducing-jsx.html)
[React Docs - rendering elements](https://reactjs.org/docs/rendering-elements.html)
[React Docs - Components and props](https://reactjs.org/docs/components-and-props.html)

## Note-Taking Type: Summarize each reading

## React Tutorial through ‘Passing Data Through Props’

### What is React? it is a JS library for creating UI's using components. There are different kinds of components. React.Component are subclasses of classes in JS. Components ahve paramaters that define the props('properties') and uses the render method to return a React Element, which is a "view" heirarchy or a lightweight description of what to render. HTML syntax is transormed during buildtime to a React Element using React.createElement('eL', {className: 'actualClassName'})

### What is JSX? It allows you to place any JS expressions, using curly braces, inside JSX. Where each React Element is a JS Object that you are allowed to store as a variable and pass around in the program

### React Components are customizable!

## React Docs - introducing JSX

### What is JSX?(...again) it is syntax EXTENSION of JS and it creates React Elements

### Why JSX? uses coupled units, "components", that contain markup and logic

### Embedding Expressions in JSX - valid JS is placed inside curly braces in JSX, this is embedding

my example:
          HTML Markup:
          \<div id="root">something</div>

          JS Logic:
          function nameIt(name){
            return name.toUpperCase();
          }

          let personName = 'billy';

          const element = <h1>JSX : {nameIt(personName)}</h1>
                
          ReactDOM.render(

          element,
          document.getElementById('root')
          )

### JSX as an Expression - this means that JSX can be used in function calls and evaluate objects, JSX can be used in if statements and for loops, can use string literals as attributes, and can also use curly braces to embed JS expression in an attribute (src, href, etc). It is either or and never both in the same attribute

### Specifying Children in JSX

- emty tags can be closed with \/>
- tags may contain children: div > h1 > h2
- it prevents injection attacks because everything is converted to string before it is rendered

### JSX Represents Objects

[click here to go the top of the page](#-Readings)

## Rendering Elements

### What are Elements in React?

- An element is what you want to display on the screen
- They are not DOM elements
- the React DOM auto updates the DOM to match React Elements
- React Elements are plain Objects
- They are the simplest building blocks in React, and they are the consitituent elementary building blocks of React Components

### Rendering Elements to the DOM

- Must have a "root" DOM node where it will then be managed by the React DOM. If using only React, you need only one root, if integrating React you can use as many root nodes as needed

- To render a React Element use  ReactDOM.render(element, root);

### Updating the Rendered Element

- React Elements are IMMUTABLE. This means that when an element is created, you cannot change its corresponding children or attributes.

- The React DOM only updates what is necessary

[click here to go the top of the page](#-Readings)

## React Docs - Components and Props

[Detailed Docs on React.Component](https://reactjs.org/docs/react-component.html)

### Components

- are similar to functions because they take in inputs (props) and return React Elements, which in turn describe what should be rendered

### Function and Class Components

- function components === JS functions

- What does a React Component look like? 2 examples:

[Source for Following Example](https://reactjs.org/docs/components-and-props.html)

    Using a JS Function
    function Welcome(props) {
      return <h1>Hello, {props.name}</h1>;
    }

    Using an ES6 Class
    class Welcome extends React.Component {
      render() {
        return <h1>Hello, {this.props.name}</h1>;
      }
    }

### Rendering a Component

- React Elements, are not limited to just DOM Tags, they can also represent "user-defined" components

- React passes JSX att+children to component as single object(props)

- Review of How React Renders a Component
  1. call ReactDOM.render() using \<Element>
  2. React calls the Element component with object {prop: 'value'} as the props
  3. the component returns Reat Element as a result
  4. React DOM updates the DOM match

### Composing Components

- Components can reference other components, this allos for component abstraction that allows you to build buttons, forms, dialogs, etc.

### Extracting Components

- components can be split into smaller components

- per the reading, props should be named from the components Own-Point-Of-View versus its context

### Props are Read-Only

- it must never modify its own props, they dont change their inputs and always return the same results for respective inputs