## AWS CSA Associate 模拟题6
353.
You want to pass queue messages that are 1GB each. How should you achieve this?
- [ ] Use Kinesis as a buffer stream for message bodies. Store the checkpoint id for the placement in the Kinesis Stream in SQS.
- [x] Use the Amazon SQS Extended Client Library for Java and Amazon S3 as a storage mechanism for message bodies. (Amazon SQS messages with Amazon S3 can be useful for storing and retrieving messages with a message size of up to 2 GB. To manage Amazon - [ ] - [ ] SQS messages with Amazon S3, use the Amazon SQS Extended Client Library for Java. )
- [ ] Use SQS’s support for message partitioning and multi-part uploads on Amazon S3.
- [ ] Use AWS EFS as a shared pool storage medium. Store filesystem pointers to the files on disk in the SQS message bodies.

354.
Company ABCD has recently launched an online commerce site for bicycles on AWS. They have a “Product” DynamoDB table that stores details for each bicycle, such as, manufacturer, color, price, quantity and size to display in the online store. Due to customer demand, they want to include an image for each bicycle along with the existing details. Which approach below provides the least impact to provisioned throughput on the “Product” table?
- [ ] Serialize the image and store it in multiple DynamoDB tables
- [ ] Create an “Images” DynamoDB table to store the Image with a foreign key constraint to the “Product” table
- [ ] Add an image data type to the “Product” table to store the images in binary format
- [x] Store the images in Amazon S3 and add an S3 URL pointer to the “Product” table item for each image

355.
Which of the following provides the fastest storage medium?
- [ ] Amazon S3
- [ ] Amazon EBS using Provisioned IOPS (PIOPS)
- [x] SSD Instance (ephemeral) store (SSD Instance Storage provides 100,000 IOPS on some instance types, much faster than any network-attached storage)
- [ ] AWS Storage Gateway

356.
Which of the following are use cases for Amazon DynamoDB? Choose 3 answers
- [ ] Storing BLOB data.
- [x] Managing web sessions
- [x] Storing JSON documents
- [x] Storing metadata for Amazon S3 objects
- [ ] Running relational joins and complex updates.
- [ ] Storing large amounts of infrequently accessed data.

357.
A client application requires operating system privileges on a relational database server. What is an appropriate configuration for highly available database architecture?
- [ ] A standalone Amazon EC2 instance
- [ ] Amazon RDS in a Multi-AZ configuration
- [ ] Amazon EC2 instances in a replication configuration utilizing a single Availability Zone
- [x] Amazon EC2 instances in a replication configuration utilizing two different Availability Zones

358.
You are developing a new mobile application and are considering storing user preferences in AWS, which would provide a more uniform cross-device experience to users using multiple mobile devices to access the application. The preference data for each user is estimated to be 50KB in size. Additionally 5 million customers are expected to use the application on a regular basis. The solution needs to be cost-effective, highly available, scalable and secure, how would you design a solution to meet the above requirements?
- [ ] Setup an RDS MySQL instance in 2 availability zones to store the user preference data. Deploy a public facing application on a server in front of the database to manage security and access credentials
- [x] Setup a DynamoDB table with an item for each user having the necessary attributes to hold the user preferences. The mobile application will query the user preferences directly from the DynamoDB table. Utilize STS. Web Identity Federation, and DynamoDB Fine Grained Access Control to authenticate and authorize access (DynamoDB provides high availability as it synchronously replicates data across three facilities within an AWS Region and scalability as it is designed to scale its provisioned throughput up or down while still remaining available. Also suitable for storing user preference data)
- [ ] Setup an RDS MySQL instance with multiple read replicas in 2 availability zones to store the user preference data .The mobile application will query the user preferences from the read replicas. Leverage the MySQL user management and access privilege system to manage security and access credentials.
- [ ] Store the user preference data in S3 Setup a DynamoDB table with an item for each user and an item attribute pointing to the user’ S3 object. The mobile application will retrieve the S3 URL from DynamoDB and then access the S3 object directly utilize STS, Web identity Federation, and S3 ACLs to authenticate and authorize access.

359.
A customer is running an application in US-West (Northern California) region and wants to setup disaster recovery failover to the Asian Pacific (Singapore) region. The customer is interested in achieving a low Recovery Point Objective (RPO) for an Amazon RDS multi-AZ MySQL database instance. Which approach is best suited to this need?
- [ ] Synchronous replication
- [x] Asynchronous replication
- [ ] Route53 health checks
- [ ] Copying of RDS incremental snapshots

