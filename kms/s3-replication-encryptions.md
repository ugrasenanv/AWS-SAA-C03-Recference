# S3 Replication Encryption Considerations

## Default Replication

- **Unencrypted Objects**: Replicated by default.
- **SSE-S3 Encrypted Objects**: Replicated by default.

## SSE-C Encrypted Objects

- **Replication**: Objects encrypted with SSE-C (customer provided key) can be replicated.

## SSE-KMS Encrypted Objects

- **Enable Option**: You need to enable the option for replication.
    - **Specify KMS Key**: Specify which KMS Key to encrypt the objects within the target bucket.
    - **KMS Key Policy**: Adapt the KMS Key Policy for the target key.
    - **IAM Role**: An IAM Role with `kms:Decrypt` for the source KMS Key and `kms:Encrypt` for the target KMS Key.
    - **KMS Throttling Errors**: Might get KMS throttling errors, in which case you can ask for a Service Quotas increase.

## Multi-Region AWS KMS Keys

- **Usage**: Can use multi-region AWS KMS Keys.
- **Treatment**: Currently treated as independent keys by S3 (the object will still be decrypted and then encrypted).