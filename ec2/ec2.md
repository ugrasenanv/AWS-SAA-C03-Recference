# EC2 Essentials

## Class Ports in EC2

- **SSH (Secure Shell)**: Port 22, used to log into a Linux instance.
- **FTP (File Transfer Protocol)**: Port 21, used to upload files into a file share.
- **SFTP (Secure File Transfer Protocol)**: Port 22, used to upload files using SSH.
- **HTTP**: Port 80, used to access unsecured websites.
- **HTTPS**: Port 443, used to access secured websites.
- **RDP (Remote Desktop Protocol)**: Port 3389, used to log into a Windows instance.

## EC2 Instance Types

- **On-demand**: Pay the full price for short workloads with predictable pricing.
- **Reserved**: Plan ahead for long workloads and get a good discount.
- **Savings Plans**: Commit to a certain amount of usage for a long workload.
- **Spot instances**: Bid for the empty rooms and the highest bidder keeps the rooms.
- **Dedicated hosts**: Book an entire physical server and control instance placement.
- **Capacity Reservations**: Reserve capacity in a specific AZ for any duration.

## Detailed Instance Types

### Reserved Instances

- Up to 72% discount compared to On-demand.
- Reserve a specific instance attributes (Instances type, Region, Tenancy, OS).
- Reservation Period - 1 year (+discount) or 3 years(+++discount).
- Payment Options - No Upfront (+), Partial Upfront (++), All Upfront(+++).
- Reserved Instance's scope - Regional or Zonal (reserve capacity in an AZ).
- Recommended for steady-state usage applications (think database).
- You can buy and sell in the Reserved Instance Marketplace.

### Savings Plans

- Get a discount based on long-term usage (up to 72% - same as RIs).
- Commit to a certain type of usage (10$/hour for 1 or 3 years).
- Usage beyond EC2 Saving Plans is billed at the On-Demand price.

### Dedicated Hosts

- A physical server with EC2 instance capacity fully dedicated to your use.
- Allow you to address compliance requirements and use your existing server-bound software licenses(per-socket, per-core, pre-VM software licenses).
- Purchasing options:
    - On-demand - pay per second for active Dedicated Host.
    - Reserved - 1 or 3 years (No Upfront, Partial Upfront, All Upfront).
- The most expensive option.
- Useful for software that have complicated licensing model (BYOL - Bring your own license).

### Dedicated Instances

- Instances run on hardware that's dedicated to you.
- May share hardware with other instances in the same account.
- No control over instance placement.

### Capacity Reservations

- Reserve On-Demand instances capacity in a specific AZ for any duration.
- You always have access to EC2 capacity when you need it.
- No time commitment (create/cancel anytime), no billing discounts.
- Combine with Regional Reserved Instances and Savings Plans to benefit from billing discounts.
- You're charged at On-Demand rate whether you run instances or not.
- Suitable for short-term, uninterrupted workloads that need to be in a specific AZ.

### Spot Instance Requests

- Can get a discount of up to 90% compared to On-Demand.
- Define max spot price and get the instance while current spot price < max.
- The hourly spot price varies based on offer and capacity.
- If the current spot price > your max price you can choose to stop or terminate your instance with a 2 minutes grace period.
- Other strategy: Spot block.
    - Block spot instance during a specified time frame (1 to 6 hours) without interruptions.
    - In rare situations, the instance may be reclaimed.
    - Used for batch jobs, data analysis, or workloads that are resilient to failures.
    - Not great for critical jobs or database.

### Storage Optimized EC2 instances

- Great for workloads requiring high, sequential read/write access to large data sets on local storage.

# EC2 - Elastic Compute Cloud (Infrastructure as a Service)

EC2 primarily provides the ability to:

- Rent virtual machines (EC2)
- Store data on virtual drives (EBS)
- Distribute load across machines (ELB)
- Scale the services using an auto-scaling group (ASG)

## EC2 User Data

EC2 User data scripts allow for bootstrapping of our instances. Bootstrapping refers to the execution of commands when a machine starts. This script is only run once at the instance's first start. EC2 user data is used to automate boot tasks such as:

- Installing updates
- Installing software
- Downloading common files from the internet
- Any other task you can think of

The EC2 User Data script runs with the root user.
