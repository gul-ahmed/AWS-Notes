# AWS Elastic Compute Cloud

Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides resizable compute capacity in the cloud. It allows users to run virtual servers, known as instances, on-demand. EC2 instances can be used for a wide range of applications, including hosting websites, running applications, and processing data.

Key features of Amazon EC2 include:

- **Scalability:** Users can easily scale the number of instances up or down based on their computing requirements. This enables applications to handle varying workloads efficiently.
- **Variety of Instance Types:** EC2 offers a variety of instance types optimized for different use cases, such as compute-optimized, memory-optimized, storage-optimized, and GPU instances.
- **Configurability:** Users can choose different operating systems, instance types, storage options, and networking configurations to meet their specific needs.
- **Pay-as-You-Go Pricing:** EC2 follows a pay-as-you-go pricing model, where users are charged only for the compute capacity they use. This allows for cost-effective provisioning of resources.
- **Elastic Load Balancing:** Users can distribute incoming traffic across multiple EC2 instances using Elastic Load Balancing (ELB) to achieve high availability and fault tolerance.
- **Security:** EC2 instances can be launched within a Virtual Private Cloud (VPC), allowing users to define their network topology and control network access. Additionally, AWS provides features such as Security Groups and Network Access Control Lists (NACLs) to enhance security.
- **Integration with Other AWS Services:** EC2 instances can be integrated with various AWS services, including Amazon RDS (Relational Database Service), Amazon S3 (Simple Storage Service), and AWS Lambda, to build comprehensive and scalable applications.
- **Elastic Block Store (EBS):** EC2 instances can be associated with EBS volumes to provide scalable and persistent block storage.

- To use Amazon EC2, users typically launch instances from pre-configured Amazon Machine Images (AMIs), which are templates containing the necessary information to launch an instance, including the operating system and any additional software.

# INSTANCE TYPES

AWS provides a variety of instance types, which are essentially virtual servers that you can rent to run your applications. Each instance type is optimized for different use cases to provide a balance of compute, memory, storage, and networking resources. 

Here's a brief overview of the main AWS instance types:

1. **General Purpose Instances (T-series, M-series):**

General purpose instances provide a balance of compute, memory and networking resources, and can be used for a variety of diverse workloads. These instances are ideal for applications that use these resources in equal proportions such as web servers and code repositories. 

- **T-series:** Burstable performance instances designed for applications with variable workloads. They accumulate "CPU credits" during periods of low usage, which can be used during bursts of high activity.
- **M-series:** Balanced instances that provide a good combination of compute, memory, and networking resources. Suitable for a wide range of applications.


2. **Compute Optimized Instances (C-series):**

Compute Optimized instances are ideal for compute bound applications that benefit from high performance processors. Instances belonging to this category are well suited for batch processing workloads, media transcoding, high performance web servers, high performance computing (HPC), scientific modeling, dedicated gaming servers and ad server engines, machine learning inference and other compute intensive applications.

3. **Memory Optimized Instances (R-series, X-series, U-series, Z-series):**

Memory optimized instances are designed to deliver fast performance for workloads that process large data sets in memory.

- **R-series:** Optimized for memory-intensive applications, such as in-memory databases and real-time big data analytics.
- **X-series:** Designed for large-scale in-memory data stores and applications that require high memory bandwidth and capacity.
- **U-series:** Memory-optimized instances with a good balance of memory, compute, and network resources.
- **Z-series:** Instances with the highest memory capacity among AWS instances, suitable for memory-intensive enterprise applications.


4. **Storage Optimized Instances (I-series, D-series, H-series):**

Storage optimized instances are designed for workloads that require high, sequential read and write access to very large data sets on local storage. They are optimized to deliver tens of thousands of low-latency, random I/O operations per second (IOPS) to applications.

- **I-series:** Designed for high-speed, low-latency storage, suitable for NoSQL databases and transactional workloads.
- **D-series:** Instances with a balance of compute, memory, and storage for applications that require high-speed local storage.
- **H-series:** Optimized for applications that require very high storage throughput and high sequential I/O performance.



5. **Accelerated Computing Instances (P-series, F-series, G-series, Inf1, EC2 Mac Instances):**

Accelerated computing instances use hardware accelerators, or co-processors, to perform functions, such as floating point number calculations, graphics processing, or data pattern matching, more efficiently than is possible in software running on CPUs.

- **P-series:** Instances with powerful GPUs for general-purpose GPU computing.
- **F-series:** Instances with customizable FPGA accelerators.
- **G-series:** Instances with NVIDIA GPUs suitable for graphics-intensive applications.
- **Inf1:**  Instances featuring AWS Inferentia chips for high-performance machine learning inference.
- **EC2 Mac Instances:** Instances specifically designed for macOS workloads.

# EC2 INSTANCE PRICING MODEL

**On-Demand Instances:**

- Pay-as-you-go pricing with no upfront costs or long-term commitments.
- Suitable for applications with variable workloads or short-term projects.
- Billed per second, with a one-minute minimum usage cost.


**Reserved Instances:**

- Reserved Instances offer significant cost savings compared to On-Demand pricing.
- Requires a one or three-year commitment to a specific instance type in a particular region.
- Provides capacity reservation, ensuring availability during peak times.
- Offers different payment options: All Upfront, Partial Upfront, or No Upfront.


**Spot Instances:**

- Allows you to bid for unused EC2 capacity at potentially lower prices than On-Demand instances.
- Ideal for applications with flexible start and end times, or for workloads that can handle interruptions.
- The instance runs as long as the bid price is higher than the current Spot market price.


**Dedicated Hosts:**

- Provides physical EC2 servers dedicated to your use.
- Allows you to use your existing server-bound software licenses.
- Useful for regulatory or compliance requirements that may necessitate dedicated physical servers.


**Savings Plans:**

- Offers significant savings (up to 72%) compared to On-Demand pricing.
- Requires a commitment to a consistent amount of compute usage (measured in $/hr) for a 1 or 3-year period.
- Provides flexibility to use different instance types within a region, family, or size, as long as the total usage remains within the commitment.
