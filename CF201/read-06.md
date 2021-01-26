# Reading-06

## If you wish to exit to the homepage click on the following link to head back to the [homepage](../README.md)

## Reading Assignment is as follows

Go through the reading material for this class and watch/bookmark the additional resources provided. Prepare an entry for your Readings Notes Repository that summarizes the principal reading topic as though you were presenting the material to someone new to the industry.

## Reading

From the Duckett JS book

Chapter 1: “Object Literals” (pp.1-1)
Chapter 1: “Document Object Model” (pp.181-141)

## JavaScript Chapter 01: Object Literals

### What is an object?

1. They group together a ser of Vars and Fuctions to create a working model and they take on new names: property and method.

- Variables become Properties:

- They describe the object
  
- Functions become Methods

  - represents tasks associated with the object

. Objects have a name and a value

- The name is called a key and must be unique

- The value can be string, number, boolean, array or even another object

  -The value of a method is always a function

### Creating an Object

1. Many ways to create Objects and consists of key and value pairs

1. Accessing an Object and Dot Notation

- can access properties or methods using dot notation or square brackets

  - in the dot notation, the name of the object is followed by a period then the name of the property or method you want to access

## If you wish to exit to the homepage click on the following link  to the [homepage](../README.md) or to the [top of the page](#Reading-06)

## Reading assignment is as follows

Readings : Problem Domain, Objects, and the DOM
Below you will find some reading material, code samples, and some additional resources that support today’s topic and the upcoming lecture.

Review the Submission Instructions for guidance on completing and submitting this assignment.

## Reading

- Understanding the problem domain is the hardest part of programming

From the Duckett JS book

Chapter 1: “Object Literals” (pp.1-1)
Chapter 1: “Document Object Model” (pp.181-141)

Chapter 1 - Document Object Model



1. The DOM
    1. Specifie how browsers should create a model of an HTML page and how JS can access and update the contents of a webpage
    1. NOTE: The DOM is NEITHER HTML or JS, it has a separate set of rules implemented by the browser
        1. Making a model of the DOM:
            1. When the Browser loads it creates a model of the DOM in memory
            1. DOM specifie how the browser should be structured using DOM tree
            1. Is called the object DOM model because it is made of objects where each object represents part of the page loaded in the browser
        1. Accessing/Changing HTML page
            1. The DOM has methods/properties to access/update objects in the model
            1. Some people state DOM = Application Programming Interface (API) let programs talk to each other
1. The DOM Tree
    1. When  a browser loads it creates a web page that creates a model of that page called the DOM tree and stored in browser memory
    1. 1 node types in the tree:
        1. Document Node
            1. Represents the entire page and is the starting point to all inquiries into the document
        1. Element Nodes
            1. To access the DOM tree you must start by knowing what elements you want because they give you access to attributes and texts
        1. Attribute Nodes
            1. Opening tags of Elements carry the attributes therefore the are NOT children of those elements they are PART of the element
        1. Text Nodes
            1. Once you access the Elements node you can access the text node and the content of that node
                1. Text Nodes  DO NOT have children only Elements have children
