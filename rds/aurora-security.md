# Aurora Security

## At-rest Encryption

- Utilizes AWS Key Management Service (KMS) for encrypting the database master and its replicas.
- Encryption must be defined at launch time; it cannot be applied retroactively to an existing database without encryption.
- If the master database is not encrypted, its read replicas cannot be encrypted either.
- To encrypt an unencrypted database, create a DB snapshot and then restore it as an encrypted database.

## In-flight Encryption

- Aurora is TLS-ready by default, ensuring data is encrypted during transit.
- Utilize AWS TLS root certificates on the client-side to establish a secure connection.

## IAM Authentication

- Supports IAM roles for database authentication, offering an alternative to traditional username and password methods.
- Enhances security by leveraging AWS IAM's robust access control capabilities.

## SSH Access

- SSH access is not available for Aurora instances, except on RDS Custom, to maintain a high level of security.

## Audit Logs

- Audit logs can be enabled to track and record database activities.
- Logs can be sent to AWS CloudWatch Logs for longer retention and analysis.