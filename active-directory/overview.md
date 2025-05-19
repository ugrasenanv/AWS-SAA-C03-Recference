# Microsoft Active Directory (AD)

- **Availability**: Found on any Windows Server with AD Domain Services.
- **Database of Objects**: Includes User Accounts, Computers, Printers, File Shares, Security Groups.
- **Centralized Security Management**: Allows for creating accounts and assigning permissions.
- **Organization**:
    - **Trees**: Objects are organized in trees.
    - **Forest**: A group of trees forms a forest.

## AWS Managed Microsoft AD

- **Creation**: Create your own AD in AWS.
- **Management**: Manage users locally.
- **Support**: Supports Multi-Factor Authentication (MFA).
- **Trust Connections**: Establish trust connections with your on-premise AD.

## AD Connector

- **Function**: Acts as a Directory Gateway (proxy) to redirect to on-premise AD.
- **Support**: Supports MFA.
- **User Management**: Users are managed on the on-premise AD.

## Simple AD

- **Function**: AD-compatible managed directory on AWS.
- **Limitation**: Cannot be joined with on-premise AD.