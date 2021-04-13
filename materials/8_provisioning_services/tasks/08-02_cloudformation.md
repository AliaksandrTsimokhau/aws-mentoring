# Domain: Automation and Optimization 

## Topic: Cloudformation 

### Task: Create VPC 

Create a stack using Cloudformation template. The stack should contain at least the following resources: 

- VPC with CIDR 10.0.0.0/16 
- Three public subnets 
- Three private subnets 
- NAT Gateway 
- Internet Gateway 
- Public route table for public subnets with traffic routing via Internet gateway 
- Private route table for private subnets with traffic routing via NAT gateway 
- Elastic IP attached to NAT gateway 

And output exported: 
- VPCId 
- Public subnets names 
- Private subnet names 