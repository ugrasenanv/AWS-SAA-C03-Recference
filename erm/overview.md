# EMR - Node Types & Purchasing

Amazon EMR (Elastic MapReduce) provides a managed Hadoop framework that makes it easy, fast, and cost-effective to process vast amounts of data across resizable clusters of Amazon EC2 instances.

## Node Types

- **Master Node**: Manages the cluster, coordinates tasks, and manages cluster health. This node is long-running.
- **Core Node**: Runs tasks and stores data. This node is also long-running.
- **Task Node**: (Optional) Runs tasks but does not store data. These nodes are usually Spot instances.

## Purchasing Options

- **On-demand**: Reliable and predictable. These instances won't be terminated unexpectedly.
- **Reserved**: Requires a minimum commitment of 1 year. Offers cost savings, and EMR will automatically use reserved instances if available.
- **Spot Instances**: Cheaper but can be terminated at any time. These instances are less reliable.

## Cluster Types

- **Long-running Cluster**: Designed to run continuously.
- **Transient (Temporary) Cluster**: Designed for temporary use and can be terminated after the job is completed.