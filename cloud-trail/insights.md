# CloudTrail Insights

Enabled CloudTrail Insights to detect unusual activity in your AWS account.

## Features

- **Detection of Unusual Activity**:
    - Inaccurate resource provisioning
    - Hitting service limits
    - Bursts of AWS IAM actions
    - Gaps in periodic maintenance activity

## How It Works

- **Baseline Creation**:
    - CloudTrail Insights analyzes normal management events to create a baseline.

- **Continuous Analysis**:
    - Continuously analyzes write events to detect unusual patterns.

## Anomaly Detection

- **Anomalies**:
    - Appear in the CloudTrail console.
    - Event is sent to S3.
    - An EventBridge event is generated.