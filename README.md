# aws-vpc-project
AWS Project Used In Production


Diagram
![AWS Project Used In Production](https://github.com/UnnatiRami/aws-vpc-project/blob/main/vpc-example-private-subnets.png?raw=true)


# AWS VPC Project

This project involves creating a VPC for a production environment with enhanced resiliency and security. The project includes the following steps:

1. **Create a VPC:**
    - Create a VPC with a CIDR block (10.0.0.0/16).

2. **Create Subnets:**
    - Create private subnets in two Availability Zones ( 10.0.128.0/20 and 10.0.0.0/20).
    - Create public subnets in two Availability Zones (10.0.128.0/20 and 10.0.16.0/20).

3. **Create an Internet Gateway:**
    - Attach the Internet Gateway to the VPC.

4. **Create Route Tables:**
    - Create a public route table and associate it with the public subnets.
    - Create a private route table and associate it with the private subnets.

5. **Set Up NAT Gateways:**
    - Create NAT Gateways in both Availability Zones in the public subnets.
    - Update the private route tables to route traffic to the NAT Gateways.

6. **Launch EC2 Instances:**
    - Launch EC2 instances in the private subnets.

7. **Set Up an Application Load Balancer:**
    - Create an Application Load Balancer in the public subnets.
    - Configure the load balancer to forward traffic to the EC2 instances in the private subnets.

8. **Configure Auto Scaling:**
    - Set up an Auto Scaling group to manage the EC2 instances in the private subnets.

9. **Security Groups:**
    - Create security groups to allow necessary traffic between the components.



