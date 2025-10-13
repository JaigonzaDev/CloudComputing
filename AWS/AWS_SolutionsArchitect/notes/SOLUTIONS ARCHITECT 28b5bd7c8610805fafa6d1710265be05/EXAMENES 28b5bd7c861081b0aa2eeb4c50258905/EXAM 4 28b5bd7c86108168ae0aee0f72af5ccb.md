# EXAM 4

A solutions architect is implementing a complex Java application with a MySQL database. The Java application must be deployed on Apache Tomcat and must be highly available.

What should the solutions architect do to meet these requirements?

A. Deploy the application in AWS Lambda. Configure an Amazon API Gateway API to connect with the Lambda functions.

B. Deploy the application by using AWS Elastic Beanstalk. Configure a load-balanced environment and a rolling deployment policy

C. Migrate the database to Amazon ElastiCache. Configure the ElastiCache security group to allow access from the application.

D. Yauch an Amazon EC2 instance. Install a MySQL server on the EC2 instance. Configure the application on the server. Create an AMI. Use the AMI to create a launch template with an Auto caling group.

Básicamente la D también es valida pero la B es menos engorrosa, porque AWS elastic Beanstalk es compatible con apache tomcat.

---

A company maintains an Amazon RDS database that maps users to cost centers. The company has accounts in an organization in AWS Organizations. The company needs a solution that will tag all resources that are created in a specific AWS account in the organization. The solution must tag each resource with the cost center ID of the user who created the resource.

Which solution will meet these requirements?

A. Move the specific AWS account to a new organizational unit (OU) in Organizations from the management account. Create a service control policy (SCP) that requires all existing resources to have the correct cost center tag before the resources are created. Apply the SCP to the new OU.

B. Create an AWS Lambda function to tag the resources after the Lambda function looks up the appropriate cost center from the RDS database. Configure an Amazon EventBridge rule that reacts to AWS CloudTrail events to invoke the Lambda function.

C. Create an AWS CloudFormation stack to deploy an AWS Lambda function. Configure the Lambda function to look up the appropriate cost center from the RDS database and to tag resources. Create an Amazon EventBridge scheduled rule to invoke the CloudFormation stack.

D. Create an AWS Lambda function to tag the resources with a default value. Configure an Amazon EventBridge rule that reacts to AWS CloudTrail events to invoke the Lambda function when a resource is missing the cost center tag.

Es la B ya que las SCP policy no deja hacer politicas para que no se creen maquinas según no tegan el tag, lo que puede hacer es que si tienen ciertos tags no se creen. También hay que tener en cuenta lo que pone al principio de la pregunta que las bases de datos están mapeadas los costes a los usuarios. 

---

A company uses AWS Organizations. The company wants to operate some of its AWS accounts with different budgets. The company wants to receive alerts and automatically prevent provisioning of additional resources on AWS accounts when the allocated budget threshold is met during a specific period.

Which combination of solutions will meet these requirements? (Select THREE.)

A. Use AWS Budgets to create a budget. Set the budget amount under the Cost and Usage Reports section of the required AWS accounts.

B. Use AWS Budgets to create a budget. Set the budget amount under the Billing dashboards of the required AWS accounts.

C. Create an 1AM user for AWS Budgets to run budget actions with the required permissions.

D. Create an 1AM role for AWS Budgets to run budget actions with the required permissions.

E. Add an alert to notify the company when each account meets its budget threshold. Add a budget action that selects the 1AM identity created with the appropriate config rule to prevent provisioning of additional resources.

F. Add an alert to notify the company when each account meets its budget threshold. Add a budget action that selects the 1AM identity created with the appropriate service control policy (SCP) to prevent provisioning of additional resources.

Básicamente la opción B antes que la A ya que Billing dashboards deja ver a tiempo real, automatizar opcines en base a esto en cambio Cost and Usage reports como su propio nombre indica en diferencia a billing solo sirve para hacer reportes detallados pero no mucho mas no te deja ver cosas a tiempo real sino en un momento específico.

---

A company is running an SMB file server in its data center. The file server stores large files that are accessed frequently for the first few days after the files are created. After 7 days the files are rarely accessed.

The total data size is increasing and is close to the company's total storage capacity. A solutions architect must increase the company's available storage space without losing low-latency access to the most recently accessed files. The solutions architect must also provide file lifecycle management to avoid future storage issues.

Which solution will meet these requirements?

A. Use AWS DataSync to copy data that is older than 7 days from the SMB file server to AWS.

B. Create an Amazon S3 File Gateway to extend the company's storage space. Create an S3 Lifecycle policy to transition the data to S3 Glacier Deep Archive after 7 days.

C. Create an Amazon FSx for Windows File Server file system to extend the company's storage space.

D. Install a utility on each user's computer to access Amazon S3. Create an S3 Lifecycle policy to transition the data to S3 Glacier Flexible Retrieval after 7 days.

