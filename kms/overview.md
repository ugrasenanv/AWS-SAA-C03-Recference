# AWS Key Management Service (KMS)

- **Common Use**: Anytime you hear encryption for an AWS service, it's most likely KMS.
- **Key Management**: AWS manages encryption keys for us.
- **Integration**: Fully integrated with IAM for authorization.
- **Auditing**: Able to audit KMS Key usage using CloudTrail.
- **Service Integration**: Seamlessly integrated into most AWS services (EBS, S3, RDS, SSM, etc.).
- **Security**: Never store your secrets in plaintext, especially in your code.
- **API Access**: KMS Key Encryption also available through API calls (SDK, CLI).
- **Terminology**: KMS Keys is the new name of KMS Customer Master Key.

## Types of KMS Keys

### Symmetric (AES-256 keys)

- **Usage**: Single encryption key that is used to Encrypt and Decrypt.
- **Integration**: AWS services that are integrated with KMS use Symmetric CMKs.
- **Access**: You never get access to the KMS key unencrypted (must call KMS API to use).

### Asymmetric (RSA & ECC key pairs)

- **Usage**: Public (Encrypt) and Private Key (Decrypt) pair.
- **Operations**: Used for Encrypt/Decrypt, or Sign/Verify operations.
- **Access**: The public key is downloadable, but you can't access the Private Key unencrypted.
- **Use Case**: Encryption outside of AWS by users who can't call the KMS API.

## Types of KMS Keys

- **AWS Owned Keys (free)**: SSE-S3, SSE-SQS, SSE-DDB (default key).
- **AWS Managed Key**: Free (aws/service-name, example: aws/rds or aws/ebs).
- **Customer Managed Keys Created in KMS**: $1/month.
- **Customer Managed Keys Imported**: $1/month + pay for API call to KMS ($0.03/10000 calls).

## Automatic Key Rotation

- **AWS Managed KMS Key**: Automatic every 1 year.
- **Customer-managed KMS Key**: (must be enabled) automatic & on-demand.
- **Imported KMS Key**: Only manual rotation possible using alias.

## KMS Key Policies

- **Control Access**: Control access to KMS keys, similar to S3 bucket policies.
- **Difference**: You cannot control access without them.

### Default KMS Key Policy

- **Creation**: Created if you don't provide a specific KMS Key Policy.
- **Access**: Complete access to the key to the root user = entire AWS account.

### Custom KMS Key Policy

- **Definition**: Define users, roles that can access the KMS key.
- **Administration**: Define who can administer the key.
- **Use Case**: Useful for cross-account access of your KMS key.

## Copying Snapshots Across Accounts

1. Create a Snapshot, encrypted with your own KMS Key.
2. Attach a KMS Key Policy to authorize cross-account access.
3. Share the encrypted snapshot.
4. (In target) Create a copy of the Snapshot, encrypt it with a CMK in your account.

