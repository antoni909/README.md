# Reading-13

## If you wish to exit to the homepage click on the following link to head back to the [homepage](../README.md)

## Local Storage Native Apps vs Web Apps

1. for native apps, the os provides abstraciton for storinga and retrieving data such as preferences/runtime. Can come up with solutions for more advanced storage

1. for web apps, this was not applicable

## Storage before HTML5

1. All solutions for data storage were third party and accessible through only one browswer. "HTML5 standerdizes API, implemented natively and consistently across multiple broswers" \(Mark Pilgrim, Dive into HTML5)

## Introducing HTML5 Storage

1. HTML5 Storage \== DOM storage \== Local Storage

1. What is it?

    - it's how web pages store key:value pairs LOCALLY in the client web browser. It is a way of implementing persistent local storage via web app

1. How to access it?

    - via HTML5 global window object locaStorage 

1. Does my browswer support it?

    - 2 ways to check \(methods from Mark Pilgrim, Dive into HTML5)
        \function supports_html5_storage() {
              try {
                return 'localStorage' in window && window['localStorage'] !== null;
              } catch (e) {
                return false;
              }
            }
        \if (Modernizr.localstorage) {
            // window.localStorage is available!
          } else {
            // no native support for HTML5 storage :(
            // maybe try dojox.storage or a third-party solution
          }

1. Storage is based on key:val pairs --> data based on named key --> retrieve data with name key 

    - data types can be strings, booleans, integers or floats but all data is stored as a string and must coerce other data types 

1. Using localStorage object Example \(from methods from Mark Pilgrim, Dive into HTML5)

        Calling setItem() with a named key that already exists will silently overwrite the previous value. 
        
        Calling getItem() with a non-existent key will return null rather than throw an exception.

            \var foo = localStorage.getItem("bar");
            localStorage.setItem("bar", foo);

        Instead of using the getItem() and setItem() use square brackets:
       
            \var foo = localStorage["bar"];
            localStorage["bar"] = foo;

        Deleting all key:val pairs

            \interface Storage {
            deleter void removeItem(in DOMString key);
            void clear();
            };
        Getting total number of vals in storage and iterating through all keys by index

            interface Storage {
              readonly attribute unsigned long length;
              getter DOMString key(in unsigned long index);
            };

1. Tracking Changes to HTML5 Storage Area

1. HTML5 limitations
    1. 5 megabytes - all data stored as strings
    1. QUOTA_EXCEEDED_ERR - exception thrown when data > 5 megabytes
    1. no - no you cannot ask for more space

1. other options versus HTML5 storage

    - Indexed Database API

    - SQL