La opción C no resuelve el tema de los futuros problemas por almacenamiento.

---

A company wants to migrate its three-tier application from on premises to AWS. The web tier and the application tier are running on third-party virtual machines (VMs). The database tier is running on MySQL.

The company needs to migrate the application by making the fewest possible changes to the architecture. The company also needs a database solution that can restore data to a specific point in time.

Which solution will meet these requirements with the LEAST operational overhead?

A. Migrate the web tier and the application tier to Amazon EC2 instances in private subnets. Migrate the database tier to Amazon RDS for MySQL in private subnets.

B. Migrate the web tier to Amazon EC2 instances in public subnets. Migrate the application tier to EC2 instances in private subnets. Migrate the database tier to Amazon Aurora MySQL in private subnets.

C. Migrate the web tier to Amazon EC2 instances in public subnets. Migrate the application tier to EC2 instances in private subnets. Migrate the database tier to Amazon RDS for MySQL in private subnets.

D. Migrate the web tier and the application tier to Amazon EC2 instances in public subnets. Migrate the database tier to Amazon Aurora MySQL in public subnets.

En este caso la mejor opción es usar amazon RDS antes que aurora ya que para SQL tradicional habría que adaptar la base con algunos cambios para que sea totalmente compatible con aurora, aurora se suele utilizar para casos de escala masiva. RDS tiene un replicación mas lenta que aurora en multiples zonas por lo que aurora también ganaría en estos casos. Y si la empresa quiere evitar la administración del tamaño de las instancias.

---

A company hosts a frontend application that uses an Amazon API Gateway API backend that is integrated with AWS Lambda When the API receives requests, the Lambda function loads many libranes Then the Lambda function connects to an Amazon RDS database processes the data and returns the data to the frontend application. The company wants to ensure that response latency is as low as possible for all its users with the fewest number of changes to the company's operations

Which solution will meet these requirements'?

A. Establish a connection between the frontend application and the database to make queries faster by bypassing the API

B. Configure provisioned concurrency for the Lambda function that handles the requests

C. Cache the results of the queries in Amazon S3 for faster retneval of similar datasets.

D. Increase the size of the database to increase the number of connections Lambda can establish at one time

Provisioned concurrency para las funciones Lambda te deja poner el número de instancias pre inicializadas para que cuando llegen peticiones las procese al instante, el problema que hay aquí es que si lambda no le llegan peticiones durante un tiempo se pone en estado inactivo y tarda en volver a arrancar entonces en estos casos donde pone “loads many libraries” se puede producir latencias en lo que tarda en empezar.

---

A company is deploying a new public web application toAWS. The application Will run behind an Application Load Balancer (ALE). The application needs to be encrypted at the edge with an SSL/TLS certificate that is issued by an external certificate authority (CA). The certificate must be rotated each year before the certificate expires.

What should a solutions architect do to meet these requirements?

A. Use AWS Certificate Manager (ACM) to issue an SSUTLS certificate. Apply the certificate to the ALB Use the managed renewal feature to automatically rotate the certificate.

B. Use AWS Certificate Manager (ACM) to issue an SSUTLS certificate_ Import the key material from the certificate. Apply the certificate to the ALB Use the managed renewal teature to automatically rotate the certificate.

C. Use AWS Private Certificate Authority to issue an SSL/TLS certificate from the root CA. Apply the certificate to the ALB. use the managed renewal feature to automatically rotate the certificate

D. Use AWS Certificate Manager (ACM) to import an SSL/TLS certificate. Apply the certificate to the ALB_ Use Amazon EventBridge to send a notification when the certificate is nearing expiration. Rotate the certificate manually.

Vale la A y la B no son correctas por no hay un metodo para renovar automaticamente el certificado de seguridad, luego la C esta mal porque Private Certificate Authority no gestiona certificado externos es del propio AWS. El certificado siempre se aplica al sitio donde se va dirigir el tráfico es decir en este caso el primer punto de conexión es el ALB.

---

A company uses a 100 GB Amazon RDS for Microsoft SQL Server Single-AZ DB instance in the us-east-1 Region to store customer transactions. The company needs high availability and automate recovery for the DB instance. The company must also run reports on the RDS database several times a year. The report process causes transactions to take longer than usual to post to the customer‘ accounts.

Which combination of steps will meet these requirements? (Select TWO.)

A. Modify the DB instance from a Single-AZ DB instance to a Multi-AZ deployment.

B. Take a snapshot of the current DB instance. Restore the snapshot to a new RDS deployment in another Availability Zone.

C. Create a read replica of the DB instance in a different Availability Zone. Point All requests for reports to the read replica.

D. Migrate the database to RDS Custom.

E. Use RDS Proxy to limit reporting requests to the maintenance window.

El proxy solo sirve para gestionar el tema del tráfico, crear una read replica no tiene que ver con la gestión Multi-AZ por lo que es la opción correcta.

---