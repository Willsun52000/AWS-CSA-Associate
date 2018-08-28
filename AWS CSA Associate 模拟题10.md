## AWS CSA Associate 模拟题10

642.
Amazon RDS automated backups and DB Snapshots are currently supported for only the __________ storage engine
- [x] InnoDB
- [ ] MyISAM

643.
Automated backups are enabled by default for a new DB Instance.
- [x] TRUE
- [ ] FALSE

644.
Amazon RDS DB snapshots and automated backups are stored in
- [x] Amazon S3
- [ ] Amazon EBS Volume
- [ ] Amazon RDS
- [ ] Amazon EMR

645.
You receive a frantic call from a new DBA who accidentally dropped a table containing all your customers. Which Amazon RDS feature will allow you to reliably restore your database to within 5 minutes of when the mistake was made?
- [ ] Multi-AZ RDS
- [ ] RDS snapshots
- [ ] RDS read replicas
- [x] RDS automated backup

646.
Disabling automated backups ______ disable the point-in-time recovery.
- [ ] if configured to can
- [ ] will never
- [x] will

647.
Changes to the backup window take effect ______.
- [ ] from the next billing cycle
- [ ] after 30 minutes
- [x] immediately
- [ ] after 24 hours

648.
You can modify the backup retention period; valid values are 0 (for no backup retention) to a maximum of ___________ days.
- [ ] 45
- [x] 35
- [ ] 15
- [ ] 5

649.
Amazon RDS automated backups and DB Snapshots are currently supported for only the ______ storage engine
- [ ] MyISAM
- [x] InnoDB 

650.
What happens to the I/O operations while you take a database snapshot?
- [x] I/O operations to the database are suspended for a few minutes while the backup is in progress.
- [ ] I/O operations to the database are sent to a Replica (if available) for a few minutes while the backup is in progress.
- [ ] I/O operations will be functioning normally
- [ ] I/O operations to the database are suspended for an hour while the backup is in progress

651.
True or False: When you perform a restore operation to a point in time or from a DB Snapshot, a new DB Instance is created with a new endpoint.
- [ ] FALSE
- [x] TRUE 

652.
True or False: Manually created DB Snapshots are deleted after the DB Instance is deleted.
- [ ] TRUE
- [x] FALSE

653.
A user is running a MySQL RDS instance. The user will not use the DB for the next 3 months. How can the user save costs?
- [ ] Pause the RDS activities from CLI until it is required in the future
- [ ] Stop the RDS instance
- [x] Create a snapshot of RDS to launch in the future and terminate the instance now
- [ ] Change the instance size to micro

654.
Can I encrypt connections between my application and my DB Instance using SSL?
- [ ] No
- [x] Yes
- [ ] Only in VPC
- [ ] Only in certain regions

655.
Which of these configuration or deployment practices is a security risk for RDS?
- [ ] Storing SQL function code in plaintext
- [ ] Non-Multi-AZ RDS instance
- [ ] Having RDS and EC2 instances exist in the same subnet
- [x] RDS in a public subnet (Making RDS accessible to the public internet in a public subnet poses a security risk, by making your database directly addressable and spammable. DB instances deployed within a VPC can be configured to be accessible from the Internet or from EC2 instances outside the VPC. If a VPC security group specifies a port access such as TCP port 22, you would not be able to access the DB instance because the firewall for the DB instance provides access only via the IP addresses specified by the DB security groups the instance is a member of and the port defined when the DB instance was created. Refer link)

656.
A user has launched an RDS MySQL DB with the Multi AZ feature. The user has scheduled the scaling of instance storage during maintenance window. What is the correct order of events during maintenance window? 1. Perform maintenance on standby 2. Promote standby to primary 3. Perform maintenance on original primary 4. Promote original master back as primary
- [ ] 1, 2, 3, 4
- [x] 1, 2, 3
- [ ] 2, 3, 4, 1

657.
Can I control if and when MySQL based RDS Instance is upgraded to new supported versions?
- [ ] No
- [ ] Only in VPC
- [x] Yes

658.
A user has scheduled the maintenance window of an RDS DB on Monday at 3 AM. Which of the below mentioned events may force to take the DB instance offline during the maintenance window?
- [ ] Enabling Read Replica
- [ ] Making the DB Multi AZ
- [ ] DB password change
- [x] Security patching

