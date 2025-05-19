# Kinesis Data Streams vs. Kinesis Data Firehose

Amazon Kinesis offers two solutions for handling real-time streaming data: Kinesis Data Streams and Kinesis Data Firehose. Each service is designed to meet different needs in the data processing and analytics pipeline.

## Kinesis Data Streams

Kinesis Data Streams is a highly scalable and customizable streaming service designed for real-time data ingestion and processing.

- **Customization**: Requires writing custom producer and consumer code to handle streaming data.
- **Latency**: Offers real-time processing with latencies as low as 200 milliseconds.
- **Scaling**: Users must manage scaling through shard splitting and merging.
- **Data Storage**: Provides data storage for 1 to 365 days, enabling data replay for processing.
- **Replay Capability**: Supports the ability to replay data, facilitating scenarios like reprocessing and analysis.

## Kinesis Data Firehose

Kinesis Data Firehose is a fully managed service for loading streaming data into AWS data stores and external destinations.

- **Destination Integration**: Directly loads streaming data into Amazon S3, Amazon Redshift, Amazon OpenSearch Service, third-party services, or custom HTTP endpoints.
- **Management**: Fully managed service, requiring no ongoing administration or scaling efforts.
- **Latency**: Provides near real-time data delivery with minimal configuration.
- **Scaling**: Automatically scales to match the throughput of incoming data without user intervention.
- **Data Storage**: Does not offer data storage within the service itself.
- **Replay Capability**: Lacks the ability to replay data, focusing instead on efficient data delivery to specified destinations.

By understanding the differences between Kinesis Data Streams and Kinesis Data Firehose, users can choose the appropriate service based on their specific requirements for real-time data processing and analysis.