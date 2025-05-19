# Default Encryption vs. Bucket Policies in Amazon S3

Amazon S3 provides mechanisms to ensure your data is encrypted at rest, enhancing the security of your stored data. Here, we compare two approaches: Default Encryption and the use of Bucket Policies for enforcing encryption.

## Default Encryption

- **SSE-S3 Encryption**: When default encryption is enabled, Amazon S3 automatically applies Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3) to new objects stored in the bucket.
- **Automatic**: This encryption is applied without needing to specify any additional encryption headers when uploading objects.

## Bucket Policies for Enforcing Encryption

- **Forced Encryption**: You can enforce encryption on uploads (PUT operations) by using a bucket policy. This policy can refuse any API call that attempts to store an S3 object without the appropriate encryption headers.
- **SSE-KMS and SSE-C**: The policy can require that objects be encrypted with either Server-Side Encryption with AWS KMS-Managed Keys (SSE-KMS) or Server-Side Encryption with Customer-Provided Keys (SSE-C).
- **API Call Refusal**: Any PUT operation that does not include the required encryption headers will be denied, ensuring that all objects are encrypted according to the specified standards.

## Example Bucket Policy for Enforcing Encryption

```json
{
    "Version": "2012-10-17",
    "Id": "PutObjPolicy",
    "Statement": [
        {
            "Sid": "DenyIncorrectEncryptionHeader",
            "Effect": "Deny",
            "Principal": "*",
            "Action": "s3:PutObject",
            "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME/*",
            "Condition": {
                "StringNotEquals": {
                    "s3:x-amz-server-side-encryption": ["aws:kms", "AES256"]
                }
            }
        },
        {
            "Sid": "DenyUnEncryptedObjectUploads",
            "Effect": "Deny",
            "Principal": "*",
            "Action": "s3:PutObject",
            "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME/*",
            "Condition": {
                "Null": {
                    "s3:x-amz-server-side-encryption": "true"
                }
            }
        }
    ]
}