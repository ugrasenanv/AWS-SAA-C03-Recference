# Route 53 - Routing Policies

Routing policies in Route 53 define how it responds to DNS queries. It's important not to confuse this with load balancer routing, which actively routes traffic. DNS, including Route 53, does not route traffic but responds to DNS queries by directing users to specific IP addresses.

## Supported Routing Policies

- **[Simple](./simple-routing)**: Uses a single resource that performs a given function for your domain, e.g., a web server for your website.

- **[Weighted](./weighted-routing.md)**: Assigns weights to resources to specify the proportion of DNS queries that each should handle.

- **[Latency-Based](./latencty-routing.md)**: Redirects users to the resource that offers the lowest latency, making it ideal for applications where user experience is dependent on latency.

- **[Failover](./failover-routing.md)**: Configures active-passive failover, directing traffic to a secondary resource if the primary is unhealthy.

- **[Geolocation](./geolocation-routing.md)**: Routes traffic based on the geographic location of your users.

- **[Multi-Value Answer](./multi-value-routing.md)**: Responds to DNS queries with up to eight healthy records selected at random.

- **[Geoproximity](./geoproximity-routing.md)** (using Route 53 Traffic flow feature): Routes traffic based on the geographic location of your users and your resources, optionally adjusting traffic distribution based on bias values.