# reading notes apr072022

The required reading today was a youtube video

[AWS SNS and SQS](https://www.youtube.com/watch?v=mXk0MNjlO7A)

## Technical Comparison

### SNS

- Publisher subscriber system
- Publishing messages to a topic can deliver to many subscribers (fan out) of different types (SQS, Lambda, Email)
- Do `other systems` care about an event?


### SQS

- Queueing service for message processing.
- A system must poll the Queue to discover new events
- Messages in the queue are typically processed by a single consumer
- Does `your system` care about an event?

## An example- credit card transactions

many different consumers care about this event. Transaction SNS is used when sending information to customer reminder service and a customer receives an email.

At the same time SQS is used when Transaction Analytics Queue is used and when Transaction Fraud Detection Queue is used.  

When SQS is used, there is a corresponding Service (EC2) that pools the queue.  For example the transaction analytics service polls the transaction analytics queue.  Also, the transaction fraud detection queue is polled by the transaction fraud detection service(EC2)

## Things I want to know more about.