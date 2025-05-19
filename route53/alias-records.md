# Route 53 - Alias Records

- Maps a hostname to an AWS resource.
- An extension to DNS functionality.
- Automatically recognizes changes in the resource's IP addresses.
- Unlike CNAME, it can be used for the top node of DNS namespace (Zone Apex), e.g., `example.com`.
- Alias Record is always of type A/AAAA for AWS resources (IPv4/IPv6).
- You can't set the TTL.