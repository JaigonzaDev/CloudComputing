# Exam 5

The engineering team at an online fashion retailer uses AWS Cloud to manage its technology infrastructure. The Amazon EC2 server fleet is behind an Application Load Balancer and the fleet strength is managed by an Auto Scaling group. Based on the historical data, the team is anticipating a huge traffic spike during the upcoming Thanksgiving sale.

As an AWS solutions architect, what feature of the Auto Scaling group would you leverage so that the potential surge in traffic can be preemptively addressed?

Auto Scaling group target tracking scaling policy

Auto Scaling group scheduled action

Auto Scaling group step scaling policy

Auto Scaling group lifecycle hook

The engineering team can create a scheduled action for the Auto Scaling group to pre-emptively provision additional instances for the sale duration. This makes sure that adequate instances are ready before the sale goes live. The scheduled action tells Amazon EC2 Auto Scaling to perform a scaling action at specified times. To create a scheduled scaling action, you specify the start time when the scaling action should take effect, and the new minimum, maximum, and desired sizes for the scaling action. At the specified time, Amazon EC2 Auto Scaling updates the group with the values for minimum, maximum, and desired size that are specified by the scaling action.

---

A financial services company runs its flagship web application on AWS. The application serves thousands of users during peak hours. The company needs a scalable near-real-time solution to share hundreds of thousands of financial transactions with multiple internal applications. The solution should also remove sensitive details from the transactions before storing the cleansed transactions in a document database for low-latency retrieval.

As an AWS Certified Solutions Architect Associate, which of the following would you recommend?

Persist the raw transactions into Amazon DynamoDB. Configure a rule in Amazon DynamoDB to update the transaction by removing sensitive data whenever any new raw transaction is written. Leverage Amazon DynamoDB Streams to share the transactions data with the internal applications

Batch process the raw transactions data into Amazon S3 flat files. Use S3 events to trigger an AWS Lambda function to remove sensitive data from the raw transactions in the flat file and then store the cleansed transactions in Amazon DynamoDB. Leverage DynamoDB Streams to share the transactions data with the internal applications

Feed the streaming transactions into Amazon Kinesis Data Streams. Leverage AWS Lambda integration to remove sensitive data from every transaction and then store the cleansed transactions in Amazon DynamoDB. The internal applications can consume the raw transactions off the Amazon Kinesis Data Stream

Feed the streaming transactions into Amazon Kinesis Data Firehose. Leverage AWS Lambda integration to remove sensitive data from every transaction and then store the cleansed transactions in Amazon DynamoDB. The internal applications can consume the raw transactions off the Amazon Kinesis Data Firehose

Cuando hay varios accesos a los datos data stream. Si solo llega a uno servicio data firehose.

---

A company wants to ensure high availability for its Amazon RDS database. The development team wants to opt for Multi-AZ deployment and they would like to understand what happens when the primary instance of the Multi-AZ configuration goes down.

As a Solutions Architect, which of the following will you identify as the outcome of the scenario?

An email will be sent to the System Administrator asking for manual intervention

The application will be down until the primary database has recovered itself

The URL to access the database will change to the standby database

The CNAME record will be updated to point to the standby database

Failover is automatically handled by Amazon RDS so that you can resume database operations as quickly as possible without administrative intervention. When failing over, Amazon RDS simply flips the canonical name record (CNAME) for your DB instance to point at the standby, which is in turn promoted to become the new primary. Multi-AZ means the URL is the same, the failover is automated, and the CNAME will automatically be updated to point to the standby database.

---

A pharmaceutical company is considering moving to AWS Cloud to accelerate the research and development process. Most of the daily workflows would be centered around running batch jobs on Amazon EC2 instances with storage on Amazon Elastic Block Store (Amazon EBS) volumes. The CTO is concerned about meeting HIPAA compliance norms for sensitive data stored on Amazon EBS.

Which of the following options outline the correct capabilities of an encrypted Amazon EBS volume? (Select three)

Any snapshot created from the volume is encrypted

Any snapshot created from the volume is NOT encrypted

Data moving between the volume and the instance is encrypted

Data moving between the volume and the instance is NOT encrypted

Data at rest inside the volume is NOT encrypted

Data at rest inside the volume is encrypted

**Data moving between the volume and the instance is encrypted**

