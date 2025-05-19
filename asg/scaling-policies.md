# Scaling Policies

## Dynamic Scaling

### Target Tracking Scaling

- Simple to set up.
- Example: I want the average ASG CPU to stay at around 40%.

### Simple/Step Scaling

- When a CloudWatch alarm is triggered (example CPU > 70%), then add 2 units.
- When a CloudWatch alarm is triggered (example CPU < 30%), then remove 1 unit.

## Scheduled Scaling

- Anticipate scaling based on known usage patterns.
- Example: Increase the min capacity to 10 at 5 pm on Fridays.

## Predictive Scaling

- Continuously forecast load and schedule scaling ahead.

## Good Metrics to Scale On

- CPU Utilization: Average CPU utilization across your instances.
- RequestCountPerTarget: To make sure the number of requests per EC2 instances is stable.
- Average Network In/Out (if your application is network bound).
- Any custom metric (that you push using CloudWatch).

## ASG - Scaling Cooldowns

- After a scaling activity happens, you are in the cooldown period (default 300 seconds).
- During the cooldown period, the ASG will not launch or terminate additional instances (to allow for metrics to stabilize)
- Advice: Use a ready to use AMI to reduce configuration time in order to be serving request fasters and reduce the cooldown period