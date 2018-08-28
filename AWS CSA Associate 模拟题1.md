## AWS CSA Associate 模拟题1
1.
Amazon SQS (Simple Queue Service) guarantees the delivery of a message AT LEAST once, but cannot guarantee it will not create duplicates.
**Choose the correct answer:**
- [x] True
- [ ] False

2.
Which of the following will occur when an EC2 instance in a VPC with an associated Elastic IP is stopped and started?
**Choose the correct answer:**
- [ ] The ENI (Elastic Network Interface) is detatched
- [ ] The Elastic IP will be dissociated from the instance
- [x] The underlying host for the instance can be changed
- [x] All data on instance-store devices will be lost

3.
Data stored on EBS volumes are automatically and redundantly stored in multiple physical volumes in the same Availability Zone as part of the normal operations of the EBS service and at no additional charge.
**Choose the correct answer:**
- [x] True
- [ ] False

4.
If an instance that belongs to an Elastic Load Balancer's health check fails, what occurs to the instance that fails?
**Choose the correct answer:**
- [x] The ELB will de-register the instance and stop sending traffic to the unhealthy instance
- [ ] The ELB will continue serving the traffic until the instance is removed
- [ ] The Auto Scaling group will launch a new instance
- [ ] ELB launches a new healthy instance

5.
Company B provides an online image recognition service and utilizes SQS to decouple system components for scalability. The SQS consumer's readers poll the image queue as often as possible to keep end-to-end throughput as high as possible. However, Company B is realizing that polling in tight loops is burning CPU cycles and increasing costs with empty responses. How can Company B reduce the number of empty responses?
**Choose the correct answer:**
- [ ] Enable short polling on the SQS message by setting the ReceiveMessageWaitTimeSeconds to a number = 0
- [ ] Scale the component making the request using Auto Scaling based off the number of messages in the queue
- [ ] Enable short polling on the SQS queue by setting the ReceiveMessageWaitTimeSeconds to a number > 0
- [x] Enable long polling by setting the ReceiveMessageWaitTimeSeconds to a number > 0

6.
By default, is data in S3 encrypted?
**Choose the correct answer:**
- [x] No, but it can be when the right APIs are called for SSE
- [ ] Yes, S3 always encrypts data for security
- [ ] Yes, but only in government cloud data centers
- [ ] No, it must be encrypted before upload

7.
While running an EC2 instance, you've been storing data on one of the instance's volumes. However, to save money, you shut down the instance for the weekend. The following week, after starting the instance, you notice that all your work has been lost and is no longer available on the EC2 instance. What might be the cause of this?
**Choose the correct answer:**
- [ ] The EBS volume was not big enough to handle all of the processing data
- [ ] The instance might have been compromised
- [x] The EC2 instance was using instance store volumes, which are ephemeral and only live for the life of the instance
- [ ] The EC2 instance was using EBS backed root volumes, which are ephemeral and only live for the life of the instance

8.
Which of the following is true of an SQS message?
**Choose the correct answer:**
- [ ] SQS messages must be in JSON format
- [ ] SQS messages can live in the queue up to thirty days
- [x] SQS messages are guaranteed to be delivered at least once
- [ ] SQS messages must be less than 32 KB in size

9.
To maintain compliance with HIPPA laws, all data being backed up or stored on Amazon S3 needs to be encrypted at rest. What is the best method for encryption for your data, assuming S3 is being used for storing the healthcare-related data?
**Choose the 2 correct answers:**
- [ ] Store the data on EBS volumes with encryption enabled instead of using Amazon S3
- [x] Encrypt the data locally using your own encryption keys, then copy the data to Amazon S3 over HTTPS endpoints
- [x] Enable SSE on an S3 bucket to make use of AES-256 encryption
- [ ] Store the data in encrypted EBS snapshots

10.
What URL might you query on an EC2 instance to find the public AND private IP address of an instance?
**Choose the correct answer:**
- [ ] http://169.254.169.254/latest/user-data/
- [ ] http://254.169.254.169/latest/meta-data/
- [ ] http://169.254.169.169/latest/meta-data/
- [x] http://169.254.169.254/latest/meta-data/

11.
If your organization is concerned about storing sensitive data in the cloud, you should _______.
**Choose the 3 correct answers:**
- [x] Enable S3 Encryption
- [x] Encrypt the file system on an EBS volume using Linux tools
- [x] Enable EBS Encryption
- [ ] With AWS you do not need to worry about encryption