Amazon Elastic Block Store (Amazon EBS) provides block-level storage volumes for use with Amazon EC2 instances. When you create an encrypted Amazon EBS volume and attach it to a supported instance type, data stored at rest on the volume, data moving between the volume and the instance, snapshots created from the volume and volumes created from those snapshots are all encrypted. It uses AWS Key Management Service (AWS KMS) customer master keys (CMK) when creating encrypted volumes and snapshots. Encryption operations occur on the servers that host Amazon EC2 instances, ensuring the security of both data-at-rest and data-in-transit between an instance and its attached Amazon EBS storage.

---

A Customer relationship management (CRM) application is facing user experience issues with users reporting frequent sign-in requests from the application. The application is currently hosted on multiple Amazon EC2 instances behind an Application Load Balancer. The engineering team has identified the root cause as unhealthy servers causing session data to be lost. The team would like to implement a distributed in-memory cache-based session management solution.

As a solutions architect, which of the following solutions would you recommend?

Use Amazon DynamoDB for distributed in-memory cache based session management

Use Application Load Balancer sticky sessions

Use Amazon Elasticache for distributed in-memory cache based session management

Use Amazon RDS for distributed in-memory cache based session management

Sticky sessions cuando no haya auto escalado y sean sessiones cortas y sin importancia de que se pierdan los datos. En el caso de haber autoscaling o que necesites avaliability pones un elasticaches bases en cached memory.

---

A DevOps engineer at an IT company was recently added to the admin group of the company's AWS account. The `AdministratorAccess` managed policy is attached to this group.

Can you identify the AWS tasks that the DevOps engineer CANNOT perform even though he has full Administrator privileges (Select two)?

Configure an Amazon S3 bucket to enable AWS Multi-Factor Authentication (AWS MFA) delete

Close the company's AWS account

Change the password for his own IAM user account

Delete the IAM user for his manager

Delete an Amazon S3 bucket from the production environment

An IAM user with full administrator access can perform almost all AWS tasks except a few tasks designated only for the root account user. Some of the AWS tasks that only a root account user can do are as follows: change account name or root password or root email address, change AWS support plan, close AWS account, enable AWS Multi-Factor Authentication (AWS MFA) on S3 bucket delete, create Cloudfront key pair, register for GovCloud. Even though the DevOps engineer is part of the admin group, he cannot configure an Amazon S3 bucket to enable AWS MFA delete or close the company's AWS account.

---

The engineering team at an e-commerce company uses an AWS Lambda function to write the order data into a single DB instance Amazon Aurora cluster. The team has noticed that many order- writes to its Aurora cluster are getting missed during peak load times. The diagnostics data has revealed that the database is experiencing high CPU and memory consumption during traffic spikes. The team also wants to enhance the availability of the Aurora DB.

Which of the following steps would you combine to address the given scenario? (Select two)

Create a standby Aurora instance in another Availability Zone to improve the availability as the standby can serve as a failover target

Use Amazon EC2 instances behind an Application Load Balancer to write the order data into Amazon Aurora cluster

Create a replica Aurora instance in another Availability Zone to improve the availability as the replica can serve as a failover target

Increase the concurrency of the AWS Lambda function so that the order-writes do not get missed during traffic spikes

Handle all read operations for your application by connecting to the reader endpoint of the Amazon Aurora cluster so that Aurora can spread the load for read-only connections across the Aurora replica

---

A company is looking for a technology that allows its mobile app users to connect through a Google login and have the capability to turn on AWS Multi-Factor Authentication (AWS MFA) to have maximum security. Ideally, the solution should be fully managed by AWS.

Which technology do you recommend for managing the users' accounts?

Amazon Cognito

AWS Identity and Access Management (AWS IAM)

Write an AWS Lambda function with Auth0 3rd party integration

Enable the AWS Google Login Service

Amazon Cognito lets you add user sign-up, sign-in, and access control to your web and mobile apps quickly and easily. Amazon Cognito scales to millions of users and supports sign-in with social identity providers, such as Facebook, Google, and Amazon, and enterprise identity providers via SAML 2.0. Here Cognito is the best technology choice for managing mobile user accounts.

---

Reporters at a news agency upload/download video files (about 500 megabytes each) to/from an Amazon S3 bucket as part of their daily work. As the agency has started offices in remote locations, it has resulted in poor latency for uploading and accessing data to/from the given Amazon S3 bucket. The agency wants to continue using a serverless storage solution such as Amazon S3 but wants to improve the performance.

As a solutions architect, which of the following solutions do you propose to address this issue? (Select two)

