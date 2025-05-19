# Node Types in Amazon EKS

Amazon Elastic Kubernetes Service (EKS) supports various node types to cater to different use cases and operational preferences. Here's an overview of the node types available in EKS.

## Managed Node Groups

Managed Node Groups simplify the process of managing nodes (EC2 instances) in your EKS cluster.

- **Automated Management**: EKS creates and manages the nodes for you.
- **Auto Scaling Groups (ASG)**: Nodes are part of an ASG managed by EKS, ensuring that your cluster scales according to demand.
- **Instance Types**: Supports both on-demand or spot instances, giving you flexibility in cost and availability.

## Self-Managed Nodes

For users who prefer more control, self-managed nodes allow you to create and register nodes to your EKS cluster.

- **User Managed**: Nodes are created and managed by you but are registered to the EKS cluster.
- **Amazon EKS Optimized AMI**: Can utilize prebuilt AMIs optimized for EKS, simplifying setup.
- **Flexibility**: Supports on-demand or spot instances, according to your cost and performance needs.

## AWS Fargate

AWS Fargate offers a serverless compute engine for containers, eliminating the need to manage nodes altogether.

- **Serverless**: With Fargate, there's no need to provision or manage servers; AWS handles the infrastructure.
- **Maintenance-Free**: Offers a completely hands-off approach to running containers, ideal for simplifying operations.