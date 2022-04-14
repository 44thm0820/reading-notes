# Readings - Day 19 - 

## Reading

[SQS and SNS Basics - youtube video from aws online tech talks](https://www.youtube.com/watch?v=UesxWuZMZqI)

### Learning Objectives

Learning Objectives:
- Understand key messaging use cases, including service-to-service communication, asynchronous work item backlog, and state change notifications 
- Learn how to get started using message queues and topics with just a few simple APIs, and quickly integrate with other AWS services 
- Hear how customers, like Capital One, are benefiting from migrating applications to a fully managed messaging solution in the cloud

#### 

Small startups to the biggest global enterprises are designing applications using microservices and distributed architecture to improve resiliency and scale faster. AWS messaging services â€“ Amazon Simple Queue Service (SQS) and Amazon Simple Notification Service (SNS) â€“ make it easy to decouple communication between software components and build modern applications that are fault-tolerant and easy to scale. Messaging is a key part of Amazonâ€™s own e-commerce platform architecture, and used in mission-critical backend systems such as Amazon Retail Ordering workflow. In this session, we will show how you can use Amazon SQS and Amazon SNS fully managed messaging to decouple your application architecture, enable asynchronous communication between different services, and eliminate the pain associated with operating dedicated messaging software and infrastructure. We will demonstrate common messaging design patterns for building reliable and scalable applications in the cloud.

#### 

Chapters
  - Modern Apps
  - JSON Message
  - XML Message
  - Payload and Attributes
  - Amazon Simple Notification
  - Streams
  - Amazon Kinesis
  - Service to Service Communications
  - Capacity Imbalance
  - Overload
  - Queue as a Safe and Fast Buffer
  - Improving Synchronous Latency
  - Use Background Thread
  - Safe Asynchronous Tasks
  - Private Task Queues
  - Shared Task Queue
  - Microservices
  - Negotiation Everyone!
  - Decouple by Publishing Event through SNS
  - There's more! Queues in SNS
  - There's more! Pub/Sub messaging in SNS
  - Enterprises using Amazon SQS


QUEUES are durable buffers for your messages.

[AWS SQS vs SNS](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)

### TLDR

SQS and SNS are important components for scalable, large scale, distributed, cloud-based applications:

SNS is a distributed publish-subscribe service. Publish and consume batches of messages


SQS is distributed queuing service. One subscriber is needed.


Bookmark and Review

[SNS Javascript SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SNS.html)

[SQS Javascript SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SQS.html)


## Things I want to know more about

more examples of sqs and sns