**Selección correcta**

**Use Amazon CloudFront distribution with origin as the Amazon S3 bucket. This would speed up uploads as well as downloads for the video files**

**Create new Amazon S3 buckets in every region where the agency has a remote office, so that each office can maintain its storage for the media assets**

**Move Amazon S3 data into Amazon Elastic File System (Amazon EFS) created in a US region, connect to Amazon EFS file system from Amazon EC2 instances in other AWS regions using an inter-region VPC peering connection**

**Tu selección es correcta**

**Enable Amazon S3 Transfer Acceleration (Amazon S3TA) for the Amazon S3 bucket. This would speed up uploads as well as downloads for the video files**

**Spin up Amazon EC2 instances in each region where the agency has a remote office. Create a daily job to transfer Amazon S3 data into Amazon EBS volumes attached to the Amazon EC2 instances**

Tenía que elegir 2.

---

A junior developer is learning to build websites using HTML, CSS, and JavaScript. He has created a static website and then deployed it on Amazon S3. Now he can't seem to figure out the endpoint for his super cool website.

As a solutions architect, can you help him figure out the allowed formats for the Amazon S3 website endpoints? (Select two)

http://s3-website-Region.bucket-name.amazonaws.com

http://bucket-name.s3-website-Region.amazonaws.com

http://bucket-name.Region.s3-website.amazonaws.com

http://s3-website.Region.bucket-name.amazonaws.com

http://bucket-name.s3-website.Region.amazonaws.com

https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteEndpoints.html

Depending on your Region, your Amazon S3 website endpoints follow one of these two formats.

