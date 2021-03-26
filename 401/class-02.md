# Express

## Terms:
<dt><abbr title="Node Package Manager">NPM</abbr></dt>
<dd>npm is the world's largest software registry. Open source developers from every continent use npm to share and borrow packages, and many organizations use npm to manage private development as well.

npm consists of three distinct components:
* the website
* the Command Line Interface (CLI)
* the registry</dd>
<dt>Web Server</dt>
<dd>A web server is a software that uses <abbr title="Hypertext Transfer Protocol">HTTP</abbr> and other protocols to respond to client requests made over the World Wide Web. The main job of a web server is to display website content through storing, processing and delivering webpages to users.</dd>
<dt>Express</dt>
<dd>Express is the most popular Node web framework, and is the underlying library for a number of other popular Node web frameworks.</dd>
<dt>Routing</dt>
<dd>Routing defines the way in which the client requests are handled by the application endpoints.

Simple routing for GET request use app.get() method:

```js
var express = require('express')
var app = express()

app.get('/', function(req, res) {
    res.send('Hello Sir')
})
```

</dd>
<dt><abbr title="Web Request/Responce Cycle">WRRC</abbr></dt>
<dd>Web request response cycle, details how information moves between client/server</dd>
<dt><abbr title="Test Driven Development">TDD</abbr></dt>
<dd>

- Refers to a style of programming in which three activities are tightly interwoven: coding, testing (unit tests) and design (refactoring)
- Can be described by this set of rules:
  - Write a single unit test describing an aspect of the program
  - Run the test, which should fail because the program lacks that feature
  - Write just enough code, the simplest possible, to make the test pass
  - Refactor the code until it conforms to the simplicity criteria
  - Repeat, accumulating unit tests over time

</dd>
<dt><abbr title="Continious Intergration">CI</abbr></dt>
<dt><abbr title="Continious Development / Continious Deployment">CD</abbr></dt>
<dd>

- Continuous Integration/Continous Delivery
- Continuous Integration(CI) ensures everyone's changes integrate with current version of project, catch bugs, and reduce merge conflicts
- Continuous Delivery (CD) is the practice of developing software in such a way that you could release at any time
- Continuous deployment is extension of continous delivery, process that allows you to deploy newly developed features into production

</dd>

## Questions:
1. What’s the difference between PUT and PATCH?

They both are used to update data in the database, PUT overrides the existing element with the new data, while PATCH edits just the given property without modifying any other properties.

2. Provide links to 3 services or tools that allow you to “mock” an API for development like json-server

    1. [MongoDB](https://www.mongodb.com/)

    2. [Firebase](https://firebase.google.com/)

    3. [Postman](https://www.postman.com/)

3. Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?
- Info from MDN [here](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)
  - Informational responses (100-199)
  - Successful responses (200-299)
  - Redirects (300-399)
  - Client errors (400-499)
  - Server errors (500-599)

4. Compare and contrast SOAP and ReST
- SOAP (Simple Object Access Protocol) is a standards-based web service communication protocol, relies exclusively on XML to provide messaging services
- REST (Representational State Transfer) is another standard, made in response to the shortcomings of SOAP, and to create a simpler method of accessing web services
- REST is most commonly used when exposing a public API over the internet while SOAP exposes components of application logic as services rather than data
- REST accesses data while SOAP performs operations through more rigid set of messaging 
- Benefits of REST over SOAP: uses HTTP for simplicity, allows greater variety of data formats, generally faster and uses less bandwidth
- Benefits of SOAP over REST: if you need more security, offers built-in retry logic for failed communications, highly extensible through other protocols and technologies
- Comparisons of REST versus SOAP from [SmartBear](https://smartbear.com/blog/soap-vs-rest-whats-the-difference/) and [Stackify](https://stackify.com/soap-vs-rest/)