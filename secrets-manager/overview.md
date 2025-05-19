# AWS Secrets Manager

## Overview

- **Newer Service**: Meant for storing secrets.
- **Rotation**: Capability to force rotation of secrets every X days.
- **Automation**: Automate generation of secrets on rotation (uses Lambda).
- **Integration**: Integration with Amazon RDS (MySQL, PostgreSQL, Aurora).
- **Encryption**: Secrets are encrypted using KMS.
- **Primary Use**: Mostly meant for RDS integration.

## Multi-Region Secrets

- **Replication**: Replicate secrets across multiple AWS Regions.
- **Synchronization**: Secrets Manager keeps read replicas in sync with the primary secret.
- **Promotion**: Ability to promote a read replica secret to a standalone secret.

## Use Cases

- **Multi-Region Apps**
- **Disaster Recovery Strategies**
- **Multi-Region Databases**