12.
You manage a web application on EC2 instances. Incoming requests are saved as messages in an SQS queue with the maximum message retention period. You return from a week and a half vacation to find that the part of the application which processes received requests is hung and the queue has grown to 1,000 messages. While you are working on resolving the application issue, you need to post an update to end users. What information should that update include?
**Choose the correct answer:**
- [ ] An apology for the delay in processing requests, assurance that the application will be operational shortly, and a note that requests greater than ten days old will need to be resubmitted (as they have surpassed the SQS queue’s retention period)
- [ ] An apology for the delay in processing requests, assurance that the application will be operational shortly, and a note that recently received requests will need to be re-submitted (as the SQS queue has reached the maximum of 1,000 messages, meaning recently submitted requests could not be saved as SQS messages)
- [x] An apology for the delay in processing requests, assurance that the application will be operational shortly, and a note that all received requests will be processed at that time.
- [ ] An apology for the delay in processing requests , assurance that the application will be operational shortly, and a note that all requests made in the last ten days will need to be resubmitted (because the portion of the application that processes received requests was down)

13.
You design an application that checks for new items in an S3 bucket once per hour. If new items exist, a message is added to an SQS queue. You have several EC2 instances which retrieve messages from the SQS queue, parse the file, and send you an email containing the relevant information from the file. You upload one test file to the bucket, wait a couple hours, and find that you have hundreds of emails from the application. What is the most likely cause for this volume of email?
**Choose the correct answer:**
- [ ] You can only have one EC2 instance polling the SQS queue at a time
- [ ] This is expected behavior when using short polling because SQS does not guarantee that there will not be duplicate messages processed
- [ ] This is expected behavior when using long polling because SQS does not guarantee that there will not be duplicate messages processed
- [x] Your application does not issue a delete command to the SQS queue after processing the message

14.
Your web application front end consists of multiple EC2 instances behind an Elastic Load Balancer. You configured the ELB to perform health checks on these EC2 instances. If an instance fails to pass health checks, which statement is true?
**Choose the correct answer:**
- [x] The ELB stops sending traffic to the instance that failed its health check.
- [ ] The instance is replaced automatically by the ELB
- [ ] The instance gets quarantined by the ELB for root cause analysis
- [ ] The instance gets terminated automatically by the ELB

15.
You create an SQS queue and decide to test it out by creating a simple application which looks for messages in the queue. When a message is retrieved, the application is supposed to delete the message. You create three test messages in your SQS queue and discover that messages 1 and 3 are quickly deleted, but message 2 remains in the queue. What is a possible cause for this behavior?
**Choose the 2 correct answers:**
- [ ] Message 2 uses JSON formatting
- [ ] You failed to set the correct permissions on message 2
- [x] The order that messages are received in is not guaranteed in SQS
- [x] Your application is using short polling

16.
What is the minimum size of an S3 object?
**Choose the correct answer:**
- [ ] 1 Byte
- [ ] 1 GB
- [x] 0 Bytes
- [ ] 1 TB

17.
Currently, you're helping design and architect a highly-available application. After building the initial environment, you've found that part of your application does not work correctly until port 443 is added to the security group. After adding port 443 to the appropriate security group, how much time will it take before the changes are applied and the application begins working correctly?
**Choose the correct answer:**
- [ ] It will take 60 seconds for the rules to apply to all Availability Zones within the region
- [ ] Generally, it takes 2-5 minutes for the rules to propagate
- [x] Changes apply instantly to the security group, and the application should be able to imediately respond to 443 requests
- [ ] Immediately after a reboot of the EC2 instances belong to that security group

18.
To prevent in-flight tampering, all requests sent with API keys over REST or Query API should be sent over HTTPS connection.
**Choose the correct answer:**
- [x] True
- [ ] False

19.
You and a colleague create an SQS queue and create several messages in it. You both test your ability to manually poll the queue by using the command-line API calls. After testing, you find that your colleague’s polling attempt retrieved messages 1, 3, and 5. Your polling attempt retrieved messages 4, 6, and 8. Nether of your attempts retrieved messages 2 or 7. What is a possible cause for this behavior?
**Choose the 2 correct answers:**
- [x] You and your colleague did not see the same messages because of the visibility timeout
- [ ] When manually polling the queue, you can only retrieve messages that you created
- [ ] SQS security group rules are prohibiting you and your colleague from retrieving messages from SQS servers in different subnets from your client computers
- [x] You and your colleague used short polling

20.
Your company has moved a legacy application from an on-premises data center to the cloud. The legacy application requires a static IP address hard-coded into the backend, which prevents you from deploying the application with high availability and fault tolerance using the ELB. Which steps would you take to apply high availability and fault tolerance to this application?
**Choose the 2 correct answers:**
- [x] Ensure that the instance it's using has an elastic IP address assigned to it
- [x] Write a custom script that pings the health of the instance, and, if the instance stops responding, switches the elastic IP address to a standby instance
- [ ] Do not migrate the application to the cloud until it can be converted to work with the ELB and Auto Scaling
- [ ] Create an AMI of the instance and launch it using Auto Scaling, which will deploy the instance again if it becomes unhealthy

21.
Which of the following AWS services allow you access to the underlying operating system?
**Choose the 2 correct answers:**
- [ ] Amazon RDS
- [ ] Amazon S3
- [x] Amazon EMR
- [x] Amazon Elastic Beanstalk

