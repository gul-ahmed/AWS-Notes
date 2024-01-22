# Introduction to Security Groups

security group acts as a virtual firewall for your instances to control inbound and outbound traffic.

Security Groups are the fundamental of network security in AWS.

They control how traffic is allowed into or out of our EC2 Instances.

It acts as a virtual firewall at the instance level to control traffic at both the protocol and port level.

### Key Characteristics:
**Stateful:**
- Security groups are stateful, which means if you allow inbound traffic from a specific IP address, the corresponding outbound traffic is automatically allowed.

**Applies to Instances:** 
- Security groups are associated with instances, not subnets. Each instance in a Virtual Private Cloud (VPC) can be associated with one or more security groups.

### Rules and Permissions:
- Security group rules are defined based on a combination of IP protocol, port range, and source or destination IP address (or security group).
- Security groups only contain **ALLOW** rules

### Default Security Group:
- When you launch an instance in a VPC without specifying a security group, it's automatically associated with the default security group for that VPC.
- By default, this group allows all outbound traffic and denies all inbound traffic.

### Inbound and Outbound Rules:
**Inbound Rules:**
- Control the traffic coming into instances. For example, you can allow SSH (port 22) traffic from a specific IP range.

**Outbound Rules:**
- Control the traffic leaving instances. By default, all outbound traffic is allowed, but you can customize these rules.

### Rule Evaluation:
- Security group rules are evaluated based on the principle of **most specific rule wins**.
- If there's a rule allowing traffic from a specific IP range and another rule denying all traffic, the more specific rule takes precedence.

### Changes to Security Groups:
- Changes to security groups are applied immediately, without the need to restart instances.
- It's possible to modify the rules of a security group while it's associated with a running instance.

### Integration with Other AWS Services:
Security groups can be associated with various AWS services, including EC2 instances, Relational Database Service (RDS) instances, and Elastic Load Balancers (ELB).

### Security Groups Good to know
- Can be attached to multiple instances
- Locked down to a region / VPC combination
- Does live “outside” the EC2 – if traffic is blocked the EC2 instance won’t see it
- It’s good to maintain one separate security group for SSH access
- If your application is not accessible (time out), then it’s a security group issue
- All inbound traffic is blocked by default
- All outbound traffic is authorised by default
