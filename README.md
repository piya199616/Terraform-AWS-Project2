# Terraform-AWS-Project2

Today we will be deploying a 3-tier ALB using Terraform in AWS.

Previously I have used classic load balancer so this is an upgrade to project1.

AWS Services :- EC2 Instances, VPC, Nat Gateway , Internet Gateway, security groups, Application Load balancer.

** So Here We will Deploy our Application in 2 Availability Zones **

Project Architecture

![diagram](https://user-images.githubusercontent.com/98099702/230690300-bddd3eb2-21c6-4321-8b2d-0dedb237c3a8.jpg)

# What we will provision:

- 1 VPC,6 subnets (Public, Private, Database),1 Nat gateway in Public Subnet, 1 Internet Gateway attached to VPC.

- 1 Bastion host and 2 private EC2 instances in 2 AZs.

- 1 Application Load Balancer.

- 3 Security Groups (bastion host, Private Ec2, and Load balancer)

- with the help of provisioner, we will copy the file from local(the private key file you copied) to the Bastion host, Run some commands on the remote host.
