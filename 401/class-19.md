# AWS: Events

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

- **Serverless API**: using API Gateway you can create RESTful APIs that enable real-time two-way communication applications, API Gateway supports containerized and serverless workloads as well as web applications (source: AWS [API Gateway](https://aws.amazon.com/api-gateway/))
- **Triggers**: an AWS Lambda resource or resource in another service that you configure to invoke your function in response to lifecycle events, external requests or on a schedule, a function can have multiple triggers (source: AWS Lambda [docs](https://docs.aws.amazon.com/lambda/latest/dg/lambda-invocation.html))
- **Dynamo vs Mongo**: (source: [MongoDB](https://www.mongodb.com/compare/mongodb-dynamodb))
  - Mongo can be deployed anywhere, Dynamo is only available on AWS
  - Mongo is JSON based document store, Dynamo is limited key-value store with JSON support
  - Mongo is rich query language, Dynamo is key-value queries
- **Dynamoose vs Mongoose**: Dynamoose is a DynamoDB API structured like Mongoose, lets us provide a schema and perform CRUD operations against a DynamoDB table, installed via node and configured based on role

## SQS and SNS

### SQS (Simple Queue Service)

- Distributed queuing system
- Messages are not pushed to receivers, receivers have to poll SQS to receive messages
- Messages can’t be received by multiple receivers at the same time
- Anyone's receiver can receive a message, process and delete it, other receivers do not receive the same message later
- Mainly used to decouple applications or integrate applications
- Messages can be stored in SQS for a short duration of time (max 14 days)

### SNS (Simple Notification Service)

- Fast, flexible, and fully managed push notification service that lets you send individual messages or bulk messages
- Distributed publish/subscribe system
- Messages are pushed to subscribers as and when they are sent by publishers to SNS
- SNS supports several end points such as email, SMS, HTTP endpoint, and SQS
- If you want an unknown number and type of subscribers to receive messages, you need SNS