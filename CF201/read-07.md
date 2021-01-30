# Reading-07

## If you wish to exit to the homepage click on the following link to head back to the [homepage](../README.md)

## Reading Assignment is as follows

- From the Duckett HTML book:

  - Chapter 6: “Tables” (pp.126-145)

- From the Duckett JS Book:

  - Chapter 3: “Functions, Methods, and Objects” (pp.106-144)

- Domain Modeling Notes

## Chapter 6 - Tables

1. How to Create Tables - they use grid formats where each block in a grid is called a table cell and structured as follows:
    1. Table tag - used to create a table startf
    1. Width attribute - how wide some tables should be
    1. Cell padding attr - add space inside each cell
    1. Cells spacing attr - give space between each cell
1. Thead tag - contents of the table headings go inside the ‘table heading’ tag
1. Table head - similar to td tag but it is used for the heading for column or row
    1. Scope attribute - indicates if column or row
    1. Width attribute - how wide that column should be
1. Table body - the main table body should fit inside this element
1. Table row - indicates start of each row (left to right) 
1. Table data - is the ‘cell’ in the row, cells run left to right
    1. Colspan attribute - indicate how many columns that cell should run across
    1. Rowspan attribute - cell spans down into multiple rows
1. Table footer - content like totals, should fit inside the footer tag

## Chapter 3 - Functions Methods and Objects

1. Creating an Object: Constructor Notation
    1. How to create a blank object - use the **_new _** keyword and the **_Object()_** constructor, next you can add properties using dot notation, example:

        var hotel = new Object();
        hotel.name = 'Monarch';
        hotel.rooms = 40;
        hotel.booked = 1;
        hote.checkAvail = function(){
        return this.rooms - this.booked;
        };

    1. To update/delete/clear value of properties

        hotel.name = ‘MonarchTwo’’;
        delete hotel.name;
        hotel.name = ‘ ’;

1. Creating Multiple Objects: Constructor Notation - Use a function as template for creating objects. First letter is Uppercase in Constructor Function name

    1. Create template with objects properties/methods:
        function **Hotel**(name,rooms,booked) {
        hotel.name = name;
        hotel.rooms = rooms;
        hotel.booked = booked;
        hotel.checkAvail = function(){
        return this.rooms - this.booked;
            }
        }
    1. Create instances (some version made from the original) using the constructor function using keyword: **_new _**and the object constructor **_ Object()_** _where properties of each object are given as arguments to the function, in this case Hotel._  
        1. Var parkHotel = **new** Hotel(‘Park’, 40, 1);
1. RECAP: 1 Ways to Create Objects
    1. My fav :) → Create an Object With Properties & Methods
        1. Step 1: LIteral Notation
            1. Object is created then properties and methods are added after
            1. use: **new Object();**to construct a new object and add/rem accordingly  using **object **name
        1. Step 1: Object Constructor Notation
            1. Object is created then properties and methods are added after, key value pairs use comma 
            1. A function is used to create multiple object and **this** keyword is used instead of object name
    1. Create the Object, Then add properties & methods
1. **This** - it is a keyword used inside functions and objects. **_ Where _**a function is declared alters what the keyword refers to. It always refers the one object in which the function operates
    1. Function in Global Scope  
This means that the function is in a free global context = default object = default context = window object 
So, if the **this** keyword is used it is referring to the window object/ global object
    1. Function as a Method of an Object 
When the keyword **this** is used in a method, it refers only to the container object note, for example using : this.width*this.height would be the same as shape.width*shape.height if the name of the object is shape. 
If you were creating multiple objects using an object constructor, this would refer to the specific instance of the object that contains it
    1. Function Expression as a Method 
Read further docs on this topic
    1. Global Variables 
_All_ global variables become properties of the window object, this is why when a function is in the global context, you can access global variables using the window object , as well as other properties.
1. When accessing store data which is better to use an Object or Array?  
If need to use name or key → Object 
If order is important use → Array
1. Data can be stored in vars, arr, single or multiple objs
    1. Individual objects: 
Order is not important for storing data, use object literal notation where properties /methods are given in curly braces:

        var hotel = {
          name: ‘jack’,  
          age: 40,  
          height: 1
          };

        1. To access this data use dot notation for example: 
hotel.name //retrieves the string ‘jack’

    1. Multiple Objects:
        1. Objects created with constructors are best when many objects w/ similar functionality (multiple instances within a page) 

