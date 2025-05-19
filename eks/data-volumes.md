# Data Volumes in Amazon EKS

Amazon Elastic Kubernetes Service (EKS) supports various data volume options for your containers, leveraging the Container Storage Interface (CSI) compliant drivers. This allows for the specification of `StorageClass` manifests in your EKS cluster to manage storage resources efficiently.

## Supported Storage Options

EKS supports a range of AWS storage services, each suitable for different use cases:

- **Amazon EBS (Elastic Block Store)**: Offers block-level storage volumes for persistent storage at the pod level. Ideal for databases or other storage-intensive applications.

- **Amazon EFS (Elastic File System)**: Provides a simple, scalable, fully managed elastic NFS file system for use with AWS Cloud services and on-premises resources. It's compatible with AWS Fargate, making it a flexible option for serverless applications.

- **Amazon FSx for Lustre**: A fully managed file system that is optimized for compute-intensive workloads, such as high-performance computing, machine learning, and media data processing workflows.

- **Amazon FSx for NetApp ONTAP**: Offers a fully managed enterprise storage service with rich data management features, supporting NFS, SMB, and iSCSI protocols.

## Specifying a StorageClass

To utilize these storage options in your EKS cluster, you need to define a `StorageClass` resource. This manifest tells Kubernetes how to provision storage for your pods based on the underlying storage system.
