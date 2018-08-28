## AWS CSA Associate 模拟题11

715.
An organization is planning to create 5 different AWS accounts considering various security requirements. The organization wants to use a single payee account by using the consolidated billing option. Which of the below mentioned statements is true with respect to the above information?
- [ ] Master (Payee) account will get only the total bill and cannot see the cost incurred by each account
- [x] Master (Payee) account can view only the AWS billing details of the linked accounts
- [ ] It is not recommended to use consolidated billing since the payee account will have access to the linked accounts
- [ ] Each AWS account needs to create an AWS billing policy to provide permission to the payee account

716.*
An organization has setup consolidated billing with 3 different AWS accounts. Which of the below mentioned advantages will organization receive in terms of the AWS pricing?
- [ ] The consolidated billing does not bring any cost advantage for the organization
- [x] All AWS accounts will be charged for S3 storage by combining the total storage of each account
- [ ] EC2 instances of each account will receive a total of 750*3 micro instance hours free
- [ ] The free usage tier for all the 3 accounts will be 3 years and not a single year

717.
An organization has added 3 of his AWS accounts to consolidated billing. One of the AWS accounts has purchased a Reserved Instance (RI) of a small instance size in the us-east-1a zone. All other AWS accounts are running instances of a small size in the same zone. What will happen in this case for the RI pricing?
- [ ] Only the account that has purchased the RI will get the advantage of RI pricing
- [ ] One instance of a small size and running in the us-east-1a zone of each AWS account will get the benefit of RI pricing
- [x] Any single instance from all the three accounts can get the benefit of AWS RI pricing if they are running in the same zone and are of the same size
- [ ] If there are more than one instances of a small size running across multiple accounts in the same zone no one will get the benefit of RI

718.
An organization is planning to use AWS for 5 different departments. The finance department is responsible to pay for all the accounts. However, they want the cost separation for each account to map with the right cost centre. How can the finance department achieve this?
- [x] Create 5 separate accounts and make them a part of one consolidated billing
- [ ] Create 5 separate accounts and use the IAM cross account access with the roles for better management
- [ ] Create 5 separate IAM users and set a different policy for their access
- [ ] Create 5 separate IAM groups and add users as per the department’s employees

719.
An AWS account wants to be part of the consolidated billing of his organization’s payee account. How can the owner of that account achieve this?
- [ ] The payee account has to request AWS support to link the other accounts with his account
- [ ] The owner of the linked account should add the payee account to his master account list from the billing console
- [x] The payee account will send a request to the linked account to be a part of consolidated billing (Check Process)
- [ ] The owner of the linked account requests the payee account to add his account to consolidated billing

720.*
You are looking to migrate your Development (Dev) and Test environments to AWS. You have decided to use separate AWS accounts to host each environment. You plan to link each accounts bill to a Master AWS account using Consolidated Billing. To make sure you keep within budget you would like to implement a way for administrators in the Master account to have access to stop, delete and/or terminate resources in both the Dev and Test accounts. Identify which option will allow you to achieve this goal.
- [ ] Create IAM users in the Master account with full Admin permissions. Create cross-account roles in the Dev and Test accounts that grant the Master account access to the resources in the account by inheriting permissions from the Master account.
- [ ] Create IAM users and a cross-account role in the Master account that grants full Admin permissions to the Dev and Test accounts.
- [x] Create IAM users in the Master account. Create cross-account roles in the Dev and Test accounts that have full Admin permissions and grant the Master account access.
- [ ] Link the accounts using Consolidated Billing. This will give IAM users in the Master account access to resources in the Dev and Test accounts

721.
When using consolidated billing there are two account types. What are they?
- [x] Paying account and Linked account
- [ ] Parent account and Child account
- [ ] Main account and Sub account.
- [ ] Main account and Secondary account.

722.
A customer needs corporate IT governance and cost oversight of all AWS resources consumed by its divisions. The divisions want to maintain administrative control of the discrete AWS resources they consume and keep those resources separate from the resources of other divisions. Which of the following options, when used together will support the autonomy/control of divisions while enabling corporate IT to maintain governance and cost oversight? Choose 2 answers
- [ ] Use AWS Consolidated Billing and disable AWS root account access for the child accounts. (Need to link accounts and disabling root access is just a best practice)
- [x] Enable IAM cross-account access for all corporate IT administrators in each child account. (Provides IT goverance)
- [ ] Create separate VPCs for each division within the corporate IT AWS account.
- [x] Use AWS Consolidated Billing to link the divisions’ accounts to a parent corporate account (Will provide cost oversight)
- [ ] Write all child AWS CloudTrail and Amazon CloudWatch logs to each child account’s Amazon S3 ‘Log’ bucket (Preferred approach would be to store logs from multiple accounts to a single S3 bucket with CloudTrail for IT Goverance and CloudWatch alerts for Cost Oversight)

723.
An organization has 10 departments. The organization wants to track the AWS usage of each department. Which of the below mentioned options meets the requirement?
- [ ] Setup IAM groups for each department and track their usage
- [x] Create separate accounts for each department, but use consolidated billing for payment and tracking
- [ ] Create separate accounts for each department and track them separately
- [ ] Setup IAM users for each department and track their usage

724.*
You have deployed a web application targeting a global audience across multiple AWS Regions under the domain name example.com. You decide to use Route 53 Latency-Based Routing to serve web requests to users from the region closest to the user. To provide business continuity in the event of server downtime you configure weighted record sets associated with two web servers in separate Availability Zones per region. During a DR test you notice that when you disable all web servers in one of the regions Route 53 does not automatically direct all users to the other region. What could be happening? (Choose 2 answers)
- [ ] Latency resource record sets cannot be used in combination with weighted resource record sets.
- [x] You did not setup an http health check for one or more of the weighted resource record sets associated with the disabled web servers
- [ ] The value of the weight associated with the latency alias resource record set in the region with the disabled servers is higher than the weight for the other region.
- [ ] One of the two working web servers in the other region did not pass its HTTP health check
- [x] You did not set “Evaluate Target Health” to “Yes” on the latency alias resource record set associated with example.com in the region where you disabled the servers.

725.
The compliance department within your multi-national organization requires that all data for your customers that reside in the European Union (EU) must not leave the EU and also data for customers that reside in the US must not leave the US without explicit authorization. What must you do to comply with this requirement for a web based profile management application running on EC2?
- [ ] Run EC2 instances in multiple AWS Availability Zones in single Region and leverage an Elastic Load Balancer with session stickiness to route traffic to the appropriate zone to create their profile (should be in 2 different regions – US and Europe)
- [ ] Run EC2 instances in multiple Regions and leverage Route 53’s Latency Based Routing capabilities to route traffic to the appropriate region to create their profile (Latency based routing policy would not guarantee the compliance requirement)
- [x] Run EC2 instances in multiple Regions and leverage a third party data provider to determine if a user needs to be redirect to the appropriate region to create their profile
- [ ] Run EC2 instances in multiple AWS Availability Zones in a single Region and leverage a third party data provider to determine if a user needs to be redirect to the appropriate zone to create their profile(should be in 2 different regions – US and Europe)

726.
A US-based company is expanding their web presence into Europe. The company wants to extend their AWS infrastructure from Northern Virginia (us-east-1) into the Dublin (eu-west-1) region. Which of the following options would enable an equivalent experience for users on both continents?
- [ ] Use a public-facing load balancer per region to load-balance web traffic, and enable HTTP health checks.
- [ ] Use a public-facing load balancer per region to load-balance web traffic, and enable sticky sessions.
- [x] Use Amazon Route 53, and apply a geolocation routing policy to distribute traffic across both regions
- [ ] Use Amazon Route 53, and apply a weighted routing policy to distribute traffic across both regions.

727.
You have been asked to propose a multi-region deployment of a web-facing application where a controlled portion of your traffic is being processed by an alternate region. Which configuration would achieve that goal?
- [x] Route 53 record sets with weighted routing policy
- [ ] Route 53 record sets with latency based routing policy
- [ ] Auto Scaling with scheduled scaling actions set
- [ ] Elastic Load Balancing with health checks enabled

