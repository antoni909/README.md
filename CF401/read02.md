# Express

## The Assignment

Review, Research, and Discussion

### What’s the difference between PUT and PATCH?

Both are able to create updates on a resource, however they do so differently.

PUT - idempotent (quality of producing the same result even if the same request is made multiple times)[medium.com](https://medium.com/backticks-tildes/restful-api-design-put-vs-patch-4a061aa3ed0b) is a full resource, meaning that minor changes come with the entire 'prefabricated' resource and not just the minor change.

PATCH - Not idempotent and makes minor changes at the resource location and will not re-attempt the request if it fails.

### Provide links to 3 services or tools that allow you to “mock” an API for development like json-server

- [Insomnia](https://insomnia.rest/)

- [Postman](https://www.postman.com/)

- [Mockapi.io](https://www.mockapi.io/)

### Compare and contrast Swagger and APIDoc.js 1

both can be used to document APIs

[Swagger](https://swagger.io/)

- open source
- test/document APIs

[APIDoc.js](https://apidocjs.com/)

- creates documentation from annotations inline in source code

### Which HTTP status codes should be sent with each type of (un)successful API call?

[W3.org](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html)

1xx - informational
2xx - successful
    200 - okay
    201 - created
    202 - accepted
3xx - redirection
4xx - client error
    400 - bad request
    401 - unathorized
    402 - payment required
    403 - forbidden
    404 - not found
    405 - method not allowed
5xx - server error
    500 - internal server error
    501 - service unavailable

### Compare and contrast SOAP and ReST

both are approaches to online data transmission and define how to build APIs

REST - (respresentation state transfer) is lightweight set of guidlines using HTTP wehre requests can be responded via different formats (JSON,text,XML, etc)[red hat](https://www.redhat.com/en/topics/integration/whats-the-difference-between-soap-rest)

SOAP - (simpe object access protocol) designed so that languages on  different platforms can communicate. Since it uses protocols === rules which leads to longer page loadouts.[red hat](https://www.redhat.com/en/topics/integration/whats-the-difference-between-soap-rest)

### Document the following Vocabulary Terms

Web Server - connects to the internet and supports phsyical data interchange with other devices connected to the internet. Includes software that uses HTTP server that understands urls and HTTP requests and responses.([per MDN](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_web_server))
Express - is a node.js minimalist framework that has createable handlers for HTTP requests, sets ports for web apps, incorporates middleware. Express is unopinnionated therefore it is really flexable in how an app is structured. [per MDN](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)
Routing - requesting data based on specific server endpoints/paths. For example: myapp.com/home or myapp.com/home/data.
WRRC - web request response cycle and is a cycle between servers and clients where clients get served information via a request(GET,POST,PUT,DELETE)[medium.com](https://medium.com/@jen_strong/the-request-response-cycle-of-the-web-1b7e206e9047).

#### Which 3 things had you heard about previously and now have better clarity on?

express.js framework and how it differs/works with node.js
test driven development
npm

#### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

express
web servers/routing
CI/CD and TDD

#### What are you most excited about trying to implement or see how it works?

I want to learn how to incorporate testing into my applications. I believe, at this point that it would improve upon the quality of my code.
