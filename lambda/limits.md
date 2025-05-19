# AWS Lambda Limits

AWS Lambda has specific limits for both execution and deployment phases to ensure efficient resource utilization and performance. Understanding these limits is crucial for optimizing your Lambda functions.

## Execution Limits

- **Memory Allocation**: Ranges from 128MB to 10GB, adjustable in 1MB increments, affecting both performance and cost.
- **Maximum Execution Time**: Limited to 900 seconds (15 minutes), after which the function is terminated.
- **Environment Variables**: Limited to 4KB in size, used for storing configuration settings and secrets.
- **Disk Capacity in "/tmp"**: Provides 512MB of storage for temporary files during function execution.
- **Concurrency Executions**: Default limit of 1000 concurrent executions, with the possibility of increasing this limit upon request.

## Deployment Limits

- **Lambda Function Deployment Size**: The compressed .zip file size must not exceed 50MB.
- **Size of Uncompressed Deployment**: The total size of code and dependencies after extraction must not exceed 250MB.
- **Usage of "/tmp" Directory**: Functions can use the /tmp directory to load additional files at startup, subject to the available disk capacity limit.
- **Size of Environment Variables**: Similar to the execution phase, limited to 4KB.

These limits are designed to balance the flexibility of AWS Lambda with the need for managing resources effectively across all users.