728.
Your company is moving towards tracking web page users with a small tracking image loaded on each page. Currently you are serving this image out of us-east, but are starting to get concerned about the time it takes to load the image for users on the west coast. What are the two best ways to speed up serving this image? Choose 2 answers
- [x] Use Route 53’s Latency Based Routing and serve the image out of us-west-2 as well as us-east-1
- [x] Serve the image out through CloudFront
- [ ] Serve the image out of S3 so that it isn’t being served of your web application tier
- [ ] Use EBS PIOPs to serve the image faster out of your EC2 instances

729.
Your API requires the ability to stay online during AWS regional failures. Your API does not store any state, it only aggregates data from other sources – you do not have a database. What is a simple but effective way to achieve this uptime goal?
- [ ] Use a CloudFront distribution to serve up your API. Even if the region your API is in goes down, the edge locations CloudFront uses will be fine.
- [ ] Use an ELB and a cross-zone ELB deployment to create redundancy across datacenters. Even if a region fails, the other AZ will stay online.
- [ ] Create a Route53 Weighted Round Robin record, and if one region goes down, have that region redirect to the other region.
- [x] Create a Route53 Latency Based Routing Record with Failover and point it to two identical deployments of your stateless API in two different regions. Make sure both regions use Auto Scaling Groups behind ELBs. (Refer link)

730.
What is the minimum time Interval for the data that Amazon CloudWatch receives and aggregates?
- [ ] One second
- [ ] Five seconds
- [x] One minute
- [ ] Three minutes
- [ ] Five minutes

731.
In the ‘Detailed’ monitoring data available for your Amazon EBS volumes, Provisioned IOPS volumes automatically send _____ minute metrics to Amazon CloudWatch.
- [ ] 3
- [x] 1
- [ ] 5
- [ ] 2

732.
Using Amazon CloudWatch’s Free Tier, what is the frequency of metric updates, which you receive?
- [x] 5 minutes
- [ ] 500 milliseconds.
- [ ] 30 seconds
- [ ] 1 minute

733.
What is the type of monitoring data (for Amazon EBS volumes) which is available automatically in 5-minute periods at no charge called?
- [x] Basic
- [ ] Primary
- [ ] Detailed
- [ ] Local

734.
A user has created an Auto Scaling group using CLI. The user wants to enable CloudWatch detailed monitoring for that group. How can the user configure this?
- [ ] When the user sets an alarm on the Auto Scaling group, it automatically enables detail monitoring
- [x] By default detailed monitoring is enabled for Auto Scaling (Detailed monitoring is enabled when you create the launch configuration using the AWS CLI or an API)
- [ ] Auto Scaling does not support detailed monitoring
- [ ] Enable detail monitoring from the AWS console

735.
A user is trying to understand the detailed CloudWatch monitoring concept. Which of the below mentioned services provides detailed monitoring with CloudWatch without charging the user extra?
- [ ] AWS Auto Scaling
- [x] AWS Route 53
- [ ] AWS EMR
- [ ] AWS SNS

736.
A user is trying to understand the detailed CloudWatch monitoring concept. Which of the below mentioned services does not provide detailed monitoring with CloudWatch?
- [x] AWS EMR
- [ ] AWS RDS
- [ ] AWS ELB
- [ ] AWS Route53

737.
A user has enabled detailed CloudWatch monitoring with the AWS Simple Notification Service. Which of the below mentioned statements helps the user understand detailed monitoring better?
- [ ] SNS will send data every minute after configuration
- [ ] There is no need to enable since SNS provides data every minute
- [ ] AWS CloudWatch does not support monitoring for SNS
- [x] SNS cannot provide data every minute

738.
A user has configured an Auto Scaling group with ELB. The user has enabled detailed CloudWatch monitoring on Auto Scaling. Which of the below mentioned statements will help the user understand the functionality better?
- [ ] It is not possible to setup detailed monitoring for Auto Scaling
- [x] In this case, Auto Scaling will send data every minute and will charge the user extra
- [ ] Detailed monitoring will send data every minute without additional charges
- [ ] Auto Scaling sends data every minute only and does not charge the user

739.
Which of the following notification endpoints or clients does Amazon Simple Notification Service support? Choose 2 answers
- [x] Email
- [ ] CloudFront distribution
- [ ] File Transfer Protocol
- [x] Short Message Service
- [ ] Simple Network Management Protocol

740.
What happens when you create a topic on Amazon SNS?
- [ ] The topic is created, and it has the name you specified for it.
- [x] An ARN (Amazon Resource Name) is created
- [ ] You can create a topic on Amazon SQS, not on Amazon SNS.
- [ ] This question doesn’t make sense.

741.
A user has deployed an application on his private cloud. The user is using his own monitoring tool. He wants to configure that whenever there is an error, the monitoring tool should notify him via SMS. Which of the below mentioned AWS services will help in this scenario?
- [ ] None because the user infrastructure is in the private cloud/
- [x] AWS SNS
- [ ] AWS SES
- [ ] AWS SMS

742.
A user wants to make so that whenever the CPU utilization of the AWS EC2 instance is above 90%, the redlight of his bedroom turns on. Which of the below mentioned AWS services is helpful for this purpose?
- [ ] AWS CloudWatch + AWS SES
- [x] AWS CloudWatch + AWS SNS
- [ ] It is not possible to configure the light with the AWS infrastructure services
- [ ] AWS CloudWatch and a dedicated software turning on the light

743.
A user is trying to understand AWS SNS. To which of the below mentioned end points is SNS unable to send a notification?
- [ ] Email JSON
- [ ] HTTP
- [ ] AWS SQS
- [x] AWS SES

744.
A user is running a webserver on EC2. The user wants to receive the SMS when the EC2 instance utilization is above the threshold limit. Which AWS services should the user configure in this case?
- [ ] AWS CloudWatch + AWS SES
- [x] AWS CloudWatch + AWS SNS
- [ ] AWS CloudWatch + AWS SQS
- [ ] AWS EC2 + AWS CloudWatch

745.
A user is planning to host a mobile game on EC2 which sends notifications to active users on either high score or the addition of new features. The user should get this notification when he is online on his mobile device. Which of the below mentioned AWS services can help achieve this functionality?
- [x] AWS Simple Notification Service
- [ ] AWS Simple Queue Service
- [ ] AWS Mobile Communication Service
- [ ] AWS Simple Email Service

746.*
You are providing AWS consulting service for a company developing a new mobile application that will be leveraging amazon SNS push for push notifications. In order to send direct notification messages to individual devices each device registration identifier or token needs to be registered with SNS, however the developers are not sure of the best way to do this. You advise them to: –
- [ ] Bulk upload the device tokens contained in a CSV file via the AWS Management Console
- [ ] Let the push notification service (e.g. Amazon Device messaging) handle the registration
- [ ] Implement a token vending service to handle the registration
- [x] Call the CreatePlatformEndpoint API function to register multiple device tokens. (Refer documentation)

747.
A company is running a batch analysis every hour on their main transactional DB running on an RDS MySQL instance to populate their central Data Warehouse running on Redshift. During the execution of the batch their transactional applications are very slow. When the batch completes they need to update the top management dashboard with the new data. The dashboard is produced by another system running on-premises that is currently started when a manually-sent email notifies that an update is required The on-premises system cannot be modified because is managed by another team. How would you optimize this scenario to solve performance issues and automate the process as much as possible?
- [ ] Replace RDS with Redshift for the batch analysis and SNS to notify the on-premises system to update the dashboard
- [ ] Replace RDS with Redshift for the batch analysis and SQS to send a message to the on-premises system to update the dashboard
- [x] Create an RDS Read Replica for the batch analysis and SNS to notify me on-premises system to update the dashboard
- [ ] Create an RDS Read Replica for the batch analysis and SQS to send a message to the on-premises system to update the dashboard.

748.
Which of the following are valid SNS delivery transports? Choose 2 answers.
- [x] HTTP
- [ ] UDP
- [x] SMS
- [ ] DynamoDB
- [ ] Named Pipes

