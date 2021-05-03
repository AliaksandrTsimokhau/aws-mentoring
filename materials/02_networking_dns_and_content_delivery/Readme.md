# VPC - A virtual network dedicated to your AWS account. 

## Service Overview 

Amazon Virtual Private Cloud (Amazon VPC) lets you provision a logically isolated section of the Amazon Web Services (AWS) Cloud where you can launch AWS resources in a virtual network that you define. You have complete control over your virtual networking environment, including selection of your own IP address range, creation of subnets, and configuration of route tables and network gateways 

### Concepts for VPCs: 

**Virtual private cloud (VPC)** — A virtual network dedicated to your AWS account. 

**Subnet** — A range of IP addresses in your VPC. 

**Route table** — A set of rules, called routes, that are used to determine where network traffic is directed to. 

**Internet gateway** — A gateway that you attach to your VPC to enable communication between resources in your VPC and the internet. 

**VPC endpoint** — Enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Instances in your VPC do not require public IP addresses to communicate with resources in the service. Traffic between your VPC and the other service does not leave the Amazon network.  

**CIDR block** — Classless Inter-Domain Routing. An internet protocol address allocation and route aggregation methodology. For more information, see Classless Inter-Domain Routing in Wikipedia. 

**Use cases / Considerations**

What can we do with a VPC? 

- Launch instances into a subnet of your choose  
- Assign custom IP address ranges in each subnet  
- Configure route tables between subnets 
- Create Internet gateway and attach it to our VPC  
- Much better security control over your AWS resources  
- Instance security groups  
- Subnet network access control lists (ACLs) 


## Governance 

Monitoring tools/service: 
- VPC Flow logs 
- CloudWatch 

## Cautions 

You can create 5 VPCs per Region. The quota for internet gateways per Region is directly correlated to this one. Increasing this quota increases the quota on internet gateways per Region by the same amount. You can have 100s of VPCs per Region for your needs even though the default quota is 5 VPCs per Region.  

You can request an increase for these quotas. For some of these quotas, you can view your current quota using the Limits page of the Amazon EC2 console. 

## Pricing considerations 

https://aws.amazon.com/vpc/pricing/ 
 
## More details 

