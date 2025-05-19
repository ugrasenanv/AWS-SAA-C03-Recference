# EBS vs EFS

## EBS (Elastic Block Store)

- Can be attached to one instance at a time (except multi-attach io1/io2)
- Locked at the Availability Zone (AZ) level
- gp2: IO increases as the disk size increases
- gp3 & io1: Can increase IO independently
- To migrate an EBS volume across AZs, take a snapshot and restore it to another AZ
- EBS backups use IO and shouldn't be run while your application is handling a lot of traffic
- Root EBS Volumes of instances get terminated by default if the EC2 instance gets terminated (this can be disabled)

## EFS (Elastic File System)

- Can be mounted on hundreds of instances across AZs
- Ideal for sharing website files (e.g., WordPress)
- Only for Linux Instances (POSIX)
- Has a higher price point than EBS
- Can leverage storage tiers for cost savings