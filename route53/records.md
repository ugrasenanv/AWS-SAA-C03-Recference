# Route 53 - DNS Records

DNS records in Amazon Route 53 are used to control how traffic is routed for your domain. Each DNS record within Route 53 contains several pieces of information critical for directing traffic appropriately.

## Components of a DNS Record

- **Domain/Subdomain Name**: The name for which the DNS record is created, such as `example.com` or `sub.example.com`.
- **Record Type**: Specifies the type of the DNS record, such as A, AAAA, CNAME, or NS.
- **Value**: The output that the DNS record points to, which could be an IP address or another domain name, depending on the record type.
- **Routing Policy**: Determines how Amazon Route 53 responds to queries: simple, weighted, latency, failover, geolocation, or multivalue answer routing.

## Common Record Types

- **A Record**: Maps a hostname to an IPv4 address. For example, mapping `example.com` to `12.34.56.78`.
- **AAAA Record**: Maps a hostname to an IPv6 address.
- **CNAME Record**: Maps a hostname to another hostname. The target domain name must have an A or AAAA record. CNAME records cannot be created for the zone apex (e.g., `example.com`). Instead, they are used for subdomains like `www.example.com`.
- **NS Record**: Specifies the Name Servers for the Hosted Zone, controlling how traffic is routed for a domain.

## Routing Policies

Route 53 supports various routing policies to manage traffic efficiently:

- **Simple Routing**: A straightforward policy for routing traffic to a single resource.
- **Weighted Routing**: Distributes traffic across multiple resources, specifying a weight for each.
- **Latency Routing**: Routes traffic based on the lowest network latency for your end user.
- **Failover Routing**: Routes traffic to a backup resource in case the primary is unavailable.
- **Geolocation Routing**: Routes traffic based on the geographic location of your users.
- **Multivalue Answer Routing**: Responds to DNS queries with up to eight healthy records selected at random.

By configuring DNS records and routing policies in Route 53, you can effectively manage how traffic is directed for your domains and subdomains, ensuring optimal performance and reliability for your users.