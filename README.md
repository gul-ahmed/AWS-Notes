# AWS INTRODUCTION

Amazon Web Services (AWS) is a comprehensive and widely used cloud computing platform provided by Amazon.com. Launched in 2006, AWS offers a broad set of scalable and cost-effective cloud services, allowing businesses, organizations, and individuals to build and deploy applications and services with ease. AWS is a pioneer in cloud computing and has played a significant role in shaping the landscape of the industry.


# AWS GLOBAL INFRASTRUCTURE

Amazon Web Services (AWS) has built a global infrastructure that is designed to provide reliable, scalable, and low-latency cloud services to users around the world. 

This infrastructure consists of a network of data centers strategically located in different geographic regions, each containing multiple Availability Zones (AZs).

AWS's global infrastructure aims to provide consistent and reliable services to users worldwide. Organizations can deploy resources in the region that best meets their performance, regulatory, and data residency requirements.

**Regions:**

- AWS has established physical locations around the world called "Regions." Each region is a separate geographic area with multiple Availability Zones.


**Availability Zones (AZs):**

- Each AWS Region is divided into multiple isolated Availability Zones, which are essentially separate data centers within the region.
- Availability Zones are designed to provide redundancy and fault tolerance. They are interconnected through high-speed, low-latency networks.


**Edge Locations:**

- AWS has a global network of Edge Locations that are used by the Content Delivery Network (CDN) service, Amazon CloudFront. 
- These Edge Locations are located in cities worldwide and are used to cache and deliver content to end-users with low latency.


**Global Accelerator:**

- AWS Global Accelerator is a service that uses Anycast to route traffic over the AWS global network to the optimal AWS endpoint based on health, geography, and routing policies.
- It helps improve the availability and performance of applications by utilizing the AWS global network infrastructure.


**Wavelength Zones:**

- In collaboration with telecommunication providers, AWS has introduced Wavelength Zones that bring AWS services to the edge of the 5G networks. This allows for ultra-low latency applications, such as augmented reality and virtual reality.


# AWS SERVICE OFFERINGS

Amazon Web Services (AWS) provides a comprehensive suite of cloud services across various categories to meet the diverse needs of businesses and individuals. Some key AWS service offerings include:

| Category 			| Service                                      | Description                                   |
|----------			|----------------------------------------------|-----------------------------------------------|
| **Compute**		| Amazon EC2 (Elastic Compute Cloud)           | Virtual servers in the cloud.                  |
|          			| AWS Lambda                                   | Serverless computing service for running code without provisioning servers.|
| **Storage**		| Amazon S3 (Simple Storage Service)           | Scalable object storage for data and backup.   |
|          			| Amazon EBS (Elastic Block Store)             | Persistent block storage volumes for EC2 instances.|
|         			| Amazon EFS (Elastic File System)             | Scalable network file storage service in the cloud.|
| **Databases**	| Amazon RDS (Relational Database Service)     | Managed relational databases.|
|          			| Amazon DynamoDB                              | Fully managed NoSQL database service.|
|          			| Amazon Aurora                                | MySQL and PostgreSQL compatible relational database.|
|**Networking**	| Amazon VPC (Virtual Private Cloud)           | Isolated cloud network for resources.|
|          			| Amazon Route 53                              | Scalable domain name system (DNS) web service.|
|          			| AWS Direct Connect                           | Dedicated network connection to AWS.|
| **Security and Identity**  | AWS Identity and Access Management (IAM)     | Identity and access management service.|
|          			| AWS Key Management Service (KMS)             | Managed encryption keys for data security.|
|          			| Amazon GuardDuty                             | Managed threat detection service.|
| **Analytics** | Amazon Redshift                              | Fully managed data warehouse service.|
|          			| Amazon Athena                                | Serverless query service for analyzing data in Amazon S3.|
|          			| Amazon QuickSight                            | Business analytics and visualization service.|
| **Management and Monitoring**     | Amazon CloudWatch                            | Monitoring and observability service.|
|          			| AWS CloudTrail                               | Audit and track user activity and API usage.|



These are just a few examples, and AWS offers many more services to address various computing, storage, database, analytics, and application deployment needs. The platform is continually evolving with new services and features being added regularly.

