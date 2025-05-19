# Kinesis Data Streams - Capacity Modes

Amazon Kinesis Data Streams offers two capacity modes to accommodate different use cases and operational preferences: Provisioned Mode and On-Demand Mode. Each mode is designed to provide flexibility in managing the throughput of data streams.

## Provisioned Mode

In Provisioned Mode, you have the control to manually select the number of shards that your data stream will use. This mode is ideal for applications with predictable workloads.

- **Shard Provisioning**: You decide the number of shards. Each shard provides a dedicated throughput capacity.
- **Throughput**:
    - **Ingress**: 1MB/s or 1,000 records per second, per shard.
    - **Egress**: 2MB/s per shard. This applies to both classic consumers and enhanced fan-out consumers.
- **Scaling**: Can be done manually or programmatically via the AWS API.
- **Pricing**: Charges are based on the number of shards provisioned, calculated per hour.

## On-Demand Mode

On-Demand Mode eliminates the need to manage shard capacity. It automatically adjusts the throughput of the stream based on the incoming data volume.

- **Capacity Management**: No need to provision shards manually. The service manages capacity based on usage.
- **Default Throughput**:
    - **Ingress**: Up to 4MB/s or 4,000 records per second. This is the default provisioned capacity.
- **Automatic Scaling**: Scales automatically based on the peak throughput observed during the last 30 days.
- **Pricing**: Billed based on the stream's hourly rate and the amount of data ingested and retrieved.

By choosing the appropriate capacity mode, you can optimize the performance and cost-efficiency of your Kinesis Data Streams according to your application's needs.