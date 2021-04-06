# Read-06

## Reading: Node.JS

Below you will find some reading material, code samples, and some additional resources that support today’s topic and the upcoming lecture.

Review the Submission Instructions for guidance on completing and submitting this assignment.

## Reading

[An Introduction to Node.js on sitepoint.com](https://www.sitepoint.com/an-introduction-to-node-js/)
6 Reasons for Pair Programming

## Bookmark/Skim

[Geocoding API Docs](https://locationiq.com/)
[Axios docs](https://www.npmjs.com/package/axios)
[MDN async and await](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Async_await)

## An Introduction to Node.JS from sitepoint.com

- What is node and when to use it?
 built on google chromes V8 js engine, this allows for JavaScript to be run on our computers, this is called JavaScript runtime

- How to install Node and using npm

  - Node Binaries versus Version Manager
  version manager allows you to install multiple versions of Node to allow you to switch between them seemlessly.
  
  - node --version
  tells you what version of node is on computer

  - node has support for ES6 and over allowing you to use the latest/modern JS syntax, such as template liters, object destructure, new array methods, etc

  - Installing:
    - npm install -g jshint  this installs globally
    - npm init -y            this installs locally

  - Working with package.json files
    - node_modules is a folder where npm saves lodash and lodash dependencies
    - [npm how-to for beginners](https://www.sitepoint.com/npm-guide/)

- What is node used for?

  - node with npm are used to automate the process of developing js apps
    - npm for install
    - node for building tools
  
  - build tools that bundle js files/dependencies to static assets, run tests, automatic linting, style check etc.
  - some resources:
    - [webpack guide](https://www.sitepoint.com/webpack-beginner-guide/)
    - [ESlint for JS](https://www.sitepoint.com/up-and-running-with-eslint-the-pluggable-javascript-linter/)
    - [intro to Gulp](https://www.sitepoint.com/introduction-gulp-js/)
    - [unit test JS using mocha/chai](https://www.sitepoint.com/unit-test-javascript-mocha-chai/)
  - Modern Frameworks like React/Angular rely on node as a sensible environment to run on
    - [Modern JS apps](https://www.sitepoint.com/anatomy-of-a-modern-javascript-application/)

- Node.js on the server and its Execution Model

  - Node runs single thread
  - The Execution
    1. Node apps pass (async tasks + callback) to event loop
    2. event loop manages "thread pool" and executes tasks
    3. event loop executes each callback as tasks get completed

- Downsides?
  - blcoking I/O calls should be avoided
  - errors should be handled correctly
  - call back are messy
    - Solution to this are Promises and Asynch Await

- Running a Server using Node:
  - uses Node's native HTTP module + createServer() method of that module
  - this creates a new web-based server OBJECT
  - this object passes anonymous function that is invoked for every NEW connection made on the serverf
    - anonnymous funciton called using request and response arguments
  - Tell the server to listen to incoming requests on PORT 3000
    - [docs on running server](https://nodejs.org/en/docs/guides/anatomy-of-an-http-transaction/)
    - [tutorial](https://www.sitepoint.com/build-a-simple-web-server-with-node-js/)

- What apps work best with node ?

  - real time interaction/collaboration
    - chat sites, handling mulitple requests, data streaming
  - [build/structure a NODE APP](https://www.sitepoint.com/node-js-mvc-application/)

- Advantages of Node.js
  - speed
  - scalability
  - same language front and back, server and client
  - speaks JSON
  - ubiquitous

### [back to top](#-Read-06)

### [back to home page](/README.md)

## Axios

- Features
  - make XML HTTP requests from browser or node.js
  - supports Promise API
  - intercepts or transforms or cancel requests/response
  - automatic transforms to JSON data formata
  - Support for protecting against XSRF

- Installing
  - using npm
    npm install axios
  - using jsDelivr CDN
    \<script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>
  
- Example usage
  - retrive axios and its methods using require method
    \const axios = require('default').default;
  
  - Performing GET request
    - make a request for a user with a given ID

      \axios.get('/user',{
        params: { 
          id: 12345
         }
      })
      .then( function(response){ console.log('response');} )
      .catch( function(error){ console.log( 'error' ); } )
      .then( function(){ //code here will always execute })
      };
      - OR make a request using async await instead

        \async function getUser(){
          try{
            const response = await axios.get('/user?id=12345');
            console.log(response);
          } catch (errror) {
            console.log(errror);
          }
        }

  - Performing a Post Request
  - Performing Multiple Requests

- Axios API
  - requests can be made by passing relavent configs to axios
- Request Config
  - there are availble options for making requests where only the URL is needed
  - requests default to GET if method is not specified



## (source: MDN) Asynchronous Programming using Asynch and Await

- Basics of Asynch and Await

  - to turn into an async function the async keyword is placed in front of a function declaration and this means that it is expecting the await keyword too.
  - async functions return values are guaranteed to ve converted to Promises
  - can use arrow function notation
  - the .then() is used to "consume" the return value of promises
  - async tells functions to return a promise RATHER than a direct value
  - await keywork only works with async functions

### [back to the top](#-Read-06)

### [back to the home page](/README.md)
