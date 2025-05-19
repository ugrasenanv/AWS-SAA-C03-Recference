# CloudTrail Events Retention

Events are stored for 90 days in CloudTrail.

## Extended Retention

- **Log to S3**: To keep events beyond this period, log them to S3.
- **Use Athena**: Use Athena to query the stored events.