659.
A user has launched an RDS postgreSQL DB with AWS. The user did not specify the maintenance window during creation. The user has configured RDS to update the DB instance type from micro to large. If the user wants to have it during the maintenance window, what will AWS do?
- [ ] AWS will not allow to update the DB until the maintenance window is configured
- [x] AWS will select the default maintenance window if the user has not provided it
- [ ] AWS will ask the user to specify the maintenance window during the update
- [ ] It is not possible to change the DB size from micro to large with RDS

660.
Can I test my DB Instance against a new version before upgrading?
- [ ] No
- [x] Yes
- [ ] Only in VPC

661.
You run a web application with the following components Elastic Load Balancer (ELB), 3 Web/Application servers, 1 MySQL RDS database with read replicas, and Amazon Simple Storage Service (Amazon S3) for static content. Average response time for users is increasing slowly. What three CloudWatch RDS metrics will allow you to identify if the database is the bottleneck? Choose 3 answers
- [x] The number of outstanding IOs waiting to access the disk
- [x] The amount of write latency
- [ ] The amount of disk space occupied by binary logs on the master.
- [x] The amount of time a Read Replica DB Instance lags behind the source DB Instance
- [ ] The average number of disk I/O operations per second.

662.
Typically, you want your application to check whether a request generated an error before you spend any time processing results. The easiest way to find out if an error occurred is to look for an __________ node in the response from the Amazon RDS API.
- [ ] Incorrect
- [x] Error
- [ ] FALSE

663.
In the Amazon CloudWatch, which metric should I be checking to ensure that your DB Instance has enough free storage space?
- [ ] FreeStorage
- [x] FreeStorageSpace
- [ ] FreeStorageVolume
- [ ] FreeDBStorageSpace

664.
A user is receiving a notification from the RDS DB whenever there is a change in the DB security group. The user does not want to receive these notifications for only a month. Thus, he does not want to delete the notification. How can the user configure this?
- [ ] Change the Disable button for notification to “Yes” in the RDS console
- [ ] Set the send mail flag to false in the DB event notification console
- [ ] The only option is to delete the notification from the console
- [x] Change the Enable button for notification to “No” in the RDS console

665.
A sys admin is planning to subscribe to the RDS event notifications. For which of the below mentioned source categories the subscription cannot be configured?
- [ ] DB security group
- [ ] DB snapshot
- [x] DB options group
- [ ] DB parameter group

666.
A user is planning to setup notifications on the RDS DB for a snapshot. Which of the below mentioned event categories is not supported by RDS for this snapshot source type?
- [x] Backup (Refer link)
- [ ] Creation
- [ ] Deletion
- [ ] Restoration

667.
A system admin is planning to setup event notifications on RDS. Which of the below mentioned services will help the admin setup notifications?
- [ ] AWS SES
- [ ] AWS Cloudtrail
- [ ] AWS CloudWatch
- [x] AWS SNS

668.
A user has setup an RDS DB with Oracle. The user wants to get notifications when someone modifies the security group of that DB. How can the user configure that?
- [ ] It is not possible to get the notifications on a change in the security group
- [ ] Configure SNS to monitor security group changes
- [x] Configure event notification on the DB security group
- [ ] Configure the CloudWatch alarm on the DB for a change in the security group

669.
It is advised that you watch the Amazon CloudWatch “_____” metric (available via the AWS Management Console or Amazon Cloud Watch APIs) carefully and recreate the Read Replica should it fall behind due to replication errors.
- [ ] Write Lag
- [ ] Read Replica
- [x] Replica Lag
- [ ] Single Replica

670.
You are running a database on an EC2 instance, with the data stored on Elastic Block Store (EBS) for persistence At times throughout the day, you are seeing large variance in the response times of the database queries Looking into the instance with the isolate command you see a lot of wait time on the disk volume that the database’s data is stored on. What two ways can you improve the performance of the database’s storage while maintaining the current persistence of the data? Choose 2 answers
- [ ] Move to an SSD backed instance
- [x] Move the database to an EBS-Optimized Instance
- [x] Use Provisioned IOPs EBS
- [ ] Use the ephemeral storage on an m2.4xLarge Instance Instead

