# Elastic Load Balancing (EBS)

Elastic Load Balancing is a service that automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances.

## Why Use a Load Balancer

- **Spread Load**: Distributes traffic across multiple downstream instances.
- **Single Access Point**: Exposes a single point of access (DNS) to your application.
- **Handle Failures**: Seamlessly handles failures of downstream instances.
- **Health Checks**: Performs regular health checks on your instances.
- **SSL Termination**: Provides SSL termination (HTTPS) for websites.
- **Enforce Stickiness**: Enforces stickiness with cookies.
- **High Availability**: Ensures high availability across zones.
- **Traffic Separation**: Separates public traffic from private traffic.

## Types of Load Balancers on AWS

AWS provides four types of managed Load Balancers:

- **Classic Load Balancer (CLB)**: This is the old generation load balancer introduced in 2009. It supports HTTP, HTTPS, TCP, and SSL (secure TCP).
- **Application Load Balancer (ALB)**: This is a new generation load balancer introduced in 2016. It supports HTTP, HTTPS, and WebSocket.
- **Network Load Balancer (NLB)**: This is a new generation load balancer introduced in 2017.
- **Gateway Load Balancer (GWLB)**: Introduced in 2020, it operates at layer 3 (Network layer) - IP protocol.

Some load balancers can be set up as internal (private) or external (public) ELBs.