360.
You are designing a file -sharing service. This service will have millions of files in it. Revenue for the service will come from fees based on how much storage a user is using. You also want to store metadata on each file, such as title, description and whether the object is public or private. How do you achieve all of these goals in a way that is economical and can scale to millions of users?
- [ ] Store all files in Amazon Simple Storage Service (53). Create a bucket for each user. Store metadata in the filename of each object, and access it with LIST commands against the S3 API.
- [x] Store all files in Amazon 53. Create Amazon DynamoDB tables for the corresponding key -value pairs on the associated metadata, when objects are uploaded.
- [ ] Create a striped set of 4000 IOPS Elastic Load Balancing volumes to store the data. Use a database running in Amazon Relational Database Service (RDS) to store the metadata.
- [ ] Create a striped set of 4000 IOPS Elastic Load Balancing volumes to store the data. Create Amazon DynamoDB tables for the corresponding key-value pairs on the associated metadata, when objects are uploaded.

361.
Company ABCD has recently launched an online commerce site for bicycles on AWS. They have a “Product” DynamoDB table that stores details for each bicycle, such as, manufacturer, color, price, quantity and size to display in the online store. Due to customer demand, they want to include an image for each bicycle along with the existing details. Which approach below provides the least impact to provisioned throughput on the “Product” table?
- [ ] Serialize the image and store it in multiple DynamoDB tables
- [ ] Create an “Images” DynamoDB table to store the Image with a foreign key constraint to the “Product” table
- [ ] Add an image data type to the “Product” table to store the images in binary format
- [x] Store the images in Amazon S3 and add an S3 URL pointer to the “Product” table item for each image

362.
You are designing Internet connectivity for your VPC. The Web servers must be available on the Internet. The application must have a highly available architecture. Which alternatives should you consider? (Choose 2 answers)
- [ ] Configure a NAT instance in your VPC. Create a default route via the NAT instance and associate it with all subnets. Configure a DNS A record that points to the NAT instance public IP address (NAT is for internet connectivity for instances in private subnet)
- [ ] Configure a CloudFront distribution and configure the origin to point to the private IP addresses of your Web servers. Configure a Route53 CNAME record to your CloudFront distribution.
- [x] Place all your web servers behind ELB. Configure a Route53 CNAME to point to the ELB DNS name.
- [x] Assign EIPs to all web servers. Configure a Route53 record set with all EIPs. With health checks and DNS failover.

363.
You are designing a system which needs, at minimum, 8 m4.large instances operating to service traffic. When designing a system for high availability in the us-east-1 region, which has 6 Availability Zones, you company needs to be able to handle death of a full availability zone. How should you distribute the servers, to save as much cost as possible, assuming all of the EC2 nodes are properly linked to an ELB? Your VPC account can utilize us-east-1’s AZ’s a through f, inclusive.
- [ ] 3 servers in each of AZ’s a through d, inclusive.
- [ ] 8 servers in each of AZ’s a and b.
- [x] 2 servers in each of AZ’s a through e, inclusive. (You need to design for N+1 redundancy on Availability Zones. ZONE_COUNT = (REQUIRED_INSTANCES / INSTANCE_COUNT_PER_ZONE) + 1. To minimize cost, spread the instances across as many possible zones as you can. By using a though e, you are allocating 5 zones. Using 2 instances, you have 10 total instances. If a single zone fails, you have 4 zones left, with 2 instances each, for a total of 8 instances. By spreading out as much as possible, you have increased cost by only 25% and significantly de-risked an availability zone failure. Refer link)
- [ ] 4 servers in each of AZ’s a through c, inclusive.

364.
You are putting together a WordPress site for a local charity and you are using a combination of Route53, Elastic Load Balancers, EC2 & RDS. You launch your EC2 instance, download WordPress and setup the configuration files connection string so that it can communicate to RDS. When you browse to your URL however, nothing happens. Which of the following could NOT be the cause of this.
- [ ] You have forgotten to open port 80/443 on your security group in which the EC2 instance is placed.
- [ ] Your elastic load balancer has a health check, which is checking a webpage that does not exist; therefore your EC2 instance is not in service.
- [ ] You have not configured an ALIAS for your A record to point to your elastic load balancer
- [x] You have locked port 22 down to your specific IP address therefore users cannot access your site using HTTP/HTTPS

365.
How can you secure data at rest on an EBS volume?
- [ ] Encrypt the volume using the S3 server-side encryption service
- [ ] Attach the volume to an instance using EC2’s SSL interface.
- [ ] Create an IAM policy that restricts read and write access to the volume.
- [ ] Write the data randomly instead of sequentially.
- [x] Use an encrypted file system on top of the EBS volume

