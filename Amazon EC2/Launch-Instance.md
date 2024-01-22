# What is Amazon Machine Image (AMI)?

An Amazon Machine Image (AMI) is like a template (pre-configured virtual machine image) for creating virtual servers in AWS. It contains everything needed for a server, including the operating system and software. 

AMIs allow users to quickly launch and replicate instances with specific configurations, making it easy to scale up or deploy applications. 

They are identified by a unique ID and can be shared with others. AMIs are fundamental for managing and deploying virtual servers in AWS.

### Components of an AMI:
- **Root Volume:** The root volume is a block device that contains the operating system and other system-level configurations.
- **Block Device Mapping:** AMIs may include additional block device mappings for data storage or additional volumes.

### Creating an AMI:
- Users can create custom AMIs based on their specific configurations and requirements.
- The process involves launching an EC2 instance, customizing it, and then creating an image from the instance.

### Public and Private AMIs:
- **Public AMIs:** AWS provides a collection of pre-configured AMIs that are publicly available for users. These can be used as a starting point for various purposes.
- **Private AMIs:** Users can create their own custom AMIs and keep them private within their AWS account.


### AMI Types:
**Instance Store-backed AMIs:**
- Instance store is ephemeral storage and is dependent on the lifecycle of the Instance
- Instance store is deleted if the instance is terminated or if the EBS backed instance, with attached instance store volumes, is stopped
- Instance store volumes cannot be stopped
- Instance store volumes have their AMI in S3 and have higher boot times compared to EBS backed instances, as all the parts have to be retrieved from S3 before the instance is made available

**EBS-backed AMIs:**
- EBS volumes are independent of the EC2 instance lifecycle and can persist independently
- EBS backed instances can be stopped without losing the volumes
- EBS instance can also be persisted without losing the volumes on instance termination if the Delete On Termination flag is disabled
- EBS backed instances boot up much faster than the Instance store backed instances as only the parts required to boot the instance needs to be retrieved from the snapshot before the instance is made available






