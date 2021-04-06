# Event Driven Applications

## Review, Research, and Discussion

1. **Why is access control important?**

Access control is a security technique that can be used to regulate who or what can view or use any given resource.

2. **Describe an application that would need access control:**

Almost any type of application, for example a public facing website of some kind that has a need for users to only view content, a select group to be able to edit content, and another smaller group of administrators to be able to update and delete content.

3. **What is a role used for?**

A role is used to determine what type of capabilities a user has. Administrators for example have all capabilities (read, write, update, delete), while a regular user may only have read capabilities.

4. **Why is role based access control more scalable than discretionary or mandatory access control?**

The assignment of access rights in RBAC is very systematic and repeatable, easier to audit user rights (users are in only one of a few categories), and easier to correct any issues that are identified. There is no case by case assignment of roles, users fall into one of already pre-assigned roles/capabilities.

## Vocabulary Terms

- Authorization: process of giving the user permission to access a specific resource or function (access control or client privilege), in secure environments authorization must follow authentication (source: [okta docs](https://www.okta.com/identity-101/authentication-vs-authorization/))
- Role Based Access Control (RBAC): an approach to restricting system access to authorized users, a policty-neutral access-control mechanism defined around roles and priviledges/capabilities
- Capabilities: the functions that a user has access to (read, create, update, or delete for example)

## Event Driven Programming

- Event driven programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision
- Every time you interact with a webpage through it's user interface, an event is happening
- These events have associated functions that, when triggered, are executed to make a change to the user interace in some way
- Event-driven programming makes use of the following concepts:
  - event handler is a callback function that will be called when an event is triggered
  - main loop listens for event triggers and calls the associated event handler for that event
- EventEmitter: Node.js nativey provides this module, allows us to get started incorporating event driven programming into projects right away
- Access the EventEmitter class through the `events` module, one imported you need to create a new object from the class to start using it

```js
const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter();
```

- Use EventEmitters `on` method to set the listener
- Use the `emit` method to trigger the event
- Removing listeners with `removeListener` or `removeAllListeners`
- Must pass reference to the exact function you wish to remove when using the `removeListener` method, which means wherever you want to remove the event you need to make sure the function is able to be referenced from that place in your code (often best to name the event handling function and declare them before you register the event listener as opposed to leaving them anonymous)

### Object Oriented Programming + Event-Driven Programming

- Object oriented approach promotes the idea that all behavior of an individual unit (or object) be handled from code within that unit, so apps are built with many different units that all speak to and interact with each other
- By registering event listeners we can actually reverse the flow of communication between objects, rather than an object neding to reach inside another object to trigger a function, our objects can just emit events and whichever objects are listening to those events will process it in the way they have been told to
- Source of an objects behavior is now entirely contained within itself, rather than needing to be accessed by external objects

## Node docs: [Events](https://nodejs.org/api/events.html)

- All objects that emit events are instances of the `EventEmitter` class
- These objects expose an `eventEmitter.on()` function that allows one or more functions to be attached to named events emitted by the object
- When the `EventEmitter` object emits an event, all of the functions attached to that specific event are called synchronously, any values returned by the called listeners are ignored and discarded
- `eventEmitter.on()` is used to register listeners
- `eventEmitter.emit())` is used to trigger the event
- The `eventEmitter.emit()` method allows an arbitrary set of arguments to be passed to the listener functions
- When an ordinary listener function is called, the standard `this` keyword is intentionally set to reference the EventEmitter instance to which the listener is attached
- Using arrow functions as listeners is possible, but the `this` keyword will no longer reference the `EventEmitter`
- The `EventEmitter` calls all listeners synchronously in the order in which they were registered
- When appropriate, listener functions can switch to an asynchronous mode of operation using the `setImmediate()` or `process.nextTick()` methods
- When a listener is registered using the `eventEmitter.on()` method, that listener is invoked every time the named event is emitted
- Using the `eventEmitter.once()` method, it is possible to register a listener that is called at most once for a particular event, once the event is emitted, the listener is unregistered and then called