366.
Your company policies require encryption of sensitive data at rest. You are considering the possible options for protecting data while storing it at rest on an EBS data volume, attached to an EC2 instance. Which of these options would allow you to encrypt your data at rest? (Choose 3 answers)
- [x] Implement third party volume encryption tools
- [ ] Do nothing as EBS volumes are encrypted by default
- [x] Encrypt data inside your applications before storing it on EBS
- [x] Encrypt data using native data encryption drivers at the file system level
- [ ] Implement SSL/TLS for all services running on the server

367.
A company is storing data on Amazon Simple Storage Service (S3). The company’s security policy mandates that data is encrypted at rest. Which of the following methods can achieve this? Choose 3 answers
- [x] Use Amazon S3 server-side encryption with AWS Key Management Service managed keys
- [x] Use Amazon S3 server-side encryption with customer-provided keys
- [ ] Use Amazon S3 server-side encryption with EC2 key pair.
- [ ] Use Amazon S3 bucket policies to restrict access to the data at rest.
- [x] Encrypt the data on the client-side before ingesting to Amazon S3 using their own master key
- [ ] Use SSL to encrypt the data while in transit to Amazon S3.

368.
Which 2 services provide native encryption
- [ ] Amazon EBS
- [x] Amazon Glacier
- [ ] Amazon Redshift (is optional)
- [ ] Amazon RDS (is optional)
- [x] Amazon Storage Gateway

369.
With which AWS services CloudHSM can be used (select 2)
- [ ] S3
- [ ] DynamoDb
- [x] RDS
- [ ] ElastiCache
- [x] Amazon Redshift

370.
In the shared security model, AWS is responsible for which of the following security best practices (check all that apply) :
- [x] Penetration testing
- [ ] Operating system account security management (User responsibility)
- [x] Threat modeling
- [ ] User group access management (User responsibility)
- [x] Static code analysis (AWS development cycle responsibility)

371.
You are running a web-application on AWS consisting of the following components an Elastic Load Balancer (ELB) an Auto-Scaling Group of EC2 instances running Linux/PHP/Apache, and Relational DataBase Service (RDS) MySQL. Which security measures fall into AWS’s responsibility?
- [ ] Protect the EC2 instances against unsolicited access by enforcing the principle of least-privilege access (User responsibility)
- [x] Protect against IP spoofing or packet sniffing
- [ ] Assure all communication between EC2 instances and ELB is encrypted (User responsibility)
- [ ] Install latest security patches on ELB. RDS and EC2 instances (User responsibility)

372.
In AWS, which security aspects are the customer’s responsibility? Choose 4 answers
- [ ] Controlling physical access to compute resources (AWS responsibility)
- [x] Patch management on the EC2 instances operating system
- [x] Encryption of EBS (Elastic Block Storage) volumes
- [x] Life-cycle management of IAM credentials
- [ ] Decommissioning storage devices (AWS responsibility)
- [x] Security Group and ACL (Access Control List) settings

373.
Per the AWS Acceptable Use Policy, penetration testing of EC2 instances:
- [ ] May be performed by AWS, and will be performed by AWS upon customer request.
- [x] May be performed by AWS, and is periodically performed by AWS.
- [ ] Are expressly prohibited under all circumstances.
- [ ] May be performed by the customer on their own instances with prior authorization from AWS.
- [ ] May be performed by the customer on their own instances, only if performed from EC2 instances

374.
Which is an operational process performed by AWS for data security?
- [ ] AES-256 encryption of data stored on any shared storage device (User responsibility)
- [x] Decommissioning of storage devices using industry-standard practices
- [ ] Background virus scans of EBS volumes and EBS snapshots (No virus scan is performed by AWS on User instances)
- [ ] Replication of data across multiple AWS Regions (AWS does not replicate data across regions unless done by User)
- [ ] Secure wiping of EBS data when an EBS volume is unmounted (data is not wiped off on EBS volume when unmounted and it can be remounted on other EC2 instance)

375.
You are designing a social media site and are considering how to mitigate distributed denial-of-service (DDoS) attacks. Which of the below are viable mitigation techniques? (Choose 3 answers)
- [ ] Add multiple elastic network interfaces (ENIs) to each EC2 instance to increase the network bandwidth.
- [ ] Use dedicated instances to ensure that each instance has the maximum performance possible.
- [x] Use an Amazon CloudFront distribution for both static and dynamic content.
- [ ] Use an Elastic Load Balancer with auto scaling groups at the web app and Amazon Relational Database Service (RDS) tiers
- [x] Add alert Amazon CloudWatch to look for high Network in and CPU utilization.
- [x] Create processes and capabilities to quickly add and remove rules to the instance OS firewall.

