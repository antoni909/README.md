# Read-08

## Readings: APIs

## Documentation for SuperAgent

source content: [SuperAgent](https://visionmedia.github.io/superagent/)

Is a light-weight progressive AJAX API

    -flexible
    -readable
    -low learning curve
    -works witn Node.js

## Request Basics

- make request using request object

- then call using .then() or await to send request
  
- Example:

          request
          .get('/search')
          .then(res => {
          // res.body, res.headers, res.status
          })
          .catch(err => {
          // err.message, err.response
          });

- Can choose request types
  - GET
  - HEAD
  - POST/PUT

## [MDN CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)

stands for Cross-Origin Resource Sharing and is a way of letting browsers know the origin of the request

requests are blocked if request has not opted in to CORS

### [back to the top](#-Read-08)

## RegEx Tutorial

[source content of tutorial](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)


Basics:

        abc               matches all instances of the string
        ^abc              matches characters after the symbol ^
        abc$              matches characters before the symbol $
        ^abc$             matches exact start and end is abc

        abc*              matches string 'ab' that has  0 or more 'c'
        abc?              matches string 'ab' that has  0 or 1 'c'
        abc+              matches string 'ab' that has  1 or more 'c'
        abc{num}          matches string 'ab' and num 'c'
        abc{num,}         matches string 'ab' and num 'c' or more 'c'
        abc{num1,num2}    mathces string 'ab' and num1 'c' up to num2 'c'
        a(bc)*            matches string 'a' and 0 or more copies of bc sequences
        a(bc){num1,num2}  matches string 'a' and num1 'bc' up to num2 'bc' copies of bc sequences

        a[bcd] or a[b-d]  matches string 'a' and b or c or d
        a(b | c)          matches string 'a' and b or c and captures b or c 

        \d                matches single DIGIT character (0-9)
        \w                matches WORD alphanumeric/underscore character ( a-z, A-Z, _ )
        \s                matches whitespace (tabs and lines)
        .                 matches any character

        \D                matches single non-digit character (negates \d)

## Reg Ex tutorial

Practice at:

[regexr](https://regexr.com/)

[regexr 101](https://regex101.com/)

### [to the top](#-Read-08)

### [back to the home page](/README.md)
