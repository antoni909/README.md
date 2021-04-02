# Read-05

## Putting it [React] all together

## [Back to Home Page](../README.md)

## Source Documentation

- [React Docs](https://reactjs.org/docs/thinking-in-react.html)

## The Reading Assignment

Go through the reading material for this class and watch/bookmark the additional resources provided. Prepare an entry for your Readings Notes Repository that summarizes the principal reading topic as though you were presenting the material to someone new to the industry.

## The Reading

- the following is a summary of the though process behind building a React App

1. Step 0: Start with a Mock

- Mock is the design concept of how the app should look

- Have Data ready for use (JSON format is best for me)

1. "Fracture" the UI into a heirarchy of Components

- Create "Boxes" around every component/subcomponent in the Mock layout and give names

- How to know if it is a component or not?

  - Same idea as knowing to create a new function/object or not...
  - apply single purpose principle
  - the data archetecture and components should complement each other, therefore each component should match ONE piece of data in data model (MVC)

  - Last Question: Do I have a Clear Component Heirarchy???

1. Build a Static Version in React

- Note:

  - Static === Props :(

  - Interactive === State :)

- What is the purpose of building a static model?

  - to build a version that takes your data model and renders the UI but has no interactivity!! - (React Docs). It is importatnt to remove interactivity from static version (Props from State)

- How to build a static version??? DO NOT USE STATE - (React DOCS)

  - build components that RE-USE other components and PASS data using PROPS.

    - with Props, you are able to pass data from parent to child component
    - this.props.thingFromParent ; is how the child component will RECIEVE a property from its parent component

- Can build components Top-to-Bottom or vice versa

  - by the end you will have a LIBRARY of usable components that render you data model
  - components will only have render methods
  - the top-most component will have the pure data imported to it.

1. Identify the Minimal Representation of UI State

- Build an Interactive Version, how do I do that?

  - Need to TRIGGER changes to UNDERLYING data model...using State

    - Base Principle: D.R.Y = Do Not Repeat Yourself
  
  - Think of all of the pieces of data and ask/figure out which one is state...

    - you can achieve this by asking yourself:

      - is it passed from Parent using PROPS... no need State then.
      - does it change over time?... no need State then.
      - compute based on other STATE or PROPS in the component?... no need State then.

1. Identify where State should live

- Once you find which components need State, must identify which Component mutates/OWNS the State. How do i figure this out?

  - For EACH State in the app, find:

    - every component that RENDERS based on STATE
    - common owner component
    - common owner or component higher up in the heirarachy
    - If cant find, create a new component where its sole purpose is for holding the State and place it above the common owner component

1. Add Inverse Data Flow

- This is where data is allowed to flow Up and Down the heirarchy, meaning that components at the bottom of the heirarchy need to be able to UPDATE state of components in the upper parts of the heirarchy

1. That is about it, should be done done by this step.

## [Back to the Top of the Page](#-Read-05)

## [Back to Home Page!](../README.md)