22.
What is the maximum size of a general SSD EBS volume?
**Choose the correct answer:**
- [ ] 2TiB
- [x] 16TiB
- [ ] 16TB
- [ ] 4Gib

23.
Your supervisor calls you wanting to know why an SWF workflow you created has not made any progress in the last three weeks. What is the most likely explanation for the workflow’s behavior?
**Choose the correct answer:**
- [ ] The workflow has exceeded SWF’s 14-day maximum workflow execution time
- [ ] The last task has exceeded SWF’s 14-day maximum task execution time
- [ ] SWF does not support the tasks you created for on-premises servers, so the workflow has entered a paused state
- [x] SWF is awaiting human input from an activity task you assigned to your supervisor

24.
While implementing a disaster recovery strategy in another region, you are attempting to move the data from one EBS volume to another in a separate region. What is the best way to do this? Keep in mind this is not a live production replication copy.
**Choose the correct answer:**
- [ ] Copy the snapshot from S3 by enabling S3 region replication
- [ ] Configure VPC peering to setup a direct link and copy a snapshot of the volume
- [ ] Configure rsync on your instance and sync the data across regions to another configured EC2 instance
- [x] Take a snapshot of the EBS volume and copy it to the desired region

25.
In order to establish a successful site-to-site VPN connection from your on-premises network to the VPC (Virtual Private Cloud), which of the following needs to be configured inside of the VPC?
**Choose the correct answer:**
- [ ] The main route table to route traffic through a NAT instance
- [ ] An Elastic IP address to the Virtual Private Gateway
- [x] A public IP address on the customer gateway for the on-premise network
- [ ] A dedicated NAT instance in a public subnet

26.
One of your more important clients is a Telecom business who needs to process some real-time data in a distributed manner. They suggest to you that they think they should use either Amazon SQS or Amazon Kinesis to achieve this and they want you to tell them what would be the difference between the two. After some research, you decide that they should use Kinesis and are trying to put together some reasons for this. One of the below statements is INCORRECT, regarding this. Which one?
**Choose the correct answer:**
- [ ] Kinesis has the ability to consume data records in the same order a few hours later
- [ ] Kinesis has the ability for multiple applications to consume the same stream concurrently
- [x] Kinesis cannot route related data records to the same record processor (as in streaming MapReduce).
- [ ] Amazon SQS, because of its distributed nature, does not, despite what the name suggests, guarantee FIFO(First in First Out). Kinesis can guarantee FIFO

27.
The AMI ID used in an Auto Scaling policy is configured in the _______.
**hoose the correct answer:**
- [x] Launch configuration
- [ ] Group policy
- [ ] Auto Scaling group
- [ ] None of the above

28.
Amazon Auto Scaling is not meant to handle instant load spikes but is built to grow with a gradual increase in usage over a short time period.
**Choose the correct answer:**
- [x] True
- [ ] False

29.
You are consulting for a finance company that has specific backup and archiving policies. This company's RTO for all financial documents created in the past 6 months is 1 hour. You need to configure a setup that allows for all documents that are 6 months or older to be sent automatically for archiving in a lower-cost but highly durable archive environment. Given that the company is using a Storage Gateway, gateway-stored configuration, which of the following would be the best setup to reach the objectives?
**Choose the correct answer:**
- [ ] Enable an S3 lifecycle policy to integrate into Amazon EBS for a good backup solution
- [ ] Enable an S3 lifecycle policy to immediately send all objects added to the bucket to Glacier
- [ ] Enable versioning on the S3 connected bucket to the Gateway Storage configuration
- [x] Enable S3 versioning with a lifecycle policy that sends objects older than 6 months to Amazon Glacier

30.
You are asked to perform a security audit on a company’s AWS environment. You log in to their AWS account with the root user credentials and discover that they are using a VPN to connect to and manage their private EC2 instances. Upon further inspection, you find that they are not regularly patching their RDS instances. Finally, you notice that they are using IAM policies rather than bucket policies to manage access to their S3 buckets. What do you cite as the most critical security risk in your report?
**Choose the correct answer:**
- [x] The company allows people to log in with their AWS account’s root user
- [ ] The company has not been patching their RDS instances
- [ ] The company’s employees are not using a bastion host to connect to their private EC2 instances
- [ ] The company is not using bucket policies to manage S3 bucket access

31.
One of your instances is reporting an unhealthy system status check. However, this is not something you should have to monitor and repair on your own. How might you automate the repair of the system status check failure in an AWS environment?
**Choose the correct answer:**
- [ ] Write a script that queries the EC2 API for each instance status check
- [x] Create CloudWatch metrics that stop and start the instance based off of status check alarms
- [ ] Implement a third-party monitoring tool such as Nagios
- [ ] Write a script that periodically shuts down and starts instances

