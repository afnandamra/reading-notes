# AWS: S3 and Lambda

## Review, Research, and Discussion

1. **What’s the difference between a FIFO and a standard queue?**

FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing. FIFO queues provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers. (source: [Medium](https://medium.com/awesome-cloud/aws-difference-between-sqs-standard-and-fifo-first-in-first-out-queues-28d1ea5e153))

2. **How can the server be assured a message was properly received?**

By having the client emit a "received" event back to the server upon receipt of the message

3. **What classic design pattern is best represented by event driven programming?**

Observer design pattern, an object (subject) maintains a list of its dependents (observers) and notifies them automatically of any state changes usually by calling one of their methods (source: [Wikipedia](https://en.wikipedia.org/wiki/Observer_pattern))

4. **How do you test an event driven system?**

With unit tests which test individual components of the system, as well as integration tests for verifying the server and clients are communicating back and forth

## Vocabulary Terms

- **Server instances:** An instance is a single copy of the software running on a single physical or virtual server. If you run two copies of the software on the same physical or virtual server, that counts as two instances. When you run two copies of the software on two different physical or virtual servers, that also counts as two instances. (Source: [Flexera/Rightscale](https://docs.rightscale.com/cm/dashboard/manage/instances_and_servers/instances_and_servers_concepts.html))
- **Containers:** A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. (Source: [AWS docs](https://aws.amazon.com/getting-started/deep-dive-containers/))
- **Cloud Services:** a wide range of services delivered on demand to companies and customers over the internet, these services are designed to provide easy, affordable access to applications and resources without the need for internal infrastructure or hardware (source: [Citrix](https://www.citrix.com/glossary/what-is-a-cloud-service.html))
- **Cloud Architecture:** the way technology components combine to build a cloud, in which resources are pooled through virtualization technology and shared across a network (source: [VMware](https://www.vmware.com/topics/glossary/content/cloud-architecture))
  - Components of cloud architecture include:
    - front-end platform (client or device used to access the cloud)
    - back-end platform (servers and storage)
    - cloud-based delivery model
    - network
- **AWS:** Amazon Web Services, a subsidiary of Amazon providing on-demand cloud computing platforms and APIs to individuals, companies, and governments on a metered pay-as-you-go basis (source: Wikipedia)
- **EC2/Beanstalk vs Heroku:** EC2/Beanstalk is an Infrastructure as a Service product (IaaS), while Heroku is a  Platform as a Service (PaaS) product (source: [RubyGarage](https://rubygarage.org/blog/heroku-vs-amazon-web-services))

## AWS: S3 and Lambda

### AWS S3

- Cloud object storage service that offers scalability, data availability, security and performance
- Capability to scale your storage resources up and down to meet fluctuating demands
- Stores data across the S3 storage classes which support different data access levels at corresponding rates
- Store your data in Amazon S3 and secure it from unauthorized access with encryption features and access management tools
- S3 is the only object storage service that allows you to block public access to all of your objects at the bucket or the account level
- S3 Access Points make it easy to manage data access with specific permissions for your applications using a shared data set
- Use cases: backup and restore, disaster recovery, archive, data lakes and big data analytics, hybrid cloud storage, cloud-native applications

### AWS Lambda

- AWS Lambda is a serverless computing service provided by Amazon Web Services (AWS)
- The Lambda functions can perform any kind of computing task, from serving web pages and processing streams of data to calling APIs and integrating with other AWS services
- Each Lambda function runs in its own container
- When a function is created, Lambda packages it into a new container and then executes that container on a multi-tenant cluster of machines managed by AWS
- Before the functions start running, each function’s container is allocated its necessary RAM and CPU capacity
- Once the functions finish running, the RAM allocated at the beginning is multiplied by the amount of time the function spent running
- The customers then get charged based on the allocated memory and the amount of run time the function took to complete
- One of the distinctive architectural properties of AWS Lambda is that many instances of the same function, or of different functions from the same AWS account, can be executed concurrently
- Common use cases for Lambda: scalable APIs, data processing, task automation

### CDN

- Content Delivery Network (CDN) is a geographically distributed group of servers that work together to provide fast delivery of Internet content
- A CDN allows for the fast transfer of data needed for loading Internet content including HTML pages, JavaScript files, stylesheets, images, and videos
- CDNs work through servers nearest to the website visitor respond to the request
- The content delivery network copies the pages of a website to a network of servers that are spread out at geographically different locations, caching the contents of the page
- When a user requests a webpage that is part of a content delivery network, the CDN will redirect the request from the originating site’s server to a server in the CDN that is closest to the user and deliver the cached content
- CDNs will also communicate with the originating server to deliver any content that has not been previously cached
- Speed is improved by distributing content closer to the website visitors by using a nearby CDN server, causing visitors to experience faster page loading times