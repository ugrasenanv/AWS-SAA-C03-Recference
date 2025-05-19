# Producing Messages to SQS

To produce messages to an Amazon SQS queue, you use the AWS SDK, specifically the `SendMessage` API. This allows your application to send messages to the queue, which are then stored by SQS until they are deleted by a consumer.

## Key Points

- **SDK Usage**: Utilize the AWS SDK's `SendMessage` API to send messages to your SQS queue.
- **Message Persistence**: Once a message is sent to the queue, it remains there until explicitly deleted by a message consumer.
- **Message Retention**: Messages have a default retention period of 4 days, which can be configured up to a maximum of 14 days.
- **Throughput**: SQS standard queues offer unlimited throughput, meaning there is no limit to the number of messages you can send to the queue.