32.
Your company wants to back up the onsite file server to AWS but does not want to serve the files from S3 to your office network when files need to be accessed. Which service and setup would you use to accomplish this task?
**Choose the correct answer:**
- [ ] Configure an EBS volume, open the security group to allow for NFS, and mount the volume on the local network
- [ ] Use Amazon Storage Gateway and gateway-cached volumes to store the data locally and asynchronously backup point-in-time snapshots to S3
- [x] Use Amazon Storage Gateway and gateway-stored volumes to store the data locally and asynchronously backup point-in-time snapshots to S3
- [ ] Use Amazon import/export

33.
Which of the following services allow the administrator access to the underlying operating system?
**Choose the 2 correct answers:**
- [ ] Amazon RDS
- [x] Amazon EMR
- [ ] DynamoDB
- [x] Amazon EC2

34.
Your company has an application that requires access to a NoSQL database. Your IT department has no desire to manage the NoSQL servers. Which Amazon service provides a fully-managed and highly available NoSQL service?
**Choose the correct answer:**
- [ ] SimpleDB
- [ ] Amazon RDS
- [ ] ElasticMap Reduce
- [x] DynamoDB

35.
You are a consultant tasked with migrating an on-premises application architecture to AWS. During your design process, you have to give consideration to current on-premises security and determine which security attributes you are responsible for on AWS. Which of the following does AWS provide for you as part of the shared responsibility model?
**Choose the correct answer:**
- [ ] Instance security
- [ ] Virtualization infrastructure
- [ ] User access to the AWS environment
- [x] Physical network infrastructure

36.
Auto Scaling is a tool used for creating elastic and self-healing applications.
**Choose the correct answer:**
- [x] True
- [ ] False

37.
You are designing a global application that takes advantage of multiple regions. As part of your application, the need to synchronize from one region to another is required to ensure your application is serving the same data when employing latency-based Route 53 DNS records. To ensure this happens, you have determined that using the AWS CLI to sync files from the primary storage servers to S3 is the best method. How might you implement AWS CLI authentication against the S3 service?
**Choose the correct answer:**
- [ ] Create a cross-account role and deploy the EC2 instances that need to sync data into separate AWS accounts
- [ ] For each region, create an IAM EC2 instance role and assign it to the instance that needs to utilize the AWS CLI to sync the data from S3
- [ ] Assign API credentials for a standard user, configure the API keys in the AMI, and copy the AMI to all the regions for deployment
- [x] Create an EC2 IAM role and assign it to each EC2 instance that utilizes the AWS CLI to sync the data

38.
Which of the following is not expected behavior from SQS and may indicate a problem with your application?
**Choose the correct answer:**
- [ ] Messages are retrieved from your SQS queue in a different order than they were created
- [ ] A message in your SQS queue is duplicated
- [ ] A 500 KB message fails to be created in an SQS queue
- [x] Messages in JSON format fail to be created in the SQS queue

39.
Your supervisor asks you to create a decoupled application using EC2 instances polling an SQS queue. Which of the following is not necessary to accomplish this goal?
**Choose the correct answer:**
- [ ] An IAM role allowing EC2 instances to modify an SQS queue
- [ ] Application code which polls for messages in an SQS queue
- [x] An Elastic Load Balancer to distribute traffic from EC2 instances to the SQS queue
- [ ] Multiple EC2 application server instances

40.
Amazon Glacier is designed for:
**Choose the 2 correct answers:**
- [x] Infrequently accessed data
- [x] Data archives
- [ ] Active database storage
- [ ] Cached session data

41.
Your EC2 instances are configured to run behind an Amazon VPC. You have assigned two web serves instances to an Elastic Load Balancer. However, the instances and the ELB are not reachable via URL to the elastic load balancer serving the web app data from the EC2 instances. How might you resolve the issue so that your instances are serving the web app data to the public internet?
**Choose the correct answer:**
- [x] Attach an internet gateway to the VPC and route it to the subnet
- [ ] Add an elastic IP address to the instance
- [ ] Use Amazon Elastic Load Balancer to serve requests to your instances located in the internal subnet
- [ ] None of the above

42.
Your AWS environment contains several reserved EC2 instances dedicated to a project that has just been cancelled. Your supervisor wants to stop incurring charges for these reserved instances immediately and recuperate as much of the reserved instance cost as possible. What can you do to avoid being charged for them?
**Choose the 2 correct answers:**
- [x] Terminate the instances as soon as possible
- [ ] Contact AWS and explain the situation
- [ ] Sell the reserved instances on the AWS Reserved Instance Marketplace
- [ ] Stop the instances as soon as possible

