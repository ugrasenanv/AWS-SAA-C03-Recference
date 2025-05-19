# Default VPC Walkthrough

All new AWS accounts have a default VPC. New EC2 instances are launched into the default VPC if no subnet is specified. The default VPC has Internet connectivity, and all EC2 instances inside it have public IPv4 addresses. We also get a public and a private IPv4 DNS names.

## VPC in AWS - IPv4

**VPC (Virtual Private Cloud)**

- Can have multiple VPCs in an AWS region (max. 5 per region - soft limit)
- Max. CIDR per VPC is 5, for each CIDR
    - Min. size is /28 (16 IP addresses)
    - Max. size is /16 (65536 IP addresses)

Because VPC is private, only the Private IPv4 ranges are allowed:
- **10.0.0.0 - 10.255.255.255** (10.0.0.0/8)
- **172.16.0.0 - 172.31.255.255** (172.16.0.0/12)
- **192.168.0.0 - 192.168.255.255** (192.168.0.0/16)

VPC CIDR should not overlap with your other networks.