671.
Which AWS service can help design architecture to persist in-flight transactions?
- [ ] Elastic IP Address
- [x] SQS
- [ ] Amazon CloudWatch
- [ ] Amazon ElastiCache

672.
A company has a workflow that sends video files from their on-premise system to AWS for transcoding. They use EC2 worker instances that pull transcoding jobs from SQS. Why is SQS an appropriate service for this scenario?
- [ ] SQS guarantees the order of the messages.
- [ ] SQS synchronously provides transcoding output.
- [ ] SQS checks the health of the worker instances.
- [x] SQS helps to facilitate horizontal scaling of encoding tasks

673.
Which statement best describes an Amazon SQS use case?
- [ ] Automate the process of sending an email notification to administrators when the CPU utilization reaches 70% on production servers (Amazon EC2 instances) (CloudWatch + SNS + SES)
- [x] Create a video transcoding website where multiple components need to communicate with each other, but can’t all process the same amount of work simultaneously (SQS provides loose coupling)
- [ ] Coordinate work across distributed web services to process employee’s expense reports (SWF – Steps in order and might need manual steps)
- [ ] Distribute static web content to end users with low latency across multiple countries (CloudFront + S3)

674.
Your application provides data transformation services. Files containing data to be transformed are first uploaded to Amazon S3 and then transformed by a fleet of spot EC2 instances. Files submitted by your premium customers must be transformed with the highest priority. How should you implement such a system?
- [ ] Use a DynamoDB table with an attribute defining the priority level. Transformation instances will scan the table for tasks, sorting the results by priority level.
- [ ] Use Route 53 latency based-routing to send high priority tasks to the closest transformation instances.
- [x] Use two SQS queues, one for high priority messages, and the other for default priority. Transformation instances first poll the high priority queue; if there is no message, they poll the default priority queue
- [ ] Use a single SQS queue. Each message contains the priority level. Transformation instances poll high-priority messages first.

675.
Your company plans to host a large donation website on Amazon Web Services (AWS). You anticipate a large and undetermined amount of traffic that will create many database writes. To be certain that you do not drop any writes to a database hosted on AWS. Which service should you use?
- [ ] Amazon RDS with provisioned IOPS up to the anticipated peak write throughput.
- [x] Amazon Simple Queue Service (SQS) for capturing the writes and draining the queue to write to the database
- [ ] Amazon ElastiCache to store the writes until the writes are committed to the database.
- [ ] Amazon DynamoDB with provisioned write throughput up to the anticipated peak write throughput.

676.
A customer has a 10 GB AWS Direct Connect connection to an AWS region where they have a web application hosted on Amazon Elastic Computer Cloud (EC2). The application has dependencies on an on-premises mainframe database that uses a BASE (Basic Available. Sort stale Eventual consistency) rather than an ACID (Atomicity, Consistency, Isolation, Durability) consistency model. The application is exhibiting undesirable behavior because the database is not able to handle the volume of writes. How can you reduce the load on your on-premises database resources in the most cost-effective way?
- [ ] Use an Amazon Elastic Map Reduce (EMR) S3DistCp as a synchronization mechanism between the onpremises database and a Hadoop cluster on AWS.
- [x] Modify the application to write to an Amazon SQS queue and develop a worker process to flush the queue to the on-premises database
- [ ] Modify the application to use DynamoDB to feed an EMR cluster which uses a map function to write to the on-premises database.
- [ ] Provision an RDS read-replica database on AWS to handle the writes and synchronize the two databases using Data Pipeline.

677.
An organization has created a Queue named “modularqueue” with SQS. The organization is not performing any operations such as SendMessage, ReceiveMessage, DeleteMessage, GetQueueAttributes, SetQueueAttributes, AddPermission, and RemovePermission on the queue. What can happen in this scenario?
- [ ] AWS SQS sends notification after 15 days for inactivity on queue
- [x] AWS SQS can delete queue after 30 days without notification
- [ ] AWS SQS marks queue inactive after 30 days
- [ ] AWS SQS notifies the user after 2 weeks and deletes the queue after 3 weeks.

