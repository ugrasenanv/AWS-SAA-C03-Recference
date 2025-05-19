## S3 Security Overview

### User-based Security

- **IAM Policies**: Define what API calls are allowed for a specific user from AWS Identity and Access Management (IAM). These policies can be attached directly to IAM users, groups, or roles to grant or deny access to S3 resources.

### Resource-based Security

- **Bucket Policies**: Set at the bucket level, these policies allow for bucket-wide rules that can be configured via the S3 console. They enable scenarios such as granting access to users from other AWS accounts (cross-account access).
- **Object Access Control List (ACL)**: Provides a finer grain of control over individual objects within an S3 bucket. This allows for specific permissions to be set on a per-object basis. Object ACLs can be disabled if not needed.
- **Bucket Access Control List (ACL)**: Similar to object ACLs but applied at the bucket level. These are less common and can also be disabled.

### Access Decision Logic

An IAM principal (user or role) can access an S3 object if:
- The IAM permissions attached to the principal **ALLOW** access to the object, **OR**
- The resource policy (bucket policy) **ALLOWS** access to the object,
- And there is no explicit **DENY** statement in either the IAM permissions or the resource policy.

### Encryption

- **Encryption in Transit**: S3 supports HTTPS for secure data transmission.
- **Encryption at Rest**: Objects in S3 can be encrypted using various methods, including:
    - **Server-Side Encryption** (SSE):
        - **SSE-S3**: Uses keys managed by AWS S3.
        - **SSE-KMS**: Uses AWS Key Management Service (KMS) for key management, providing additional controls.
        - **SSE-C**: Allows customers to provide their encryption keys.
    - **Client-Side Encryption**: The data is encrypted on the client's side before being uploaded to S3. The client is also responsible for decrypting the data when needed.