Use a template that can be used for multiple objects using an **object constructor** : 
 
        function MyObjectTemplateName(param1, param2) ( 
	      this.param1 = param1;
	      this.param2 = param2;
        )

        → followed by the instances(the multiple iterations of the above function that created the original template) you can add/clear/rm properties/methods 
 
        var objectInstanceOneName = new MyObjectTemplateName (argument1, argument2);
        1. To access data properties/methods use dot notation

1. Arrays _are_ special objects where in the key:value pair, the key is the Zero-Index-based value, both have similar structures: 

        Object:  object = {name1:value1, name2:value2, name3:value3}; 

        Array: array = [value1, value2, value3]; and key → zero-based  

1. Arrays and Objects - both can be combined to create complex data structures
    1. Objects of Arrays - objects can hold arrays as values of their properties
        1. Object properties can hold arrays and can access them using the dot chain notation and an array value can be accessed via its index number
    1. Arrays of Objects - arrays can store a series of objects in order
        1. The value of an element in an array can be an object, to access you use the index value of the array followed by dot notation
1. What are Built-in Objects? - know what tools are available
      1. Browser Object Model
            1. Topmost object is the window object = current browser/tab and its child objects which represent other browser features
            1. Window Object - page 124 
      1. Document Object Model
            1. Creates a model of the current web page and the Document Object is the topmost object
      1. Global JavaScript Objects
            1. NOT a single model instead it is a GROUP of individual objects
            1. String Object- when working with data type: string, you can access the methods of the global object String
            1. Number Object - You can use the following methods when working with numbers:
                  1. isNan
                  1. toFixed
                  1. toPrecision
                  1. toExponential
            1. Math Object - pg 134
            1. Date/time Object
                1. Creating an Instance of the Date Object
                    1. Step 1 : create an Instance of global Date Object

                    1. Step 1 : specify date/time by passing arguments into the date constructor Date(args...);
1. Data Types → 1 in JavaScript
Note: Undefined and Null values do not have objects
  1. Simple
        31. String
        32. Number
        33. Boolean
        34. Undefined is declared but no value is assigned...yet/ever
        35. Null is var with no val..could have been but lost its val somehow...
  1. Complex
  1. Object
        -arrays are objects 
        -functions are objects

## Do you wish to exit to the homepage? click on the following link to head back to the [homepage](../README.md)

## Or do you want to go to the [top of the page?](#Reading-07)

### Domain Modeling Notes

What is it? 
create concept model that a solution to ONE problem
Describes:
Various entities and entity attributes/behaviors
Constraints to Problem Domain
Essentially this is Object-Oriented model
Object Oriented model
Entity stores data ---> properties
Entity encapsulates behavior → methods
Define Constructor Function & Initialize Properties
Build ‘self-contained’ Objects
With same attributes and behaviors 
This way, if algorithm changes you only have to make small changes


Example EpicFailVideo Constructor FUNCTION 
var EpicFailVideo = function(epicRating, hasAnimals) {
    this.epicRating = epicRating;
    this.hasAnimals = hasAnimals;
} //parameters stored inside this.epicRating, this.hasAnimals
var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);
//when function called: parameters are stored in this.epicRating and this.hasAnimals
//Data must be stored inside this.x to ensure other objects can access data
console.log(parkourFail);
console.log(corgiFail);
// result
EpicFailVideo {epicRating: 7, hasAnimals: false}
epicRating: 7
hasAnimals: false
EpicFailVideo {epicRating: 4, hasAnimals: true}
epicRating: 4
hasAnimals: true
Key understanding:
the new keyword instantiates = creates an object
constructor function initializes properties inside that object using this 
object stored in a var for later/subsequent use
Generate random numbers
random number models random user behavior
Prototype = an object’s stunt double..like a substitute for original object
Methods can be added to constructor function prototype 
How Objects Find Methods: 
Object asked to run a method → 
object cannot find method in own set of methods → 
object searches Prototypes methods → 
Object finds methods in Prototype →
Object calls method and passes argument → 
the method called runs and returns  
When prototypes are shared among 2 or more objects, those objects execute the same code when that method is called from the prototype so shared code → prog consume < mem → good for all types device
In Summary:
When modeling ONE entity build self-contained objects with same attributes/behaviors → Model attributes with Constructor Function that define + initialize properties → Model behavior with one-task oriented methods → create instances with new keyword + call to constructor function → store that new object in a var to access its properties/methods from ‘outside’ → use this  var within methods to access object’s properties/methods from inside

