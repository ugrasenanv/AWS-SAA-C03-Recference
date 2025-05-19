# ECS Service Auto Scaling

Amazon ECS Auto Scaling adjusts the number of tasks in your ECS service automatically. This feature leverages AWS Application Auto Scaling to ensure that your services maintain optimal performance and cost efficiency. There are several metrics and methods to configure auto-scaling, catering to different use cases.

## Key Metrics for Auto Scaling

- **ECS Service Average CPU Utilization**: Scales the number of tasks based on the average CPU utilization of your service.
- **ECS Service Average Memory Utilization**: Scales based on the average memory utilization of the tasks in your service.
- **ALB Request Count Per Target**: Utilizes the number of requests per target in an Application Load Balancer as a metric for scaling.

## Auto Scaling Policies

### Target Tracking

Automatically adjusts the number of tasks to keep a selected metric as close as possible to the target value. Suitable for most use cases where the load varies over time.

### Step Scaling

Scales in or out in steps, based on CloudWatch alarms. This method is useful for fine-grained control over scaling actions in response to changing metrics.

### Scheduled Scaling

Allows scaling actions to be scheduled based on predictable workload changes. This is ideal for scenarios where you expect sharp increases or decreases in load at specific times.

## ECS vs. EC2 Auto Scaling

- **ECS Service Auto Scaling** focuses on the task level, adjusting the number of tasks within an ECS service.
- **EC2 Auto Scaling** operates at the EC2 instance level, managing the number of instances within an EC2 Auto Scaling group.

## Fargate Auto Scaling

- **Simplicity**: Setting up auto-scaling with Fargate is straightforward due to its serverless nature, eliminating the need to manage underlying instances.

By leveraging ECS Auto Scaling, you can ensure that your services are always running with the optimal number of tasks, improving both performance and cost efficiency.