678.
A user is using the AWS SQS to decouple the services. Which of the below mentioned operations is not supported by SQS?
- [ ] SendMessageBatch
- [ ] DeleteMessageBatch
- [ ] CreateQueue
- [x] DeleteMessageQueue

679.
A user has created a queue named “awsmodule” with SQS. One of the consumers of queue is down for 3 days and then becomes available. Will that component receive message from queue?
- [x] Yes, since SQS by default stores message for 4 days
- [ ] No, since SQS by default stores message for 1 day only
- [ ] No, since SQS sends message to consumers who are available that time
- [ ] Yes, since SQS will not delete message until it is delivered to all consumers

680.
A user has created a queue named “queue2” in US-East region with AWS SQS. The user’s AWS account ID is 123456789012. If the user wants to perform some action on this queue, which of the below Queue URL should he use?
- [x] http://sqs.us-east-1.amazonaws.com/123456789012/queue2
- [ ] http://sqs.amazonaws.com/123456789012/queue2
- [ ] http://sqs. 123456789012.us-east-1.amazonaws.com/queue2
- [ ] http://123456789012.sqs.us-east-1.amazonaws.com/queue2

681.
A user has created a queue named “myqueue” with SQS. There are four messages published to queue, which are not received by the consumer yet. If the user tries to delete the queue, what will happen?
- [ ] A user can never delete a queue manually. AWS deletes it after 30 days of inactivity on queue
- [x] It will delete the queue
- [ ] It will initiate the delete but wait for four days before deleting until all messages are deleted automatically.
- [ ] I t will ask user to delete the messages first

682.
A user has developed an application, which is required to send the data to a NoSQL database. The user wants to decouple the data sending such that the application keeps processing and sending data but does not wait for an acknowledgement of DB. Which of the below mentioned applications helps in this scenario?
- [ ] AWS Simple Notification Service
- [ ] AWS Simple Workflow
- [x] AWS Simple Queue Service
- [ ] AWS Simple Query Service

683.*
You are building an online store on AWS that uses SQS to process your customer orders. Your backend system needs those messages in the same sequence the customer orders have been put in. How can you achieve that?
- [ ] It is not possible to do this with SQS
- [x] You can use sequencing information on each message
- [ ] You can do this with SQS but you also need to use SWF
- [ ] Messages will arrive in the same order by default

684.
A user has created a photo editing software and hosted it on EC2. The software accepts requests from the user about the photo format and resolution and sends a message to S3 to enhance the picture accordingly. Which of the below mentioned AWS services will help make a scalable software with the AWS infrastructure in this scenario?
- [ ] AWS Glacier
- [ ] AWS Elastic Transcoder
- [ ] AWS Simple Notification Service
- [x] AWS Simple Queue Service

685.*
Refer to the architecture diagram of a batch processing solution using Simple Queue Service (SQS) to set up a message queue between EC2 instances, which are used as batch processors. Cloud Watch monitors the number of Job requests (queued messages) and an Auto Scaling group adds or deletes batch servers automatically based on parameters set in Cloud Watch alarms. You can use this architecture to implement which of the following features in a cost effective and efficient manner? 
- [ ] Reduce the overall time for executing jobs through parallel processing by allowing a busy EC2 instance that receives a message to pass it to the next instance in a daisy-chain setup.
- [ ] Implement fault tolerance against EC2 instance failure since messages would remain in SQS and worn can continue with recovery of EC2 instances implement fault tolerance against SQS failure by backing up messages to S3.
- [ ] Implement message passing between EC2 instances within a batch by exchanging messages through SOS.
- [x] Coordinate number of EC2 instances with number of job requests automatically thus Improving cost effectiveness
- [ ] Handle high priority jobs before lower priority jobs by assigning a priority metadata field to SQS messages.

686.
How does Amazon SQS allow multiple readers to access the same message queue without losing messages or processing them many times?
- [ ] By identifying a user by his unique id
- [ ] By using unique cryptography
- [x] Amazon SQS queue has a configurable visibility timeout
- [ ] Multiple readers can’t access the same message queue

687.
A user has created photo editing software and hosted it on EC2. The software accepts requests from the user about the photo format and resolution and sends a message to S3 to enhance the picture accordingly. Which of the below mentioned AWS services will help make a scalable software with the AWS infrastructure in this scenario?
- [ ] AWS Elastic Transcoder
- [ ] AWS Simple Notification Service
- [x] AWS Simple Queue Service
- [ ] AWS Glacier

