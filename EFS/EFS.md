# Amazon EFS

Amazon EFS: scalable file storage for multiple EC2 instances.

Unlike EBS, **EFS can be mounted by multiple EC2 instances**, meaning many virtual machines may store files within an EFS instance. 

**But its main feature is its  scalability**. EFS can grow or shrink according to demand, with more and  more files being added without disturbing your application or having to  provision new infrastructure.

### **EFS’s key benefits** 

Within its role as a shared file storage service for multiple EC2 instances, EFS provides many benefits: 

- Adaptive throughput – EFS’s performance can scale in-line with its storage,  operating at a higher throughput for sudden, high-volume file dumps,  reaching up to 500,000 IOPS or 10 GB per second
- Totally elastic – once you’ve spun up an EFS instance, you can add add files  without worrying about provisioning or disturbing your application’s  performance
- Additional accessibility – EFS can be mounted from different EC2 instances, but it can also cross the AWS region boundary via the use of VPC peering

### **When to use EFS?**

EFS may be used whenever you need a  shared file storage option for multiple EC2 instances with automatic,  high-performance scaling. 

This makes it a great candidate for  file storage for content management systems; for lift and shift  operations, as its autoscaling potential means you do not need to  re-architect; for application development, as EFS’s shareable file  storage is ideal for storing code and media files.