43.
Your company is building it's first deployment on AWS and is concerned about security in the cloud. There will be a lot of online payment transactions happening once the infrastructure is deployed. Your security officer has come to you and wants to know whether they should be using the Hardware Security Module (HSM) or AWS Key Management Service (KMS) for encryption. Which of the following would be the most correct response to give him?
**Choose the correct answer:**
- [ ] AWS CloudHSM should be always be used for any payment transactions
- [x] KMS is probably adequate unless additional protection is necessary for some applications and data that are subject to strict contractual or regulatory requirements for managing cryptographic keys, then HSM should be used
- [ ] AWS CloudHSM does not support the processing, storage, and transmission of credit card data by a merchant or service provider, as it has not been validated as being compliant with Payment Card Industry (PCI) Data Security Standard (DSS); hence, you will need to use KMS
- [ ] It probably doesn't matter as they both do the same thing

44.
After building a new VPC from scratch, you have attached an internet gateway to the only route table within your VPC. This means all instances currently belong to a public subnet. While trying to connect to one of the instances over the internet gateway, you experience connectivity issues preventing any communication from your machine to the instance over the internet. After investigating, you notice that the security group has proper permissions and you need to:
**Choose the correct answer:**
- [ ] Attach the internet gateway to the VPC
- [x] Change the route table Destination for the IGW to be 0.0.0.0/0
- [ ] Change the route table Destination for the IGW to be 10.0.0.0/16
- [ ] Update the local route to 0.0.0.0/0

45.
Your supervisor is upset that a client’s purchase from your website was processed twice. You find out that the order process involves EC2 instances processing messages from an SQS queue. What action would you recommend to ensure this does not happen again?
**Choose the correct answer:**
- [x] Modify the order process to use SWF
- [ ] Increase the visibility timeout for the queue
- [ ] Insert code into the application to delete messages after processing
- [ ] Use long polling rather than short polling

46.
After migrating an application architecture from on-premises to AWS you will not be responsible for the ongoing maintenance of packages for the following AWS services that your application uses:
**Choose the 2 correct answers:**
- [x] RDS
- [ ] Elastic Beanstalk
- [ ] EC2
- [x] DynamoDB

47.
When designing a cloud service based on AWS and you choose to use RRS on S3 instead of S3 standard storage type, what type of trade offs do you have to build your application around?
**Choose the correct answer:**
- [ ] With RRS, in order to build automation buckets, you need to have specific ACLs added
- [ ] RRS only has 99.99% availability
- [ ] With RRS you have to check-in and check-out jobs which can take up to 6 hours
- [x] RRS only has 99.99% durability and you have to design automation around replacing lost objects

48.
Which statement is true about Amazon SQS?
**Choose the 2 correct answers:**
- [ ] Amazon SQS guarantees delivery of AT LEAST 1 message and the message order which it is sent/received
- [x] Amazon SQS (Simple Queue Service) guarantees delivery of AT LEAST 1 message but cannot guarantee it will not create duplicates
- [ ] Amazon SQS (Simple Queue Service) guarantees delivery of AT LEAST 1 message and guarantees it will not create duplicates
- [x] Amazon SQS guarantees delivery of AT LEAST 1 message but cannot guarantee message order, although does attempt to

49.
Your supervisor asks you to create a highly available website which serves static content from EC2 instances. Which of the following is not a requirement to accomplish this goal?
**Choose the correct answer:**
- [ ] Multiple subnets
- [ ] Multiple Availability Zones
- [x] An SQS queue
- [ ] An Auto Scaling group to recover from EC2 instance failures

50.
Your application's usage peaks at 90% during the hours of 9 AM and 10 AM everyday. All other hours require only 10% of the peak resources. What is the best way to scale your application so you're only paying for max resources during peak hours?
**Choose the correct answer:**
- [ ] Run enough instances to handle peek capacity
- [ ] Proactive event-based scaling
- [ ] Auto Scaling by demand
- [x] Proactive Cycle Scaling

51.
You've been contacted by a client who is having connectivity issues on their Amazon Virtual Private Cloud and EC2 instances. After logging in to the environment, you notice that the customer is using four instances that all belong to a subnet with an attached internet gateway. The instances also belong to the same security group. However, one of the instances is not able to send or receive traffic like the other three. After logging in to the internal network and investigating, you find that the instance is working as expected and determine it is not an operating system issue. Which of the following is missing from the environment and is preventing that single instance from connecting?
**Choose the correct answer:**
- [x] The EC2 instance does not have a public IP address associated with it
- [ ] The EC2 instance is not a member of the same Auto Scaling group/policy
- [ ] A proper route table configuration that sends traffic from the instance to the internet through the internet gateway
- [ ] The EC2 instance is running in an Availability Zone that does not support internet gateways

52.
You are the system administrator for your company's AWS account of approximately 200 IAM users. A new company policy has just been introduced that will change the access of 50 of the IAM users to have unlimited access to S3 buckets. How can you implement this effectively so that there is no need to apply the policy at the individual user level?
**Choose the correct answer:**
- [ ] Create a policy and apply it to multiple users using a JSON script
- [x] Use the IAM groups and add users, based upon their role, to different groups and apply the policy to group
- [ ] Create a new role and add each user to the IAM role
- [ ] Create an S3 bucket policy with unlimited access which includes each user's AWS account ID

