# Aurora High Availability and Read Scaling

- Aurora provides high availability by maintaining 6 copies of your data across 3 Availability Zones (AZs). This ensures that your data is safe and available even in the event of a failure.

- For write operations, at least 4 out of the 6 copies are needed. For read operations, at least 3 out of the 6 copies are needed.

- Aurora uses self-healing storage with peer-to-peer replication. This means that data blocks and disks are continuously scanned for errors and replaced automatically.

- The storage is striped across hundreds of volumes. This distributes the data and workload evenly, improving performance and reliability.

- In an Aurora cluster, one instance takes on the role of the master, handling all write operations. Automated failover is supported, allowing the master role to be quickly reassigned to a replica in the event of a failure. This failover typically happens in less than 30 seconds.

- In addition to the master, you can have up to 15 Aurora Read Replicas. These replicas share the same underlying volume as the master, which allows them to serve read traffic with minimal replica lag.

- Aurora also supports cross-region replication. This allows you to create a read replica in a different region, which can be promoted to the master in the event of a regional failure.