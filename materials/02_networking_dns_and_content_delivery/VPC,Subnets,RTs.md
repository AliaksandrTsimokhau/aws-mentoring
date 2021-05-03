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