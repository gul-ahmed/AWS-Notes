# EBS Overview

Amazon Elastic Block Store (EBS) is a block storage service provided by Amazon Web Services (AWS) for use with Amazon Elastic Compute Cloud (EC2) instances. 

It enables users to create scalable and high-performance block-level storage volumes that can be attached to EC2 instances. 

EBS volumes are designed for durability and high availability, providing a reliable storage solution for various applications.

# Volume Types:

| Volume Type              | Description                                             | Characteristics                                                                                                                                                                  |
|--------------------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **General Purpose SSD (gp2**) | Balanced price and performance for various workloads.    | Suitable for boot volumes and small to medium-sized databases. <br>Burst performance available for short periods.                                                            |
| **Provisioned IOPS SSD (io2)**| High-performance volumes with provisioned IOPS.          | Ideal for I/O-intensive workloads requiring consistent performance. <br>Higher durability and more IOPS per GB compared to io1.                                              |
| **Throughput Optimized HDD (st1)** | Designed for high-throughput workloads.            | Suitable for big data, data warehouses, and log processing. <br>Low-cost magnetic storage with better throughput.                                                            |
| **Cold HDD (sc1)**           | Cost-effective volumes for less frequently accessed data. | Suitable for large, sequential workloads with infrequent access. <br>Low-cost magnetic storage with lower throughput compared to st1.                                          |
| **Magnetic (standard)**      | Legacy volume type with traditional magnetic hard drives. | Being phased out. <br>Used for workloads with low I/O requirements where cost is a significant factor.                                                                      |


# Snapshots:

- EBS snapshots are point-in-time copies of EBS volumes.
- They are stored incrementally, which means only the changes since the last snapshot are saved.
- Snapshots can be used for backup, data recovery, and to create new volumes.


# Volume Encryption:

- EBS volumes can be encrypted using AWS Key Management Service (KMS) keys.
- Encryption helps protect sensitive data and ensures compliance with security standards.


# Lifecycle Management:

- Users can create, delete, and attach EBS volumes to EC2 instances as needed.
- Volumes persist independently of the lifecycle of an EC2 instance, allowing data to be retained even if the instance is terminated.