749.
What is the format of structured notification messages sent by Amazon SNS?
- [ ] An XML object containing MessageId, UnsubscribeURL, Subject, Message and other values
- [ ] An JSON object containing MessageId, DuplicateFlag, Message and other values
- [ ] An XML object containing MessageId, DuplicateFlag, Message and other values
- [x] An JSON object containing MessageId, unsubscribeURL, Subject, Message and other values

750.
Which of the following are valid arguments for an SNS Publish request? Choose 3 answers.
- [x] TopicAm
- [x] Subject
- [ ] Destination
- [ ] Format
- [x] Message
- [ ] Language

751.
EC2 EBS-backed (EBS root) instance is stopped, what happens to the data on any ephemeral store volumes?
- [ ] Data is automatically saved in an EBS volume.
- [ ] Data is unavailable until the instance is restarted.
- [x] Data will be deleted and will no longer be accessible.
- [ ] Data is automatically saved as an EBS snapshot.

752.
When an EC2 instance that is backed by an S3-based AMI is terminated, what happens to the data on the root volume?
- [ ] Data is automatically saved as an EBS snapshot.
- [ ] Data is automatically saved as an EBS volume.
- [ ] Data is unavailable until the instance is restarted.
- [x] Data is automatically deleted.

753.
 Which of the following will occur when an EC2 instance in a VPC (Virtual Private Cloud) with an associated Elastic IP is stopped and started? (Choose 2 answers)
- [ ] The Elastic IP will be dissociated from the instance
- [x] All data on instance-store devices will be lost
- [ ] All data on EBS (Elastic Block Store) devices will be lost
- [ ] The ENI (Elastic Network Interface) is detached
- [x] The underlying host for the instance is changed

754.
Which of the following provides the fastest storage medium?
- [ ] Amazon S3
- [ ] Amazon EBS using Provisioned IOPS (PIOPS)
- [x] SSD Instance (ephemeral) store (SSD Instance Storage provides 100,000 IOPS on some instance types, much faster than any network-attached storage)
- [ ] AWS Storage Gateway

755.
A web company is looking to implement an intrusion detection and prevention system into their deployed VPC. This platform should have the ability to scale to thousands of instances running inside of the VPC. How should they architect their solution to achieve these goals?
- [ ] Configure an instance with monitoring software and the elastic network interface (ENI) set to promiscuous mode packet sniffing to see an traffic across the VPC. (virtual instance running in promiscuous mode to receive or“sniff” traffic)
- [ ] Create a second VPC and route all traffic from the primary application VPC through the second VPC where the scalable virtualized IDS/IPS platform resides.
- [ ] Configure servers running in the VPC using the host-based ‘route’ commands to send all traffic through the platform to a scalable virtualized IDS/IPS (host based routing is not allowed)
- [x] Configure each host with an agent that collects all network traffic and sends that traffic to the IDS/IPS platform for inspection.

756.*
You are designing an intrusion detection prevention (IDS/IPS) solution for a customer web application in a single VPC. You are considering the options for implementing IDS/IPS protection for traffic coming from the Internet. Which of the following options would you consider? (Choose 2 answers)
- [x] Implement IDS/IPS agents on each Instance running In VPC
- [ ] Configure an instance in each subnet to switch its network interface card to promiscuous mode and analyze network traffic. (virtual instance running in promiscuous mode to receive or“sniff” traffic)
- [ ] Implement Elastic Load Balancing with SSL listeners In front of the web applications (ELB with SSL does not serve as IDS/IPS)
- [x] Implement a reverse proxy layer in front of web servers and configure IDS/IPS agents on each reverse proxy server

757.
A company is building a two-tier web application to serve dynamic transaction-based content. The data tier is leveraging an Online Transactional Processing (OLTP) database. What services should you leverage to enable an elastic and scalable web tier?
- [x] Elastic Load Balancing, Amazon EC2, and Auto Scaling
- [ ] Elastic Load Balancing, Amazon RDS with Multi-AZ, and Amazon S3
- [ ] Amazon RDS with Multi-AZ and Auto Scaling
- [ ] Amazon EC2, Amazon DynamoDB, and Amazon S3

758.
You have been given a scope to deploy some AWS infrastructure for a large organization. The requirements are that you will have a lot of EC2 instances but may need to add more when the average utilization of your Amazon EC2 fleet is high and conversely remove them when CPU utilization is low. Which AWS services would be best to use to accomplish this?
- [ ] Amazon CloudFront, Amazon CloudWatch and Elastic Load Balancing
- [ ] Auto Scaling, Amazon CloudWatch and AWS CloudTrail
- [x] Auto Scaling, Amazon CloudWatch and Elastic Load Balancing
- [ ] Auto Scaling, Amazon CloudWatch and AWS Elastic Beanstalk

759.
A user has configured ELB with Auto Scaling. The user suspended the Auto Scaling AddToLoadBalancer, which adds instances to the load balancer. process for a while. What will happen to the instances launched during the suspension period?
- [x] The instances will not be registered with ELB and the user has to manually register when the process is resumed
- [ ] The instances will be registered with ELB only once the process has resumed
- [ ] Auto Scaling will not launch the instance during this period due to process suspension
- [ ] It is not possible to suspend only the AddToLoadBalancer process

760.
You have an Auto Scaling group associated with an Elastic Load Balancer (ELB). You have noticed that instances launched via the Auto Scaling group are being marked unhealthy due to an ELB health check, but these unhealthy instances are not being terminated. What do you need to do to ensure trial instances marked unhealthy by the ELB will be terminated and replaced?
- [ ] Change the thresholds set on the Auto Scaling group health check
- [x] Add an Elastic Load Balancing health check to your Auto Scaling group
- [ ] Increase the value for the Health check interval set on the Elastic Load Balancer
- [ ] Change the health check set on the Elastic Load Balancer to use TCP rather than HTTP checks

761.
What is the order of most-to-least rapidly-scaling (fastest to scale first)? A) EC2 + ELB + Auto Scaling B) Lambda C) RDS
- [x] B, A, C (Lambda is designed to scale instantly. EC2 + ELB + Auto Scaling require single-digit minutes to scale out. RDS will take at least 15 minutes, and will apply OS patches or any other updates when applied.)
- [ ] C, B, A
- [ ] C, A, B
- [ ] A, C, B

762.*
A user has hosted an application on EC2 instances. The EC2 instances are configured with ELB and Auto Scaling. The application server session time out is 2 hours. The user wants to configure connection draining to ensure that all in-flight requests are supported by ELB even though the instance is being deregistered. What time out period should the user specify for connection draining?
- [ ] 5 minutes
- [x] 1 hour (max allowed is 3600 secs that is close to 2 hours to keep the in flight requests alive)
- [ ] 30 minutes
- [ ] 2 hours

763.
Your company Is moving towards tracking web page users with a small tracking Image loaded on each page Currently you are serving this image out of US-East, but are starting to get concerned about the time It takes to load the image for users on the west coast. What are the two best ways to speed up serving this image? Choose 2 answers
- [x] Use Route 53’s Latency Based Routing and serve the image out of US-West-2 as well as US-East-1
- [x] Serve the image out through CloudFront
- [ ] Serve the image out of S3 so that it isn’t being served oft of your web application tier
- [ ] Use EBS PIOPs to serve the image faster out of your EC2 instances

764.
An organization is planning to use AWS for their production roll out. The organization wants to implement automation for deployment such that it will automatically create a LAMP stack, download the latest PHP installable from S3 and setup the ELB. Which of the below mentioned AWS services meets the requirement for making an orderly deployment of the software?
- [x] AWS Elastic Beanstalk
- [ ] AWS CloudFront
- [ ] AWS CloudFormation
- [ ] AWS DevOps

765.
What does Amazon Elastic Beanstalk provide?
- [ ] A scalable storage appliance on top of Amazon Web Services.
- [x] An application container on top of Amazon Web Services
- [ ] A service by this name doesn’t exist.
- [ ] A scalable cluster of EC2 instances

766.
You want to have multiple versions of your application running at the same time, with all versions launched via AWS Elastic Beanstalk. Is this possible?
- [ ] However if you have 2 AWS accounts this can be done
- [ ] AWS Elastic Beanstalk is not designed to support multiple running environments
- [x] AWS Elastic Beanstalk is designed to support a number of multiple running environments
- [ ] However AWS Elastic Beanstalk is designed to support only 2 multiple running environments

