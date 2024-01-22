# EBS Overview

Amazon Elastic Block Store (EBS) is a block storage service provided by Amazon Web Services (AWS) for use with Amazon Elastic Compute Cloud (EC2) instances. 

It enables users to create scalable and high-performance block-level storage volumes that can be attached to EC2 instances. 

EBS volumes are designed for durability and high availability, providing a reliable storage solution for various applications.

### Volume Types:

| Volume Type              | Description                                             | Characteristics                                                                                                                                                                  |
|--------------------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **General Purpose SSD (gp2**) | Balanced price and performance for various workloads.    | Suitable for boot volumes and small to medium-sized databases. <br>Burst performance available for short periods.                                                            |
| **Provisioned IOPS SSD (io2)**| High-performance volumes with provisioned IOPS.          | Ideal for I/O-intensive workloads requiring consistent performance. <br>Higher durability and more IOPS per GB compared to io1.                                              |
| **Throughput Optimized HDD (st1)** | Designed for high-throughput workloads.            | Suitable for big data, data warehouses, and log processing. <br>Low-cost magnetic storage with better throughput.                                                            |
| **Cold HDD (sc1)**           | Cost-effective volumes for less frequently accessed data. | Suitable for large, sequential workloads with infrequent access. <br>Low-cost magnetic storage with lower throughput compared to st1.                                          |
| **Magnetic (standard)**      | Legacy volume type with traditional magnetic hard drives. | Being phased out. <br>Used for workloads with low I/O requirements where cost is a significant factor.                                                                      |


### Snapshots:

- EBS snapshots are point-in-time copies of EBS volumes.
- They are stored incrementally, which means only the changes since the last snapshot are saved.
- Snapshots can be used for backup, data recovery, and to create new volumes.


### Volume Encryption:

- EBS volumes can be encrypted using AWS Key Management Service (KMS) keys.
- Encryption helps protect sensitive data and ensures compliance with security standards.

### EBS Encryption

When you create an encrypted EBS volume, you get the following:
- Data at rest is encrypted inside the volume
- All the data in flight moving between the instance and the volume is encrypted
- All snapshots are encrypted
- All volumes created from the snapshot
- Encryption and decryption are handled transparently (you have nothing to do)
- Encryption has a minimal impact on latency
- EBS Encryption leverages keys from KMS (AES-256)
- Copying an unencrypted snapshot allows encryption
- Snapshots of encrypted volumes are encrypted

### Encryption: encrypt an unencrypted EBS volume

1. Create an EBS snapshot of the volume
2. Encrypt the EBS snapshot ( using copy )
3. Create new ebs volume from the snapshot ( the volume will also be encrypted )
4. Now you can attach the encrypted volume to the original instance


### Lifecycle Management:

- Users can create, delete, and attach EBS volumes to EC2 instances as needed.
- Volumes persist independently of the lifecycle of an EC2 instance, allowing data to be retained even if the instance is terminated.


# EFS Overview

Amazon Elastic File System (Amazon EFS) is a scalable, fully managed file storage service provided by Amazon Web Services (AWS). 

It is designed to provide scalable, elastic, and highly available shared file storage for use with AWS Cloud services and on-premises resources.

**Scalability:**
- Amazon EFS is designed to grow and shrink automatically as you add or remove files, so you don't need to provision and manage capacity.

**Fully Managed:**
- AWS takes care of the operational aspects, such as hardware provisioning, software configuration, and maintenance. This allows you to focus on your applications rather than managing storage infrastructure.

**Shared File Storage:**
- Amazon EFS allows multiple Amazon EC2 instances to access the same file system simultaneously, making it suitable for workloads that require shared access to data.

**Compatibility:**
- It is compatible with the Network File System version 4 (NFSv4) protocol, which is a widely used file system protocol for UNIX and Linux systems.

**Performance:**
- EFS is designed to provide low-latency performance and throughput for a broad spectrum of workloads.

**Regional Availability:**
- Amazon EFS is regionally distributed and provides high availability and durability across multiple Availability Zones within a region.

**Security:**
- It supports AWS Identity and Access Management (IAM) for access control and integrates with Virtual Private Cloud (VPC) for network security.

**Backup and Restore:**
- EFS provides features for creating backups and restoring file systems, ensuring data protection.

**Lifecycle Management:**
- EFS supports lifecycle management policies, allowing you to automatically move files to Standard-IA (Infrequent Access) storage class after a certain period.

**Use Cases:**
- Common use cases for Amazon EFS include content repositories, big data analytics, web serving, and application development.

**Performance Modes:**
- EFS offers two performance modes: General Purpose (default) and Max I/O.
- General Purpose mode is suitable for most workloads, while Max I/O mode is designed for latency-sensitive workloads.

**Throughput Modes:**
- EFS supports two throughput modes: Bursting and Provisioned Throughput.
- Bursting mode is suitable for most workloads, while Provisioned Throughput is designed for applications with high throughput requirements.
