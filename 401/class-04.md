# Data Modeling

## Review, Research, and Discussion:

1. Name 3 advantages to Test Driven Development
  - Reduction in defect rates
  - overheads are more than offset by reduction in effort of projects' final phases
  - improved design qualities in code

2. In what case would you need to use `beforeEach()` or `afterEach()` in a test suite?
  - Use `beforeEach()` if a method needs to be called before a test is run
  - Use `afterEach()` if you need to reset the environment after a test has run

3. What is one downside of Test Driven Development?
  - not running tests frequently enough or writing too many tests at once

4. What's the primary difference between ES6 Classes and Constructor/Prototype Classes?
  - Inheritance is much more efficient and simple for ES6 classes.
  
5. Why REST?
  - Can be used well where network bandwidth is a constraint
  - Don't need to maintain a state of information from one request to another
  - Good for caching a lot of requests
  - Much easier to code/implement for web services than SOAP

## Terms:

- **Functional programming**:
  - Software is composed using pure functions (avoid shared state, mutable data, side-effects)
  - If functions are interrelated, changing one function could break everything else

- **<abbr title="Object-Oriented Programming">OOP</abbr>**:
    
  - Encapsulation, Abstraction, Inheritance, Polymorphism
  - Related properties and methods can be grouped together

- **Class**:
  - templates for creating objects. The `constructor()` method is used for creating and initializing an object created with a `class`. Can only be one `constructor()` per class

- **`super`**: this is used to call the constructor of the super (parent) class

- **`this`**: `this` refers to the current object being instantiated

- **<abbr title="Test Driven Development">TDD</abbr>**: Refers to a style of programming in which three activities are tightly interwoven: coding, testing (unit tests) and design (refactoring)

- **Jest**: JavaScript Testing Framework; Jest runs previously failed tests first and reorganizes runs based on how long test files take

- **Continuous Integration (CI)**:
  - consistent merging from multiple places into one multiple times a day

- **REST**: **Re**presentational **S**tate **T**ransfer. Uses HTTP requests to retrieve/use data

- **Data Model**: Data model is a diagram that illustrates relationships and behaviors of different pieces of an application and how those pieces depend on one another

### Sources
- [Medium: Functional Programming](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0)
- [Medium: Object Oriented Programming](https://medium.com/swlh/what-is-object-oriented-programming-f5b42f3ac826)
- [this - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)
- [Jest docs](https://jestjs.io/)
- [CI from Atlassian](https://www.atlassian.com/continuous-delivery/continuous-integration)
- [REST from CodeAcademy](https://www.codecademy.com/articles/what-is-rest)

## NoSQL vs SQL

### NoSQL

- primarily called non-relational database
- document based, key-value pairs, graph databases, or wide-column stores
- dynamic schema for unstructured data
- horizonally scalable
- queries are focused on collection of documents, sometimes called unstructured query language (UnQL)

### SQL

- primarly called relational databases
- table databases
- predefined schema
- vertically scalable
- use structured query language

## NoSQL Modeling Techniques

- Often compared by various non-functional criteria, such as scalability, performance, and consistency
- Often starts from the application-specific queries as opposed to relational modeling
- Often requires a deeper understanding of data structures and algorithms than relational database modeling does
- Data duplication and denormalization are first class citizens