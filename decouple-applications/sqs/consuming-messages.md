# Consuming Messages from SQS

Consuming messages from an Amazon SQS queue involves polling the queue for messages, processing those messages, and then deleting them from the queue to prevent reprocessing. This can be done using various AWS services such as EC2 instances, servers, or AWS Lambda functions.

## Key Steps

1. **Polling SQS**: Use the `ReceiveMessage` API to poll the SQS queue for messages. You can receive up to 10 messages in a single request, which is the maximum allowed by SQS to optimize batch processing.
2. **Processing Messages**: After receiving the messages, process them according to your application's logic. For example, you might insert the message content into an Amazon RDS database.
3. **Deleting Messages**: Once a message is successfully processed, delete it from the queue using the `DeleteMessage` API. This requires the message's receipt handle, which is provided when the message is received.