688.
How do you configure SQS to support longer message retention?
- [x] Set the MessageRetentionPeriod attribute using the SetQueueAttributes method
- [ ] Using a Lambda function
- [ ] You can’t. It is set to 14 days and cannot be changed
- [ ] You need to request it from AWS

689.
A user has developed an application, which is required to send the data to a NoSQL database. The user wants to decouple the data sending such that the application keeps processing and sending data but does not wait for an acknowledgement of DB. Which of the below mentioned applications helps in this scenario?
- [ ] AWS Simple Notification Service
- [ ] AWS Simple Workflow
- [ ] AWS Simple Query Service
- [x] AWS Simple Queue Service

690.
If a message is retrieved from a queue in Amazon SQS, how long is the message inaccessible to other users by default?
- [ ] 0 seconds
- [ ] 1 hour
- [ ] 1 day
- [ ] forever
- [x] 30 seconds

691.
Which of the following statements about SQS is true?
- [ ] Messages will be delivered exactly once and messages will be delivered in First in, First out order
- [ ] Messages will be delivered exactly once and message delivery order is indeterminate
- [ ] Messages will be delivered one or more times and messages will be delivered in First in, First out order
- [x] Messages will be delivered one or more times and message delivery order is indeterminate (Before the introduction of FIFO queues)

692.
How long can you keep your Amazon SQS messages in Amazon SQS queues?
- [ ] From 120 secs up to 4 weeks
- [ ] From 10 secs up to 7 days
- [x] From 60 secs up to 2 weeks
- [ ] From 30 secs up to 1 week

693.
When a Simple Queue Service message triggers a task that takes 5 minutes to complete, which process below will result in successful processing of the message and remove it from the queue while minimizing the chances of duplicate processing?
- [x] Retrieve the message with an increased visibility timeout, process the message, delete the message from the queue
- [ ] Retrieve the message with an increased visibility timeout, delete the message from the queue, process the message
- [ ] Retrieve the message with increased DelaySeconds, process the message, delete the message from the queue
- [ ] Retrieve the message with increased DelaySeconds, delete the message from the queue, process the message

694.
You need to process long-running jobs once and only once. How might you do this?
- [ ] Use an SNS queue and set the visibility timeout to long enough for jobs to process.
- [ ] Use an SQS queue and set the reprocessing timeout to long enough for jobs to process.
- [x] Use an SQS queue and set the visibility timeout to long enough for jobs to process.
- [ ] Use an SNS queue and set the reprocessing timeout to long enough for jobs to process.

695.
You are getting a lot of empty receive requests when using Amazon SQS. This is making a lot of unnecessary network load on your instances. What can you do to reduce this load?
- [ ] Subscribe your queue to an SNS topic instead.
- [x] Use as long of a poll as possible, instead of short polls. (Refer link)
- [ ] Alter your visibility timeout to be shorter.
- [ ] Use <code>sqsd</code> on your EC2 instances.

696.
You have an asynchronous processing application using an Auto Scaling Group and an SQS Queue. The Auto Scaling Group scales according to the depth of the job queue. The completion velocity of the jobs has gone down, the Auto Scaling Group size has maxed out, but the inbound job velocity did not increase. What is a possible issue?
- [x] Some of the new jobs coming in are malformed and unprocessable. (As other options would cause the job to stop processing completely, the only reasonable option seems that some of the recent messages must be malformed and unprocessable)
- [ ] The routing tables changed and none of the workers can process events anymore. (If changed, none of the jobs would be processed)
- [ ] Someone changed the IAM Role Policy on the instances in the worker group and broke permissions to access the queue. (If IAM role changed no jobs would be processed)
- [ ] The scaling metric is not functioning correctly. (scaling metric did work fine as the autoscaling caused the instances to increase)

