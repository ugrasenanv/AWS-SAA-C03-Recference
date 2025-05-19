# EC2 Instance Store

- EC2 Instance Store provides high-performance hardware disks for your EC2 instances. Unlike EBS volumes, which are network drives with good but limited performance, EC2 Instance Store offers better I/O performance.

- However, EC2 Instance Store volumes are ephemeral, meaning they lose their storage if the instance is stopped. This makes them suitable for buffer, cache, scratch data, or temporary content that does not need to be persistent.

- It's important to note that there is a risk of data loss if the hardware fails. Therefore, managing backups and replication of data stored on EC2 Instance Store volumes is your responsibility.