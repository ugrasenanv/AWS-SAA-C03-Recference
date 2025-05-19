# Logs Subscriptions

Amazon CloudWatch Logs allows you to get real-time log events for processing and analysis by sending them to various destinations.

## Real-Time Log Events

- **Purpose**: Get real-time log events from CloudWatch Logs for processing and analysis.

## Destinations

- **Kinesis Data Streams**: Send log events to Kinesis Data Streams for real-time processing.
- **Kinesis Data Firehose**: Send log events to Kinesis Data Firehose for near real-time delivery to destinations like S3.
- **AWS Lambda**: Send log events to AWS Lambda for real-time processing and custom handling.

## Subscription Filter

- **Purpose**: Filter which log events are delivered to your destination.
- **Usage**: Define a filter pattern to specify the log events you want to subscribe to.

By setting up log subscriptions, you can efficiently process and analyze log data in real-time using the destination of your choice.

![CloudWatch Logs](../z_resources/images/cloudwatch/cloudwatch-logs.png)