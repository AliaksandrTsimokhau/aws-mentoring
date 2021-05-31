# AWS Cloud Overview

- AWS Fundamentals
- Regions and Zones
- Access and manage Amazon Web Services
- Protecting your AWS account
- Logging and Monitoring
- Taking care of Billing in Cloud

# Amazon Web Services
Amazon Web Services (AWS) is the world’s most comprehensive and broadly adopted cloud platform, offering over 200 fully featured services from data centers globally.
AWS has the most extensive global cloud infrastructure. No other cloud provider offers as many Regions with multiple Availability Zones connected by low latency, high throughput, and highly redundant networking. AWS has 80 Availability Zones within 25 geographic regions around the world, and has announced plans for 15 more Availability Zones and 5 more AWS Regions.
![image.png](./image.png)
The platform is developed with a combination of infrastructure as a service (IaaS), platform as a service (PaaS) and packaged software as a service (SaaS) offerings.

**What are the services provided by AWS?**

Each type of service  is categorized under a domain:
- AWS Networking and Content Delivery services
- AWS Compute services
- AWS Storage services
- Database services
- Analytics 
- Developer Tools
- Management tools
- IoT
- Security
- Enterprise app

# AWS Networking and Content Delivery services


|Category|Service description|AWS service|
| :- | :- | :- |
|Network foundations|Define and provision a logically isolated network for your AWS resources|Amazon VPC|
||<p>Connect VPCs and on-premises networks through a central hub </p><p></p>|AWS Transit Gateway|
||<p>Provide private connectivity between VPCs, services, and on-premises applications </p><p></p>|AWS PrivateLink|
|Application networking|Automatically distribute traffic across a pool of resources, such as instances, containers, IP addresses, and Lambda functions|Elastic Load Balancing|
||Provide application-level networking for containers and microservices|AWS App Mesh|
||Create, maintain, and secure APIs at any scale|Amazon API Gateway|
|<p>Edge networking</p><p></p>|<p>Securely deliver data, videos, applications, and APIs to customers globally with low latency, and high transfer speeds </p><p></p>|Amazon CloudFront|
||<p>Route users to Internet applications with a managed DNS service </p><p></p>|Amazon Route 53|
||<p>Direct traffic through the AWS Global network to improve global application performance </p><p></p>|AWS Global Accelerator|
|Network security|<p>Safeguard applications running on AWS against DDoS attacks </p><p></p>|AWS Shield|
||<p>Protect your web applications from common web exploits </p><p></p>|AWS WAF|
||<p>Centrally configure and manage firewall rules </p><p></p>|AWS Firewall Manager|




## **AWS Compute services**

|Category|Service description|AWS service|
| :- | :- | :- |
|<p>Instances (Virtual machines) </p><p></p>|Secure and resizable compute capacity (virtual servers) in the cloud|Amazon Elastic Compute Cloud (EC2)|
||Run fault-tolerant workload for up to 90% off|Amazon EC2 Spot Instances|
||Automatically add or remove compute capacity to meet changes in demand|Amazon EC2 Autoscaling|
||Easy-to-use cloud platform that offers you everything you need to build an application or website|Amazon Lightsail|
|Containers|Highly secure, reliable, and scalable way to run containers|Amazon Elastic Container Service (ECS)|
||Easily store, manage, and deploy container images|Amazon Elastic Container Registry (ECR)|
||Fully managed Kubernetes service|Amazon Elastic Kubernetes Service (EKS)|
||Serverless compute for containers|AWS Fargate|
|Serverless|Run code without thinking about servers. Pay only for the compute time you consume|AWS Lambda|

## **AWS Storage services**

|Category|Service description|AWS service|
| :- | :- | :- |
|<p>Object storage</p><p></p>|<p>Object storage built to store and retrieve any amount of data from anywhere</p><p></p>|<p>Amazon S3</p>|
|<p>File storage</p><p></p>|<p>Simple, serverless, set-and-forget, elastic file system</p><p></p>|<p>Amazon Elastic File System</p>|
||<p>Fully managed file storage built on Windows Server</p><p></p>|<p>Amazon FSx for Windows File Server</p><p></p>|
||Amazon FSx for Lustre is a fully managed service that provides cost-effective, high-performance, scalable storage for compute workload|<p>Amazon FSx for Lustre</p>|
|<p>Block storage</p>|Amazon Elastic Block Store (EBS) is an easy to use, high-performance, block-storage service|<p>Amazon Elastic Block Store</p>|

## **Database services**
##

|Category|Service description|AWS service|
| :- | :- | :- |
|Relational|Traditional applications, ERP, CRM, e-commerce|Amazon Aurora, Amazon RDS, Amazon Redshift|
|Key-value|High-traffic web apps, e-commerce systems, gaming applications|Amazon DynamoDB|
|In-memory|Caching, session management, gaming leaderboards, geospatial applications|Amazon ElastiCache for Memcached, Amazon ElastiCache for Redis|

## **AWS Security, Identity, & Compliance services**

|Category|Service description|AWS service|
| :- | :- | :- |
|<p>Identity & access management</p>|<p>Securely manage access to services and resources</p>|AWS Identity & Access Management (IAM)|
||Managed Microsoft Active Directory|AWS Directory Service|
||Identity management for your apps|Amazon Cognito|
|Detection|Managed threat detection service|Amazon GuardDuty|
||Analyze application security|Amazon Inspector|
||Record and evaluate configurations of your AWS resources|AWS Config|
||Track user activity and API usage|AWS CloudTrail|
|Data protection|Key storage and management|AWS Key Management Service (KMS)|
||Hardware based key storage for regulatory compliance|AWS CloudHSM|
||Provision, manage, and deploy public and private SSL/TLS certificates|AWS Certificate Manager|
||Rotate, manage and retrieve secrets|AWS Secrets Manager|


