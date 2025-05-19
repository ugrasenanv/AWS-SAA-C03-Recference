# Private vs Public IP (IPv4)

## Public IP

- Public IP means the machine can be identified on the internet.
- Must be unique across the whole web (not two machines can have the same public IP).
- Can be geo-located easily.

## Private IP

- Private IP means the machine can only be identified on a private network only.
- The IP must be unique across the private network.
- But two different private networks (two companies) can have the same IPs.
- Machines connect to WWW using an internet gateway (a proxy).
- Only a specified range of IPs can be used as private IP.

# Elastic IP

With an Elastic IP address, you can mask the failure of an instance or software by rapidly remapping the address to another instance in your account.

- You can only have 5 Elastic IP in your account (can ask AWS to increase that).
- Overall, try to avoid using Elastic IP:
    - They often reflect poor architectural decisions.
    - Instead, use a random public IP and register a DNS name to it.
    - Or, as we'll see later use a Load Balancer and don't use a public IP.