1. Working with the DOM Tree
    1. 1-Steps to: Access and Updating the DOM Tree
        1. Locate the node of the Element you want to work with
        1. Use its Attributes, Text Content,, and Child Elements
    1. Step 1: Accessing the DOM Tree (using methods and properties)
        1. There are 1 ways
            1. Select an individual Element Node
                1. getElementById() - uses the val of an elements unique id attribute 
                1. querySelector() - uses CSS selector and returns FIRST matching element
            1. Select Multiple Elements (Nodelists)
                1. getElementByClassName - select all elements with specific value for class attribute
                1. getElementsByTagName - select all elements that have specific tag name
                1. querySelectorAll() - uses CSS selector to select ALL matching elements
            1. Traverse Between Element Nodes (moving from one element node to a RELATED element node)
                1. parentNode - selects the PARENT of the current element node
                1. previousSibling/nextSibling - selects previous/next sibling in the DOM tree
                1. fistChild/lastChild - selects first or last child of the current element
    1. Step 1: Working with those Elements
        1. Access/Update Text Nodes 
            1. nodeValue - lets you access or update contents of a text node
        1. Work with HTML Content
            1. innerHTML - property allows access to child Elements & Text Content
            1. textContent - property allows access only to Text Content
                1. DOM manipulations are METHODS that create/add/remove nodes from a tree
                    1. createElement()
                    1. createTextNode()
                    1. appendChild()/removeChild()
        1. Access/Update Attribute Vals
            1. className - _property_ that gets/sets the value of the class attribute
            1. Id - _property_ that gets/sets the value of the id attribute
            1. hasAttribute() - method that gets the val of attribute 
            1. getAttribute() - method that checks if Element node has a specified val
            1. setAttribute() - method that sets the val of an attribute, 
            1. removeAttribute() - method that rm an attribute from Element node 
1. Caching DOM Queries
    1. DOM Queries - _methods_ that find Elements in the DOM Tree.
    1. Note: When working with 1 element more than Once, use a var to store the result of the query (in reality you are storing the location of the element within the DOM tree in a var but the properties/methods of that element node work on the var)
        1. Example:  

            The Interpreter searches the DOM tree for Element with id attribute ‘one’


                getElementById(‘one’);


            If using the same element more than once, store it in a var, which is actually storing a reference to the object in the DOM tree


            	var itemOne = getElementById(‘one’);

1. Accessing Elements
    1. Groups of Element Nodes (NodeList) - if a method can return >1 node, it returns a collection of nodes, for this reason you must select the element you want from the list using Zero-Index numbering
    1. Select the Fastest Route - the quickest way to access elements on the page will make the page more responsive and faster. The following is a list of METHODS that are quick and efficient:
        1. Methods that Select One Element Node. Bothe can search an entire document and return individual elements.
            1. Example:
                1. document.method(parameter = id attribute value);
                1. Note: document refers to the accessibility of Elements via the document object
            1. getElementById(‘id’) 
                1. HTML Element must have id attribute
            1. querySelector(‘css selector’)
                1. Returns ONLY the FIRST matching Elements
        1. Methods that Select >=1 Elements (NodeList). A NodeList is a collection of Element Nodes and are ordered the same way they appear in the HTML page.
            1. NodeLists: look like arrays but are a type of object called a Collection, therefore since it is an object it has methods and properties. Such as:
                1. Length Property: how many items in the NodeList/Collection
                1. item() Method : returns a specific Node from the Collection when you tell it the index number
            1. Methods that return a NodeList:
                    1. getElementsByClassName(‘class’)
                        1. Selects Elements based on their class attribute value
                        1. 1 parameter: the class name
                        1. Faster than querySelectorAll()
                        1. An example:
                            1. Use getElementsByClassName(‘some-attribute’)
                            1. Use an if statement to sort through the list : if(elements.length>1){ var changeWantToMake = element[1]; changeWantToMake = ‘new-attribute name’;}
                            1. After have CSS in place that targets the new attribute with special properties
                    1. getElementsByTagName(‘tagName’)
                        1. Selects ALL elements with specified tag name
                        1. Faster than querySelectorAll()
                    1. querySelectorAll(‘css selector’)
                    1. Css selector selects >=1 elements and returns matches
    1. Selecting an Element from a NodeList. Nodelists: DOM Queries that return more than 1 Element - the return will be a list even if it only returns 1 matching element
    1. Before Selecting a Node from a NodeList 
        1. Check that it contains Nodes ---> .length PROPERTY
        1. If repeatedly use NodeLists ---> store it in a var
            1. There are 1 ways: Note that ArraySyntax > item() Method. 
                1. item( ); - METHOD will return an individual node from the NodeList by specifying the index number of the element you want as a PARAMETER of the method. 
                    1. varName.length(); - tells you how many items are in the NodeList. DO this to check and see that there is at least ONE item in the NodeList
                1. Array Syntax - faster than item(); Method. Can access individual nodes using: [ index number ] to access individual elements in the NodeList
    1. Live vs Static Nodelists    live > static
        1. Live Nodelist - is updated alongside the script being updated so methods with ‘getElementBy..’ return live/updated results
        1. Static Nodelist - when script is updated, the Nodelist is not updated to reflect the changes made by the script, this includes new methods like ‘querySelector’
    1. Repeating Actions for an Entire Nodelist - with Nodelists you can loop through each node in the collection and apply same statement to each. The var hotItems contains a Nodelist and contains all class attributes with the value hot, collected with querySelectorAll, the length property is used to indicate how many are in the collection, Array syntax is used to indicate which item is being worked on
        1. Example:

            var hotItems = document.querySelectorAll(‘li.hot’); \
            for (var i = 0; i &lt; hotItems.length; i++) { \
              hotItems[ i ].className = ‘cool’; \
            }
