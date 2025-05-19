# Read Replicas - Use Cases

- Read Replicas are particularly useful when you have a production database that is taking on a normal load and you want to run a reporting application to perform some analytics.

- You can create a Read Replica to run the new workload, ensuring that the production application remains unaffected.

- Read Replicas are used for `SELECT` (read) operations only, not for `INSERT`, `UPDATE`, or `DELETE` operations.

# Network Cost

- In AWS, there's a network cost when data moves from one Availability Zone (AZ) to another.

- However, for RDS Read Replicas within the same region, you don't incur this fee.