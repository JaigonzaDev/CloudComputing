# Working with Elastic Load Balancing

[LINK](https://skillbuilder.aws/learn/U3SPYA234U/working-with-elastic-load-balancing/BRPX7TASWB)

# **Description**

This lab introduces the concept of Elastic Load Balancing (ELB). In this lab you will use ELB to load balance a set of web servers in an Availability Zone. You will launch a pair of Amazon EC2 instances, bootstrap them to install web servers and content, and then access the instances independently using Amazon EC2 DNS records. Next, you will set up ELB, add your instances to the ELB, and then access the ELB DNS record to watch your requests load balance between servers. Finally, you will look at ELB metrics in CloudWatch. To successfully complete this lab, you should be familiar with the AWS Management Console.

# **Objectives**

- Launching a multiple server web farm on Amazon EC2
- Using bootstrapping techniques to configure Linux instances with Apache, PHP, and a simple PHP application downloaded from Amazon Simple Storage Service (S3)
- Creating and configuring a load balancer that will sit in front of your Amazon EC2 web server instances
- Viewing Amazon CloudWatch metrics for the load balancer

# **AWS Services**

- Amazon Elastic Compute Cloud
- Elastic Load Balancing
- Amazon CloudWatch