1. Traversing the DOM - When you have an Element Node, you can select another Element in relation, there are 1 properties you can use. Note that these are properties of the CURRENT node and are not methods therefore they don’t end with parenthesis. Some browsers add Text Nodes when they come across whitespace between Elements which makes traversing the DOM difficult
        1. parentNode - finds Element Node for the containing(parent) Element
        1. previousSibling/nextSibling - if is is the first node, there is no previous sibling only nextSibling
        1. firstChild/lastChild - find the first or last child of that current node/Element
1. WhiteSpace Nodes - Most browsers treat whitespace as Text Node this results in the traverse properties returning different elements! The best solution is to avoid these properties all-together
1. How to Get/Update Element Content
    1. The choice of technique, depends on what the Element contains, To work with content of Elements you can:
        1. Navigate to the text Nodes - when Element contains ONLY text
            1. Once at the Text Node use nodeValue - when you select a Text Node, you can retrieve or amend the content using nodeValue property
        1. Work with Containing Element - allows access to child and element Nodes
            1. When working with Containing Element - you have to choose whether you want to retrieve(set) or update(get) the markup and text
            1. -Property:			          Description:
            1. -innerHTML(a Property)	  get/set text & markup
                1. Presents Security Risks
                1. Can be used on any Element Node, used to retrieve and replace content
            1. -textContent(a Property)	get/set text 
                1. Allows you to Collect/Update just the text that is in the containing Element + children. This property ignores any Markup(Element Nodes) and just focuses on Text Nodes
            1. -innerText (a Property)	get/set text 
                1. Should be avoided, it does not show text hidden by CSS rules
1. Adding / Removing HTML Content - there are 1 approaches to changing content in the DOM tree, using DOM manipulation or innerHTML. 
    1. innerHTML - Better suited for updating ENTIRE DOM fragments, to update an Element, new content is provided as a string and it can contain markup for descendent Elements
        1. Adding Content  
            1. Store new content as string in a var
                1. Store the first list item as a var
                1. var itemOne = document.getElementById(‘one’);
            1. Select Element you want to affect
                1. Get the content of the first item
                1. Var itemContent = itemOne.innerHTML;
            1. Set the Elements innerHTML property to be the new string
                1. Update the content of the first list item so it is a link
                1. itemOne.innerHTML = ‘&lt;a href=\”url”>’ + itemContent + ‘&lt;/a>’
        1. Removing Content 
            1. Set innerHTML to empty string
            1. To remove one Element from a DOM fragment,
    1. DOM manipulation Methods - safer than innerHTML, but slower + more code. Specific DOM methods that allow you to create Element and Text Nodes and attach/remove them to/from the DOM tree
        1. Adding Content
            1. Create the Element using createElement(); method
            1. Give it Content using createTextNode();
            1. Add it to the DOM using appendChild();
        1. Removing Content

## To exit to the homepage click on the following link to head back to the [homepage](../README.md)