767.
A .NET application that you manage is running in Elastic Beanstalk. Your developers tell you they will need access to application log files to debug issues that arise. The infrastructure will scale up and down. How can you ensure the developers will be able to access only the log files?
- [ ] Access the log files directly from Elastic Beanstalk
- [x] Enable log file rotation to S3 within the Elastic Beanstalk configuration
- [ ] Ask your developers to enable log file rotation in the applications web.config file
- [ ] Connect to each Instance launched by Elastic Beanstalk and create a Windows Scheduled task to rotate the log files to S3

768.
Which of the following groups is AWS Elastic Beanstalk best suited for?
- [x] Those who want to deploy and manage their applications within minutes in the AWS cloud.
- [ ] Those who want to privately store and manage Git repositories in the AWS cloud.
- [ ] Those who want to automate the deployment of applications to instances and to update the applications as required.
- [ ] Those who want to model, visualize, and automate the steps required to release software.

769.
When thinking of AWS Elastic Beanstalk’s model, which is true?
- [ ] Applications have many deployments, deployments have many environments.
- [ ] Environments have many applications, applications have many deployments.
- [x] Applications have many environments, environments have many deployments. (Applications group logical services. Environments belong to Applications, and typically represent different deployment levels (dev, stage, prod, forth). Deployments belong to environments, and are pushes of bundles of code for the environments to run.)
- [ ] Deployments have many environments, environments have many applications.

770.
If you’re trying to configure an AWS Elastic Beanstalk worker tier for easy debugging if there are problems finishing queue jobs, what should you configure?
- [ ] Configure Rolling Deployments.
- [ ] Configure Enhanced Health Reporting
- [ ] Configure Blue-Green Deployments.
- [x] Configure a Dead Letter Queue (Elastic Beanstalk worker environments support SQS dead letter queues, where worker can send messages that for some reason could not be successfully processed. Dead letter queue provides the ability to sideline, isolate and analyze the unsuccessfully processed messages. Refer link)

771.
When thinking of AWS Elastic Beanstalk, which statement is true?
- [ ] Worker tiers pull jobs from SNS.
- [ ] Worker tiers pull jobs from HTTP.
- [ ] Worker tiers pull jobs from JSON.
- [x] Worker tiers pull jobs from SQS. (Elastic Beanstalk installs a daemon on each EC2 instance in the Auto Scaling group to process SQS messages in the worker environment. Refer link)

772.
You are building a Ruby on Rails application for internal, non-production use, which uses MySQL as a database. You want developers without very much AWS experience to be able to deploy new code with a single command line push. You also want to set this up as simply as possible. Which tool is ideal for this setup?
- [ ] AWS CloudFormation
- [ ] AWS OpsWorks
- [ ] AWS ELB + EC2 with CLI Push
- [x] AWS Elastic Beanstalk

773.
What AWS products and features can be deployed by Elastic Beanstalk? Choose 3 answers.
- [x] Auto scaling groups
- [ ] Route 53 hosted zones
- [x] Elastic Load Balancers
- [x] RDS Instances
- [ ] Elastic IP addresses
- [ ] SQS Queues

774.
AWS Elastic Beanstalk stores your application files and optionally server log files in ____.
- [ ] Amazon Storage Gateway
- [ ] Amazon Glacier
- [ ] Amazon EC2
- [x] Amazon S3

775.
When you use the AWS Elastic Beanstalk console to deploy a new application ____.
- [ ] Need to upload each file separately
- [ ] Need to create each file and path
- [x] Need to upload a source bundle
- [ ] Need to create each file

776.
- [ ] In DynamoDB, a secondary index is a data structure that contains a subset of attributes from a table, along with an alternate key to support ____ operations.
- [ ] None of the above
- [ ] Both
- [x] Query
- [ ] Scan

777.
In regard to DynamoDB, what is the Global secondary index?
- [x] An index with a hash and range key that can be different from those on the table
- [ ] An index that has the same range key as the table, but a different hash key
- [ ] An index that has the same hash key and range key as the table
- [ ] An index that has the same hash key as the table, but a different range key

778.
In regard to DynamoDB, can I modify the index once it is created?
- [ ] Yes, if it is a primary hash key index
- [ ] Yes, if it is a Global secondary index
- [x] No
- [ ] Yes, if it is a local secondary index

779.
When thinking of DynamoDB, what are true of Global Secondary Key properties?
- [x] The partition key and sort key can be different from the table.
- [ ] Only the partition key can be different from the table.
- [ ] Either the partition key or the sort key can be different from the table, but not both.
- [ ] Only the sort key can be different from the table.

780.
You are working with a customer who is using Chef configuration management in their data center. Which service is designed to let the customer leverage existing Chef recipes in AWS?
- [ ] Amazon Simple Workflow Service
- [ ] AWS Elastic Beanstalk
- [ ] AWS CloudFormation
- [x] AWS OpsWorks

781.
Your mission is to create a lights-out datacenter environment, and you plan to use AWS OpsWorks to accomplish this. First you created a stack and added an App Server layer with an instance running in it. Next you added an application to the instance, and now you need to deploy a MySQL RDS database instance. Which of the following answers accurately describe how to add a backend database server to an OpsWorks stack? Choose 3 answers
- [x] Add a new database layer and then add recipes to the deploy actions of the database and App Server layers. (Refer link)
- [ ] Use OpsWorks’ “Clone Stack” feature to create a second RDS stack in another Availability Zone for redundancy in the event of a failure in the Primary AZ. To switch to the secondary RDS instance, set the [:database] attributes to values that are appropriate for your server which you can do by using custom JSON.
- [x] The variables that characterize the RDS database connection—host, user, and so on—are set using the corresponding values from the deploy JSON’s [:deploy][:app_name][:database] attributes. (Refer link)
- [ ] Cookbook attributes are stored in a repository, so OpsWorks requires that the “password”: “your_password” attribute for the RDS instance must be encrypted using at least a 256-bit key.
- [x] Set up the connection between the app server and the RDS layer by using a custom recipe. The recipe configures the app server as required, typically by creating a configuration file. The recipe gets the connection data such as the host and database name from a set of attributes in the stack configuration and deployment JSON that AWS OpsWorks installs on every instance. (Refer link)

782.
You are tasked with the migration of a highly trafficked node.js application to AWS. In order to comply with organizational standards Chef recipes must be used to configure the application servers that host this application and to support application lifecycle events. Which deployment option meets these requirements while minimizing administrative burden?
- [x] Create a new stack within Opsworks add the appropriate layers to the stack and deploy the application
- [ ] Create a new application within Elastic Beanstalk and deploy this application to a new environment (need to comply with chef recipes)
- [ ] Launch a Node JS server from a community AMI and manually deploy the application to the launched EC2 instance
- [ ] Launch and configure Chef Server on an EC2 instance and leverage the AWS CLI to launch application servers and configure those instances using Chef.

783.
A web-startup runs its very successful social news application on Amazon EC2 with an Elastic Load Balancer, an Auto-Scaling group of Java/Tomcat application-servers, and DynamoDB as data store. The main web application best runs on m2.xlarge instances since it is highly memory- bound. Each new deployment requires semi-automated creation and testing of a new AMI for the application servers which takes quite a while and is therefore only done once per week. Recently, a new chat feature has been implemented in node.js and waits to be integrated in the architecture. First tests show that the new component is CPU bound Because the company has some experience with using Chef, they decided to streamline the deployment process and use AWS OpsWorks as an application life cycle tool to simplify management of the application and reduce the deployment cycles. What configuration in AWS OpsWorks is necessary to integrate the new chat module in the most cost-efficient and flexible way?
- [ ] Create one AWS Ops Works stack, create one AWS Ops Works layer, create one custom recipe
- [x] Create one AWS Ops Works stack, create two AWS Ops Works layers create one custom recipe (Single environment stack, two layers for java and node.js application using built-in recipes and custom recipe for DynamoDB connectivity only as other configuration. Refer link)
- [ ] Create two AWS Ops Works stacks, create two AWS Ops Works layers create one custom recipe
- [ ] Create two AWS Ops Works stacks, create two AWS Ops Works layers create two custom recipe

