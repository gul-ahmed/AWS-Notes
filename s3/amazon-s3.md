### Amazon S3

Amazon S3, or Simple Storage Service, is a scalable and highly durable object storage service provided by Amazon Web Services (AWS). 

It is designed to store and retrieve any amount of data from anywhere on the web. 

S3 is commonly used for backup and restore, archive, content storage, data lakes for analytics, and as a primary storage for internet applications.


**Objects:**
- In Amazon S3, data is stored as objects. Each object consists of data, a key (unique within a bucket), and metadata.
- Objects can range in size from a few bytes to terabytes.

**Buckets:**
- A bucket is a container for objects stored in Amazon S3.
- Each bucket has a globally unique name, and you use this name to access the bucket and its contents.
- Buckets can be used to organize and control access to objects.
- Amazon S3 allows people to store objects (files) in “buckets” (directories)
- Buckets must have a globally unique name (across all regions all accounts)
- Buckets are defined at the region level
- S3 looks like a global service but buckets are created in a region

 **`Naming convention`**
- No uppercase, No underscore
- 3-63 characters long
- Not an IP
- Must start with lowercase letter or number
- Must NOT start with the prefix xn--
- Must NOT end with the suffix -s3alias

**Data Durability and Availability:**
- Amazon S3 is designed for 99.999999999% (11 9's) durability over a given year and 99.99% availability over a given year.
- Data is redundantly stored across multiple facilities and servers to ensure high durability.

**Data Security:**
- S3 supports both server-side and client-side encryption to help protect data at rest and in transit.
- Access control mechanisms, such as Access Control Lists (ACLs) and bucket policies, allow fine-grained control over who can access your data.

**Storage Classes:**
- Amazon S3 offers different storage classes to optimize costs based on the access patterns and durability requirements of your data.
- Common storage classes include **`STANDARD`**, **`INTELLIGENT_TIERING`**, **`ONEZONE_IA`**, **`GLACIER`**, and **`DEEP_ARCHIVE`**.

**Versioning:**
- Versioning allows you to keep multiple versions of an object in the same bucket. This helps with data protection and recovery from unintended user actions.

**Lifecycle Management:**
- Lifecycle policies enable automatic transitions of objects between storage classes or automatic deletion based on predefined rules.

**Event Notifications:**
- S3 can be configured to generate event notifications when certain events occur in your bucket. These events can trigger workflows or notifications through AWS Lambda, SQS, or SNS.

**Multipart Upload:**
- Large objects can be uploaded in parts using the **Multipart Upload** feature, improving efficiency and allowing for parallel uploads.

**Static Website Hosting:**
- Amazon S3 can be used to host static websites by configuring the bucket as a static website host.

**Transfer Acceleration:**
- S3 Transfer Acceleration enables fast, easy, and secure transfers of files to and from Amazon S3 using a globally distributed network of edge locations.


### S3 Storage Classes

| Storage Class                | Description                                                                                                       | Use Cases                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| **Standard**                 | Default storage class with low-latency and high-throughput performance.                                          | Frequently accessed data                        |
| **Intelligent-Tiering**      | Automatically moves objects between access tiers based on changing access patterns.                                | Optimizing costs for varying access patterns    |
| **One Zone-IA**              | Stores data in a single availability zone, reducing costs compared to Standard.                                   | Infrequently accessed data, easily recreatable  |
| **Glacier**                  | Designed for long-term archival with retrieval times ranging from minutes to hours.                                | Data with long-term retention requirements     |
| **Glacier Deep Archive**     | Lowest-cost storage class, optimized for rarely accessed data with long-term retention.                            | Extremely infrequently accessed data           |