697.
Company B provides an online image recognition service and utilizes SQS to decouple system components for scalability. The SQS consumers poll the imaging queue as often as possible to keep end-to-end throughput as high as possible. However, Company B is realizing that polling in tight loops is burning CPU cycles and increasing costs with empty responses. How can Company B reduce the number of empty responses?
- [ ] Set the imaging queue visibility Timeout attribute to 20 seconds
- [x] Set the Imaging queue ReceiveMessageWaitTimeSeconds attribute to 20 seconds (Long polling. Refer link)
- [ ] Set the imaging queue MessageRetentionPeriod attribute to 20 seconds
- [ ] Set the DelaySeconds parameter of a message to 20 seconds

698.
You are building a solution for a customer to extend their on-premises data center to AWS. The customer requires a 50-Mbps dedicated and private connection to their VPC. Which AWS product or feature satisfies this requirement?
- [ ] Amazon VPC peering
- [ ] Elastic IP Addresses
- [x] AWS Direct Connect
- [ ] Amazon VPC virtual private gateway

699.
Is there any way to own a direct connection to Amazon Web Services?
- [ ] You can create an encrypted tunnel to VPC, but you don’t own the connection.
- [ ] Yes, it’s called Amazon Dedicated Connection.
- [ ] No, AWS only allows access from the public Internet.
- [x] Yes, it’s called Direct Connect

700.
An organization has established an Internet-based VPN connection between their on-premises data center and AWS. They are considering migrating from VPN to AWS Direct Connect. Which operational concern should drive an organization to consider switching from an Internet-based VPN connection to AWS Direct Connect?
- [ ] AWS Direct Connect provides greater redundancy than an Internet-based VPN connection.
- [ ] AWS Direct Connect provides greater resiliency than an Internet-based VPN connection.
- [x] AWS Direct Connect provides greater bandwidth than an Internet-based VPN connection.
- [ ] AWS Direct Connect provides greater control of network provider selection than an Internet-based VPN connection.

701
Does AWS Direct Connect allow you access to all Availabilities Zones within a Region?
- [ ] Depends on the type of connection
- [ ] No
- [x] Yes
- [ ] Only when there’s just one availability zone in a region. If there are more than one, only one availability zone can be accessed directly.

702.*
A customer has established an AWS Direct Connect connection to AWS. The link is up and routes are being advertised from the customer’s end, however the customer is unable to connect from EC2 instances inside its VPC to servers residing in its datacenter. Which of the following options provide a viable solution to remedy this situation? (Choose 2 answers)
- [ ] Add a route to the route table with an IPSec VPN connection as the target (deals with VPN)
- [x] Enable route propagation to the Virtual Private Gateway (VGW)
- [ ] Enable route propagation to the customer gateway (CGW) (route propagation is enabled on VGW)
- [ ] Modify the route table of all Instances using the ‘route’ command. (no route command available)
- [ ] Modify the Instances VPC subnet route table by adding a route back to the customer’s on-premises environment.

703.*
A company has configured and peered two VPCs: VPC-1 and VPC-2. VPC-1 contains only private subnets, and VPC-2 contains only public subnets. The company uses a single AWS Direct Connect connection and private virtual interface to connect their on-premises network with VPC-1. Which two methods increase the fault tolerance of the connection to VPC-1? Choose 2 answers
- [ ] Establish a hardware VPN over the internet between VPC-2 and the on-premises network. (Peered VPC does not support Edge to Edge Routing)
- [x] Establish a hardware VPN over the internet between VPC-1 and the on-premises network
- [ ] Establish a new AWS Direct Connect connection and private virtual interface in the same region as VPC-2 (Peered VPC does not support Edge to Edge Routing)
- [ ] Establish a new AWS Direct Connect connection and private virtual interface in a different AWS region than VPC-1 (need to be in the same region as VPC-1)
- [x] Establish a new AWS Direct Connect connection and private virtual interface in the same AWS region as VPC-1

704.*
Your company previously configured a heavily used, dynamically routed VPN connection between your on premises data center and AWS. You recently provisioned a Direct Connect connection and would like to start using the new connection. After configuring Direct Connect settings in the AWS Console, which of the following options will provide the most seamless transition for your users?
- [ ] Delete your existing VPN connection to avoid routing loops configure your Direct Connect router with the appropriate settings and verity network traffic is leveraging Direct Connect.
- [ ] Configure your Direct Connect router with a higher BGP priority than your VPN router, verify network traffic is leveraging Direct Connect and then delete your existing VPN connection.
- [x] Update your VPC route tables to point to the Direct Connect connection configure your Direct Connect router with the appropriate settings verify network traffic is leveraging Direct Connect and then delete the VPN connection.
- [ ] Configure your Direct Connect router, update your VPC route tables to point to the Direct Connect connection, configure your VPN connection with a higher BGP priority. And verify network traffic is leveraging the Direct Connect connection

