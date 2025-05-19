# RDS Backups

## Automated Backups

- Daily full backup of the database (during the backup window).
- Transaction logs are backed-up by RDS every 5 minutes.
- Provides the ability to restore to any point in time (from oldest backup to 5 minutes ago).
- Retention period can be set between 1 to 35 days, set to 0 to disable automated backups.

## Manual DB Snapshots

- Manually triggered by the user.
- Retention of backup for as long as you want.

## Trick

- In a stopped RDS database, you will still pay for storage. If you plan on stopping it for a long time, consider using snapshot & restore instead to save costs.