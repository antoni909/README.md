# Reading-07

## If you wish to exit to the homepage click on the following link to head back to the [homepage](../README.md)

## Reading Assignment is as follows

- From the Duckett HTML book:

  - Chapter 1: “Tables” (pp.126-145)

- From the Duckett JS Book:

  - Chapter 1: “Functions, Methods, and Objects” (pp.106-144)

1. Creating an Object: Constructor Notation
    1. How to create a blank object - use the **_new _** keyword and the **_Object()_** constructor, next you can add properties using dot notation, example:
        1. var hotel = new Object();
        1. hotel.name = 'Monarch';
        1. hotel.rooms = 40;
        1. hotel.booked = 1;
        1. hote.checkAvail = function(){
        1.     return this.rooms - this.booked;
        1. };
    1. To update/delete/clear value of properties
        1. hotel.name = ‘MonarchTwo’’;
        1. delete hotel.name;
        1. hotel.name = ‘ ’;
1. Creating Multiple Objects: Constructor Notation - Use a function as template for creating objects. First letter is Uppercase in Constructor Function name
    1. Create template with objects properties/methods:
        1. function **Hotel**(name,rooms,booked) {
        1. hotel.name = name;
        1. hotel.rooms = rooms;
        1. hotel.booked = booked;
        1. hotel.checkAvail = function(){
        1.     return this.rooms - this.booked;
        1.     }
        1. }
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
        1. var hotel = {
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