705.*
You are designing the network infrastructure for an application server in Amazon VPC. Users will access all the application instances from the Internet as well as from an on-premises network The on-premises network is connected to your VPC over an AWS Direct Connect link. How would you design routing to meet the above requirements?
- [ ] Configure a single routing Table with a default route via the Internet gateway. Propagate a default route via BGP on the AWS Direct Connect customer router. Associate the routing table with all VPC subnets (propagating default route would cause conflict)
- [x] Configure a single routing table with a default route via the internet gateway. Propagate specific routes for the on-premises networks via BGP on the AWS Direct Connect customer router. Associate the routing table with all VPC subnets.
- [ ] Configure a single routing table with two default routes: one to the internet via an Internet gateway the other to the on-premises network via the VPN gateway use this routing table across all subnets in your VPC. (there cannot be 2 default routes)
- [ ] Configure two routing tables one that has a default route via the Internet gateway and another that has a default route via the VPN gateway Associate both routing tables with each VPC subnet. (as the instances has to be in public subnet and should have a single routing table associated with them)

706.
You are implementing AWS Direct Connect. You intend to use AWS public service end points such as Amazon S3, across the AWS Direct Connect link. You want other Internet traffic to use your existing link to an Internet Service Provider. What is the correct way to configure AWS Direct Connect for access to services such as Amazon S3?
- [ ] Configure a public Interface on your AWS Direct Connect link. Configure a static route via your AWS Direct Connect link that points to Amazon S3. Advertise a default route to AWS using BGP.
- [ ] Create a private interface on your AWS Direct Connect link. Configure a static route via your AWS Direct connect link that points to Amazon S3 Configure specific routes to your network in your VPC.
- [x] Create a public interface on your AWS Direct Connect link. Redistribute BGP routes into your existing routing infrastructure advertise specific routes for your network to AWS
- [ ] Create a private interface on your AWS Direct connect link. Redistribute BGP routes into your existing routing infrastructure and advertise a default route to AWS.

707.
You have been asked to design network connectivity between your existing data centers and AWS. Your application’s EC2 instances must be able to connect to existing backend resources located in your data center. Network traffic between AWS and your data centers will start small, but ramp up to 10s of GB per second over the course of several months. The success of your application is dependent upon getting to market quickly. Which of the following design options will allow you to meet your objectives?
- [ ] Quickly create an internal ELB for your backend applications, submit a DirectConnect request to provision a 1 Gbps cross connect between your data center and VPC, then increase the number or size of your DirectConnect connections as needed.
- [ ] Allocate EIPs and an Internet Gateway for your VPC instances to use for quick, temporary access to your backend applications, then provision a VPN connection between a VPC and existing on -premises equipment.
- [x] Provision a VPN connection between a VPC and existing on -premises equipment, submit a DirectConnect partner request to provision cross connects between your data center and the DirectConnect location, then cut over from the VPN connection to one or more DirectConnect connections as needed.
- [ ] Quickly submit a DirectConnect request to provision a 1 Gbps cross connect between your data center and VPC, then increase the number or size of your DirectConnect connections as needed.

708.
You are tasked with moving a legacy application from a virtual machine running inside your datacenter to an Amazon VPC. Unfortunately this app requires access to a number of on-premises services and no one who configured the app still works for your company. Even worse there’s no documentation for it. What will allow the application running inside the VPC to reach back and access its internal dependencies without being reconfigured? (Choose 3 answers)
- [x] An AWS Direct Connect link between the VPC and the network housing the internal services (VPN or a DX for communication)
- [ ] An Internet Gateway to allow a VPN connection. (Virtual and Customer gateway is needed)
- [ ] An Elastic IP address on the VPC instance (Don’t need a EIP as private subnets can also interact with on-premises network)
- [x] An IP address space that does not conflict with the one on-premises (IP address cannot conflict)
- [ ] Entries in Amazon Route 53 that allow the Instance to resolve its dependencies’ IP addresses (Route 53 is not required)
- [x] A VM Import of the current virtual machine (VM Import to copy the VM to AWS as there is no documentation it can’t be configured from scratch)

