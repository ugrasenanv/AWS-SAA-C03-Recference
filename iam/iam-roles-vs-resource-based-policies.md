# IAM Roles vs Resource-Based Policies

## Cross Account Access

- **Resource-Based Policy**: Attach a policy directly to a resource (e.g., S3 bucket policy).
- **IAM Role**: Use a role as a proxy.

### Key Differences

- **Assuming a Role**:
    - When a user, application, or service assumes a role, they give up their original permissions and take on the permissions assigned to the role.
- **Resource-Based Policy**:
    - The principal does not have to give up their permissions when accessing the resource.

### Example Scenario

- **User in Account A**:
    - Needs to scan a DynamoDB table in Account A.
    - Needs to dump the data into an S3 bucket in Account B.

### Supported Resources

- **S3 Buckets**
- **SNS Topics**
- **SQS Queues**