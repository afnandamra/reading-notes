# Socket.io

## Review, Research, and Discussion

1. **What is the benefit of transforming data into packets?**

Allows for data to be transferred fast and efficiently over the network and minimizes the transmission latency
(source: [GeeksforGeeks](https://www.geeksforgeeks.org/packet-switching-and-delays-in-computer-network/))

2. **UDP is often referred to as a connectionless protocol. Why is this?**

No connection needs to be established between the source and destination before you transmit data

3. **Can a socket server application have multiple socket connections?**

A server socket listens on a single port, but it is able to share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs (source: [stack overflow](https://stackoverflow.com/questions/11129212/tcp-can-two-different-sockets-share-a-port/11129641))

4. **Can a socket connection application be connected to multiple socket servers?**

Single client-side server should only connect to one socket server.

5. **Can an application be both a socket server and a socket connection?**

Yes (source: [Stack Abuse](https://stackabuse.com/node-js-websocket-examples-with-socket-io/))

## Vocabulary Terms

- **Observer Pattern:** software design pattern in which an object (named the subject) maintains a list of its dependents (observers), and notifies them automatically of any state changes, usually by calling one of their methods
- **Listener:** function that listens for an event to occur
- **Event Handler:** function that runs when a specific event fires
- **Event Driven Programming:** programming paradigm in which the flow of the program is determined by events such as user actions, message passing
- **Event Loop:** responsible for executing the code, collecting and processing events, and executing queued sub-tasks (source: [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop))
- **Event Queue:** queue where events from an application are held prior to being processed by a receiving program or system
- **Call Stack:** mechanism for an interpreter to keep track of its place in a script that calls multiple functions - what function is currently being run and what functions are called from within that function (source: [MDN](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack))
- **Emit/Raise/Trigger:** in event driven programming, emit sends a message to trigger a response and raise and event
- **Subscribe:** waiting for a published event to take place
- **Database:** organized collection of data, generally stored and accessed electronically from a computer system

## Web Sockets

- Computer communications protocol, providing full-duplex communication channels over a single TCP connection
- WebSocket handshake uses the HTTP Upgrade header to change from the HTTP protocol to the WebSocket protocol
- WebSocket protocol enables interaction between a web browser (or other client application) and a web server with lower overhead than half-duplex alternatives such as HTTP polling, facilitating real-time data transfer from and to the server
- Can be done by providing a standardized way for the server to send content to the client without being first requested by the client, and allowing messages to be passed back and forth while keeping the connection open

## Socket.io Tutorial

- Socket.IO enables real-time bidirectional event-based communication
- Works on every platform, browser or device
- Built on top of the WebSockets API (Client side) and Node.js

## Socket.io vs. Web Sockets

- WebSocket is the communication protocol which provides bidirectional communication between the client and the server over a TCP connection
- WebSocket remains open all the time so they allow the real-time data transfer
- When clients trigger the request to the server it does not close the connection, it persists and waits for client or server to terminate the request
- Socket.IO is a library which enables real-time and full duplex communication between the client and the web servers
- Uses the WebSocket protocol to provide the interface
- Divided into two parts, both WebSocket vs Socket.io are event-driven libraries:
  - client side: library that runs inside the browser
  - server side: library for Node.js
