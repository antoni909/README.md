# Express REST API

## The Assignment

Review, Research, and Discuss

### Name 3 real world use cases where you’d want to change the request with custom middleware

- make requests more efficient when making requests to database with some query

- to save time/resources when processing request object

- might want to store/verify certain properties of request object

### True or false: The route handler is middleware?

false because they are more closely defined as handler functions

### In what ways can a middleware function end the process and send data to the browser?

res.end() would end the response process and is used to end the response without any data if need to respond with data use res.send()/res.json()

### At what point in the request lifecycle can you “inject” middleware?

they can be used before or after route handlers

### What can cause express to error with “Request headers sent twice, cannot start a second response”

This error arises when you send more than 1 responses to the user or client. That means the receiver is getting two responses, when it should only be getting one, could be using .send() twice or using res.redirect() before res.send().[fjolt](https://fjolt.com/article/javascript-err-http-headers-sent)

## Document the following Vocabulary Terms

Middleware - in Express, the perform some operation on request or response and call 'next' function which might be another middleware or route handler function. [MDN](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)

They are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. These functions are used to modify req and res objects for tasks like parsing request bodies, adding response headers, etc.[tutorialspoint](https://www.tutorialspoint.com/expressjs/expressjs_middleware.htm)

Request Object - represents the HTTP request and has properties for the request query string, parameters, body, HTTP headers, and so on.[tutorialspoint](https://www.tutorialspoint.com/nodejs/nodejs_request_object.htm)

Response Object - represents the HTTP response that an Express app sends when it gets an HTTP request.[tutorialspoint](https://www.tutorialspoint.com/nodejs/nodejs_response_object.htm)

Application Middleware - these are middleware bound to instance of express using app.use() and app.someVERB()

Routing Middleware - middleware bound by instance of express.Router()

Test Driven Development - refers to a style of programming in which three activities are tightly interwoven: coding, testing (in the form of writing unit tests) and design (in the form of refactoring).[agilealliance](https://www.agilealliance.org/glossary/tdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'tdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1))

Behavioral Testing - is a testing of the external behaviour of the program, also known as black box testing. It is usually a functional testing. [tutorialspoint](https://www.tutorialspoint.com/software_testing_dictionary/behaviour_testing.htm)

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

middleware
express
web request response cycle/ objects

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

middleware
tdd
CI/CD

### What are you most excited about trying to implement or see how it works?

middleware and tdd(for improved code quality)

## Preparation Materials

Review:

[ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

- template for creating objects
- example:
    class someName {
      constructor(propOne, propTwo){
        this.propOne = propOne;
        this.propTwo = propTwo;
      }
      someMethod(){
        someAction = value;
      }
    }
- class declarations are not hoisted(unlike function declarations).
- class declarations have one constructor method (can use super to inherit properties from constructor of parent class)and methods as part of its body.
- instance properties must be defined inside of class methods
- extends keyword is used in class declarations to create a class as child of parent class

[Using Express Routing](https://expressjs.com/en/guide/routing.html)

- how an applications endpoints(URIs) responsd to client requests

- routing is defined using methods inside of Express 'app' object.

- app listens for requests and calls specific method (get,post,etc) and its callback to handle the request

[Express Routing](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)

Router is like a mini express app, it provides routing APIs: .use,.get,.param, and route

- to  call an instance of Router use: const router = express.Router()

- Used for basic routes, middleware, with parameters, middleware with parameters, login routes

© Code Fellows 2021
