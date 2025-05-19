# Aurora Backups

## Automated Backups

- Aurora automatically performs a full backup of your database daily and captures transaction logs as they are written.
- Retention period for these backups can be set between 1 and 35 days. Unlike RDS, **this cannot be disabled for Aurora**.
- Enables point-in-time recovery within the specified retention timeframe.

## Manual DB Snapshots

- Can be manually triggered by the user at any time.
- These snapshots are retained for as long as you want, providing a longer-term backup solution beyond the automated backup's retention period.