53.
You are planning on creating an EC2 instance that will create S3 objects and modify CloudWatch alarms. What is the best way to deploy this instance?
**Choose the correct answer:**
- [x] Assign an S3 policy and a CloudWatch policy to a single IAM role. Assign the IAM role to the instance at deployment time
- [ ] Assign an S3 policy to one IAM role and a CloudWatch policy to another IAM role. - [ ] Assign both IAM roles to the EC2 instance at deployment time
- [ ] Assign an S3 policy and a CloudWatch policy to a single IAM user. Have the instance execute tasks as the IAM user
- [ ] Assign an S3 policy to one IAM user and a CloudWatch policy to another IAM user. Have the instance execute tasks as the appropriate IAM user for the given task

54.
You have been told that you need to set up a bastion host by your manager in the cheapest, most secure way, and that you should be the only person that can access it via SSH. Which of the following setups would satisfy your manager's request?
**Choose the correct answer:**
- [ ] A large EC2 instance and a security group which only allows access on port 22
- [x] A small EC2 instance and a security group which only allows access on port 22 via your IP address
- [ ] A large EC2 instance and a security group which only allows access on port 22 via your IP address
- [ ] A small EC2 instance and a security group which only allows access on port 22

55.
A user needs access to Elastic Load Balancing. This is the first and possibly only time that they will require this access. Which of the following choices would be the best way to allow this access?
**Choose the correct answer:**
- [x] Delegate access to the ELB using an IAM role
- [ ] Give them temporary access to your account for 24 hours only and change the password the next day
- [ ] Create a new IAM user who only has access to the ELB resources and delete that user when he has finished his work
- [ ] Open up whichever port ELB uses in a security group and give the user access to that security group in a policy

56.
Which of the following best describes what "bastion hosts" are?
**Choose the correct answer:**
- [x] Bastion hosts are instances that sit within your public subnet and are typically accessed using SSH or RDP. Once remote connectivity has been established with a bastion host, it then acts as a ‘jump’ server, allowing you to use SSH or RDP to log in to other instances (within private subnets) deeper within your network.
- [ ] Bastion hosts are instances that sit within your private subnet and are typically accessed using SSH or RDP. Once remote connectivity has been established with the bastion host, it then acts as a 'jump' server, allowing you to use HTTPS to log in to other instances (within public subnets) deeper within your network.
- [ ] Bastion hosts are instances that sit within your public subnet and are typically accessed using SSH or RDP. Once remote connectivity has been established with the bastion host, it then acts as a ‘jump’ server, allowing you to use HTTPS to log in to other instances (within private subnets) deeper within your network.
- [ ] Bastion hosts are instances that sit within your private subnet and are typically accessed using SSH or RDP. Once remote connectivity has been established with the bastion host, it then acts as a ‘jump’ server, allowing you to use SSH or RDP to log in to other instances (within public subnets) deeper within your network.

57.
Your company is moving their entire 20 TB data warehouse to the cloud. With your current bandwidth it would take 2 months to transfer the data. Which service would allow you to quickly get your data into AWS?
**Choose the correct answer:**
- [ ] Amazon S3 MultiPart Upload
- [ ] Amazon S3 Connector
- [x] Amazon Import/Export
- [ ] Amazon Direct Connect

58.
Which of the following relational database servers are available on Amazon RDS?
Choose the 3 correct answers:
- [ ] DB2
- [x] MySQL
- [x] Aurora
- [x] MariaDB

59.
You can deny the AWS root account to EC2 instances via IAM policy.
**Choose the correct answer:**
- [ ] True
- [x] False

60.
What is the difference between an Availability Zone and an edge location?
**Choose the correct answer:**
- [ ] An Availability Zone is a grouping of AWS resources in a specific region; an edge location is a specific resource within the AWS region
- [ ] An edge location is used as a link when building load balancing between regions
- [ ] Edge locations are used as control stations for AWS resources
- [x] An Availability Zone is an Amazon resource within an AWS region; an edge location will deliver cached content to the closest location to reduce latency

61.
You are asked to review a plan that your company has made to create a new application that makes use of SQS, EC2, Auto Scaling, and CloudWatch. Which of the following action items should you advise your company not to implement?
**Choose the correct answer:**
- [ ] Utilize AutoScaling to deploy new EC2 instances if the SQS queue grows too large
- [ ] Utilize CloudWatch alarms to alert when the number of messages in the SQS queue grows too large
- [ ] Utilize an IAM role to grant EC2 instances permission to modify the SQS queue
- [x] Utilize short polling with a wait time of 20 seconds to reduce the number of empty responses from the SQS queue

62.
Which region ID is the US Standard region?
**Choose the correct answer:**
- [ ] us-east-1a
- [ ] us-east-2
- [ ] eu-east-1
- [x] us-east-1

