# Class-02 Notes

![screenshot](/assets/ReactLifeCycle.jpg "react life cycle")

[ScreenShot from author: wojtekmaj](https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/)

State and Lifecycle

“To collect data from multiple children, or to have two child components communicate with each other, you need to declare the shared state in their parent component instead. The parent component can pass the state back down to the children by using props; this keeps the child components in sync with each other and with the parent component.” - the people who built React.

- To update the UI, in the past we use the render() to change the output
- Will learn how to make a component truly: “reusable and encapsulated”
- State ~ Props in that it is private and will only be controlled by the component
- When using Class to Create a component
  - The class is created and extended from React.Component
  - Only one render()
    - Will only be called when the UPDATE happens
    - When only a single instance of the component is created this is because the component is rendered once in the respective DOM node.
    - This in turn allows additional features: Local State Lifecycle Methods
  - The body of the render method contains the return logic
  - And props are passed in via this.props.stuff inside the return()

To create a state using ES6 Classes

- Add a class constructor whose parameters is props: constructor(props);
  - Super the props from the parent class: super(props);
  - Create a new property and assign the param/argument: this.state = {propertyName:value};
  - In the render(), pass in the state: this.state.stuff

Adding LifeCycle Methods to a Class

- In an App with multiple components, it is necessary to clear up resources used
- Mounting : when a component is rendered to the DOM for the FIRST time
- Unmounting : whenever a component is removed from the DOM
- Using the Component Class, there are methods that are used to mount/unmount components and are called LifeCycle Methods :
  - componentDidMount()
    - Runs AFTER the component OUTPUT has rendered on the DOM
    - Perhaps using a set method ???
  - componentWillUnmount()
    - Perhaps using a clear method ???
  - What is setState( ) ???

Using setState()

- NEVER modify state directly, instead use the setState() method :
  - this.setState( { propertyName : value } );
  - This.state can only be assigned in the constructor
- Multiple setState() calls may be sent in single update
- this.state and this.props may run asynchronously and should not be relied on for subsequent state
  - To solve the problem, using this.setState() that has a function and not an object, this allows the setState to use the function whose first argument is the previous state and the props as the second argument.
  - Can use arrow functions or regular functions

Merged State Updates

- What is the .then() in : someFunction().then( someCode ); ???
- A setState can have many INDEPENDENT variables but you can update them separately using separate setState() calls

Data Flow - Top Down

- Parent and Child Components should not care if either has states/stateless or functions/class/
- State is local/encapsulated and therefore not accessible to other components
- The component containing the state is able to pass its State as props to child components
  -
  - <ChildComponent attr={ this.state.stuff } />
  - The child component receives the state from parent component in its props
  - The child component does not care where it received the state from

<span style="text-decoration:underline;">Handling Events</span>

- Use camelCase
- Using JSX, you do not pass in the call back function as a string, instead it is just the callback function reference
- To prevent default behavior, must define it explicitly
  - React Events != JS Native Events
  - e is a Synthetic Event ([https://reactjs.org/docs/events.html](https://reactjs.org/docs/events.html)) and is defined W3C spec
  - No need to CALL the addEventListener,
    - Instead, place the listener in element when it is initially rendered
  - When using Class Components, the event handler is a method in that Class
  - In JS, Class Methods are NOT bound by default
    - If a method is referenced ( where the name of the function is addressed without the “( )”), it needs to be binded using: .bind(this);
  - It is recommended to do the binding in the constructor or use the class fields syntax to avoid issues
- Passing Arguments…

<span style="text-decoration:underline;">Conditional Rendering in React</span>

- Ternary Operator
  - Per MDN: `condition ? exprIfTrue : exprIfFalse`
  - Where condition is the expression that will be evaluated
  - Expression if true means that the expression in the condition evaluates to truthy value (this means that it is ABLE to eval to true)
    - Truthy Values are values that are considered True:
      - All values other than falsy values
  - Expression if false means that the expression in the condition evaluates to falsy value (it is able to evaluate to false)
    - Falsy Values are values that are considered False:
      - Null
      - NaN
      - 0
      - “” - empty string
      - Undefined
- Conditional Rendering
  - Create distinct components to encapsulate needed behavior
    - Render only some of them depending on State
  - Use if/conditional operator
    - Create elements representing the CURRENT State
    - allow React to update UI to match them
- Element Variables
  - Elements can be stored in variables
    - This allows you to, conditionally, render only parts of component while the output as a whole will not change
- Embedded JSX expressions
  - Wrapped in curly braces
  - You can embed inline conditional expressions to include an element...conditionally
  - MDN Docs (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators)
    - Logical operators: &&, ! , | |
  - Using && in react
    - In JS
      - True-value && expression will eval to expression.
        - React will act on that expression
      - False-value && expression will eval to False
        - React will ignore that expression
  - Inline if-Else with Conditional Operator
    - condition ? true : false
  - Decide what is most READABLE

<span style="text-decoration:underline;">React Tutorial through Developer Tools</span>

- I downloaded the React extension to my Chrome Dev Tools

<span style="text-decoration:underline;">React Bootstrap v1.5.2(4.6)</span>

- It is a front-end framework, rebuilt for React
- Import Components individually vs entire library
- Bootstrap Layout: grid system and media obj. [https://react-bootstrap.github.io/layout/grid/](https://react-bootstrap.github.io/layout/grid/)
  - FlexBox:[https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
- Bootstrap doc for all components : [https://react-bootstrap.github.io/components/buttons/](https://react-bootstrap.github.io/components/buttons/)
  - From alerts to modals to toasts using Bootstrap

<span style="text-decoration:underline;">Netlify</span>

- Netlify Docs: [https://docs.netlify.com/](https://docs.netlify.com/)
- It is an all in one platform for projects
- Can connect projects from GitHub
- Can connect Git

