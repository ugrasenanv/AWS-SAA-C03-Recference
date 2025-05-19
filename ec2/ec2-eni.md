# Elastic Network Interface (ENI)

An ENI is a logical component within a VPC that represents a virtual network card. It can have the following attributes:

- Primary private IPv4, one or more secondary IPv4
- One Elastic IP (IPv4) per private IPv4
- One public IPv4 Elastic IP
- One or more security groups
- A MAC address

ENIs can be created independently and attached on the fly (or moved) to EC2 instances for failover. They are bound to a specific Availability Zone (AZ).

