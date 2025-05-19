# CloudWatch vs CloudTrail vs Config

## CloudWatch

- **Performance Monitoring**: Metrics, CPU, network, etc., & dashboards.
- **Events & Alerting**.
- **Log Aggregation & Analysis**.

## CloudTrail

- **API Call Recording**: Record API calls made within your account by everyone.
- **Trail Definition**: Can define trails for specific resources.
- **Global Service**.

## Config

- **Configuration Recording**: Record configuration changes.
- **Compliance Evaluation**: Evaluate resources against compliance rules.
- **Timeline**: Get a timeline of changes and compliance.
# Elastic Load Balancer

## CloudWatch

- **Monitoring**:
    - Incoming connections metric.
    - Visualize error codes as a percentage over time.
    - Make a dashboard to get an idea of your load balancer performance.

## Config

- **Tracking**:
    - Track security group rules for the Load Balancer.
    - Track configuration changes for the Load Balancer.
    - Ensure an SSL certificate is always assigned to the Load Balancer (compliance).

## CloudTrail

- **API Call Tracking**:
    - Track who made any changes to the Load Balancer with API calls.