376.
You’ve been hired to enhance the overall security posture for a very large e-commerce site. They have a well architected multi-tier application running in a VPC that uses ELBs in front of both the web and the app tier with static assets served directly from S3. They are using a combination of RDS and DynamoDB for their dynamic data and then archiving nightly into S3 for further processing with EMR. They are concerned because they found questionable log entries and suspect someone is attempting to gain unauthorized access. Which approach provides a cost effective scalable mitigation to this kind of attack?
- [ ] Recommend that they lease space at a DirectConnect partner location and establish a 1G DirectConnect connection to their VPC they would then establish Internet connectivity into their space, filter the traffic in hardware Web Application Firewall (WAF). And then pass the traffic through the DirectConnect connection into their application running in their VPC. (Not cost effective)
- [ ] Add previously identified hostile source IPs as an explicit INBOUND DENY NACL to the web tier subnet. (does not protect against new source)
- [x] Add a WAF tier by creating a new ELB and an AutoScaling group of EC2 Instances running a host-based WAF. They would redirect Route 53 to resolve to the new WAF tier ELB. The WAF tier would their pass the traffic to the current web tier The web tier Security Groups would be updated to only allow traffic from the WAF tier Security Group
- [ ] Remove all but TLS 1.2 from the web tier ELB and enable Advanced Protocol Filtering This will enable the ELB itself to perform WAF functionality. (No advanced protocol filtering in ELB)

377.
Which of these Disaster Recovery options costs the least?
- [x] Pilot Light (most systems are down and brought up only after disaster)
- [ ] Fully Working Low capacity Warm standby
- [ ] Multi site Active-Active

378.
Your company currently has a 2-tier web application running in an on-premises data center. You have experienced several infrastructure failures in the past two months resulting in significant financial losses. Your CIO is strongly agreeing to move the application to AWS. While working on achieving buy-in from the other company executives, he asks you to develop a disaster recovery plan to help improve Business continuity in the short term. He specifies a target Recovery Time Objective (RTO) of 4 hours and a Recovery Point Objective (RPO) of 1 hour or less. He also asks you to implement the solution within 2 weeks. Your database is 200GB in size and you have a 20Mbps Internet connection. How would you do this while minimizing costs?
- [ ] Create an EBS backed private AMI which includes a fresh install or your application. Setup a script in your data center to backup the local database every 1 hour and to encrypt and copy the resulting file to an S3 bucket using multi-part upload (while AMI is a right approach to keep cost down, Upload to S3 very Slow)
- [ ] Install your application on a compute-optimized EC2 instance capable of supporting the application’s average load synchronously replicate transactions from your on-premises database to a database instance in AWS across a secure Direct Connect connection. (EC2 running in Compute Optimized as well as Direct Connect is expensive to start with also Direct Connect cannot be implemented in 2 weeks)
- [ ] Deploy your application on EC2 instances within an Auto Scaling group across multiple availability zones asynchronously replicate transactions from your on-premises database to a database instance in AWS across a secure VPN connection. (While VPN can be setup quickly asynchronous replication using VPN would work, running instances in DR is expensive)
- [x] Create an EBS backed private AMI that includes a fresh install of your application. Develop a Cloud Formation template which includes your AMI and the required EC2. Auto-Scaling and ELB resources to support deploying the application across Multiple Availability Zones. Asynchronously replicate transactions from your on-premises database to a database instance in AWS across a secure VPN connection. (Pilot Light approach with only DB running and replicate while you have preconfigured AMI and autoscaling config)

379.
You are designing an architecture that can recover from a disaster very quickly with minimum down time to the end users. Which of the following approaches is best?
- [ ] Leverage Route 53 health checks to automatically fail over to backup site when the primary site becomes unreachable
- [ ] Implement the Pilot Light DR architecture so that traffic can be processed seamlessly in case the primary site becomes unreachable
- [x] Implement either Fully Working Low Capacity Standby or Multi-site Active-Active architecture so that the end users will not experience any delay even if the primary site becomes unreachable
- [ ] Implement multi-region architecture to ensure high availability