784.
You company runs a complex customer relations management system that consists of around 10 different software components all backed by the same Amazon Relational Database (RDS) database. You adopted AWS OpsWorks to simplify management and deployment of that application and created an AWS OpsWorks stack with layers for each of the individual components. An internal security policy requires that all instances should run on the latest Amazon Linux AMI and that instances must be replaced within one month after the latest Amazon Linux AMI has been released. AMI replacements should be done without incurring application downtime or capacity problems. You decide to write a script to be run as soon as a new Amazon Linux AMI is released. Which solutions support the security policy and meet your requirements? Choose 2 answers
- [ ] Assign a custom recipe to each layer, which replaces the underlying AMI. Use AWS OpsWorks life-cycle events to incrementally execute this custom recipe and update the instances with the new AMI.
- [x] Create a new stack and layers with identical configuration, add instances with the latest Amazon Linux AMI specified as a custom AMI to the new layer, switch DNS to the new stack, and tear down the old stack. (Blue-Green Deployment)
- [ ] Identify all Amazon Elastic Compute Cloud (EC2) instances of your AWS OpsWorks stack, stop each instance, replace the AMI ID property with the ID of the latest Amazon Linux AMI ID, and restart the instance. To avoid downtime, make sure not more than one instance is stopped at the same time.
- [ ] Specify the latest Amazon Linux AMI as a custom AMI at the stack level, terminate instances of the stack and let AWS OpsWorks launch new instances with the new AMI. (Will lead to downtime)
- [x] Add new instances with the latest Amazon Linux AMI specified as a custom AMI to all AWS OpsWorks layers of your stack, and terminate the old ones.

785.
When thinking of AWS OpsWorks, which of the following is not an instance type you can allocate in a stack layer?
- [ ] 24/7 instances (24/7 instances are supported and started manually and run until you stop them)
- [x] Spot instances (Does not support spot instance directly but can be used with auto scaling Refer link)
- [ ] Time-based instances (Time-based instances are run by AWS OpsWorks on a specified daily and weekly schedule)
- [ ] Load-based instances (Load-based instances are automatically started and stopped by AWS OpsWorks, based on specified load metrics, such as CPU utilization)

786.
Which of the following tools does not directly support AWS OpsWorks, for monitoring your stacks?
- [x] AWS Config (Refer link)
- [ ] Amazon CloudWatch Metrics (AWS OpsWorks uses CloudWatch to provide thirteen custom metrics with detailed monitoring for each instance in the stack)
- [ ] AWS CloudTrail (AWS OpsWorks integrates with CloudTrail to log every AWS OpsWorks API call and store the data in an S3 bucket)
- [ ] Amazon CloudWatch Logs (You can use Amazon CloudWatch Logs to monitor your stack’s system, application, and custom logs.)

787.
When thinking of AWS OpsWorks, which of the following is true?
- [x] Stacks have many layers, layers have many instances.
- [ ] Instances have many stacks, stacks have many layers.
- [ ] Layers have many stacks, stacks have many instances.
- [ ] Layers have many instances, instances have many stacks.

788.
REST or Query requests are HTTP or HTTPS requests that use an HTTP verb (such as GET or POST) and a parameter named Action or Operation that specifies the API you are calling.
- [ ] FALSE
- [x] TRUE (Refer link)

789.
Through which of the following interfaces is AWS Identity and Access Management available?
A) AWS Management Console
B) Command line interface (CLI)
C) IAM Query API
D) Existing libraries
- [ ] Only through Command line interface (CLI)
- [ ] A, B and C
- [ ] A and C
- [x] All of the above

790.
Which of the following programming languages have an officially supported AWS SDK? Choose 2 answers
- [x] PHP
- [ ] Pascal
- [x] Java
- [ ] SQL
- [ ] Perl

791.
HTTP Query-based requests are HTTP requests that use the HTTP verb GET or POST and a Query parameter named_____________.
- [x] Action
- [ ] Value
- [ ] Reset
- [ ] Retrieve

792.
You’ve been hired to enhance the overall security posture for a very large e-commerce site. They have a well architected multi-tier application running in a VPC that uses ELBs in front of both the web and the app tier with static assets served directly from S3. They are using a combination of RDS and DynamoDB for their dynamic data and then archiving nightly into S3 for further processing with EMR. They are concerned because they found questionable log entries and suspect someone is attempting to gain unauthorized access. Which approach provides a cost effective scalable mitigation to this kind of attack?
- [ ] Recommend mat they lease space at a DirectConnect partner location and establish a 1G DirectConnect connection to tneirvPC they would then establish Internet connectivity into their space, filter the traffic in hardware Web Application Firewall (WAF). And then pass the traffic through the DirectConnect connection into their application running in their VPC. (Not cost effective)
- [ ] Add previously identified hostile source IPs as an explicit INBOUND DENY NACL to the web tier subnet. (does not protect against new source)
- [x] Add a WAF tier by creating a new ELB and an AutoScaling group of EC2 Instances running a host-based WAF. They would redirect Route 53 to resolve to the new WAF tier ELB. The WAF tier would then pass the traffic to the current web tier. Web tier Security Groups would be updated to only allow traffic from the WAF tier Security Group
- [ ] Remove all but TLS 1.2 from the web tier ELB and enable Advanced Protocol Filtering This will enable the ELB itself to perform WAF functionality. (No advanced protocol filtering in ELB)

793.
What does Amazon ElastiCache provide?
- [ ] A service by this name doesn’t exist. Perhaps you mean Amazon CloudCache.
- [ ] A virtual server with a huge amount of memory.
- [x] A managed In-memory cache service
- [ ] An Amazon EC2 instance with the Memcached software already pre-installed.

794.
You are developing a highly available web application using stateless web servers. Which services are suitable for storing session state data? Choose 3 answers.
- [ ] Elastic Load Balancing
- [x] Amazon Relational Database Service (RDS)
- [ ] Amazon CloudWatch
- [x] Amazon ElastiCache
- [x] Amazon DynamoDB
- [ ] AWS Storage Gateway

795.
Which statement best describes ElastiCache?
- [ ] Reduces the latency by splitting the workload across multiple AZs
- [ ] A simple web services interface to create and store multiple data sets, query your data easily, and return the results
- [x] Offload the read traffic from your database in order to reduce latency caused by read-heavy workload
- [ ] Managed service that makes it easy to set up, operate and scale a relational database in the cloud

796.
Our company is getting ready to do a major public announcement of a social media site on AWS. The website is running on EC2 instances deployed across multiple Availability Zones with a Multi-AZ RDS MySQL Extra Large DB Instance. The site performs a high number of small reads and writes per second and relies on an eventual consistency model. After comprehensive tests you discover that there is read contention on RDS MySQL. Which are the best approaches to meet these requirements? (Choose 2 answers)
- [x] Deploy ElastiCache in-memory cache running in each availability zone
- [ ] Implement sharding to distribute load to multiple RDS MySQL instances
- [ ] Increase the RDS MySQL Instance size and Implement provisioned IOPS
- [x] Add an RDS MySQL read replica in each availability zone

797.
You are using ElastiCache Memcached to store session state and cache database queries in your infrastructure. You notice in CloudWatch that Evictions and Get Misses are both very high. What two actions could you take to rectify this? Choose 2 answers
- [x] Increase the number of nodes in your cluster
- [ ] Tweak the max_item_size parameter
- [ ] Shrink the number of nodes in your cluster
- [x] Increase the size of the nodes in the cluster

798.
You have been tasked with moving an ecommerce web application from a customer’s datacenter into a VPC. The application must be fault tolerant and well as highly scalable. Moreover, the customer is adamant that service interruptions not affect the user experience. As you near launch, you discover that the application currently uses multicast to share session state between web servers, In order to handle session state within the VPC, you choose to:
- [x] Store session state in Amazon ElastiCache for Redis (scalable and makes the web applications stateless)
- [ ] Create a mesh VPN between instances and allow multicast on it
- [ ] Store session state in Amazon Relational Database Service (RDS solution not highly scalable)
- [ ] Enable session stickiness via Elastic Load Balancing (affects user experience if the instance goes down)

