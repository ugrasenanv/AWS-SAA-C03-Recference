# Redshift Cluster

- **Leader node**: Responsible for query planning and results aggregation.
- **Compute node**: Executes the queries and sends results to the leader node.
- **Provisioning**: You provision the node size in advance.
- **Reserved Instances**: Can be used for cost savings.

## Snapshots & Disaster Recovery

- **Multi-AZ Mode**: Available for some clusters.
- **Snapshots**: Point-in-time backups of a cluster, stored internally in S3.
    - **Incremental**: Only changes are saved.
    - **Restoration**: Can restore a snapshot into a new cluster.
    - **Automated Snapshots**: Taken every 8 hours, every 5GB, or on a schedule. Retention can be set.
    - **Manual Snapshots**: Retained until you delete them.
- **Cross-Region Copy**: Configure Amazon Redshift to automatically copy snapshots (automated or manual) of a cluster to another AWS Region.

## Redshift Spectrum

- **Query Data in S3**: Query data that is already in S3 without loading it.
- **Cluster Requirement**: Must have a Redshift cluster available to start the query.
- **Execution**: The query is submitted to thousands of Redshift Spectrum nodes.