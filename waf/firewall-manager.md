# AWS Firewall Manager

## Overview

- **Manage Rules**: Manage rules in all accounts of an AWS Organization.
- **Security Policy**: Common set of security rules.

## Security Policy Components

- **WAF Rules**: For Application Load Balancer, API Gateways, CloudFront.
- **AWS Shield Advanced**: For ALB, CLB, NLB, Elastic IP, CloudFront.
- **Security Groups**: For EC2, Application Load Balancer, and ENI resources in VPC.
- **AWS Network Firewall**: At the VPC level.
- **Amazon Route 53 Resolver DNS Firewall**: Policies are created at the region level.

## Policy Application

- **Automatic Rule Application**: Rules are applied to new resources as they are created.
- **Compliance**: Ensures compliance across all and future accounts in your Organization.