380.
Your customer wishes to deploy an enterprise application to AWS that will consist of several web servers, several application servers and a small (50GB) Oracle database. Information is stored, both in the database and the file systems of the various servers. The backup system must support database recovery, whole server and whole disk restores, and individual file restores with a recovery time of no more than two hours. They have chosen to use RDS Oracle as the database. Which backup architecture will meet these requirements?
- [x] Backup RDS using automated daily DB backups. Backup the EC2 instances using AMIs and supplement with file-level backup to S3 using traditional enterprise backup software to provide file level restore (RDS automated backups with file-level backups can be used)
- [ ] Backup RDS using a Multi-AZ Deployment Backup the EC2 instances using AMIs, and supplement by copying file system data to S3 to provide file level restore (Multi-AZ is more of an Disaster recovery solution)
- [ ] Backup RDS using automated daily DB backups. Backup the EC2 instances using EBS snapshots and supplement with file-level backups to Amazon Glacier using traditional enterprise backup software to provide file level restore (Glacier not an option with the 2 hours RTO)
- [ ] Backup RDS database to S3 using Oracle RMAN. Backup the EC2 instances using AMIs, and supplement with EBS snapshots for individual volume restore. (Will use RMAN only if Database hosted on EC2 and not when using RDS)

381.
Which statements are true about the Pilot Light Disaster recovery architecture pattern?
- [ ] Pilot Light is a hot standby (Cold Standby)
- [x] Enables replication of all critical data to AWS
- [x] Very cost-effective DR pattern
- [x] Can scale the system as needed to handle current production load

382.
An ERP application is deployed across multiple AZs in a single region. In the event of failure, the Recovery Time Objective (RTO) must be less than 3 hours, and the Recovery Point Objective (RPO) must be 15 minutes. The customer realizes that data corruption occurred roughly 1.5 hours ago. What DR strategy could be used to achieve this RTO and RPO in the event of this kind of failure?
- [x] Take hourly DB backups to S3, with transaction logs stored in S3 every 5 minutes
- [ ] Use synchronous database master-slave replication between two availability zones. (Replication won’t help to backtrack and would be sync always)
- [ ] Take hourly DB backups to EC2 Instance store volumes with transaction logs stored In S3 every 5 minutes. (Instance store not a preferred storage)
- [ ] Take 15 minute DB backups stored in Glacier with transaction logs stored in S3 every 5 minutes. (Glacier does not meet the RTO)

383.
Your company’s on-premises content management system has the following architecture:
– Application Tier – Java code on a JBoss application server
– Database Tier – Oracle database regularly backed up to Amazon Simple Storage Service (S3) using the Oracle RMAN backup utility
– Static Content – stored on a 512GB gateway stored Storage Gateway volume attached to the application server via the iSCSI interfaceWhich AWS based disaster recovery strategy will give you the best RTO?
- [x] Deploy the Oracle database and the JBoss app server on EC2. Restore the RMAN Oracle backups from Amazon S3. Generate an EBS volume of static content from the Storage Gateway and attach it to the JBoss EC2 server.
- [ ] Deploy the Oracle database on RDS. Deploy the JBoss app server on EC2. Restore the RMAN Oracle backups from Amazon Glacier. Generate an EBS volume of static content from the Storage Gateway and attach it to the JBoss EC2 server. (Glacier does help to give best RTO)
- [ ] Deploy the Oracle database and the JBoss app server on EC2. Restore the RMAN Oracle backups from Amazon S3. Restore the static content by attaching an AWS Storage Gateway running on Amazon EC2 as an iSCSI volume to the JBoss EC2 server. (No need to attach the Storage Gateway as an iSCSI volume can just create a EBS volume)
- [ ] Deploy the Oracle database and the JBoss app server on EC2. Restore the RMAN Oracle backups from Amazon S3. Restore the static content from an AWS Storage Gateway-VTL running on Amazon EC2 (VTL is Virtual Tape library and doesn’t fit the RTO)

384.
What is server immutability?
- [x] Not updating a server after creation. (During the new release, a new set of EC2 instances are rolled out by terminating older instances and are disposable. EC2 instance usage is considered temporary or ephemeral in nature for the period of deployment until the current release is active)
- [ ] The ability to change server counts.
- [ ] Updating a server after creation.
- [ ] The inability to change server counts.

