# DynamoDB - Backups for Disaster Recovery

DynamoDB offers robust backup capabilities to ensure data durability and facilitate disaster recovery strategies. These include continuous backups with point-in-time recovery (PITR) and on-demand backups for long-term retention.

## Continuous Backups with Point-in-Time Recovery (PITR)

Point-in-Time Recovery (PITR) provides continuous backups of your DynamoDB table data. This feature allows you to restore your table to any point in time within the backup window, typically up to the last 35 days.

### Key Features

- **Continuous Backup**: Automatically captures changes to your DynamoDB tables without impacting performance.
- **Flexible Recovery**: Restore to any point in time within the backup window, down to a second.
- **New Table Creation**: The recovery process generates a new table, ensuring your current operations are not disrupted.

### Use Cases

- **Accidental Deletion**: Quickly recover from accidental data deletions or loss.
- **Data Corruption Recovery**: Restore data to a point before corruption occurred.

## On-Demand Backups

On-demand backups allow you to create full backups of your DynamoDB tables for long-term retention. These backups are retained until explicitly deleted and can be used for archival purposes or compliance requirements.

### Key Features

- **Long-Term Retention**: Manually triggered backups that are stored indefinitely, providing a durable snapshot of your data.
- **Performance**: Creating backups does not affect table performance or latency.
- **AWS Backup Integration**: Manage backups and configure cross-region copies through AWS Backup, enhancing disaster recovery capabilities.
- **New Table Creation**: Similar to PITR, recovering from an on-demand backup creates a new table.

### Use Cases

- **Compliance and Archival**: Meet compliance requirements by retaining backups for specified durations.
- **Cross-Region Disaster Recovery**: Utilize AWS Backup for cross-region backup copies, ensuring data availability even in the event of regional disruptions.

## Getting Started

1. **Enable PITR**: Activate PITR on your DynamoDB tables through the AWS Management Console or AWS CLI.
2. **Create On-Demand Backups**: Initiate on-demand backups as needed for long-term retention or before making significant changes to your table structure.
3. **Manage Backups with AWS Backup**: Configure and manage your DynamoDB backups, including cross-region copying, through AWS Backup for enhanced disaster recovery planning.

By leveraging both PITR and on-demand backups, you can ensure your DynamoDB data remains secure and easily recoverable in the face of potential data loss scenarios.