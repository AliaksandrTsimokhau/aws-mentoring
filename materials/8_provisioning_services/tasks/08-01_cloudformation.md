# Domain: Automation and Optimization 

## Topic: Cloudformation 

### Task: Create EC2 Instance 

Create a stack using Cloudformation template. The stack should contain the following resources: 

- EC2 instance with httpd server installed 
- Security group with SSH traffic allowed 
- Elastic IP attached to the instance 

Parameters: 
- SSH key pair (must be the name of existing keypair) 
- Instance type (with allowed values t2.micro, t2.nano, t3.micro, t2.nano) 
- AMI Id 

Output exported: 
- InstanceId 
- Availability zone 
- Elastic IP associated with the instance 
 
Create a change set with a new rule in security group allowing 80 port from anywhere. Apply the change set, check if webserver works. 