# Building Highly Available Web Application

[LINK](https://skillbuilder.aws/learn/2WBTDQFGSV/building-highly-available-web-application/2RW7UC62ZE)

# **Description**

Example Corp. creates marketing campaigns for small-to-medium-sized businesses. They recently hired you to work with the engineering teams to build out a proof of concept for their business. To date, they host their clients using an on-premises data center and decided to move their operations to the cloud to save money and transform their business with a cloud-first approach. Some members of their team have cloud experience and recommended the AWS Cloud services to build their solution. In addition, Example Corp. decided to redesign their web portal. Customers use the portal to access their accounts, create marketing plans, and run data analysis on their marketing campaigns. They would like to have a working prototype in two weeks. You must design an architecture to support this application. Your solution must be fast, durable, scalable, and more cost-effective than their existing on-premises infrastructure. This lab showcases a mechanism to provision an auto scaling environment for a full stack web application using automation techniques to orchestrate AWS resources. IT teams can adapt this mechanism to rapidly provision infrastructure to securely deliver applications that can meet evolving business requirements.

# **Objectives**

- Deploy a virtual network spread across multiple Availability Zones in a Region using a provided CloudFormation template
- Create a highly available and fully managed relational database across those Availability Zones using Amazon Relational Database Service (Amazon RDS)
- Create a database caching layer using Amazon ElastiCache
- Use Amazon Elastic File System (Amazon EFS) to provision a shared storage layer across multiple Availability Zones for the application tier, powered by Network File System (NFS)
- Create a group of web servers that automatically scales in response to load variations to complete the application tier

# **AWS Services**

- Amazon Elastic File System
- Amazon Relational Database Service
- AWS CloudFormation
- Amazon ElastiCache