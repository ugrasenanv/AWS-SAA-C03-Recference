## Latency-Based Routing Policy

- Redirects users to the resource that offers the lowest latency, making it ideal for applications where user experience is dependent on latency.
- Latency is determined by the traffic conditions between the user and the AWS Regions.
- For example, users in Germany might be directed to resources in the US if that path offers the lowest latency.
- This routing policy can be associated with health checks, providing a failover capability in case the primary resource becomes unhealthy.