385.
You need to deploy a new application version to production. Because the deployment is high-risk, you need to roll the new version out to users over a number of hours, to make sure everything is working correctly. You need to be able to control the proportion of users seeing the new version of the application down to the percentage point. You use ELB and EC2 with Auto Scaling Groups and custom AMIs with your code pre-installed assigned to Launch Configurations. There are no database-level changes during your deployment. You have been told you cannot spend too much money, so you must not increase the number of EC2 instances much at all during the deployment, but you also need to be able to switch back to the original version of code quickly if something goes wrong. What is the best way to meet these requirements?
- [ ] Create a second ELB, Auto Scaling Launch Configuration, and Auto Scaling Group using the Launch Configuration. Create AMIs with all code pre-installed. Assign the new AMI to the second Auto Scaling Launch Configuration. Use Route53 Weighted Round Robin Records to adjust the proportion of traffic hitting the two ELBs. (Use Weighted Round Robin DNS Records and reverse proxies allow such fine-grained tuning of traffic splits. Blue-Green option does not meet the requirement that we mitigate costs and keep overall EC2 fleet size consistent, so we must select the 2 ELB and ASG option with WRR DNS tuning)
- [ ] Use the Blue-Green deployment method to enable the fastest possible rollback if needed. Create a full second stack of instances and cut the DNS over to the new stack of instances, and change the DNS back if a rollback is needed. (Full second stack is expensive)
- [ ] Create AMIs with all code pre-installed. Assign the new AMI to the Auto Scaling Launch Configuration, to replace the old one. Gradually terminate instances running the old code (launched with the old Launch Configuration) and allow the new AMIs to boot to adjust the traffic balance to the new code. On rollback, reverse the process by doing the same thing, but changing the AMI on the Launch Config back to the original code. (Cannot modify the existing launch config)
- [ ] Migrate to use AWS Elastic Beanstalk. Use the established and well-tested Rolling Deployment setting AWS provides on the new Application Environment, publishing a zip bundle of the new code and adjusting the wait period to spread the deployment over time. Re-deploy the old code bundle to rollback if needed.

386.
When thinking of AWS Elastic Beanstalk, the ‘Swap Environment URLs’ feature most directly aids in what?
- [ ] Immutable Rolling Deployments
- [ ] Mutable Rolling Deployments
- [ ] Canary Deployments
- [x] Blue-Green Deployments (Complete switch from one environment to other)

387.
You were just hired as a DevOps Engineer for a startup. Your startup uses AWS for 100% of their infrastructure. They currently have no automation at all for deployment, and they have had many failures while trying to deploy to production. The company has told you deployment process risk mitigation is the most important thing now, and you have a lot of budget for tools and AWS resources. Their stack: 2-tier API Data stored in DynamoDB or S3, depending on type, Compute layer is EC2 in Auto Scaling Groups, They use Route53 for DNS pointing to an ELB, An ELB balances load across the EC2 instances. The scaling group properly varies between 4 and 12 EC2 servers. Which of the following approaches, given this company’s stack and their priorities, best meets the company’s needs?
- [ ] Model the stack in AWS Elastic Beanstalk as a single Application with multiple Environments. Use Elastic Beanstalk’s Rolling Deploy option to progressively roll out application code changes when promoting across environments. (Does not support DynamoDB also need Blue Green deployment for zero downtime deployment as cost is not a constraint)
- [x] Model the stack in 3 CloudFormation templates: Data layer, compute layer, and networking layer. Write stack deployment and integration testing automation following Blue-Green methodologies.
- [ ] Model the stack in AWS OpsWorks as a single Stack, with 1 compute layer and its associated ELB. Use Chef and App Deployments to automate Rolling Deployment. (Does not support DynamoDB also need Blue Green deployment for zero downtime deployment as cost is not a constraint)
- [ ] Model the stack in 1 CloudFormation template, to ensure consistency and dependency graph resolution. Write deployment and integration testing automation following Rolling Deployment methodologies. (Need Blue Green deployment for zero downtime deployment as cost is not a constraint)

388.
You are building out a layer in a software stack on AWS that needs to be able to scale out to react to increased demand as fast as possible. You are running the code on EC2 instances in an Auto Scaling Group behind an ELB. Which application code deployment method should you use?
- [ ] SSH into new instances those come online, and deploy new code onto the system by pulling it from an S3 bucket, which is populated by code that you refresh from source control on new pushes. (is slow and manual)
- [x] Bake an AMI when deploying new versions of code, and use that AMI for the Auto Scaling Launch Configuration. (Pre baked AMIs can help to get started quickly)
- [ ] Create a Dockerfile when preparing to deploy a new version to production and publish it to S3. Use UserData in the Auto Scaling Launch configuration to pull down the Dockerfile from S3 and run it when new instances launch. (is slow)
- [ ] Create a new Auto Scaling Launch Configuration with UserData scripts configured to pull the latest code at all times. (is slow)

