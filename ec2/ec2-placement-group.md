# Placement Groups in EC2

Placement groups are a way of placing EC2 instances close together inside an Availability Zone, or spreading them across Availability Zones, for performance, high-availability, and other benefits. When creating a placement group, you need to specify one of the following strategies for the group:

## Cluster (High Performance)

Clusters instances into a low-latency group in a single Availability Zone.

- **Pros**: Great network (10GB bandwidth between instances with Enhanced networking enabled).
- **Cons**: If the AZ fails, all instances fail at the same time.
- **Use case**: Big data job that needs to complete fast, applications that need extremely low latency and high network throughput.

## Spread (High Availability)

Spreads instances across underlying hardware (max 7 instances per group per AZ). This is suitable for critical applications.

- **Pros**: Can span across AZs, reduced risk of simultaneous failure, EC2 Instances are on different physical hardware.
- **Cons**: Limited to 7 instances per AZ per placement group.
- **Use case**: Applications that need to maximize high availability, critical applications where each instance must be isolated from failure from each other.

## Partition (Critical)

Spreads instances across many different partitions (which rely on different sets of racks) within an AZ. Scales to 100s of EC2 instances per group (Hadoop, Cassandra, Kafka).

- **Pros**: Up to 7 partitions per AZ, can span across multiple AZs in the same region, up to 100s of EC2 instances, the instances in a partition do not share racks with the instances in the other partitions.
- **Cons**: A partition failure can affect many EC2 but won't affect other partitions.
- **Use case**: HDFS, HBase, Cassandra, Kafka.