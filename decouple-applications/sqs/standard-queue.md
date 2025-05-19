# SQS - Standard Queue

Amazon SQS (Simple Queue Service) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. SQS eliminates the complexity and overhead associated with managing and operating message-oriented middleware, and it empowers developers to focus on differentiating work.

## Attributes

- **Unlimited Throughput**: SQS provides unlimited throughput, allowing an unlimited number of messages in the queue.
- **Message Retention**: By default, messages are retained in the queue for 4 days, with the option to configure retention up to 14 days.
- **Low Latency**: SQS offers low latency, with less than 10 milliseconds on publish and receive operations.
- **Message Size Limit**: Each message sent to the queue can be up to 256KB in size.
- **Duplicate Messages**: SQS standard queues may occasionally deliver duplicate messages, ensuring at least once delivery.
- **Ordering**: Messages might be delivered in an order different from which they were sent (best effort ordering), meaning that the service does not guarantee message order.

## Use Cases

SQS standard queues are ideal for applications that require high throughput, at-least-once message delivery, and can tolerate occasional duplicates or out-of-order message delivery. This makes it suitable for a wide range of applications, from simple task queues to complex workflows and transaction processing systems.