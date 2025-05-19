# API Gateway - Endpoint Types

## Edge-Optimized (Default)

- **Global Clients**: For global clients.
- **Routing**: Requests are routed through the CloudFront Edge locations (improves latency).
- **Region**: The API Gateway still lives in only one region.

## Regional

- **Same Region Clients**: For clients within the same region.
- **Manual CloudFront Integration**: Could manually combine with CloudFront for more control over caching strategies and distribution.

## Private

- **VPC Access**: Can only be accessed from your VPC using an interface VPC endpoint (ENI).
- **Resource Policy**: Use a resource policy to define access.