799.
When you are designing to support a 24-hour flash sale, which one of the following methods best describes a strategy to lower the latency while keeping up with unusually heavy traffic?
- [ ] Launch enhanced networking instances in a placement group to support the heavy traffic (only improves internal communication)
- [ ] Apply Service Oriented Architecture (SOA) principles instead of a 3-tier architecture (just simplifies architecture)
- [ ] Use Elastic Beanstalk to enable blue-green deployment (only minimizes download for applications and ease of rollback)
- [x] Use ElastiCache as in-memory storage on top of DynamoDB to store user sessions (scalable, faster read/writes and in memory storage)

800.
You are configuring your company’s application to use Auto Scaling and need to move user state information. Which of the following AWS services provides a shared data store with durability and low latency?
- [ ] AWS ElastiCache Memcached (does not provide durability as if the node is gone the data is gone)
- [ ] Amazon Simple Storage Service
- [ ] Amazon EC2 instance storage
- [x] Amazon DynamoDB

801.
Your application is using an ELB in front of an Auto Scaling group of web/application servers deployed across two AZs and a Multi-AZ RDS Instance for data persistence. The database CPU is often above 80% usage and 90% of I/O operations on the database are reads. To improve performance you recently added a single-node Memcached ElastiCache Cluster to cache frequent DB query results. In the next weeks the overall workload is expected to grow by 30%. Do you need to change anything in the architecture to maintain the high availability for the application with the anticipated additional load and Why?
- [x] You should deploy two Memcached ElastiCache Clusters in different AZs because the RDS Instance will not be able to handle the load if the cache node fails.
- [ ] If the cache node fails the automated ElastiCache node recovery feature will prevent any availability impact. (does not provide high availability, as data is lost if the node is lost)
- [ ] Yes you should deploy the Memcached ElastiCache Cluster with two nodes in the same AZ as the RDS DB master instance to handle the load if one cache node fails. (Single AZ affects availability as DB is Multi AZ and would be overloaded is the AZ goes down)
- [ ] No if the cache node fails you can always get the same data from the DB without having any availability impact. (Will overload the database affecting availability)

802.
A read only news reporting site with a combined web and application tier and a database tier that receives large and unpredictable traffic demands must be able to respond to these traffic fluctuations automatically. What AWS services should be used meet these requirements?
- [x] Stateless instances for the web and application tier synchronized using ElastiCache Memcached in an autoscaling group monitored with CloudWatch and RDS with read replicas.
- [ ] Stateful instances for the web and application tier in an autoscaling group monitored with CloudWatch and RDS with read replicas (Stateful instances will not allow for scaling)
- [ ] Stateful instances for the web and application tier in an autoscaling group monitored with CloudWatch and multi-AZ RDS (Stateful instances will allow not for scaling & multi-AZ is for high availability and not scaling)
- [ ] Stateless instances for the web and application tier synchronized using ElastiCache Memcached in an autoscaling group monitored with CloudWatch and multi-AZ RDS (multi-AZ is for high availability and not scaling)

803.
You have written an application that uses the Elastic Load Balancing service to spread traffic to several web servers. Your users complain that they are sometimes forced to login again in the middle of using your application, after they have already logged in. This is not behavior you have designed. What is a possible solution to prevent this happening?
- [ ] Use instance memory to save session state.
- [ ] Use instance storage to save session state.
- [ ] Use EBS to save session state.
- [x] Use ElastiCache to save session state.
- [ ] Use Glacier to save session slate.

804.
With which AWS services CloudHSM can be used (select 2)
- [ ] S3
- [ ] DynamoDB
- [x] RDS
- [ ] ElastiCache
- [x] Amazon Redshift

805.
You have recently joined a startup company building sensors to measure street noise and air quality in urban areas. The company has been running a pilot deployment of around 100 sensors for 3 months. Each sensor uploads 1KB of sensor data every minute to a backend hosted on AWS. During the pilot, you measured a peak of 10 IOPS on the database, and you stored an average of 3GB of sensor data per month in the database. The current deployment consists of a load-balanced auto scaled Ingestion layer using EC2 instances and a PostgreSQL RDS database with 500GB standard storage. The pilot is considered a success and your CEO has managed to get the attention or some potential investors. The business plan requires a deployment of at least 100K sensors, which needs to be supported by the backend. You also need to store sensor data for at least two years to be able to compare year over year Improvements. To secure funding, you have to make sure that the platform meets these requirements and leaves room for further scaling. Which setup will meet the requirements?
- [ ] Add an SQS queue to the ingestion layer to buffer writes to the RDS instance (RDS instance will not support data for 2 years)
- [x] Ingest data into a DynamoDB table and move old data to a Redshift cluster (Handle 10K IOPS ingestion and store data into Redshift for analysis)
- [ ] Replace the RDS instance with a 6 node Redshift cluster with 96TB of storage (Does not handle the ingestion issue)
- [ ] Keep the current architecture but upgrade RDS storage to 3TB and 10K provisioned IOPS (RDS instance will not support data for 2 years)

806.
Which two AWS services provide out-of-the-box user configurable automatic backup-as-a-service and backup rotation options? Choose 2 answers
- [ ] Amazon S3
- [x] Amazon RDS
- [ ] Amazon EBS
- [x] Amazon Redshift

807.
Your department creates regular analytics reports from your company’s log files. All log data is collected in Amazon S3 and processed by daily Amazon Elastic Map Reduce (EMR) jobs that generate daily PDF reports and aggregated tables in CSV format for an Amazon Redshift data warehouse. Your CFO requests that you optimize the cost structure for this system. Which of the following alternatives will lower costs without compromising average performance of the system or data integrity for the raw data?
- [ ] Use reduced redundancy storage (RRS) for PDF and CSV data in Amazon S3. Add Spot instances to Amazon EMR jobs. Use Reserved Instances for Amazon Redshift. (Spot instances impacts performance)
- [x] Use reduced redundancy storage (RRS) for all data in S3. Use a combination of Spot instances and Reserved Instances for Amazon EMR jobs. Use Reserved instances for Amazon Redshift (Combination of the Spot and reserved with guarantee performance and help reduce cost. Also, RRS would reduce cost and guarantee data integrity, which is different from data durability)
- [ ] Use reduced redundancy storage (RRS) for all data in Amazon S3. Add Spot Instances to Amazon EMR jobs. Use Reserved Instances for Amazon Redshift (Spot instances impacts performance)
- [ ] Use reduced redundancy storage (RRS) for PDF and CSV data in S3. Add Spot Instances to EMR jobs. Use Spot Instances for Amazon Redshift. (Spot instances impacts performance and Spot instance not available for Redshift)

808.
Your team is excited about the use of AWS because now they have access to programmable infrastructure. You have been asked to manage your AWS infrastructure in a manner similar to the way you might manage application code. You want to be able to deploy exact copies of different versions of your infrastructure, stage changes into different environments, revert back to previous versions, and identify what versions are running at any particular time (development test QA. production). Which approach addresses this requirement?
- [ ] Use cost allocation reports and AWS Opsworks to deploy and manage your infrastructure.
- [ ] Use AWS CloudWatch metrics and alerts along with resource tagging to deploy and manage your infrastructure.
- [ ] Use AWS Elastic Beanstalk and a version control system like GIT to deploy and manage your infrastructure.
- [x] Use AWS CloudFormation and a version control system like GIT to deploy and manage your infrastructure.

809.
An organization is planning to use AWS for their production roll out. The organization wants to implement automation for deployment such that it will automatically create a LAMP stack, download the latest PHP installable from S3 and setup the ELB. Which of the below mentioned AWS services meets the requirement for making an orderly deployment of the software?
- [x] AWS Elastic Beanstalk
- [ ] AWS CloudFront
- [ ] AWS CloudFormation
- [ ] AWS DevOps

810.
You are working with a customer who is using Chef configuration management in their data center. Which service is designed to let the customer leverage existing Chef recipes in AWS?
- [ ] Amazon Simple Workflow Service
- [ ] AWS Elastic Beanstalk
- [ ] AWS CloudFormation
- [x] AWS OpsWorks

