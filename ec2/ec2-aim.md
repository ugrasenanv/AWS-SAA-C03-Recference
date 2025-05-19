# AMI Overview

AMI stands for Amazon Machine Image. AMIs are customizations of an EC2 instance. You can add your own software, configurations, operating system, monitoring tools, and more. This results in faster boot and configuration times because all your software is pre-packaged.

AMIs are built for a specific region, but they can be copied across regions. You can launch EC2 instances from:

- A Public AMI: These are provided by AWS.
- Your Own AMI: You can create and maintain these yourself.
- An AWS Marketplace AMI: These are AMIs that someone else has created and potentially sells.

## AMI Process (from an EC2 instance)

The process of creating an AMI from an EC2 instance involves the following steps:

1. Start an EC2 instance and customize it.
2. Stop the instance to ensure data integrity.
3. Build an AMI. This will also create EBS snapshots.
4. Launch instances from your AMI.