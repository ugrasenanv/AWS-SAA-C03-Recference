# Amazon Inspector

- **Automated Security Assessments**
- **For EC2 Instances**: Leveraging the AWS System Manager (SSM) agent
    - Analyze against unintended network accessibility
    - Analyze the running OS against known vulnerabilities

## For Container Images

- **Push to Amazon ECR**: Assessment of container images as they are pushed

## For Lambda Functions

- **Identifies Software Vulnerabilities**: In function code and package dependencies
- **Assessment of Functions**: As they are deployed

## Reporting & Integration

- **AWS Security Hub**
- **Send Findings to Amazon EventBridge**