s3-website dash (-) Region ‐ [http://bucket-name.s3-website.Region.amazonaws.com](http://bucket-name.s3-website.region.amazonaws.com/)

s3-website dot (.) Region ‐ [http://bucket-name.s3-website-Region.amazonaws.com](http://bucket-name.s3-website-region.amazonaws.com/)

---

A developer in your team has set up a classic 3 tier architecture composed of an Application Load Balancer, an Auto Scaling group managing a fleet of Amazon EC2 instances, and an Amazon Aurora database. As a Solutions Architect, you would like to adhere to the security pillar of the well-architected framework.

How do you configure the security group of the Aurora database to only allow traffic coming from the Amazon EC2 instances?

Add a rule authorizing the Auto Scaling group subnets CIDR

Add a rule authorizing the Amazon Aurora security group

Add a rule authorizing the Elastic Load Balancing security group

Add a rule authorizing the Amazon EC2 security group

For the given scenario, the Amazon EC2 instances that are part of the Auto Scaling Group are the ones accessing the database layer. The correct response is to add a rule to the security group attached to Aurora authorizing the Amazon EC2 instance's security group.

---

A company wants to publish an event into an Amazon Simple Queue Service (Amazon SQS) queue whenever a new object is uploaded on Amazon S3.

Which of the following statements are true regarding this functionality?

Only FIFO Amazon SQS queue is allowed as an Amazon S3 event notification destination, whereas Standard SQS queue is not allowed

Both Standard Amazon SQS queue and FIFO SQS queue are allowed as an Amazon S3 event notification destination

Neither Standard Amazon SQS queue nor FIFO SQS queue are allowed as an Amazon S3 event notification destination

Only Standard Amazon SQS queue is allowed as an Amazon S3 event notification destination, whereas FIFO SQS queue is not allowed

---

A startup has created a cost-effective backup solution in another AWS Region. The application is running in warm standby mode and has Application Load Balancer (ALB) to support it from the front. The current failover process is manual and requires updating the DNS alias record to point to the secondary Application Load Balancer in another Region in case of failure of the primary Application Load Balancer.

As a Solutions Architect, what will you recommend to automate the failover process?

Enable an Amazon Route 53 health check

Enable an Amazon EC2 instance health check

Configure AWS Trusted Advisor to check on unhealthy instances

Enable an ALB health check

Amazon Route 53 realiza verificaciones de estado en los **nodos del ELB**. Si detecta que el ELB no está accesible o no está respondiendo correctamente, **redirige el tráfico** a otro ELB saludable, o incluso a otra región si así está configurado.

Amazon Route 53 se integra con los **chequeos de salud de EC2** que realiza ELB. Si ELB detecta que una instancia EC2 está respondiendo pero la aplicación no está funcionando correctamente (por ejemplo, devolviendo errores HTTP 500), Route 53 puede redirigir el tráfico a otro **endpoint saludable** de otra instancia EC2.

Route 53 tiene la capacidad de manejar el **fallo de una AZ completa**. Si detecta que las instancias EC2 en una AZ fallan o no están accesibles, puede **redirigir el tráfico automáticamente** a una región o AZ que esté saludable, asegurando que los usuarios sigan accediendo a tu aplicación sin interrupciones.

Determining the health of an ELB endpoint is more complex than health checking a single IP address. For example, what if your application is running fine on Amazon EC2, but the load balancer itself isn't reachable? Or if your load balancer and your Amazon EC2 instances are working correctly, but a bug in your code causes your application to crash? Or how about if the Amazon EC2 instances in one Availability Zone of a multi-AZ ELB are experiencing problems?

Amazon Route 53 DNS Failover handles all of these failure scenarios by integrating with ELB behind the scenes. Once enabled, Route 53 automatically configures and manages health checks for individual ELB nodes. Amazon Route 53 also takes advantage of the Amazon EC2 instance health checking that ELB performs (information on configuring your ELB health checks is available here). By combining the results of health checks of your Amazon EC2 instances and your ELBs, Amazon Route 53 DNS Failover can evaluate the health of the load balancer and the health of the application running on the Amazon EC2 instances behind it. In other words, if any part of the stack goes down, Amazon Route 53 detects the failure and routes traffic away from the failed endpoint.

Using Amazon Route 53 DNS Failover, you can run your primary application simultaneously in multiple AWS regions around the world and failover across regions. Your end-users will be routed to the closest (by latency), healthy region for your application. Amazon Route 53 automatically removes from service any region where your application is unavailable - it will pull an endpoint out of service if there is region-wide connectivity or operational issue, if your application goes down in that region, or if your ELB or Amazon EC2 instances go down in that region.

---

A DevOps engineer at an organization is debugging issues related to an Amazon EC2 instance. The engineer has SSH'ed into the instance and he needs to retrieve the instance public IP from within a shell script running on the instance command line.

Can you identify the correct URL path to get the instance public IP?

http://254.169.254.169/latest/user-data/public-ipv4

http://169.254.169.254/latest/user-data/public-ipv4

http://169.254.169.254/latest/meta-data/public-ipv4

http://254.169.254.169/latest/meta-data/public-ipv4

---

The data engineering team at an e-commerce company has set up a workflow to ingest the clickstream data into the raw zone of the Amazon S3 data lake. The team wants to run some SQL based data sanity checks on the raw zone of the data lake.

What AWS services would you recommend for this use-case such that the solution is cost-effective and easy to maintain?

Use Amazon Athena to run SQL based analytics against Amazon S3 data

Load the incremental raw zone data into Amazon RDS on an hourly basis and run the SQL based sanity checks

Load the incremental raw zone data into an Amazon EMR based Spark Cluster on an hourly basis and use SparkSQL to run the SQL based sanity checks

Load the incremental raw zone data into Amazon Redshift on an hourly basis and run the SQL based sanity checks

---

An application hosted on Amazon EC2 contains sensitive personal information about all its customers and needs to be protected from all types of cyber-attacks. The company is considering using the AWS Web Application Firewall (AWS WAF) to handle this requirement.

Can you identify the correct solution leveraging the capabilities of AWS WAF?

AWS WAF can be directly configured on Amazon EC2 instances for ensuring the security of the underlying application data

AWS WAF can be directly configured only on an Application Load Balancer or an Amazon API Gateway. One of these two services can then be configured with Amazon EC2 to build the needed secure architecture

Create Amazon CloudFront distribution for the application on Amazon EC2 instances. Deploy AWS WAF on Amazon CloudFront to provide the necessary safety measures

Configure an Application Load Balancer (ALB) to balance the workload for all the Amazon EC2 instances. Configure Amazon CloudFront to distribute from an Application Load Balancer since AWS WAF cannot be directly configured on ALB. This configuration not only provides necessary safety but is scalable too

**AWS WAF can be directly configured on Amazon EC2 instances for ensuring the security of the underlying application data** - AWS WAF can be deployed on Amazon CloudFront, the Application Load Balancer (ALB), and Amazon API Gateway. It cannot be configured directly on an Amazon EC2 instance.

---

A leading media company wants to do an accelerated online migration of hundreds of terabytes of files from their on-premises data center to Amazon S3 and then establish a mechanism to access the migrated data for ongoing updates from the on-premises applications.

As a solutions architect, which of the following would you select as the MOST performant solution for the given use-case?

Use AWS DataSync to migrate existing data to Amazon S3 and then use File Gateway to retain access to the migrated data for ongoing updates from the on-premises applications

Use Amazon S3 Transfer Acceleration (Amazon S3TA) to migrate existing data to Amazon S3 and then use AWS DataSync for ongoing updates from the on-premises applications

Use AWS DataSync to migrate existing data to Amazon S3 as well as access the Amazon S3 data for ongoing updates

Use File Gateway configuration of AWS Storage Gateway to migrate data to Amazon S3 and then use Amazon S3 Transfer Acceleration (Amazon S3TA) for ongoing updates from the on-premises applications

AWS DataSync cannot be used to facilitate ongoing updates to the migrated files from the on-premises applications.

AWS Storage Gateway is a hybrid cloud storage service that gives you on-premises access to virtually unlimited cloud storage. The service provides three different types of gateways – Tape Gateway, File Gateway, and Volume Gateway – that seamlessly connect on-premises applications to cloud storage, caching data locally for low-latency access. File gateway offers SMB or NFS-based access to data in Amazon S3 with local caching.

The combination of AWS DataSync and File Gateway is the correct solution. AWS DataSync enables you to automate and accelerate online data transfers to AWS storage services. File Gateway then provides your on-premises applications with low latency access to the migrated data.

---

An e-commerce company uses Amazon Simple Queue Service (Amazon SQS) queues to decouple their application architecture. The engineering team has observed message processing failures for some customer orders.

As a solutions architect, which of the following solutions would you recommend for handling such message failures?

Use a dead-letter queue to handle message processing failures

Use a temporary queue to handle message processing failures

Use long polling to handle message processing failures

Use short polling to handle message processing failures

Dead-letter queues can be used by other queues (source queues) as a target for messages that can't be processed (consumed) successfully. Dead-letter queues are useful for debugging your application or messaging system because they let you isolate problematic messages to determine why their processing doesn't succeed. Sometimes, messages can’t be processed because of a variety of possible issues, such as when a user comments on a story but it remains unprocessed because the original story itself is deleted by the author while the comments were being posted. In such a case, the dead-letter queue can be used to handle message processing failures.

**Use long polling to handle message processing failures**

Amazon SQS provides short polling and long polling to receive messages from a queue. By default, queues use short polling. With short polling, Amazon SQS sends the response right away, even if the query found no messages. With long polling, Amazon SQS sends a response after it collects at least one available message, up to the maximum number of messages specified in the request. Amazon SQS sends an empty response only if the polling wait time expires. Neither short polling nor long polling can be used to handle message processing failures.

---

You are a cloud architect at an IT company. The company has multiple enterprise customers that manage their own mobile applications that capture and send data to Amazon Kinesis Data Streams. They have been getting a `ProvisionedThroughputExceededException` exception. You have been contacted to help and upon analysis, you notice that messages are being sent one by one at a high rate.

Which of the following options will help with the exception while keeping costs at a minimum?

Use batch messages

Decrease the Stream retention duration

Increase the number of shards

Use Exponential Backoff

**Increase the number of shards** - Increasing shards could be a short term fix but will substantially increase the cost, so this option is ruled out.

When a host needs to send many records per second (RPS) to Amazon Kinesis, simply calling the basic PutRecord API action in a loop is inadequate. To reduce overhead and increase throughput, the application must batch records and implement parallel HTTP requests. This will increase the efficiency overall and ensure you are optimally using the shards.

---

A mobile chat application uses Amazon DynamoDB as its database service to provide low latency chat updates. A new developer has joined the team and is reviewing the configuration settings for Amazon DynamoDB which have been tweaked for certain technical requirements. AWS CloudTrail service has been enabled on all the resources used for the project. Yet, Amazon DynamoDB encryption details are nowhere to be found.

Which of the following options can explain the root cause for the given issue?

By default, all Amazon DynamoDB tables are encrypted using Data keys, which do not write to AWS CloudTrail logs

By default, all Amazon DynamoDB tables are encrypted using AWS owned keys, which do not write to AWS CloudTrail logs

By default, all Amazon DynamoDB tables are encrypted under AWS managed Keys, which do not write to AWS CloudTrail logs

By default, all Amazon DynamoDB tables are encrypted under Customer managed keys, which do not write to AWS CloudTrail logs

AWS owned keys are not stored in your AWS account. They are part of a collection of KMS keys that AWS owns and manages for use in multiple AWS accounts. AWS services can use AWS owned keys to protect your data. AWS owned keys used by DynamoDB are rotated every year (approximately 365 days).

You cannot view, manage, or use AWS owned keys, or audit their use. However, you do not need to do any work or change any programs to protect the keys that encrypt your data. You are not charged a monthly fee or a usage fee for use of AWS owned keys, and they do not count against AWS KMS quotas for your account.

All DynamoDB tables are encrypted. There is no option to enable or disable encryption for new or existing tables. By default, all tables are encrypted under an AWS owned key in the DynamoDB service account. However, you can select an option to encrypt some or all of your tables under a customer managed key or the AWS managed key for DynamoDB in your account.

---

Which of the following is true regarding cross-zone load balancing as seen in Application Load Balancer versus Network Load Balancer?

By default, cross-zone load balancing is disabled for Application Load Balancer and enabled for Network Load Balancer

By default, cross-zone load balancing is enabled for Application Load Balancer and disabled for Network Load Balancer

By default, cross-zone load balancing is disabled for both Application Load Balancer and Network Load Balancer

By default, cross-zone load balancing is enabled for both Application Load Balancer and Network Load Balancer

By default, cross-zone load balancing is enabled for Application Load Balancer and disabled for Network Load Balancer. When cross-zone load balancing is enabled, each load balancer node distributes traffic across the registered targets in all the enabled Availability Zones. When cross-zone load balancing is disabled, each load balancer node distributes traffic only across the registered targets in its Availability Zone.

---

An online gaming company wants to block access to its application from specific countries; however, the company wants to allow its remote development team (from one of the blocked countries) to have access to the application. The application is deployed on Amazon EC2 instances running under an Application Load Balancer with AWS Web Application Firewall (AWS WAF).

As a solutions architect, which of the following solutions can be combined to address the given use-case? (Select two)

Use Application Load Balancer geo match statement listing the countries that you want to block

Use AWS WAF geo match statement listing the countries that you want to block

Use Application Load Balancer IP set statement that specifies the IP addresses that you want to allow through

Create a deny rule for the blocked countries in the network access control list (network ACL) associated with each of the Amazon EC2 instances

Use AWS WAF IP set statement that specifies the IP addresses that you want to allow through

An Application Load Balancer cannot block or allow traffic based on geographic match conditions or IP based conditions. El network load balancer tampoco y no permite WAF encima.

---

A retail company wants to establish encrypted network connectivity between its on-premises data center and AWS Cloud. The company wants to get the solution up and running in the fastest possible time and it should also support encryption in transit.

As a solutions architect, which of the following solutions would you suggest to the company?

Use AWS Direct Connect to establish encrypted network connectivity between the on-premises data center and AWS Cloud

Use AWS Secrets Manager to establish encrypted network connectivity between the on-premises data center and AWS Cloud

Use AWS Data Sync to establish encrypted network connectivity between the on-premises data center and AWS Cloud

Use AWS Site-to-Site VPN to establish encrypted network connectivity between the on-premises data center and AWS Cloud

**Use AWS Site-to-Site VPN to establish encrypted network connectivity between the on-premises data center and AWS Cloud**

AWS Site-to-Site VPN enables you to securely connect your on-premises network or branch office site to your Amazon Virtual Private Cloud (Amazon VPC). You can securely extend your data center or branch office network to the cloud with an AWS Site-to-Site VPN connection. A VPC VPN Connection utilizes IPSec to establish encrypted network connectivity between your on-premises network and Amazon VPC over the Internet. IPsec is a protocol suite for securing IP communications by authenticating and encrypting each IP packet in a data stream.

Incorrect options:

**Use AWS Direct Connect to establish encrypted network connectivity between the on-premises data center and AWS Cloud** - AWS Direct Connect lets you establish a dedicated network connection between your network and one of the AWS Direct Connect locations. Using industry-standard 802.1q VLANs, this dedicated connection can be partitioned into multiple virtual interfaces. AWS Direct Connect does not encrypt your traffic that is in transit. To encrypt the data in transit that traverses AWS Direct Connect, you must use the transit encryption options for that service. As AWS Direct Connect does not support encrypted network connectivity between an on-premises data center and AWS Cloud, therefore this option is incorrect.

---

A streaming solutions company is building a video streaming product by using an Application Load Balancer (ALB) that routes the requests to the underlying Amazon EC2 instances. The engineering team has noticed a peculiar pattern. The Application Load Balancer removes an instance from its pool of healthy instances whenever it is detected as unhealthy but the Auto Scaling group fails to kick-in and provision the replacement instance.

What could explain this anomaly?

The Auto Scaling group is using ALB based health check and the Application Load Balancer is using Amazon EC2 based health check

Both the Auto Scaling group and Application Load Balancer are using ALB based health check

The Auto Scaling group is using Amazon EC2 based health check and the Application Load Balancer is using ALB based health check

Both the Auto Scaling group and Application Load Balancer are using Amazon EC2 based health check

el EC2 health check que hacer el ASG de normal lo hacer sobre el hipervisor y no sobre el cotenido de la instancia, el aplication load balancer si que comprueba si la aplicacion funciona con sus health checks.

If the Auto Scaling group (ASG) is using EC2 as the health check type and the Application Load Balancer (ALB) is using its in-built health check, there may be a situation where the ALB health check fails because the health check pings fail to receive a response from the instance. At the same time, ASG health check can come back as successful because it is based on EC2 based health check. Therefore, in this scenario, the ALB will remove the instance from its inventory, however, the Auto Scaling Group will fail to provide the replacement instance. This can lead to the scaling issues mentioned in the problem statement.

---

A media company is evaluating the possibility of moving its IT infrastructure to the AWS Cloud. The company needs at least 10 terabytes of storage with the maximum possible I/O performance for processing certain files which are mostly large videos. The company also needs close to 450 terabytes of very durable storage for storing media content and almost double of it, i.e. 900 terabytes for archival of legacy data.

As a Solutions Architect, which set of services will you recommend to meet these requirements?

Amazon S3 standard storage for maximum performance, Amazon S3 Intelligent-Tiering for intelligent, durable storage, and Amazon S3 Glacier Deep Archive for archival storage

Amazon EBS for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage

Amazon EC2 instance store for maximum performance, AWS Storage Gateway for on-premises durable data access and Amazon S3 Glacier Deep Archive for archival storage

Amazon EC2 instance store for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage

Amazon EBS volumes are particularly well-suited for use as the primary storage for file systems, databases, or for any applications that require fine granular updates and access to raw, unformatted, block-level storage.

For high I/O performance, instance store volumes are a better opti

---

The engineering team at a weather tracking company wants to enhance the performance of its relational database and is looking for a caching solution that supports geospatial data.

As a solutions architect, which of the following solutions will you suggest?

Use Amazon ElastiCache for Redis

Use Amazon ElastiCache for Memcached

Use AWS Global Accelerator

Use Amazon DynamoDB Accelerator (DAX)

Redis has purpose-built commands for working with real-time geospatial data at scale. You can perform operations like finding the distance between two elements (for example people or places) and finding all elements within a given distance of a point. Memcached no.

---

Your company is evolving towards a microservice approach for their website. The company plans to expose the website from the same load balancer, linked to different target groups with different URLs, that are similar to these - checkout.mycorp.com, www.mycorp.com, mycorp.com/profile, and mycorp.com/search.

As a Solutions Architect, which Load Balancer type do you recommend to achieve this routing feature with MINIMUM configuration and development effort?

Create an NGINX based load balancer on an Amazon EC2 instance to have advanced routing capabilities

Create a Classic Load Balancer

Create a Network Load Balancer

Create an Application Load Balancer

Path-based Routing: You can route a client request based on the URL path of the HTTP header. You can use path conditions to define rules that route requests based on the URL in the request (also known as path-based routing). Example path patterns: /img/* /img/*/pics The path pattern is used to route requests but does not alter them. For example, if a rule has a path pattern of /img/*, the rule would forward a request for /img/picture.jpg to the specified target group as a request for /img/picture.jpg. The path pattern is applied only to the path of the URL, not to its query parameters.

HTTP header-based routing: You can route a client request based on the value of any standard or custom HTTP header.

HTTP method-based routing: You can route a client request based on any standard or custom HTTP method.

Query string parameter-based routing: You can route a client request based on query string or query parameters.

Source IP address CIDR-based routing: You can route a client request based on source IP address CIDR from where the request originates.

Path based routing and host based routing are only available for the Application Load Balancer (ALB). Therefore this is the correct option for the given use-case.

---