# EFS (Elastic File System)

EFS (Elastic File System) is a managed NFS (Network File System) that can be mounted on many EC2 instances. EFS works with EC2 instances in multi-AZ. It is highly available, scalable, and expensive (3x gp2). You pay per use.

## EFS - Performance & Storage Classes

EFS can scale to support thousands of concurrent NFS clients, and 10 GB+ /s throughput. It can grow to a petabyte-scale network file system, automatically.

### Performance Mode

Performance mode is set at EFS creation time. The default mode is General Purpose, which is suitable for latency-sensitive use cases like web servers, CMS, etc.

### Throughput Mode

There are three throughput modes:

- Bursting: 1TB = 50MiB/s + burst of up to 100MiB/s
- Provisioned: Set your throughput regardless of storage size, e.g., 1GiB/s for 1 TB storage
- Elastic: Automatically scales throughput up or down based on your workloads. It can provide up to 3GiB/s for reads and 1GiB/s for writes. This mode is used for unpredictable workloads.

## EFS Storage Classes

EFS offers different storage tiers, and you can implement lifecycle management features to move files after N days:

- Standard: For frequently accessed files
- Infrequent access (EFS-IA): Lower price to store, but there is a cost to retrieve files
- Archive: For rarely accessed data (a few times each year), 50% cheaper than EFS-IA

## Availability and Durability

- Standard: Multi-AZ, great for production environments
- One Zone: One AZ, great for development environments. Backup is enabled by default.