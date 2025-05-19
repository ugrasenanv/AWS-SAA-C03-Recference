# Calculated Health Checks in Route 53

Calculated Health Checks allow you to aggregate the results of multiple health checks into a single, composite health check. This feature is particularly useful for managing complex architectures or for performing maintenance without causing widespread health check failures.

## Key Features

- **Logical Operators**: Use `OR`, `AND`, or `NOT` to combine the results of child health checks.
- **Child Health Checks**: You can monitor up to 256 child health checks under a single calculated health check.
- **Passing Criteria**: Specify the number of child health checks that need to pass for the calculated health check to be considered healthy.

## Use Cases

- **Maintenance Mode**: By adjusting the logical operators and passing criteria, you can perform maintenance on part of your infrastructure without causing the overall health check to fail. This is useful for minimizing the impact on your application's perceived availability.

## Configuration Example

1. **Create Child Health Checks**: Begin by setting up individual health checks for each component of your application.
2. **Create a Calculated Health Check**: Combine these child health checks using a calculated health check. Choose an appropriate logical operator based on your requirements.
    - For maintenance, you might use an `OR` condition with a threshold that allows for one or more components to be down without affecting the overall health status.
3. **Specify Passing Criteria**: Decide how many child health checks must pass for the calculated health check to be considered healthy. This number can be adjusted based on the criticality of each component.

By leveraging calculated health checks, you can achieve a more nuanced monitoring setup that reflects the actual health of your distributed system or application.