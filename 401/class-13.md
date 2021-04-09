# Message Queues

## Review, Research, and Discussion

1. **What does it mean that web sockets are bidirectional? Why is this useful?**

Data flows both ways (full-duplex), a web socket can both send and receive which is useful because it allows data to be sent and received on the same channel.

2. **Does socket.io use HTTP? Why?**

Yes, it can. Socket.io will try to establish a WebSocket () if possible but if it cannot it will fall back on HTTP (source: [Socket.io](https://socket.io/docs/v3/index.html))

3. **What happens when a client emits an event?**

The event will be sent to the server, which will be listening for the event if already connected

4. **What happens when a server emits an event?**

Whatever client is listening for the event (maybe all, or maybe one specific client) will respond

5. **What happens if a client “misses” an event?**

Unhandled messages are ignored, behaves as if there is no event listener for the event

6. **How can we mitigate this?**

Can avoid missing an event by always having handlers installed and then deciding in the handlers whether to do anything with the message or not(source: [stack overflow](https://stackoverflow.com/questions/32816290/what-happens-with-unhandled-socket-io-events))

## Vocabulary Terms

- **Socket:** one endpoint of a two-way communication link between two programs running on the network, a socket is bound to a port number so that the TCP layer can identify the application that data is destined to be sent to (source: [Oracle](https://docs.oracle.com/javase/tutorial/networking/sockets/definition.html))
- **Web Socket:** communication protocol that provides a full-duplex and low-latency channel between the server and the browser (source: [Socket.io](https://socket.io/docs/v3/index.html))
- **Socket.io:** a library that enables real-time, bidirectional, and event-based communication between the browser and the server, consists of a Node.js server and a javascript client library for the browser
- **Client:** program separate from the server that initiates requests for services or info from the server
- **Server:** provides function, info, or service back to the client, acts as the main hub for communication
- **OSI Model:** open systems interconnection model is a model that characterizes and standardizes the communication functions of a telecommunication or computing system without regard to its underlying internal structure and technology (source: [Wikipedia](https://en.wikipedia.org/wiki/OSI_model))
  - 7 layers: physical layer, data link layer, network layer, transport layer, session layer, presentation layer, application layer
- **TCP Model:** transmission control protocol, essentially a concise version of the OSI model (source: [GeeksforGeeks](https://www.geeksforgeeks.org/tcp-ip-model/))
  - 4 layers: network access layer, internet layer, transport layer, application layer
- **TCP:** transmission control protocol, one of the main protocols of the internet protocol suite (source: [Wikipedia](https://en.wikipedia.org/wiki/Transmission_Control_Protocol))
- **UDP:** user datagram protocol, connectionless protocol so there is no need to establish a connection prior to data transfer (source: [GeeksforGeeks](https://www.geeksforgeeks.org/user-datagram-protocol-udp/))
- **Packets:** formatted unit of data carried by a packet-switched network, packet consists of control information and user data/payload (source: [Cloudflare](https://www.cloudflare.com/learning/network-layer/what-is-a-packet/))

## Socket.io Chat example

- Sockets have traditionally been the solution around which most real-time chat systems are architected, providing a bi-directional communication channel between a client and a server
- The server can push messages to clients
- Whenever you write a chat message, the idea is that the server will get it and push it to all other connected clients
- Setup steps [here](https://socket.io/get-started/chat/)

## Rooms and Namespaces

- Room is an arbitrary channel that sockets can join and leave, it can be used to broadcast events to a subset of clients
- Rooms are a server-only concept (client does not have access to the list of rooms it has joined)
- Can join to subscribe the socket to a given channel ```socket.join()```
- Each socket in Socket.io is identified by a random unique identifier (Socket#id), each socket automatically joins a room identified by its own id
- Upon disconnection, sockets leave all the channels they were part of automatically

## Socket.io Emit Cheatsheet [here](https://socket.io/docs/v3/emit-cheatsheet/index.html)
