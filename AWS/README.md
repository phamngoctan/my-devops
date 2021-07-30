# AWS for beginner course
## General topics
### Building blocks of cloud computing

- Basic architecture of a computer
- Servers vs desktops and laptops
- Client Server communication
- HDDs and SSDs
- Storage - block vs file vs object
- IP address
- Networking - Routers and Switches
- Networking - Firewalls
- Databases
- Server Virtualization (VM)
- Docker containers

### Cloud Computing terminologies

- Legacy IT
    - On premise
    - Hardware plan, servers, wires
    - Software to manage
    - Backup system
    - Router, Switch, Firewall config
- Cloud computing characteristics
    - On-demand, self-service
    - Broad network access: internet or a Wide Area Network (WAN)
    - Resource pooling
    - Rapid scaling
    - Measured service
- Cloud service Models
    - Private Cloud (Hardwares, Hyperviser) (Linux OS, Java runtime) (Data, Java webapp)
    - IaaS (Linux OS, Java runtime) (Data, Java webapp)
    - PaaS (Data, Java webapp)
    - SaaS (Java webapp only)
- Cloud computing deployment models
    - Private cloud (VMware, Microsoft, RedHat, OpenStack)
    - Public cloud (AWS, Microsoft Azure, GCP)
    - Hybrid Cloud (mix between Private & Public cloud)
    - Multicloud (two or more public clouds, and possibly multiple private clouds)

### Cloud Architecture

- Stateful vs stateless services
- Scale up vs scaling out
- Load balancing
- Fault tolerance
- Loose coupling
- Monolithic & microservices architectures
- Event driven architecture

## AWS basic

- AWS overview
- AWS Global Infrastructure
    - Region: consists of two or more Availability Zones
        - Availability zone: is composed of one or more data centers
- AWS pricing
- AWS free tier account
- Billing alarm
    - Setup the billing preferences
    - Setup the thresholds
    - Email to receive the alert
- Identity and Access Management (IAM)
    - An IAM user is an entity that represents a person or service
    - IAM can have multiple policies. Policies are documents the define permissions and can be applied to users, groups and roles
    - Assign IAM users to group
    - IAM Roles are "assumed" by trusted entities and can be used for delegation. Give permissions for you to do other services on AWS.
    - Authentication methods
        - Access key (access to API)
        - Password (AWS management console)
- Amazon virtual private cloud (VPC) HERE
    - VPC is a logically isolated portion of the AWS cloud within a region
    - Public subnet, private subnet
    - Virtual servers into a VPC subnet
    - Between subnets, router is used for config the requests to local VPC or to the internet gateway
    - Internet gateway is used to connect to the Internet
- Security groups and network access control lists (NACLs)
    - Security groups apply at instance level (example: EC2 instance - virtual server)
    - Network ACL applies at subnet level (in - out from the subnet)
    - Stateful (Security groups) and stateless firewalls (Network ACLs)
- AWS public and private services (good one)
    - Services that have public endpoints/IP addresses
    - Services that have public IP addresses but exist within the VPC
- Install the AWS command line interface

## Amazon elastic compute cloud (EC2)

- EC2 overview
    - NAT stands for Network Address Translation
    - Instances in the public subnet are allowed to communicate with Internet by default
    - Instances in the private subnet are not allowed to go outside the VPC
    - To connect outside, we need to impl NAT gateway in the public subnet, then set the rule for outbound request to the nat-gateway-id to go to the Internet :) Good to know this
- EC2 instance
    - 5 machine types


