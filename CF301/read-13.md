# Read-13

CRUD Reading/Video

[Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

[Build A REST API With Node.js, Express, & MongoDB - Quick](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw)

## Things I want to know more about

- What are REST API's and RESTFUL API's???
  Representational State Transfer(REST) is a standard style for a specific type of API. Allows for 'HTTP Services'.
  - Rest API's are standardized, stateless, scalable
  - High Performance because they support Caching
  API's are about communication, how servers talk to each other
  RESTFUL are services that use REST APIS
  - apply CRUD principle to Request Object using HTTP Methods/Operations
    Create --> POST
    Read   --> GET
    Update --> PUT
    Delete --> DELETE
    - the different parts of an Request Object
        Header - can have api keys, authentication data
        Operation(HTTP METHOD: POST,GET,PUT,DELETE)
        Endpoint
        Param/Body - data sent in request
    - the different parts of an Response Object
- How to use REST client on VScode

## Status Codes Based On REST Methods

In your own words, describe what each group of status code represents:
100’s = client request will fail
200’s = successful validation requirements
300’s = resource is not available anymore
400’s = invalid client request to server
500’s = server not responding

What is a status code 202?
A: in asynchrounous processing , a 202 code means that the request was sent successfuly

What is a status code 308?
A: is a Permanent Redirect, used when the resource has moved to a different URL and the client can be notified

What code would you use if an update didn’t return data to a client?
A: 204 No Content

What code would you use if a resource used to exist but no longer does?
A: 410 Gone

What is the ‘Forbidden’ status code?
A: when clients cant access every resource, the client has not permission to access the resource

CREATE ----> using HTTPs POST method
these are endpoints

  - used to create NEW resources or access tokens

READ ----> using HTTPs GET method
used to fetch resources

UPDATE ----> PUT or PATCH method
which one is used depends on the amount of data the client is sending the server

PUT - replace the entire old version with the new version
PATCH - add,update,delete certain parts of the old version

  - 204 means no Content
  - 202 means Accepted

DELETE ----> uses the DELETE method

## Build A REST API With Node.js, Express, & MongoDB

### Why do we need to pull our MongoDB database string out of our server and put it into our .env?

A: when we deploy our application,we have our mongoDB url visible in our server.js app, we also want to use something that is not our localhost,so we place it in env file and create a variable for it.

### What is middleware?

A: generally, it is code that is designed to link two seperate applications. It runs once the server gets a request, but before it get passed to the routes

app.use() allows you to use middleware

### What does app.use(express.json()) do?

A: sets up server to accept JSON
from [stack overflow](https://stackoverflow.com/questions/23259168/what-are-express-json-and-express-urlencoded#:~:text=a.-,express.,application%20using%20the%20code%3A%20app.&text=urlencoded()%20is%20a%20method,Object%20as%20strings%20or%20arrays.)

basically, it is middleware code, and it is a method used in express that will accept the incoming Request Object as a JSON Object. It is part of the bodyParser([options])

### What does the /:id mean in a route?

A: the colon in front of id means that it is a parameter, can access by typing req.params.id, this will give you access for whatever gets typed after the slash

### What is the difference beween PUT and PATCH?

A: patch only updatas based only on what the user passes, for example if they pass just the name it will only update the name, whereas PUT changes everything

### How do you make a default value in a schema?

A: they can be defined with a function inside the Schema or with a value

### What does a 500 error status code mean?

A: there was a problem with server and not the client

### What is the difference between a status 200 and a status 201?

A: used with POST route, it means create was sucessful

### [top of page](#-Read-13)

### [home page](/README.md)
