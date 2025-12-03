[العربي](./cloud-computing_ar.md)

# <a name="-10-cloud-computing"></a>☁️ Chapter 10: Cloud Computing

## 1. What is it?

Cloud Computing is the on-demand delivery of computing resources (like servers, storage, databases, networking, software) over the internet with a pay-as-you-go pricing model.

Simply put, instead of buying, owning, and maintaining physical data centers and servers, you can access these technology services from a cloud provider.

The best analogy: Instead of building your own power plant, you subscribe to the public utility company and pay only for what you consume. The cloud is the "utility company" for the computing world. The most famous providers are AWS, Azure, and GCP.

## 2. What does the specialist do?

A Cloud Engineer designs, builds, deploys, and manages applications and infrastructure on cloud platforms. Their tasks include:

* Designing cloud solutions: Designing a secure, scalable, and highly available infrastructure on the cloud.
* System Migration: Helping companies move their existing applications and infrastructure from on-premise servers to the cloud.
* Managing Infrastructure as Code (IaC): Writing code to automatically create and manage cloud resources.
* Cost Optimization: Monitoring and analyzing cloud spending and finding ways to reduce costs.
* Ensuring Security and Compliance: Implementing security best practices to ensure the cloud environment is protected.

## 3. Sub-domains

* Cloud Architecture: Focuses on the high-level design of the cloud infrastructure.
* Cloud Administration: Focuses on the day-to-day operations of managing the cloud environment.
* Cloud Security: Specializes in protecting infrastructure and data on the cloud.
* Cloud Networking: Specializes in designing and managing virtual networks within the cloud.
* FinOps (Cloud Financial Management): A new specialization that focuses on managing and optimizing cloud costs.

## 4. Expanded Key Concepts

* "as a Service" Models:
  * `IaaS (Infrastructure as a Service)`: You rent the basic infrastructure (virtual servers, storage). You manage the operating system and everything above it. (Example: AWS EC2).
  * `PaaS (Platform as a Service)`: The provider manages the platform for you (OS, runtime environment). You just deploy your code. (Example: Heroku).
  * `SaaS (Software as a Service)`: You use a complete, ready-made software over the internet. (Example: Gmail).
* Deployment Models:
  * `Public Cloud`: Resources are owned by the service provider and available to the public over the internet.
  * `Private Cloud`: Resources are used exclusively by a single company.
  * `Hybrid Cloud`: A mix of public and private clouds.
* Core Cloud Principles:
  * `Scalability & Elasticity`: The ability to scale (increase resources) and elasticity (automatically increase resources based on demand).
  * `High Availability & Fault Tolerance`: Designing systems that remain operational even if some components fail, often by distributing them across different geographical regions.
* `Serverless Computing`: An evolution of PaaS where the provider manages everything. You write your code as "Functions" that run only when called, and you pay only for the execution time in milliseconds. (Example: AWS Lambda).

## 5. Expanded Tools & Technologies

* Cloud Providers: AWS (Amazon Web Services), Microsoft Azure, GCP (Google Cloud Platform).
* Compute Services: AWS EC2, Azure VMs (IaaS); AWS Lambda, Azure Functions (Serverless).
* Storage Services: AWS S3, Azure Blob Storage (Object Storage); AWS EBS (Block Storage).
* Database Services: Amazon RDS (Managed SQL); Amazon DynamoDB (Managed NoSQL).
* Networking Services: Amazon VPC (Virtual Networks); AWS ELB (Load Balancers).
* Infrastructure as Code (IaC): Terraform, AWS CloudFormation.
* Containers: Docker, and managed Kubernetes services like Amazon EKS, Azure AKS, Google GKE.

## 6. In-Depth Workflow

Project: Migrate a web application from an on-premise server to a scalable and highly available architecture on AWS.

 1. Assessment and Design: The cloud engineer analyzes the current application. They decide to run the web servers on multiple EC2 instances for availability and migrate the database to Amazon RDS (a managed database service).
 2. Writing Infrastructure Code (IaC): Instead of creating resources manually, the engineer writes a Terraform script that describes the required infrastructure:
     * A Virtual Private Cloud (VPC).
     * An Auto Scaling Group to increase the number of EC2 servers if CPU usage exceeds 70%.
     * A Load Balancer to distribute visitors across the servers.
     * An RDS database with a backup replica in a different Availability Zone.
 3. Deployment: The engineer runs `terraform apply`. Terraform communicates with AWS and builds all this infrastructure automatically.
 4. Data Migration: The engineer exports the data from the local database and imports it into the new RDS database.
 5. Application Deployment: The DevOps team updates the CI/CD pipeline to deploy the application code to the new EC2 servers.
 6. Cutover: After testing, the domain's DNS record is updated to point to the new load balancer's address. Visitors now start accessing the application on the cloud.
 7. Monitoring and Optimization: The engineer uses Amazon CloudWatch to monitor the infrastructure's performance. They might notice pressure on the database and decide to upgrade it, or they might set up alerts to track costs.

## 7. Common Job Roles

* Cloud Engineer
* Cloud Architect
* Cloud Support Engineer
* Cloud Security Engineer
* FinOps Specialist

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Availability Zone (AZ)`** | An independent, isolated data center within a single geographic region. |
| **`Auto Scaling`** | Automatically increasing or decreasing resources based on demand. |
| **`Blob Storage`** | Object Storage, a type of storage for saving files like images and videos. |
| **`CDN`** | Content Delivery Network, to speed up content delivery to users around the world. |
| **`CloudFormation`** | An IaC tool from AWS. |
| **`CloudWatch`** | The monitoring service from AWS. |
| **`EC2`** | The virtual server service (IaaS) from AWS. |
| **`EKS`** | The managed Kubernetes service from AWS. |
| **`Elasticity`** | The cloud's ability to automatically scale up and down. |
| **`Fault Tolerance`** | The ability of a system to continue operating even if some of its components fail. |
| **`High Availability`** | A design that ensures a system is available for the maximum possible time. |
| **`IaaS`** | Infrastructure as a Service. |
| **`IaC`** | Infrastructure as Code. |
| **`IAM`** | Identity and Access Management, for controlling user permissions on the cloud. |
| **`Lambda`** | The serverless computing service from AWS. |
| **`Load Balancer`** | A load balancer. |
| **`PaaS`** | Platform as a Service. |
| **`Region`** | A geographic area that contains multiple data centers (AZs). |
| **`RDS`** | The managed relational database service from AWS. |
| **`S3`** | The object storage service from AWS. |
| **`SaaS`** | Software as a Service. |
| **`Serverless`** | Serverless computing. |
| **`VPC`** | Virtual Private Cloud, your isolated network within the cloud. |
| **`VM`** | Virtual Machine. |

</details>

[⬆️ Back to Table of Contents](README.md)

