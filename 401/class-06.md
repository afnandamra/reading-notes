# Authentication

## Review, Research, and Discussion:

1. **Explain what a “Singleton” is (in Computer Science terms)**: class that allows only a single instance of itself to be created and gives access to that created instance, it contains static variables that can accomodate unique and private instances of itself. It is used in scenarios when a user wants to restrict instantiation of a class to only one object (source: Techopedia)
2. **Explain how the Singleton pattern can be used with Node modules, specifically with classes**: Singleton design pattern restricts the instantiation of a class to a single instance (source: [Medium](https://medium.com/better-programming/what-is-a-singleton-2dc38ca08e92))
3. **If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?**:
``` js
const express = require('express')
const app = express()
const myFunction = (request, response, next) => {... next()}
app.use(myFunction)
app.get('/route', (request, response) => {...})
app.listen(PORT)
```
- Writing middleware for use in Express apps docs [here](https://expressjs.com/en/guide/writing-middleware.html)
- Creating custom middleware in Express.js overview here from [DigitalOcean](https://www.digitalocean.com/community/tutorials/nodejs-creating-your-own-express-middleware)

## Vocabulary Terms
- **Router Middleware**: works in the same way as application-level middleware, except it is bound to an instance of `express.Router()`
- **Dynamic Module Loading**: mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory (source: Wikipedia)
- **Singleton Pattern**: restricts the instantiation of a class to a single instance
- **CRUD (create, read, update, delete) -> REST Method Matches**: create --> POST, read --> GET, update --> PUT/PATCH, delete --> DELETE
- **Mock Testing**: an approach to unit testing that lets you make assertions about how the code under test is interacting with other system modules, dependencies are replaced with objects that simulate the behavior of the real ones (source: Devopedia)

### Sources
- [Medium: NodeJS Middleware](https://medium.com/@selvaganesh93/how-node-js-middleware-works-d8e02a936113)

## Securing Passwords
- Hashing is the greatest way for protecting passwords and considered to be pretty safe for ensuring the integrity of data or passwords
- There are some weaknesses in cryptographic hash algorithm that allows an attacker to calculate the original value of hashed password:
  - Brute force attack: attack can simply keep trying different inputs
  - Hash collision attack: hash functions have infinite input length and a predefined output length, so there is inevitably going to be the possibility of two different inputs that produce the same output hash
  - BCrypt: algorithm that uses technique called key stretching, based on Blowfish symmetric block cipher aryptographic algorithm and introduces a work factor (also known as security factor) which allows you to determine how expensive the hash function will be

## Basic Authentication
- Basic access authentication is a method for an HTTp user agent (web browser) to provide a user name and password when making a request
- In basic HTTP authentication, request contains a header field in the form of `Authorization: Basic <credentials>` where credentials is the Base64 encoding of ID and password joined by a single colon
- HTTP basic authentication (BA) is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages
- Since BA mechanism does not provide confidentiality protection for the transmitted credentials, it is typically used in conjunction with HTTPS to provide confidentiality

### Server Side
- When the server wants to user agent to authenticate itself towards the server, the server must respond appropriately to unathenticated requests (`HTTP 401 Unauthorized status`)
- WWW-Authenticate field for basic authentication: `WWW-Authenticate: Basic realm="User Visible Realm"`
- Server may choose to include the charset parameter to indicate that the server expects the client to use UTF-8 for encoding (`charset="UTF-8"`)

### Client Side
- When the user agent wants to send authentication credentials to the server, it may use the Authorization field
- Authorization field is constructed by:
  - Username and password combined with a single colon
  - Resulting string is encoded into an octet sequence
  - Resulting string is encoded using variant of Base64
  - Authorization method and a space is then prepended to the encoded string

## OWASP Cheat Sheet [here](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)
- Authentication: process of verifying than an individual, entity or website is whom it claims to be
- Session management: process by which a server maintains the state of an entity interacting with it
- User IDs: make sure usernames/userIDs are case-insensitive
- Passwords: minimum length of 8 characters, common maximum length is 64 characters
- Transmit passwords only over TLS (transport layer protection) or other strong transport
- Require re-authentication for sensitive features
- Account lockout: prevent any more login attempts afeter a series of failed logins

## bcrypt docs [here](https://www.npmjs.com/package/bcrypt)
- Library to help has passwords
- Dependencies: NodeJS
- `npm install bcrypt`