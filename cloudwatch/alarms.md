# CloudWatch Alarms

Amazon CloudWatch Alarms are used to trigger notifications for any metric based on various conditions and states.

## Features

- **Alarm States**:
    - **OK**: The metric is within the defined threshold.
    - **INSUFFICIENT\_DATA**: Not enough data is available to determine the state.
    - **ALARM**: The metric is outside the defined threshold.

- **Period**:
    - Length of time in seconds to evaluate the metric.
    - High resolution custom metrics: 10s, 30s, or multiples of 60s.

## Alarm Targets

- **EC2 Actions**:
    - Stop, terminate, reboot, or recover an EC2 instance.
- **Auto Scaling**:
    - Trigger Auto Scaling actions.
- **SNS Notifications**:
    - Send notifications to SNS, from which you can perform various actions.

## Composite Alarms

- **Single Metric Alarms**:
    - CloudWatch Alarms are based on a single metric.
- **Composite Alarms**:
    - Monitor the states of multiple other alarms.
    - Use AND and OR conditions.
    - Reduce "alarm noise" by creating complex composite alarms.