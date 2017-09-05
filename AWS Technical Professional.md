# AWS Technical Professional Online Training 
## Module 1: Introduction to AWS 
### Part I: Introduction to AWS 

**Cloud computing** – on demand IT resources. Accessible online and pay as you go. 
It address the following issues of the traditional computing model: 
* Low Cost 
* Elastic 
* Flexible 
* Secure

| AWS | On-premises | 
| --- | --- |
| No upfront investment | slow and expensive. Large initial purchases – install and configure, physical space,  cooling, power cabling, networking, racks, servers, storage|
| Low on-going costs | labour certification, patches, and upgrade cycles |
| Focus on innovation | Systems Administrator
| Flexible capacity – provision the resources you need, turn off what you don't need | Fixed capacity – idle resources, inadequate capacity |
| Speed and agility – fast and on demand provisioning | Procurement setup – lengthy, labour-intensive provisioning |
| Global reach on-demand | Limited geographic locations |
 
### Part II: AWS Infrastructure 
Choosing which region – optimise latency, minimise cost, regulatory requirements 
Should encrypt data since traffic transfers over the internet

**Availability Zone (AZ)** - collection of data centres within each region, isolated from other AZs, Connected by a low-latency (high response) link 
Host a content delivery network (CDN) 
 
## Module 2: AWS Core Services
### 1. Compute ### 
* Amazon EC2 (Elastic Compute Cloud)
* Amazon ECS (EC2 Container Services)
* AWS Lambda

#### Amazon EC2 Instance Types: ####
* Memory
* Compute
* Storage and I/O
* GPU (Graphics Processing Unit) optimised
* General Purpose
* Smaller Instances

Easily resize an instance up or down.

**Amazon Machine Image (AMI)** - Choose an operating system type and version, create and customise your own AMIs 

**General Purpose** – balanced set of resources, high performance on a low cost platform 
For applications that require balanced CPU and memory performance like coding, high traffic content management systems, and memcached

**Compute Optimised** – has a proportionally more CPU resources than memory or RAM, ideal for more compute-intensive applications

**Storage and I/O Optimised** – high disk performance or proportionally high storage density per instance, ideal for applications that benefit from a high sequence of I/O performance across very large datasets. It has high levels of CPU, memory, and network performance.

**GPU Optimised instance** -  high CPU and network performance. for applications: 3D graphics, HPC, rendering media processing applications

**Memory Optimized** -  large memory sizes for high throughput applications including relational and NoSQL databases, in-memory analytic solutions, scientific and other memory-intensive applications

**Smaller Instances (T Family)** low-intensity workloads such bastion (a special purpose computer on a network specifically designed and configured to withstand attacks) and jump host (used to manage devices in a separate security zone), test and development environments, learning and experimentation, low CPU workloads but can spike to handle more CPU workloads

#### EC2 Pricing Models ####
* On-Demand - pay by the hour, no long-term commitments. for spiky workloads.
* Reserved - pay upfront, 50-70% lower hourly rate. for steady-state workloads.
* Spot - bid for unused EC2 capacity. price depends on supply and demand. for time-insensitive workloads.
* Dedicated - in your VPC (Virtual Private Cloud), isolated steady-state workloads, dedicated instance allows exclusive use of third-party libraries. for highly sensitive workloads.

*Amazon Marketplace* - pre-configured AMIs, software ready to launch, quickly deploy: 1-click launch, EC2 management console

### Amazon ECS (EC2 Container Services) ###
Amazon ECS - a highly scalable , high performance container management service that supports Docker container and allows you to easily run applications on a managed cluster of Amazone EC2 instance.
* Eliminates the need to install, operate, and scale your own cluster
* With simple API calls: launch and stop Docker-enabled applications, query the complete state of your cluster, access features like security groups, Elastic Load Balancing, EBS (Elastic Block Store) volumes, and IAM (Identity and Access Management) roles
* Schedule the placement of containers across your clusters
* Integrate your own scheduler or third-party schedulers
* No additional charge for Amazon ECS
### Amazon Lambda ###
An event-driven task compute service. Runs code without provisioning or managing servers. Only pay for the compute time you consume. Zero administration. Runs and scales your code.

### 2. Storage & Delivery Content Delivery ###
* Amazon Elastic Block Store (EBS)
* Amazon Simple Storage Service (S3)
* Amazon Glacier
* Amazon Import/Export Snowball
* Amazon CloudFront

#### Amazon EBS ###
Like a hard drive. 1GB to 16TB per volume. multiple volumes in one EC2 instance. For applications that require database, file system, and block-level storage
Durability and backup - automatic replication within its AZ, snapshot backup to Amazon S3
I/O Provisioning - provision a specific I/O performance, select a burstable performance model, scale to tens of thousands of Input/Output Processors (IOPs) and EC2 instances
* Standard - Bursty I/O requirements such as boot volumes
* Provision IOPs - I/O intensive workloads such as databases
* General Purpose - Moderate I/O workloads such as medium-sized databases

#### Amazon S3 ####
durable and scalable object store similar to a collection of static files. has web interface for management of storage objects. For static web content (CSS, HTML, Javascript), backups, and storage before loading to data warehouse or Hadoop cluster for analysis

#### Amazon Glacier ####
For data storage for archiving and backup. Automated lifecycle process. 

| Traditional Backup Environments | Glacier |
| --- | --- |
| Low Durability | High durability 9.99999999 % |
| Long recovery time | Retrieve in several hours |
| Expensive | Just $0.01 per GB/month |

#### Amazon Import/Export Snowball ####
addresses common challenges with large-scale data transfers including high network costs, long transfer times, and security concerns. For cloud migration, disaster recovery, datacenter decommission, content distribution
1. Create a job in the AWS Management Console.
2. Snowball appliance will be shipped to you.
3. Attach the appliance to your network for file directories to transfer
4. Return the appliance and track it with the E ink label. AWS will transfer files to your S3 bucket.

#### Amazon CloudFront ####
A global content delivery network. Integrates with Amazon S3 in retrieving the static files.

### 3. Database ###
#### Amazon Relational Database Service (RDS) ####
- Cost-efficient, Resizable, Database Administration, Pay-as-you-go
- Elastic, Flexible, Secure, Low Cost
#### Amazon DynamoDB ####
- Fast and flexible NoSQl Database service.
- Fit for gaming, mobile, web, ad tech, IoT
#### Amazon Database Migration Services ####
- For database migration. Minimising downtime during migration. Supports homogenous and heterogenous migration.
#### Amazon Redshift #### 
- For data warehousing and analytics

### 4. Networking ###
#### Amazon VPC ####
#### AWS Direct Connect ####
#### Amazon Route 53 ####