63.
When designing an application architecture utilizing EC2 instances and the ELB, to determine the instance size required for your application, what questions might be important?
**Choose the 2 correct answers:**
- [x] Determining the minimum memory requirements for an application
- [ ] Determining where the client intends to serve most of the traffic
- [ ] Determining the peek expected usage for a clients application
- [x] Determining the required I/O operations

64.
You have 5 Cloudformation templates. Each template is for a different application architecture. These architectures vary between your blog apps and your gaming apps. What determines the cost of using the Cloudformation templates?
**Choose the correct answer:**
- [ ] Only for Cloudformation templates that go over the allowed limit
- [ ] $0.10 per template per month
- [x] Cloudformation does not have a cost but you are charged for the underlying resources it builds
- [ ] The length of time it takes to build the architecture with CloudFormation

65.
You are setting up a VPC peering connection with another VPC. This is the first time that you have done this, and you are not that familiar with the limitations and rules. When reading up on this, you discover that there seems to be a lot of limitations and rules when it comes to VPC peering. Which of the following is NOT one of those limitations or rules?
**Choose the correct answer:**
- [x] A placement group cannot span peered VPCs
- [ ] You cannot create a VPC peering connection between VPCs in different regions
- [ ] You cannot create a VPC peering connection between VPCs that have matching or overlapping CIDR blocks
- [ ] You cannot have more than one VPC peering connection between the same two VPCs at the same time

66.
You create an SQS queue with the default settings for a new application your company is deploying. While new messages are added to the queue throughout the week, management has indicated that the application which retrieves the messages should only be run during your company’s weekly Sunday evening maintenance window. It is quickly noticed on Monday morning that several messages were not processed the previous evening and the messages are no longer in the queue. What is a likely cause for this issue?
**Choose the correct answer:**
- [ ] The EC2 instances the application runs on have permission to the queue, but not to some of the messages in the queue
- [x] The messages surpassed the retention period for the queue
- [ ] Your application was using long polling, so some messages may not have been returned
- [ ] The EC2 instances the application runs on are in a different subnet than the SQS queue

67.
An AWS VPC (Virtual Private Cloud) allows you to _______.
**Choose the correct answer:**
- [ ] Not have to monitor security
- [x] Connect your cloud resources to your own encrypted IPSec VPN connections
- [ ] Provision unlimited S3 resources
- [ ] None of the above

68.
Given the following region design, what is the bare minimum for configuring high availability and why? 
Two Availability Zones within a region, az-a and az-b.
**Choose the correct answer:**
- [x] Create an ELB that serves traffic to two instances, one instance in each Availability Zone, and enable cross-zone load balancing on the ELB, then create an Auto Scaling Group, because this applies high availability if a single Availability Zone is no longer available
- [ ] Create an ELB that serves traffic to two instances, one instance in each Availability Zone, and enable cross-zone load balancing on the ELB, because this applies high availability if a single Availability Zone is no longer available
- [ ] Create an ELB that serves traffic to one instance, two instances in each Availability Zone, and enable cross-zone load balancing on the ELB, because this applies high availability if a single availability zone is no longer available
- [ ] Create an ELB that serves traffic to two instances, one instance in each Availability Zone, because this applies high availability if a single Availability Zone is no longer available

69.
Does S3 provide read-after-write consistency for new objects?
**Choose the correct answer:**
- [x] Yes, for all regions
- [ ] Yes, but only for certain regions and for new objects
- [ ] Yes, but only for certain regions, not the us-standard region
- [ ] No, not for any region

70.
You own an image manipulation application. Your users take a picture, upload it to your app, and request filters to be added to the image. You need to decouple the application so your users are not waiting for the image processing to take place. How would you go about doing this?
**Choose the correct answer:**
- [ ] Integrate with DynamoDB to allow messages to be sent back and forth between our worker instances and EC2 instances
- [x] Use Amazon SQS to store the requests using metadata and JSON in the message, use S3 to store the image, and Auto Scaling to determine when to fire off more worker instances based on queue size
- [ ] Use Amazon SNS to process image requests
- [ ] Use Amazon S3 to store the images and Amazon EC2 to process the request

71.
In AWS, when a request is made, the AWS service decides whether a given request should be allowed or denied. The distinction between a request being denied or allowed by default and an explicit deny in a policy is important. Which of the following statements best describes this distinction?
**Choose the correct answer:**
- [ ] By default, a request can either be allowed or denied depending on the request, and each can be overwritten by the other. In contrast, if a policy explicitly denies a request, that deny can't be overridden.
- [ ] By default, a request is allowed, but this can be overridden by a deny. In contrast, if a policy explicitly denies a request, that deny can't be overridden.
- [ ] By default, a request is denied, but this can be overridden by an allow. In contrast, if a policy explicitly denies a request, it can be overidden but only by certain requests.
- [x] By default, a request is denied, but this can be overridden by an allow. In contrast, if a policy explicitly denies a request, that deny can't be overridden.