811.
The Trusted Advisor service provides insight regarding which four categories of an AWS account?
- [ ] Security, fault tolerance, high availability, and connectivity
- [ ] Security, access control, high availability, and performance
- [x] Performance, cost optimization, security, and fault tolerance
- [ ] Performance, cost optimization, access control, and connectivity

812.
The majority of your Infrastructure is on premises and you have a small footprint on AWS. Your company has decided to roll out a new application that is heavily dependent on low latency connectivity to LDAP for authentication. Your security policy requires minimal changes to the company’s existing application user management processes. What option would you implement to successfully launch this application?
- [ ] Create a second, independent LDAP server in AWS for your application to use for authentication (independent would not work for authentication as its a separate copy)
- [ ] Establish a VPN connection so your applications can authenticate against your existing on-premises LDAP servers (not a low latency solution)
- [x] Establish a VPN connection between your data center and AWS create a LDAP replica on AWS and configure your application to use the LDAP replica for authentication (RODCs low latency and minimal setup)
- [ ] Create a second LDAP domain on AWS establish a VPN connection to establish a trust relationship between your new and existing domains and use the new domain for authentication (Not minimal effort)

813.
A company is preparing to give AWS Management Console access to developers Company policy mandates identity federation and role-based access control. Roles are currently assigned using groups in the corporate Active Directory. What combination of the following will give developers access to the AWS console? (Select 2) Choose 2 answers
- [x] AWS Directory Service AD Connector (for Corporate Active directory)
- [ ] AWS Directory Service Simple AD
- [ ] AWS Identity and Access Management groups
- [x] AWS identity and Access Management roles
- [ ] AWS identity and Access Management users

814.
An Enterprise customer is starting their migration to the cloud, their main reason for migrating is agility, and they want to make their internal Microsoft Active Directory available to any applications running on AWS; this is so internal users only have to remember one set of credentials and as a central point of user control for leavers and joiners. How could they make their Active Directory secure, and highly available, with minimal on-premises infrastructure changes, in the most cost and time-efficient way? Choose the most appropriate
- [ ] Using Amazon Elastic Compute Cloud (EC2), they would create a DMZ using a security group; within the security group they could provision two smaller amazon EC2 instances that are running Openswan for resilient IPSEC tunnels, and two larger instance that are domain controllers; they would use multiple Availability Zones (Whats Openswan? Refer Implementation)
- [x] Using VPC, they could create an extension to their data center and make use of resilient hardware IPSEC tunnels; they could then have two domain controller instances that are joined to their existing domain and reside within different subnets, in different Availability Zones (highly available with 2 AZ’s, secure with VPN connection and minimal changes)
- [ ] Within the customer’s existing infrastructure, they could provision new hardware to run Active Directory Federation Services; this would present Active Directory as a SAML2 endpoint on the internet; any new application on AWS could be written to authenticate using SAML2 (not minimal on-premises hardware changes)
- [ ] The customer could create a stand-alone VPC with its own Active Directory Domain Controllers; two domain controller instances could be configured, one in each Availability Zone; new applications would authenticate with those domain controllers (not a central location, but a copy)

815.
A company needs to deploy virtual desktops to its customers in a virtual private cloud, leveraging existing security controls. Which set of AWS services and features will meet the company’s requirements?
- [ ] Virtual Private Network connection. AWS Directory Services, and ClassicLink (ClassicLink allows you to link an EC2-Classic instance to a VPC in your account, within the same region)
- [x] Virtual Private Network connection. AWS Directory Services, and Amazon Workspaces (WorkSpaces for Virtual desktops, and AWS Directory Services to authenticate to an existing on-premises AD through VPN)
- [ ] AWS Directory Service, Amazon Workspaces, and AWS Identity and Access Management (AD service needs a VPN connection to interact with an On-premise AD directory)
- [ ] Amazon Elastic Compute Cloud, and AWS Identity and Access Management (Need WorkSpaces for virtual desktops)

816.
An Enterprise customer is starting their migration to the cloud, their main reason for migrating is agility and they want to make their internal Microsoft active directory available to any applications running on AWS, this is so internal users only have to remember one set of credentials and as a central point of user control for leavers and joiners. How could they make their active directory secure and highly available with minimal on-premises infrastructure changes in the most cost and time efficient way? Choose the most appropriate:
- [ ] Using Amazon EC2, they could create a DMZ using a security group, within the security group they could provision two smaller Amazon EC2 instances that are running Openswan for resilient IPSEC tunnels and two larger instances that are domain controllers, they would use multiple availability zones.
- [x] Using VPC, they could create an extension to their data center and make use of resilient hardware IPSEC tunnels, they could then have two domain controller instances that are joined to their existing domain and reside within different subnets in different availability zones.
- [ ] Within the customer’s existing infrastructure, they could provision new hardware to run active directory federation services, this would present active directory as a SAML2 endpoint on the internet and any new application on AWS could be written to authenticate using SAML2 (not a  minimal change to the existing infrastructure)
- [ ] The customer could create a stand alone VPC with its own active directory domain controllers, two domain controller instances could be configured, one in each availability zone, new applications would authenticate with those domain controllers. (Standalone cannot use the same security)

817.
You run a 2000-engineer organization. You are about to begin using AWS at a large scale for the first time. You want to integrate with your existing identity management system running on Microsoft Active Directory, because your organization is a power-user of Active Directory. How should you manage your AWS identities in the simplest manner?
- [ ] Use a large AWS Directory Service Simple AD.
- [x] Use a large AWS Directory Service AD Connector. (AD Connector can be used as power-user of Microsoft Active Directory. Simple AD only works with a subset of AD functionality)
- [ ] Use a Sync Domain running on AWS Directory Service.
- [ ] Use an AWS Directory Sync Domain running on AWS Lambda.

818.
You currently operate a web application in the AWS US-East region. The application runs on an auto-scaled layer of EC2 instances and an RDS Multi-AZ database. Your IT security compliance officer has tasked you to develop a reliable and durable logging solution to track changes made to your EC2, IAM and RDS resources. The solution must ensure the integrity and confidentiality of your log data. Which of these solutions would you recommend?
- [x] Create a new CloudTrail trail with one new S3 bucket to store the logs and with the global services option selected. Use IAM roles, S3 bucket policies and Multi Factor Authentication (MFA) Delete on the S3 bucket that stores your logs. (Single New bucket with global services option for IAM and MFA delete for confidentiality)
- [ ] Create a new CloudTrail with one new S3 bucket to store the logs. Configure SNS to send log file delivery notifications to your management system. Use IAM roles and S3 bucket policies on the S3 bucket that stores your logs. (Missing Global Services for IAM)
- [ ] Create a new CloudTrail trail with an existing S3 bucket to store the logs and with the global services option selected Use S3 ACLs and Multi Factor Authentication (MFA) Delete on the S3 bucket that stores your logs. (Existing bucket prevents confidentiality)
- [ ] Create three new CloudTrail trails with three new S3 buckets to store the logs one for the AWS Management console, one for AWS SDKs and one for command line tools. Use IAM roles and S3 bucket policies on the S3 buckets that store your logs (3 buckets not needed, Missing Global services options)

819.
Which of the following are true regarding AWS CloudTrail? Choose 3 answers
- [x] CloudTrail is enabled globally (it can be enabled for all regions and also per region basis)
- [x] CloudTrail is enabled by default (was not enabled by default, however, it is enabled by default as per the latest AWS enhancements)
- [x] CloudTrail is enabled on a per-region basis (it can be enabled for all regions and also per region basis)
- [ ] CloudTrail is enabled on a per-service basis (once enabled it is applicable for all the supported services, service can’t be selected)
- [x] Logs can be delivered to a single Amazon S3 bucket for aggregation
- [ ] CloudTrail is enabled for all available services within a region. (is enabled only for CloudTrail supported services)
- [ ] Logs can only be processed and delivered to the region in which they are generated. (can be logged to bucket in any region)

819
An organization has configured the custom metric upload with CloudWatch. The organization has given permission to its employees to upload data using CLI as well SDK. How can the user track the calls made to CloudWatch?
- [ ] The user can enable logging with CloudWatch which logs all the activities
- [x] Use CloudTrail to monitor the API calls
- [ ] Create an IAM user and allow each user to log the data using the S3 bucket
- [ ] Enable detailed monitoring with CloudWatch

