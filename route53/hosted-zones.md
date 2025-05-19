# Route 53 - Hosted Zones

Hosted Zones in Amazon Route 53 act as containers for records that define how to route traffic for a domain and its subdomains. There are two types of Hosted Zones:

## Public Hosted Zones

- **Purpose**: Contains records that specify how to route traffic on the internet for public domain names.
- **Example**: Routing traffic for `application1.mypublicdomain.com`.
- **Use Case**: Ideal for services and applications accessible over the internet.

## Private Hosted Zones

- **Purpose**: Contains records that specify how to route traffic within one or more Amazon Virtual Private Clouds (VPCs) for private domain names.
- **Example**: Routing traffic for `application1.company.internal`.
- **Use Case**: Suitable for internal services and applications that should not be accessible from the internet.

## Pricing

- **Cost**: You pay $0.50 per month for each hosted zone.

Hosted Zones are a fundamental component of managing DNS and traffic routing in AWS, allowing for precise control over how traffic is directed for both public-facing and internal resources.