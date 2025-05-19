# FSx for Windows File Server

Amazon FSx for Windows File Server provides a fully managed native Microsoft Windows file system that supports the SMB protocol and Windows NTFS, offering a wide range of features designed for enterprise use.

## Key Features

- **SMB Protocol & Windows NTFS**: Ensures compatibility with Windows-based applications, supporting all features of the SMB protocol and NTFS, including file locking and hierarchical storage management.

- **Microsoft Active Directory Integration**: Seamlessly integrates with Microsoft Active Directory, allowing for simplified user and access management. Supports Access Control Lists (ACLs) and user quotas to manage data and user access efficiently.

- **Linux EC2 Instance Mounting**: Despite being a Windows-native file system, FSx for Windows File Server can be mounted on Linux EC2 instances, providing flexibility across different operating systems.

- **Support for Microsoft's DFS Namespaces**: Enables the grouping of files across multiple file systems, making it easier to manage and access files distributed across several FSx for Windows File Server instances.

## Performance and Scalability

- Capable of scaling up to tens of GB/s and millions of IOPS, supporting hundreds of petabytes of data. This makes it suitable for a wide range of high-performance workloads.

## Storage Options

- **SSD Storage**: Ideal for latency-sensitive workloads such as databases, media processing, and data analytics, offering high performance and low latency.

- **HDD Storage**: Provides a cost-effective solution for a broad spectrum of workloads, including home directories and content management systems.

## Accessibility

- **On-premises Access**: FSx for Windows File Server can be accessed from your on-premises infrastructure through VPN or AWS Direct Connect, facilitating hybrid cloud architectures and seamless data management between AWS and on-premises environments.