709.*
Which of the following services natively encrypts data at rest within an AWS region?Choose 2 answers
- [x] AWS Storage Gateway
- [ ] Amazon DynamoDB
- [ ] Amazon CloudFront
- [x] Amazon Glacier
- [ ] Amazon Simple Queue Service

710.
What does the AWS Storage Gateway provide?
- [x] It allows to integrate on-premises IT environments with Cloud Storage
- [ ] A direct encrypted connection to Amazon S3.
- [ ] It’s a backup solution that provides an on-premises Cloud storage.
- [ ] It provides an encrypted SSL endpoint for backups in the Cloud.

711.
You’re running an application on-premises due to its dependency on non-x86 hardware and want to use AWS for data backup. Your backup application is only able to write to POSIX-compatible block-based storage. You have 140TB of data and would like to mount it as a single folder on your file server. Users must be able to access portions of this data while the backups are taking place. What backup solution would be most appropriate for this use case?
- [ ] Use Storage Gateway and configure it to use Gateway Cached volumes.
- [ ] Configure your backup software to use S3 as the target for your data backups.
- [ ] Configure your backup software to use Glacier as the target for your data backups
- [x] Use Storage Gateway and configure it to use Gateway Stored volumes (Data is hosted on the On-premise server as well. The requirement for 140TB is for file server On-Premise more to confuse and not in AWS. Just need a backup solution hence stored instead of cached volumes)

712.
A customer has a single 3-TB volume on-premises that is used to hold a large repository of images and print layout files. This repository is growing at 500 GB a year and must be presented as a single logical volume. The customer is becoming increasingly constrained with their local storage capacity and wants an off-site backup of this data, while maintaining low-latency access to their frequently accessed data. Which AWS Storage Gateway configuration meets the customer requirements?
- [x] Gateway-Cached volumes with snapshots scheduled to Amazon S3
- [ ] Gateway-Stored volumes with snapshots scheduled to Amazon S3
- [ ] Gateway-Virtual Tape Library with snapshots to Amazon S3
- [ ] Gateway-Virtual Tape Library with snapshots to Amazon Glacier

713.
You have a proprietary data store on-premises that must be backed up daily by dumping the data store contents to a single compressed 50GB file and sending the file to AWS. Your SLAs state that any dump file backed up within the past 7 days can be retrieved within 2 hours. Your compliance department has stated that all data must be held indefinitely. The time required to restore the data store from a backup is approximately 1 hour. Your on-premise network connection is capable of sustaining 1gbps to AWS. Which backup methods to AWS would be most cost-effective while still meeting all of your requirements?
- [ ] Send the daily backup files to Glacier immediately after being generated (will not meet the RTO)
- [ ] Transfer the daily backup files to an EBS volume in AWS and take daily snapshots of the volume (Not cost effective)
- [x] Transfer the daily backup files to S3 and use appropriate bucket lifecycle policies to send to Glacier (Store in S3 for seven days and then archive to Glacier)
- [ ] Host the backup files on a Storage Gateway with Gateway-Cached Volumes and take daily snapshots (Not Cost effective as local storage as well as S3 storage)

714.*
A customer implemented AWS Storage Gateway with a gateway-cached volume at their main office. An event takes the link between the main and branch office offline. Which methods will enable the branch office to access their data? Choose 3 answers
- [ ] Use a HTTPS GET to the Amazon S3 bucket where the files are located (gateway volumes are only accessible from the AWS Storage Gateway and cannot be directly accessed using Amazon S3 APIs)
- [ ] Restore by implementing a lifecycle policy on the Amazon S3 bucket.
- [ ] Make an Amazon Glacier Restore API call to load the files into another Amazon S3 bucket within four to six hours.
- [x] Launch a new AWS Storage Gateway instance AMI in Amazon EC2, and restore from a gateway snapshot
- [x] Create an Amazon EBS volume from a gateway snapshot, and mount it to an Amazon EC2 instance.
- [x] Launch an AWS Storage Gateway virtual iSCSI device at the branch office, and restore from a gateway snapshot