389.
You company runs a complex customer relations management system that consists of around 10 different software components all backed by the same Amazon Relational Database (RDS) database. You adopted AWS OpsWorks to simplify management and deployment of that application and created an AWS OpsWorks stack with layers for each of the individual components. An internal security policy requires that all instances should run on the latest Amazon Linux AMI and that instances must be replaced within one month after the latest Amazon Linux AMI has been released. AMI replacements should be done without incurring application downtime or capacity problems. You decide to write a script to be run as soon as a new Amazon Linux AMI is released. Which solutions support the security policy and meet your requirements? Choose 2 answers
- [ ] Assign a custom recipe to each layer, which replaces the underlying AMI. Use AWS OpsWorks life-cycle events to incrementally execute this custom recipe and update the instances with the new AMI.
- [x] Create a new stack and layers with identical configuration, add instances with the latest Amazon Linux AMI specified as a custom AMI to the new layer, switch DNS to the new stack, and tear down the old stack. (Blue-Green Deployment)
- [ ] Identify all Amazon Elastic Compute Cloud (EC2) instances of your AWS OpsWorks stack, stop each instance, replace the AMI ID property with the ID of the latest Amazon Linux AMI ID, and restart the instance. To avoid downtime, make sure not more than one instance is stopped at the same time.
- [ ] Specify the latest Amazon Linux AMI as a custom AMI at the stack level, terminate instances of the stack and let AWS OpsWorks launch new instances with the new AMI.
- [x] Add new instances with the latest Amazon Linux AMI specified as a custom AMI to all AWS OpsWorks layers of your stack, and terminate the old ones.

390.
Your company runs an event management SaaS application that uses Amazon EC2, Auto Scaling, Elastic Load Balancing, and Amazon RDS. Your software is installed on instances at first boot, using a tool such as Puppet or Chef, which you also use to deploy small software updates multiple times per week. After a major overhaul of your software, you roll out version 2.0 new, much larger version of the software of your running instances. Some of the instances are terminated during the update process. What actions could you take to prevent instances from being terminated in the future? (Choose two)
- [ ] Use the zero downtime feature of Elastic Beanstalk to deploy new software releases to your existing instances. (No such feature, you can perform environment url swap)
- [x] Use AWS CodeDeploy. Create an application and a deployment targeting the Auto Scaling group. Use CodeDeploy to deploy and update the application in the future. (Refer link)
- [x] Run “aws autoscaling suspend-processes” before updating your application. (Refer link)
- [ ] Use the AWS Console to enable termination protection for the current instances. (Termination protection does not work with Auto Scaling)
- [ ] Run “aws autoscaling detach-load-balancers” before updating your application. (Does not prevent Auto Scaling to terminate the instances)

391.
When preparing for a compliance assessment of your system built inside of AWS. What are three best practices for you to prepare for an audit? Choose 3 answers
- [x] Gather evidence of your IT operational controls (Customer still needs to gather all the IT operation controls inline with their environment)
- [x] Request and obtain applicable third-party audited AWS compliance reports and certifications (Customers can request the reports and certifications produced by our third-party auditors or can request more information about AWS Compliance)
- [ ] Request and obtain a compliance and security tour of an AWS data center for a pre-assessment security review (AWS does not allow data center tour)
- [x] Request and obtain approval from AWS to perform relevant network scans and in-depth penetration tests of your system’s Instances and endpoints (AWS requires prior approval to be taken to perform penetration tests)
- [ ] Schedule meetings with AWS’s third-party auditors to provide evidence of AWS compliance that maps to your control objectives (Customers can request the reports and certifications produced by our third-party auditors or can request more information about AWS Compliance)

392.
In the shared security model, AWS is responsible for which of the following security best practices (check all that apply) :
- [x] Penetration testing
- [ ] Operating system account security management
- [x] Threat modeling
- [ ] User group access management
- [x] Static code analysis

393.
You are running a web-application on AWS consisting of the following components an Elastic Load Balancer (ELB) an Auto-Scaling Group of EC2 instances running Linux/PHP/Apache, and Relational DataBase Service (RDS) MySQL. Which security measures fall into AWS’s responsibility?
- [ ] Protect the EC2 instances against unsolicited access by enforcing the principle of least-privilege access (Customer owned)
- [x] Protect against IP spoofing or packet sniffing
- [ ] Assure all communication between EC2 instances and ELB is encrypted (Customer owned)
- [ ] Install latest security patches on ELB, RDS and EC2 instances (Customer owned)

