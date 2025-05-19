To create a policy for an S3 bucket that accomplishes the following goals, you can follow these steps in a markdown document:

1. **Grant Public Read Access**: This policy allows anyone to read objects from the specified bucket. It's important to replace `your-bucket-name` with the actual name of your S3 bucket.

- **Sid**: PublicRead
- **Effect**: Allow
- **Principal**: \*
- **Action**: s3:GetObject
- **Resource**: arn:aws:s3:::your-bucket-name/\*

2. **Deny Unencrypted Object Uploads**: This policy denies the upload of objects that are not encrypted with server-side encryption using AES256. This ensures that all uploaded objects are encrypted.

- **Sid**: DenyUnencryptedObjectUploads
- **Effect**: Deny
- **Principal**: \*
- **Action**: s3:PutObject
- **Resource**: arn:aws:s3:::your-bucket-name/\*
- **Condition**:
    - **StringNotEquals**:
        - **s3:x-amz-server-side-encryption**: AES256

3. **Grant Cross-Account Access**: This policy allows a specified AWS account to perform `GetObject`, `PutObject`, and `DeleteObject` actions on the bucket. Replace `account-id-of-other-account` with the AWS account ID and `username-of-other-account` with the username in that account you wish to grant access to.

- **Sid**: CrossAccountAccess
- **Effect**: Allow
- **Principal**:
    - **AWS**: arn:aws:iam::account-id-of-other-account:user/username-of-other-account
- **Action**:
    - s3:GetObject
    - s3:PutObject
    - s3:DeleteObject
- **Resource**: arn:aws:s3:::your-bucket-name/\*

Ensure to replace placeholders like `your-bucket-name`, `account-id-of-other-account`, and `username-of-other-account` with actual values relevant to your AWS S3 setup.

```
{
    "Version": "2012-10-17",
    "Id": "Policy1720364221505",
    "Statement": [
        {
            "Sid": "Stmt1720364219499",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::hienpham-bucket/*"
        }
    ]
}
```