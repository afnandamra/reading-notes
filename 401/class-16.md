# AWS: Cloud Servers

## Review, Research, and Discussion

1. **What’s the difference between a FIFO and a standard queue?**

FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing and ensure the order in which messages are sent and received is strictly preserved (source: [Medium](https://medium.com/awesome-cloud/aws-difference-between-sqs-standard-and-fifo-first-in-first-out-queues-28d1ea5e153))

2. **How can the server be assured a message was properly received?**

By having the client emit a "received" event back to the server upon receipt of the message

3. **What classic design pattern is best represented by event driven programming?**

Observer design pattern, an object (subject) maintains a list of its dependents (observers) and notifies them automatically of any state changes usually by calling one of their methods (source: [Wikipedia](https://en.wikipedia.org/wiki/Observer_pattern))

4. **How do you test an event driven system?**

With unit tests which test individual components of the system, as well as tests for verifying the server and clients are communicating back and forth

## Vocabulary Terms

- **Server:** In computing, a server is a piece of computer hardware or software that provides functionality for other programs or devices, called "clients". This architecture is called the client–server model.
- **Pub/Sub:** In software architecture, publish–subscribe is a messaging pattern where senders of messages, called publishers, do not program the messages to be sent directly to specific receivers, called subscribers, but instead categorize published messages into classes without knowledge of which subscribers, if any, there may be. Similarly, subscribers express interest in one or more classes and only receive messages that are of interest, without knowledge of which publishers, if any, there are. (source: Google Cloud [docs](https://cloud.google.com/pubsub/docs/overview))
- **WRRC:** The web is a cycle of requests and responses that flow between clients and servers. Any computer making a request is a client and any computer sending a response is a server. 

## AWS EC2

- Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable computer capacity in the cloud
- Designed to make web-scale cloud computing easier for developers
- Allows you to obtain and configure capacity with minimal friction
- Provides you with complete control of your computing resources and lets you run on Amazon's proven computing environment
- EC2 offers the broadest and the deepest compute platform with a choice of processor, storage, networking, operating system, and purchase model
- SLA commitment of 99.99% availability for each Amazon EC2 region, each region consists of at least 3 availability zones

## Videos

- Virtual machine manager: also called a hypervisor, type of software that allows us to run an operating system within another operating system (examples: VirtualBox, VMware)
- AWS Elastic Beanstalk: easy to use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, and Docker