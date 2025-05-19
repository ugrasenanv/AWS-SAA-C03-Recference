# RDS & Aurora Restore Options

Restoring an RDS or Aurora backup or a snapshot always results in the creation of a new database instance or cluster. This section outlines the steps for restoring MySQL databases for both RDS and Aurora from backups stored in Amazon S3.

## Restoring MySQL RDS Database from S3

1. **Create a Backup of Your On-Premises Database**: Use your preferred method to create a backup of your MySQL database.
2. **Store It on Amazon S3**: Upload the backup file to an Amazon S3 bucket. Ensure that the S3 bucket is in the same region as the RDS instance you plan to create.