# Deigning and Build a Scalable VPC on AWS.
This is a step by step documentation of how to design and build a scalable VPC on AWS cloud that can be used to deploy a production ready, highly available Multi-Tier Web Application on AWS Cloud.

### Scenario
You are tasked with designing and deploying a multi-tier web application for a startup. The application consists of a web front end, an application layer, and a database layer. Each layer needs to be isolated within its own subnet for security and management purposes.

### Requirements:
- VPC Configuration:
   - The VPC should span across 3 availability zones (AZs) for high availability. However the 3rd AZ will be reserved for future growth.
   - Design an IP addressing scheme that will account for current and future needs of the startup.
   
- Subnets:
  - Create public subnets in each AZ for the web tier.
  - Create private subnets in each AZ for the application tier.
  - Create private subnets in each AZ for the database tier.
Each subnet should be appropriately sized to accommodate potential scaling.

- Internet Gateway and NAT Gateway:
  - Attach an Internet Gateway (IGW) to the VPC to allow internet access for resources in public subnets.
  - Set up NAT Gateways in each AZ to allow instances in the private subnets to access the internet for updates and patches.

- Route Tables:
  - Configure route tables to direct traffic appropriately between subnets, IGW, and NAT Gateways.
    
- Security Groups and Network ACLs:
  - Define security groups to control access between the layers and external access to recources in the VPC
  - Implement network ACLs for an additional layer of security.
- Documentation
  - Document each step with diagrams and screenshots where applicable   