820.
A user is trying to understand the CloudWatch metrics for the AWS services. It is required that the user should first understand the namespace for the AWS services. Which of the below mentioned is not a valid namespace for the AWS services?
- [ ] AWS/StorageGateway
- [x] AWS/CloudTrail (CloudWatch supported namespaces)
- [ ] AWS/ElastiCache
- [ ] AWS/SWF

821.
Your CTO thinks your AWS account was hacked. What is the only way to know for certain if there was unauthorized access and what they did, assuming your hackers are very sophisticated AWS engineers and doing everything they can to cover their tracks?
- [x] Use CloudTrail Log File Integrity Validation. (Refer link)
- [ ] Use AWS Config SNS Subscriptions and process events in real time.
- [ ] Use CloudTrail backed up to AWS S3 and Glacier.
- [ ] Use AWS Config Timeline forensics.

822.
Your CTO has asked you to make sure that you know what all users of your AWS account are doing to change resources at all times. She wants a report of who is doing what over time, reported to her once per week, for as broad a resource type group as possible. How should you do this?
- [x] Create a global AWS CloudTrail Trail. Configure a script to aggregate the log data delivered to S3 once per week and deliver this to the CTO.
- [ ] Use CloudWatch Events Rules with an SNS topic subscribed to all AWS API calls. Subscribe the CTO to an email type delivery on this SNS Topic.
- [ ] Use AWS IAM credential reports to deliver a CSV of all uses of IAM User Tokens over time to the CTO.
- [ ] Use AWS Config with an SNS subscription on a Lambda, and insert these changes over time into a DynamoDB table. Generate reports based on the contents of this table.

823.
Which two AWS services provide out-of-the-box user configurable automatic backup-as-a-service and backup rotation options? Choose 2 answers
- [ ] Amazon S3
- [x] Amazon RDS
- [ ] Amazon EBS
- [x] Amazon Redshift

824.
You have been asked to automate many routine systems administrator backup and recovery activities. Your current plan is to leverage AWS-managed solutions as much as possible and automate the rest with the AWS CLI and scripts. Which task would be best accomplished with a script?
- [x] Creating daily EBS snapshots with a monthly rotation of snapshots
- [ ] Creating daily RDS snapshots with a monthly rotation of snapshots
- [ ] Automatically detect and stop unused or underutilized EC2 instances
- [ ] Automatically add Auto Scaled EC2 instances to an Amazon Elastic Load Balancer

825.
Your website is serving on-demand training videos to your workforce. Videos are uploaded monthly in high resolution MP4 format. Your workforce is distributed globally often on the move and using company-provided tablets that require the HTTP Live Streaming (HLS) protocol to watch a video. Your company has no video transcoding expertise and it required you might need to pay for a consultant. How do you implement the most cost-efficient architecture without compromising high availability and quality of video delivery?
- [x] Elastic Transcoder to transcode original high-resolution MP4 videos to HLS. S3 to host videos with lifecycle Management to archive original flies to Glacier after a few days. CloudFront to serve HLS transcoded videos from S3
- [ ] A video transcoding pipeline running on EC2 using SQS to distribute tasks and Auto Scaling to adjust the number or nodes depending on the length of the queue S3 to host videos with Lifecycle Management to archive all files to Glacier after a few days CloudFront to serve HLS transcoding videos from Glacier
- [ ] Elastic Transcoder to transcode original high-resolution MP4 videos to HLS EBS volumes to host videos and EBS snapshots to incrementally backup original rues after a few days. CloudFront to serve HLS transcoded videos from EC2.
- [ ] A video transcoding pipeline running on EC2 using SQS to distribute tasks and Auto Scaling to adjust the number of nodes depending on the length of the queue. EBS volumes to host videos and EBS snapshots to incrementally backup original files after a few days. CloudFront to serve HLS transcoded videos from EC2

826.
Your must architect the migration of a web application to AWS. The application consists of Linux web servers running a custom web server. You are required to save the logs generated from the application to a durable location. What options could you select to migrate the application to AWS? (Choose 2)
- [ ] Create an AWS Elastic Beanstalk application using the custom web server platform. Specify the web server executable and the application project and source files. Enable log file rotation to Amazon Simple Storage Service (S3). (EB does not work with Custom server executable)
- [ ] Create Dockerfile for the application. Create an AWS OpsWorks stack consisting of a custom layer. Create custom recipes to install Docker and to deploy your Docker container using the Dockerfile. Create custom recipes to install and configure the application to publish the logs to Amazon CloudWatch Logs (although this is one of the option, the last sentence mentions configure the application to push the logs to S3, which would need changes to application as it needs to use SDK or CLI)
- [ ] Create Dockerfile for the application. Create an AWS OpsWorks stack consisting of a Docker layer that uses the Dockerfile. Create custom recipes to install and configure Amazon Kinesis to publish the logs into Amazon CloudWatch. (Kinesis not needed)
- [x] Create a Dockerfile for the application. Create an AWS Elastic Beanstalk application using the Docker platform and the Dockerfile. Enable logging the Docker configuration to automatically publish the application logs. Enable log file rotation to Amazon S3. (Use Docker configuration with awslogs and EB with Docker)
- [x] Use VM import/Export to import a virtual machine image of the server into AWS as an AMI. Create an Amazon Elastic Compute Cloud (EC2) instance from AMI, and install and configure the Amazon CloudWatch Logs agent. Create a new AMI from the instance. Create an AWS Elastic Beanstalk application using the AMI platform and the new AMI. (Use VM Import/Export to create AMI and CloudWatch logs agent to log)

827.
Your company hosts an on-premises legacy engineering application with 900GB of data shared via a central file server. The engineering data consists of thousands of individual files ranging in size from megabytes to multiple gigabytes. Engineers typically modify 5-10 percent of the files a day. Your CTO would like to migrate this application to AWS, but only if the application can be migrated over the weekend to minimize user downtime. You calculate that it will take a minimum of 48 hours to transfer 900GB of data using your company’s existing 45-Mbps Internet connection. After replicating the application’s environment in AWS, which option will allow you to move the application’s data to AWS without losing any data and within the given timeframe?
- [ ] Copy the data to Amazon S3 using multiple threads and multi-part upload for large files over the weekend, and work in parallel with your developers to reconfigure the replicated application environment to leverage Amazon S3 to serve the engineering files. (Still limited by 45 Mbps speed with minimum 48 hours when utilized to max)
- [x] Sync the application data to Amazon S3 starting a week before the migration, on Friday morning perform a final sync, and copy the entire data set to your AWS file server after the sync completes. (Works best as the data changes can be propagated over the week and are fractional and downtime would be know)
- [ ] Copy the application data to a 1-TB USB drive on Friday and immediately send overnight, with Saturday delivery, the USB drive to AWS Import/Export to be imported as an EBS volume, mount the resulting EBS volume to your AWS file server on Sunday. (Downtime is not known when the data upload would be done, although Amazon says the same day the package is received)
- [ ] Leverage the AWS Storage Gateway to create a Gateway-Stored volume. On Friday copy the application data to the Storage Gateway volume. After the data has been copied, perform a snapshot of the volume and restore the volume as an EBS volume to be attached to your AWS file server on Sunday. (Still uses the internet)

828.
You are tasked with moving a legacy application from a virtual machine running inside your datacenter to an Amazon VPC. Unfortunately this app requires access to a number of on-premises services and no one who configured the app still works for your company. Even worse there’s no documentation for it. What will allow the application running inside the VPC to reach back and access its internal dependencies without being reconfigured? (Choose 3 answers)
- [x] An AWS Direct Connect link between the VPC and the network housing the internal services
- [ ] An Internet Gateway to allow a VPN connection. (Virtual and Customer gateway is needed)
- [ ] An Elastic IP address on the VPC instance
- [x] An IP address space that does not conflict with the one on-premises
- [ ] Entries in Amazon Route 53 that allow the Instance to resolve its dependencies’ IP addresses
- [x] A VM Import of the current virtual machine