- [What is VPC](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)
- [Private Addresses RFC1918](https://tools.ietf.org/html/rfc1918)
- [Prefixes](https://www.ripe.net/about-us/press-centre/understanding-ip-addressing)
- [VPC Limits](https://docs.aws.amazon.com/vpc/latest/userguide/amazon-vpc-limits.html)


# Amazon Virtual Private Cloud (Amazon VPC)

Figure 2.1 illustrates an Amazon VPC with an address space of `10.0.0.0/16`, two subnets with different address ranges (`10.0.0.0/24` and `10.0.1.0/24`) placed in different Availability Zones, and a route table with the local route specified.

![](images/2.1.jpg)

An Amazon VPC consists of the following components:
- Subnets
- Route tables
- Dynamic Host Configuration Protocol (DHCP) option sets
- Security groups
- Network Access Control Lists (ACLs)

An Amazon VPC has the following optional components:
- Internet Gateways (IGWs)
- Elastic IP (EIP) addresses
- Elastic Network Interfaces (ENIs)
- Endpoints
- Peering
- Network Address Translation (NATs) instances and NAT gateways
- Virtual Private Gateway (VPG), Customer Gateways (CGWs), and Virtual Private Networks (VPNs)

Figure 2.2 illustrates an Amazon VPC with an address space of `10.0.0.0/16`, one subnet with
an address range of `10.0.0.0/24`, a route table, an attached IGW (Internet Gateway), and a single Amazon EC2 instance with a private IP address and an EIP address. 

The route table contains two routes: the local route that permits inter-VPC communication and a route that sends all non-local traffic to the IGW (igw-id). Note that the Amazon EC2 instance has a public IP address (EIP, 198.51.100.2); this instance can be accessed from the Internet, and traffic may originate and
return to this instance.

![](images/2.2.jpg)

## More Complex Set up:

![](images/quickstart-vpc-design-fullscreen.png)

## Elastic Network Interfaces (ENIs)

An Elastic Network Interface (ENI) is a virtual network interface that you can attach to an instance in an Amazon VPC. ENIs are only available within an Amazon VPC, and they are associated with a subnet upon creation. They can have one public IP address and multiple private IP addresses. If there are multiple private IP addresses, one of them is primary. Assigning a second network interface to an instance via an ENI allows it to be dual-homed (have network presence in different subnets). An ENI created independently of a particular instance persists regardless of the lifetime of any instance to which it is attached; if an underlying instance fails, the IP address may be preserved by attaching the ENI to a replacement instance.

ENIs allow you to create a management network, use network and security appliances in your Amazon VPC, create dual-homed instances with workloads/roles on distinct subnets, or create a low-budget, high-availability solution.


## Elastic IP Addresses (EIPs)

AWS maintains a pool of public IP addresses in each region and makes them available for you to associate to resources within your Amazon VPCs. An Elastic IP Addresses (EIP) is a static, public IP address in the pool for the region that you can allocate to your account (pull from the pool) and release (return to the pool). EIPs allow you to maintain a set of IP addresses that remain fixed while the underlying infrastructure may change over time. Here are the important points to understand about EIPs:

- You must first allocate an EIP for use within a VPC and then assign it to an instance.
- EIPs are specific to a region (that is, an EIP in one region cannot be assigned to an instance within an Amazon VPC in a different region).
- There is a one-to-one relationship between network interfaces and EIPs.
- You can move EIPs from one instance to another, either in the same Amazon VPC or a different Amazon VPC within the same region.
- EIPs remain associated with your AWS account until you explicitly release them.
- There are charges for EIPs allocated to your account, even when they are not associated with a resource.

## VPC Security 

Amazon Virtual Private Cloud provides features that you can use to increase and monitor the security for your virtual private cloud (VPC): 

- A **security group** acts as a virtual firewall for your instance to control inbound and outbound traffic. When you launch an instance in a VPC, you can assign up to five security groups to the instance. Security groups act at the instance level, not the subnet level. Therefore, each instance in a subnet in your VPC can be assigned to a different set of security groups. For each security group, you add rules that control the inbound traffic to instances, and a separate set of rules that control the outbound traffic.. Security Groups are Stateful if you send a request from your instance, the response traffic for that request is allowed to flow in regardless of inbound security group rules. Responses to allowed inbound traffic are allowed to flow out, regardless of outbound rules.;  

- A **network access control list (ACL)** is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. You might set up network ACLs with rules similar to your security groups in order to add an additional layer of security to your VPC.  Network Access Control Lists are Stateless, which means that responses to allowed inbound traffic are subject to the rules for outbound traffic (and vice versa).  


The following diagram illustrates the layers of security provided by security groups and network ACLs. For example, traffic from an internet gateway is routed to the appropriate subnet using the routes in the routing table. The rules of the network ACL that is associated with the subnet control which traffic is allowed to the subnet. The rules of the security group that is associated with an instance control which traffic is allowed to the instance:

![](images/2.4.jpg)

### Difference between Security Group and ACL:

| Security Group | ACL |
|---|---|
| Operates at the instance level (first layer of defense) | Operates at the subnet level (second layer of defense) |
| Supports "allow" rules only | Supports allow rules and deny rules |
| Stateful: Return traffic is automatically allowed, regardless of any rules | Stateless: Return traffic must be explicitly allowed by rules. |
| AWS evaluates all rules before deciding whether to allow traffic | AWS processes rules in number order when deciding whether to allow traffic. |
| Applied selectively to individual instances | Automatically applied to all instances in the associated subnets; this is a backup layer of defense, so you don’t have to rely on someone specifying the security group |

### Cautions 

- Network ACLs per VPC - `2000`. You can associate one network ACL to one or more subnets in a VPC. This quota is not the same as the number of rules per network ACL. 
- Rules per network ACL - `20`. This is the one-way quota for a single network ACL. This quota is enforced separately for IPv4 rules and IPv6 rules; for example, you can have 20 ingress rules for IPv4 traffic and 20 ingress rules for IPv6 traffic. This quota includes the default deny rules (rule number `32767` for IPv4 and `32768` for IPv6, or an asterisk * in the Amazon VPC console). 
- This quota can be increased up to a maximum of `40`; however, network performance might be impacted due to the increased workload to process the additional rules 
- VPC security groups per Region – `2500`. This quota applies to individual AWS account VPCs and shared VPCs. If you increase this quota to more than `5000` security groups in a Region, we recommend that you paginate calls to describe your security groups for better performance. 
- Inbound or outbound rules per security group – `60`.  You can have 60 inbound and 60 outbound rules per security group (making a total of 120 rules). This quota is enforced separately for IPv4 rules and IPv6 rules; for example, a security group can have 60 inbound rules for IPv4 traffic and 60 inbound rules for IPv6 traffic. A rule that references a security group or AWS-managed prefix list ID counts as one rule for IPv4 and one rule for IPv6. 
- A quota change applies to both inbound and outbound rules. This quota multiplied by the quota for security groups per network interface cannot exceed 1000. For example, if you increase this quota to 100, we decrease the quota for your number of security groups per network interface to `10`. 
- If you reference a customer-managed prefix list in a security group rule, the maximum number of entries for the prefix lists equals the same number of security group rules. 
- Security groups per network interface – `5`. The maximum is `16`. This quota is enforced separately for IPv4 rules and IPv6 rules. The quota for security groups per network interface multiplied by the quota for rules per security group cannot exceed `1000`. For example, if you increase this quota to `10`, we decrease the quota for your number of rules per security group to `100`.
