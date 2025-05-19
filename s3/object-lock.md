# Amazon S3 Object Lock and Glacier Vault Lock

Amazon S3 and Glacier offer features to enforce a Write Once Read Many (WORM) model, ensuring data immutability for compliance and data retention purposes. These features are crucial for meeting strict regulatory requirements and safeguarding data from accidental or malicious alterations and deletions.

## Glacier Vault Lock

Glacier Vault Lock allows you to apply and lock a policy on a Glacier vault, making the policy immutable. This feature is designed for long-term data archiving and retention.

### Key Steps:

1. **Adopt a WORM Model**: Ensure that once data is written to a Glacier vault, it cannot be overwritten or deleted.
2. **Create a Vault Lock Policy**: Define the policy according to your compliance and data retention needs.
3. **Lock the Policy**: Once the policy is in place and confirmed, lock it to prevent any future edits or deletion.

## S3 Object Lock

S3 Object Lock provides a way to prevent object versions from being deleted for a specified period.

### Features:

- **Retention Modes**:
    - **Compliance Mode**: Object versions cannot be overwritten or deleted by any user, including the root user. Retention modes and periods cannot be altered.
    - **Governance Mode**: Prevents most users from altering or deleting object versions. Users with special permissions can override these restrictions.
- **Retention Period**: Set a fixed period during which an object is protected from deletion or alteration. This period can be extended.
- **Legal Hold**: Offers indefinite protection, regardless of the retention period. It can be applied or removed with the appropriate IAM permissions.

### Use Cases:

- **Compliance and Regulatory Requirements**: Meet legal and regulatory standards by ensuring data immutability.
- **Data Retention Policies**: Implement and enforce data retention policies for sensitive or critical information.
- **Protection Against Deletion**: Safeguard against accidental or intentional deletion of important data.

By leveraging these features, organizations can enhance their data protection strategies and comply with regulatory standards.