394.
Which of the following statements is true about achieving PCI certification on the AWS platform? (Choose 2)
- [x] Your organization owns the compliance initiatives related to anything placed on the AWS infrastructure
- [ ] Amazon EC2 instances must run on a single-tenancy environment (dedicated instance)
- [ ] AWS manages card-holder environments
- [x] AWS Compliance provides assurance related to the underlying infrastructure

394.
A photo-sharing service stores pictures in Amazon Simple Storage Service (S3) and allows application sign-in using an OpenID Connect-compatible identity provider. Which AWS Security Token Service approach to temporary access should you use for the Amazon S3 operations?
- [ ] SAML-based Identity Federation
- [ ] Cross-Account Access
- [ ] AWS IAM users
- [x] Web Identity Federation

395.
Which technique can be used to integrate AWS IAM (Identity and Access Management) with an on-premise LDAP (Lightweight Directory Access Protocol) directory service?
- [ ] Use an IAM policy that references the LDAP account identifiers and the AWS credentials.
- [ ] Use SAML (Security Assertion Markup Language) to enable single sign-on between AWS and LDAP
- [x] Use AWS Security Token Service from an identity broker to issue short-lived AWS credentials. (Refer Link)
- [ ] Use IAM roles to automatically rotate the IAM credentials when LDAP credentials are updated.
- [ ] Use the LDAP credentials to restrict a group of users from launching specific EC2 instance types.

396.
A user has created a mobile application which makes calls to DynamoDB to fetch certain data. The application is using the DynamoDB SDK and root account access/secret access key to connect to DynamoDB from mobile. Which of the below mentioned statements is true with respect to the best practice for security in this scenario?
- [ ] User should create a separate IAM user for each mobile application and provide DynamoDB access with it
- [ ] User should create an IAM role with DynamoDB and EC2 access. Attach the role with EC2 and route all calls from the mobile through EC2
- [x] The application should use an IAM role with web identity federation which validates calls to DynamoDB with identity providers, such as Google, Amazon, and Facebook
- [ ] Create an IAM Role with DynamoDB access and attach it with the mobile application

397.
You are managing the AWS account of a big organization. The organization has more than 1000+ employees and they want to provide access to the various services to most of the employees. Which of the below mentioned options is the best possible solution in this case?
- [ ] The user should create a separate IAM user for each employee and provide access to them as per the policy
- [ ] The user should create an IAM role and attach STS with the role. The user should attach that role to the EC2 instance and setup AWS authentication on that server
- [ ] The user should create IAM groups as per the organization’s departments and add each user to the group for better access control
- [x] Attach an IAM role with the organization’s authentication service to authorize each user for various AWS services

398.
What is web identity federation?
- [ ] Use of an identity provider like Google or Facebook to become an AWS IAM User.
- [x] Use of an identity provider like Google or Facebook to exchange for temporary AWS security credentials.
- [ ] Use of AWS IAM User tokens to log in as a Google or Facebook user.
- [ ] Use of AWS STS Tokens to log in as a Google or Facebook user.

399.
Games-R-Us is launching a new game app for mobile devices. Users will log into the game using their existing Facebook account and the game will record player data and scoring information directly to a DynamoDB table. What is the most secure approach for signing requests to the DynamoDB API?
- [ ] Create an IAM user with access credentials that are distributed with the mobile app to sign the requests
- [ ] Distribute the AWS root account access credentials with the mobile app to sign the requests
- [x] Request temporary security credentials using web identity federation to sign the requests
- [ ] Establish cross account access between the mobile app and the DynamoDB table to sign the requests

400.
You are building a mobile app for consumers to post cat pictures online. You will be storing the images in AWS S3. You want to run the system very cheaply and simply. Which one of these options allows you to build a photo sharing application without needing to worry about scaling expensive uploads processes, authentication/authorization and so forth?
- [x] Build the application out using AWS Cognito and web identity federation to allow users to log in using Facebook or Google Accounts. Once they are logged in, the secret token passed to that user is used to directly access resources on AWS, like AWS S3. (Amazon Cognito is a superset of the functionality provided by web identity federation. Refer link)
- [ ] Use JWT or SAML compliant systems to build authorization policies. Users log in with a username and password, and are given a token they can use indefinitely to make calls against the photo infrastructure.
- [ ] Use AWS API Gateway with a constantly rotating API Key to allow access from the client-side. Construct a custom build of the SDK and include S3 access in it.
- [ ] Create an AWS oAuth Service Domain ad grant public signup and access to the domain. - [ ] During setup, add at least one major social media site as a trusted Identity Provider for users.
