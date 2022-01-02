# AWS SAA-C02

This outline helps to prepare to AWS SAA-C02 exam.

Good luck. Hope you to pass it successfully.

[TOC]

## Amazon VPC

**How do I change the IPv4 CIDR block of my Amazon Virtual Private Cloud (Amazon VPC)?**

It's not possible to modify the IP address range of an existing virtual private cloud (VPC) or subnet. You must delete the VPC or  subnet, and then create a new VPC or subnet with your preferred CIDR  block.

To extend the IPv4 address range of your VPC, you can add an additional IPv4 CIDR block.





## Amazon ELB

**How do I attach backend instances with private IP addresses to my internet-facing load balancer in ELB?**

To attach Amazon EC2 instances located in a private subnet, create public subnets in the same Availability Zones as the private subnets used by the backend instances. Then, associate the public subnets with your load balancer.



## Amazon S3

**S3 object lock**

With S3 Object Lock, you can store objects using a write-once-read-many (WORM) model. Object Lock can help prevent objects from being deleted or overwritten for a fixed amount of time or indefinitely. You can use Object Lock to help meet regulatory requirements that require WORM storage, or to simply add another layer of protection against object changes and deletion. 



**S3 Glacier with standard retrieve**

S3 Glacier with standard retrieve allow you to access any of your archives within several hours. Standard retrievals typically complete within 3-5 hours.



**How should I choose between S3 Transfer Acceleration and Amazon CloudFront’s PUT/POST?** 

 S3 Transfer Acceleration optimizes the TCP protocol and  adds additional intelligence between the client and the S3 bucket,  making S3 Transfer Acceleration a better choice if a higher throughput  is desired. If you have objects that are smaller than 1GB or if the data set is less than 1GB in size, you should consider using Amazon  CloudFront's PUT/POST commands for optimal performance.



## Amazon cloudfront

**field-level encryption**

With Amazon CloudFront, you can enforce secure end-to-end connections to origin servers by using HTTPS. Field-level encryption adds an additional layer of security that lets you protect specific data throughout system processing so that only certain applications can see it.

Field-level encryption allows you to enable your users to securely upload sensitive information to your web servers. The sensitive information provided by your users is encrypted at the edge, close to the user, and remains encrypted throughout your entire application stack. This encryption ensures that only applications that need the data—and have the credentials to decrypt it—are able to do so. 





# Amazon Route53

**simple routing policy & multivalue routing policy**

Use a [simple routing](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-simple) policy for traffic that requires only standard DNS records, and that  doesn't require special options such as weighted routing or latency  routing. For example, use simple routing when you need to route traffic  to a single resource. You can't use multiple records of the same name  and type with simple routing. However, a single record can contain  multiple values (such as IP addresses).

 Use a [multivalue answer routing](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-multivalue) policy to help distribute DNS responses across multiple resources. For  example, use multivalue answer routing when you want to associate your  routing records **with a Route 53 health check**. For example, use  multivalue answer routing when you need to return multiple values for a  DNS query and route traffic to multiple IP addresses.



**Differences between R53 failover routing policy and multivalue policy.**

Imagine a scenario where you had servers in California, USA and North  Virginia, USA, but all of your customers are in N. Virgina. Using  Failover Routing you can have all of your traffic go to N. Virgina when  it’s online and only to California when it’s not. If you were to use the same servers in Multivalue Answer Routing then you would effectively  see a 50/50 split of traffic going to both. Your customers going to  California may see a degraded user experience. 





## Amazon DynamoDB

**read/write mode of dynamodb**

Amazon DynamoDB has two read/write capacity modes for processing reads and writes                                    on your tables:                                

- On-demand 

-  Provisioned (default, free-tier eligible) 

On-demand mode is a good option if any of the following are true: 

- You create new tables with unknown workloads. 
- You have unpredictable application traffic. 
- You prefer the ease of paying for only what you use.

Provisioned mode is a good option if any of the following are true: 

- You have predictable application traffic. 
- You run applications whose traffic is consistent or ramps gradually.                                                                      
- You can forecast capacity requirements to control costs. 



## Amazon Gateway Load Balancer

**What is Gateway Load Balancer?**

Gateway Load Balancer helps you easily deploy, scale, and manage your  third-party virtual appliances. It gives you one gateway for  distributing traffic across multiple virtual appliances while scaling  them up or down, based on demand. This decreases potential points of  failure in your network and increases availability.

![GatewayLoadBalancer](img/GatewayLoadBalancer.png)



## Amazon kinesis Streams

**Developing Producers Using the Amazon Kinesis Producer Library**

The KPL performs the following primary tasks:                                                                     

- Writes to one or more Kinesis data streams with an automatic and configurable retry                                             mechanism                                          
- Collects records and uses PutRecords to write multiple records to                                             multiple shards per request                                          
- Aggregates user records to increase payload size and improve throughput
- Integrates seamlessly with the [Kinesis Client Library](https://docs.aws.amazon.com/kinesis/latest/dev/developing-consumers-with-kcl.html) (KCL) to de-aggregate batched                                             records on the consumer                                          
- Submits Amazon CloudWatch metrics on your behalf to provide visibility into producer                                             performance                                          



## Amazon Inspector

Amazon Inspector is an automated **vulnerability management** service that continually scans Amazon Elastic Compute Cloud (EC2) and container workloads for software vulnerabilities and unintended network exposure.



## Amazon Elastic Fabric Adapter

**The concept of EFA**

An Elastic Fabric Adapter (EFA) is a network device that you can attach to your Amazon EC2 instance to accelerate High Performance Computing (HPC) and machine learning applications. EFA enables you to achieve the application performance of an on-premises HPC cluster, with the scalability, flexibility, and elasticity provided by the AWS Cloud. 