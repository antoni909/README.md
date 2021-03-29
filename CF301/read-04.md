# Read-05 Forms

## Resources

[Bootstrap Form Docs](https://react-bootstrap.github.io/components/forms/)
[formik popular open source form library for React and React Native](https://formik.org/)
[MDN - Object Initializer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer#computed_property_names)

## Forms

- Form behavior in React
  - Best to have a function to handle form submission + has access to user data entered on the form == using controlled components
- Controlled Components - controls the _value_ of a form element
  - HTML form elements:
    - Input, textarea, select
    - State is updated based on user input
  - In React
    - Mutable state is updated with setState()
  - Controlled Component is a combination of both:
    - React State === single source of change
    - When the value of a form element is controlled by React
    - Component that renders the form:
      - Controls what happens in the form and future input

## Text Area - React

- Uses value attribute
- Value is initialized in the constructor
  - This.state = { value: “ some value ” }
  - eventHandler(){this.setState({ value: event.target.value })}
  - &lt;textarea value{this.state.value}>

## Select Tag

- Creates a drop-down list
- In HTML
  - &lt;select>
    - &lt;option value=”a”> a &lt;/option>
    - &lt;option selected value=”b” > &lt;/option>
  - &lt;/select>
  - Selected attribute not used in React
- In React
  - Uses a value attribute on ROOT select tag
    - Convenient because only need update in one place
    - selected value would be in state

All work the same in React: &lt;input type="text">, &lt;textarea>, and &lt;select> all work very similarly

- Can pass an array in the value attribute, lets you select multiple options
- &lt;select multiple={true} value={['B', 'C']}>

## File Input Tag

- Uncontrolled component
- Lets you choose >=1 files
- Uploaded to server/ manipulated by js

## Handling Multiple Inputs

- When handling multiple inputs
  - Name attribute to each element
  - Let handler function choose what to do based on:
    - Event.target.name
  - Example:
    - Const name = target.name
      - In event handler
    - [name]: value
      - In setState
    - name=”someName”
      - In render
    - name=”some other name”
      - In input element being rendered

## Controlled Input Null Value

## Alternative to Controlled Components

- Another way to implement input forms in React
  - [link](https://reactjs.org/docs/uncontrolled-components.html)
