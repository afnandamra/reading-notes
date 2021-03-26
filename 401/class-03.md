# Express REST API

## Review, Research, and Discussion:

1. Name 3 real world use cases where you’d want to change the request with custom middleware
    - Authentication
    - Error handling
    - Data management
2. True or false: The route handler is middleware?

False, a route handler is the piece of code that makes an HTTP request, such as `GET`, `POST`, `PUT`, and `DELETE`.

3. In what ways can a middleware function end the process and send data to the browser?

Middleware functions are not supposed to end the process. They use a method called `next()` which passes things off to the next middleware in the chain. Also, middleware in and of itself does not send data to the browser. However, when the browser (the client) makes a request to the server, the middleware will modify what the response data will look like.

4. At what point in the request lifecycle can you “inject” middleware?

After the request is made and before the response is sent, or it could be listed after the route being requested, but before the callback. Example below:

```js
// if logger middleware were used
app.get('/', logger, (req, res) => {
  res.status(200).send('Hello');
})
```

5. What can cause express to error with “Request headers sent twice, cannot start a second response”

    - If you are calling a callback more than one time.
    - Throwing an error after the response body was already formed
    - This can happen after a response has already been sent, and you try to send another

## Terms:
<dl>
    <dt>Middleware</dt>
    <dd>Any functionality that sits in between request/response, but does not send out response itself.</dd>
    <dt>Request Object</dt>
    <dd>Represents the information in the HTTP request from the client to the server.</dd>
    <dt>Response Object</dt>
    <dd>Information in the HTTP response from the server to the client.</dd>
    <dt>Application Middleware</dt>
    <dd>Middleware that plays a role in the function of the application.</dd>
    <dt>Routing Middleware</dt>
    <dd>Middleware that plays a role in path routing.</dd>
    <dt><abbr title="Test Driven Development">TDD</abbr></dt>
    <dd>Style of programming in which three activities are tightly interwoven - coding, testing (unit tests) an design.</dd>
    <dt>Behavioral Testing</dt>
    <dd>Testing of the external behavior of the program (also known as black box testing), usually a functional testing</dd>
</dl>


### Sources

- [What is middleware?](https://www.redhat.com/en/topics/middleware/what-is-middleware)
- [More on middleware](https://expressjs.com/en/guide/using-middleware.html#middleware.application)
- [Request object](https://www.tutorialspoint.com/nodejs/nodejs_request_object.htm)
- [Response object](https://www.tutorialspoint.com/nodejs/nodejs_response_object.htm)
- [TDD](https://www.agilealliance.org/glossary/tdd/)
- [Behavior testing](https://www.tutorialspoint.com/software_testing_dictionary/behaviour_testing.htm)


## ES6 Classes

- Classes are a template for creating objects
- Classes are "special functions"
- Class syntax has two components: class expressions and class declarations
- Class declarations: use the ```class``` keyword with the name of the class

```js
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
```

- Class expression: can be named or unnamed, name given to class expression is local to the class's body

> unnamed:
```js
let Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
```

> named:
```js
let Rectangle = class Rectangle2 {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
```

- MDN docs [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)


## Using Express Routing

- Routing refers to how applications endpoints (URIs) respond to client requests
- Define routing using methods of the Express app object that correspond to HTTP methods
- Routing methods specify a callback function (sometimes called "handler functions") called when the application receives a request to the specified route (endpoint) and HTTP method
- Routing methods can have more than one callback function as arguments
- With multiple callback functions, it is important to provide ```next``` as an argument to the callback function and then call ```next()``` within the body of the function to hand off control to the next callback
- [Express routing docs](https://expressjs.com/en/guide/routing.html)


## Express Routing

- Learn how to use the new router in ExpressJS 4.0 article [here](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)
- Router is like a mini express application
- Doesn't bring in views or settings
- Provides us with routing APIs like .use, .get, .params, and route