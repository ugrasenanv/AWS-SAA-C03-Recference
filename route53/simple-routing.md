## Simple Routing Policy

- Directs traffic to a single resource, typically used for routing to a specific server or service.
- Allows specifying multiple values within the same DNS record.
    - When multiple values are present, the DNS resolver randomly selects one for the client.
- When using an Alias record with the Simple routing policy:
    - Only a single AWS resource can be specified.
- Simple routing policies cannot be associated with health checks.