72.
Your AWS environment contains several on-demand EC2 instances dedicated to a project that has just been cancelled. Your supervisor does not want to incur charges for these on-demand instances but also does not want to lose the data just yet because there is a chance the project may be revived in the next few days. What should you do to minimize charges for these instances in the meantime?
**Choose the correct answer:**
- [ ] Sell the instances on the AWS On-Demand Instance Marketplace. You can buy them back later if needed
- [x] Stop the instances as soon as possible
- [ ] Terminate the instances as soon as possible
- [ ] Contact AWS and explain the situation

73.
Which of the following statements is FALSE regarding the role of a bastion host?
**Choose the correct answer:**
- [ ] A bastion host sits on the outside of an internal network and is used as a gateway into the private network and is considered the critical strong point of the network
- [ ] A bastion host is used to SSH into the internal network to access private resources without a VPN
- [x] A bastion host should be on a private subnet and never a public subnet due to security concerns
- [ ] A bastion host should maintain extremely tight security and monitoring as it is available to the public

74.
Elasticity is a fundamental property of the cloud. What best describes elasticity?
**Choose the correct answer:**
- [x] Power to scale computing resources up and down easily with minimal friction
- [ ] The process by which scripts notify you of resource constraints so you can fix them manually
- [ ] Power to scale computing resources up easily but not down
- [ ] Ability to create services without having to administer resources

75.
You recently purchased four reserved EC2 instances in the US-East-1 region’s Availability Zone 1. Your supervisor just informed you that she would like the instances distributed equally across US-East-1 region Availability Zones 1 and 2. Can you use the reserved instances you just purchased to deploy EC2 instances in Availability Zone 2?
**Choose the correct answer:**
- [ ] No, you need to sell two of the current Availability Zone 1 reserved instances on AWS Reserved Marketplace and purchase two new reserved instances for Availability Zone 2
- [x] Yes, you can migrate the reserved instances to Availability Zone 2
- [ ] Yes, you can change the destination Availability Zone for the reserved instances by contacting AWS
- [ ] Yes, you can deploy two EC2 instances in Availability Zone 2 and they will be automatically billed as reserved instances since both Availability Zones are in the same region

76.
After deciding that, due to to strict contractual requirements, the latest AWS VPC that you deploy will need to incorporate AWS CloudHSM as an encryption solution, where within your AWS infrastructure would be the best place to physically locate the HSM appliances and why?
**Choose the correct answer:**
- [ ] Locate HSM appliances in a private subnet increases security
- [ ] Locate HSM appliances closest to the majority of potential customers decreases network latency, which can improve application performance
- [x] Locate HSM appliances near your EC2 instances decreases network latency, which can improve application performance
- [ ] Locate HSM appliances completely isolated from your EC2 instances in another region increases security

77.
You're building out an application on AWS that is running within a single region. However, you're designing with disaster recovery in mind. Your intention is to build the application so that if the current region becomes unavailable, you can failover to another region. Part of your application relies heavily on pre-built AMIs. To share those AMIs with the region you're using as a backup, what process would you take?
**Choose the correct answer:**
- [ ] Modify the image permissions to share the AMI with another account, then set the default region to the backup region
- [ ] Nothing, because all AMIs are available in any region as long as it is created within the same account
- [x] Copy the AMI from the current region to another region, modify the Auto Scaling groups in the backup region to use the new AMI ID in the backup region
- [ ] Modify the image permissions to share to the designated backup region

78.
You have 8 instances running on your VPC and all 10 of your users (5 production and 5 development) currently have access to all the instances. However, you have been told that because 4 of the instances are used for production and 4 are used for development, you will need to set up access so that the 5 production people can only access the production server and the 5 development people can only access the development server. Using policies, which of the following would be the best way to accomplish this?
**Choose the correct answer:**
- [ ] Launch the test and production instances in separate VPCs and use VPC peering
- [ ] Launch the test and production instances in different Availability Zones and use Multi Factor Authentication
- [x] Define the tags on the test and production servers, and add a condition to the IAM policy which allows access to specific tags
- [ ] Create an IAM policy with a condition which allows access to only instances that are used for production or development

79.
You are working for a startup company that is building an application that receives large amounts of data. Unfortunately, current funding has left the startup short on cash, unable to afford thousands of dollars of storage hardware. The company has opted to use AWS. Which services would you implement to store a virtually unlimited amount of data without any effort to scale when demand unexpectedly increases?
**Choose the correct answer:**
- [x] Amazon S3, because it provides unlimited amounts of storage data, scales automatically, is highly available, and durable
- [ ] Amazon EC2, because EBS volumes can scale to hold any amount of data and, when used with Auto Scaling, can be designed for fault tolerance and high availability
- [ ] Amazon Import/Export, because Amazon assists in migrating large amounts of data to Amazon S3
- [ ] Amazon Glacier, to keep costs low for storage and scale infinitely
