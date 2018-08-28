## AWS CSA Associate 模拟题3
111.
Which is an operational process performed by AWS for data security?
**Choose the correct answer:**
- [ ] AES-256 encryption of data stored on any shared storage device
- [x] Decommissioning of storage devices using industry-standard practices
- [ ] Background virus scans of EBS volumes and EBS snapshots
- [ ] Replication of data across multiple AWS Regions
- [ ] Secure wiping of EBS data when an EBS volume is unmounted

112.
You have been tasked with creating a VPC network topology for your company. The VPC network must support both Internet-facing applications and internally-facing applications accessed only over VPN. Both Internet-facing and internally-facing applications must be able to leverage at least three AZs for high availability. At a minimum, how many subnets must you create within your VPC to accommodate these requirements?
**Choose the correct answer:**
- [ ] 2
- [ ] 3
- [ ] 4
- [x] 6

113.
You receive a Spot Instance at a bid of $0.05/hr. After 30 minutes, the Spot Price increases to $0.06/hr and your Spot Instance is terminated by AWS. What was the total EC2 compute cost of running your Spot Instance?
**Choose the correct answer:**
- [x] $0.00
- [ ] $0.02
- [ ] $0.03
- [ ] $0.05
- [ ] $0.06

114.
You are developing a highly available web application using stateless web servers. Which services are suitable for storing session state data?
**Choose the 3 correct answers:**
- [ ] Amazon CloudWatch
- [x] Amazon Relational Database Service (RDS)
- [ ] Elastic Load Balancing
- [x] Amazon ElastiCache
- [ ] AWS Storage Gateway
- [x] Amazon DynamoDB

115.
You have a business-critical two-tier web app currently deployed in two AZs in a single region, using Elastic Load Balancing and Auto Scaling. The app depends on synchronous replication (very low latency connectivity) at the database layer. The application needs to remain fully available even if one application AZ goes off-line, and Auto Scaling cannot launch new instances in the remaining Availability Zones. How can the current architecture be enhanced to ensure this?
**Choose the correct answer:**
- [ ] Deploy in two regions using Weighted Round Robin (WRR), with Auto Scaling minimums set for 50 percent peak load per Region.
- [ ] Deploy in two regions using Weighted Round Robin (WRR), with Auto Scaling minimums set for 100 percent peak load per region.
- [x] Deploy in three Availability Zones, with Auto Scaling minimum set to handle 50 percent peak load per zone.
- [ ] Deploy in three Availability Zones, with Auto Scaling minimum set to handle 33 percent peak load per zone.

116.
You are deploying an application on EC2 that must call AWS APIs. What method of securely passing credentials to the application should you use?
**Choose the correct answer:**
- [x] Use AWS Identity and Access Management roles for EC2 instances.
- [ ] Pass API credentials to the instance using instance userdata.
- [ ] Embed the API credentials into your JAR files.
- [ ] Store API credentials as an object in Amazon Simple Storage Service.

117.
Which route must be added to your routing table in order to allow connections to the Internet from your subnet?
**Choose the correct answer:**
- [x] Destination: 0.0.0.0/0 --> Target: your Internet gateway
- [ ] Destination: 192.168.1.257/0 --> Target: your Internet gateway
- [ ] Destination: 0.0.0.0/33 --> Target: your virtual private gateway
- [ ] Destination: 0.0.0.0/0 --> Target: 0.0.0.0/24
- [ ] Destination: 10.0.0.0/32 --> Target: your virtual private gateway

118.
A customer's nightly EMR job processes a single 2-TB data file stored on Amazon Simple Storage Service (S3). The EMR job runs on two On-Demand core nodes and three On-Demand task nodes. Which of the following may help reduce the EMR job completion time?
**Choose the 2 correct answers:**
- [ ] Use three Spot Instances rather than three On-Demand instances for the task nodes.
- [x] Change the input split size in the MapReduce job configuration.
- [ ] Use a bootstrap action to present the S3 bucket as a local filesystem.
- [ ] Launch the core nodes and task nodes within an Amazon Virtual Cloud.
- [x] Adjust the number of simultaneous mapper tasks.
- [ ] Enable termination protection for the job flow.

119.
You have an VPC with a public subnet. Three EC2 instances currently running inside the subnet can successfully communicate with other hosts on the internet. You launch a fourth instance in the same subnet, using the same AMI and security group configuration you used for the others, but find that this instance cannot be accessed from the Internet. What should you do to enable Internet access?
**Choose the correct answer:**
- [ ] Deploy a NAT instance into the public subnet.
- [ ] Modify the routing table for the public subnet.
- [x] Assign an elastic IP address to the fourth instance.
- [ ] Configure a publicly routable IP address in the host OS of the fourth instance.

120.
Which of the following requires a custom CloudWatch metric to monitor?
**Choose the correct answer:**
- [x] Memory use
- [ ] CPU use
- [ ] Disk read operations
- [ ] Network in
- [ ] Estimated charges

121.
Which of the following is a durable key-value store?
**Choose the correct answer:**
- [x] Amazon Simple Storage Service
- [ ] Amazon Simple Workflow Service
- [ ] Amazon Simple Queue Service
- [ ] Amazon Simple Notification Service

122.
After creating a new AWS account, you use the API to request 40 on-demand EC2 instances in a single AZ. After 20 successful requests, subsequent requests failed. What could be a reason for this issue, and how would you resolve it?
**Choose the correct answer:**
- [x] You encountered a soft limit of 20 instances per region. Submit the limit increase form and retry the failed requests once approved.
- [ ] AWS allows you to provision no more than 20 instances per Availability Zone. Select a different Availability Zone and retry the failed request.
- [ ] You need to use Amazon Virtual Private Cloud (VPC) in order to provision more than 20 instances in a single Availability Zone. Simply terminate the resources already provisioned and re-launch them all in a VPC.
- [ ] You encountered an API throttling situation and should try the failed requests using an exponential decay retry algorithm.

123.
Amazon Glacier is designed for:
**Choose the 2 correct answers:**
- [ ] Frequently accessed data
- [ ] Active database storage
- [x] Data archives
- [x] Infrequently accessed data
- [ ] Cached session data

124.
You have an application running in us-west-2 that requires six EC2 instances running at all times. With three AZs available in that region (us-west-2a, us-west-2b, and us-west-2c), which of the following deployments provides 100 percent fault tolerance if any single AZ in us-west-2 becomes unavailable?
**Choose the correct answer:**
- [ ] Us-west-2a with two EC2 instances, us-west-2b with two EC2 instances, and us-west-2c with two EC2 instances
- [ ] Us-west-2a with three EC2 instances, us-west-2b with three EC2 instances, and us-west-2c with no EC2 instances
- [ ] Us-west-2a with four EC2 instances, us-west-2b with two EC2 instances, and us-west-2c with two EC2 instances
- [x] Us-west-2a with six EC2 instances, us-west-2b with six EC2 instances, and us-west-2c with no EC2 instances
- [x] Us-west-2a with three EC2 instances, us-west-2b with three EC2 instances, and us-west-2c with three EC2 instances

125.
What action is required to establish a VPC VPN connection between an on-premises data center and an Amazon VPC virtual private gateway ?
**Choose the correct answer:**
- [ ] Modify the main route table to allow traffic to a network address translation instance.
- [ ] Use a dedicated network address translation instance in the public subnet.
- [x] Assign a static Internet-routable IP address to an Amazon VPC customer gateway.
- [ ] Establish a dedicated networking connection using AWS Direct Connect.

126.
How can software determine the public and private IP addresses of the EC2 instance that it is running on?
**Choose the correct answer:**
- [x] Query the local instance metadata.
- [ ] Query the local instance userdata.
- [ ] Query the appropriate Amazon CloudWatch metric.
- [ ] Use an ipconfig or ifconfig command.

127.
A startup company hired you to help them build a mobile application, that will ultimately store billions of images and videos in S3. The company is lean on funding, and wants to minimize operational costs, however, they have an aggressive marketing plan, and expect to double their current installation base every six months. Due to the nature of their business, they are expecting sudden and large increases in traffic to and from S3, and need to ensure that it can handle the performance needs of their application. What other information must you gather from this customer in order to determine whether S3 is the right option?
**Choose the correct answer:**
- [ ] You must know how many customers the company has today, because this is critical in understanding what their customer base will be in two years.
- [x] You must find out the total number of requests per second at peak usage.
- [ ] You must know the size of the individual objects being written to S3, in order to properly design the key namespace.
- [ ] In order to build the key namespace correctly, you must understand the total amount of storage needs for each S3 bucket.

128.
You have an EC2 security group with several running EC2 instances. You change the security group rules to allow inbound traffic on a new port and protocol, and launch several new instances in the same security group. The new rules apply:
**Choose the correct answer:**
- [x] Immediately to all instances in the security group.
- [ ] Immediately to the new instances only.
- [ ] Immediately to the new instances, but old instances must be stopped and restarted before the new rules apply.
- [ ] To all instances, but it may take several minutes for old instances to see the changes.

129.
A VPC public subnet is one that:
**Choose the correct answer:**
- [x] Has at least one route in its associated routing table that uses an Internet Gateway (IGW).
- [ ] Includes a route in its associated routing table via a Network Address Translation (NAT) instance.
- [ ] Has a Network Access Control List (NACL) permitting outbound traffic to 0.0.0.0/0.
- [ ] Has the Public Subnet option selected in its configuration.

130.
In reviewing the Auto Scaling events for your application you notice that your application is scaling up and down multiple times in the same hour. What design choice could you make to optimize for cost while preserving elasticity?
**Choose the 2 correct answers:**
- [ ] Modify the Auto Scaling policy to use scheduled scaling actions
- [ ] Modify the Auto Scaling group termination policy to terminate the oldest instance first.
- [x] Modify the Auto Scaling group cool-down timers.
- [x] Modify the Amazon CloudWatch alarm period that triggers your Auto Scaling scale down policy.
- [ ] Modify the Auto Scaling group termination policy to terminate the newest instance first.

131.
What combination of the following options will protect S3 objects from both accidental deletion and accidental overwriting?
**Choose the 2 correct answers:**
- [x] Enable S3 versioning on the bucket.
- [ ] Access S3 data using only signed URLs.
- [ ] Disable S3 delete using an IAM bucket policy.
- [ ] Enable S3 Reduced Redundancy Storage.
- [x] Enable multi-factor authentication (MFA) protected access.

132.
What does Amazon S3 stand for?
**Choose the correct answer:**
- [ ] Simple Storage Solution.
- [ ] Storage Storage Storage (triple redundancy Storage).
- [ ] Storage Server Solution.
- [x] Simple Storage Service.

133.
You must assign each server to at least _____ security group
**Choose the correct answer:**
- [ ] 3
- [ ] 2
- [ ] 4
- [x] 1

134.
Before I delete an EBS volume, what can I do if I want to recreate the volume later?
**Choose the correct answer:**
- [ ] Create a copy of the EBS volume (not a snapshot)
- [x] Store a snapshot of the volume 
- [ ] Download the content to an EC2 instance
- [ ] Back up the data in to a physical disk

135,
Select the most correct answer: The device name /dev/sda1 (within Amazon EC2 ) is _____
**Choose the correct answer:**
- [ ] Possible for EBS volumes
- [x] Reserved for the root device 
- [ ] Recommended for EBS volumes
- [ ] Recommended for instance store volumes

136,
If I want an instance to have a public IP address, which IP address should I use?
**Choose the correct answer:**
- [x] Elastic IP Address 
- [ ] Class B IP Address
- [ ] Class A IP Address
- [ ] Dynamic IP Address

137.
What does RRS stand for when talking about S3?
**Choose the correct answer:**
- [ ] Redundancy Removal System
- [ ] Relational Rights Storage
- [ ] Regional Rights Standard
- [x] Reduced Redundancy Storage

138.
All Amazon EC2 instances are assigned two IP addresses at launch. Which one can only be reached from within the Amazon EC2 network?
**Choose the correct answer:**
- [ ] Multiple IP address
- [ ] Public IP address
- [x] Private IP address 
- [ ] Elastic IP Address

139.
What does Amazon SWF stand for?
**Choose the correct answer:**
- [ ] Simple Web Flow
- [x] Simple Work Flow
- [ ] Simple Wireless Forms
- [ ] Simple Web Form

140.
What is the Reduced Redundancy option in Amazon S3?
**Choose the correct answer:**
- [x] Less redundancy for a lower cost.
- [ ] It doesn't exist in Amazon S3, but in Amazon EBS.
- [ ] It allows you to destroy any copy of your files outside a specific jurisdiction.
- [ ] It doesn't exist at all

141.
Fill in the blanks: Resources that are created in AWS are identified by a unique identifier called an _____.
**Choose the correct answer:**
- [ ] Amazon Resource Number
- [ ] Amazon Resource Name tag
- [x] Amazon Resource Name
- [ ] Amazon Reesource Namespace

142.
What does the command 'ec2-run-instances ami-e3a5408a -n 20 -g appserver' do?
**Choose the correct answer:**
- [x] Start twenty instances as members of appserver group.
- [ ] Creates 20 rules in the security group named appserver
- [ ] Terminate twenty instances as members of appserver group.
- [ ] Start 20 security groups

143.
While creating an Amazon RDS DB, your first task is to set up a DB ______ that controls what IP addresses or EC2 instances have access to your DB Instance.
**Choose the correct answer:**
- [ ] Security Pool
- [ ] Secure Zone
- [ ] Security Token Pool
- [x] Security Group

144.
When you run a DB Instance as a Multi-AZ deployment, the _____ serves database writes and reads
**Choose the correct answer:**
- [ ] secondary
- [ ] backup
- [ ] stand by
- [x] primary

145.
Every user you create in the IAM system starts with ______.
**Choose the correct answer:**
- [ ] partial permissions
- [ ] full permissions
- [x] no permissions

146.
What does Amazon EC2 provide?
**Choose the correct answer:**
- [x] Virtual servers in the Cloud.
- [ ] A platform to run code (Java, PHP, Python), paying on an hourly basis.
- [ ] Computer Clusters in the Cloud.
- [ ] Physical servers, remotely managed by the customer.

147.
Amazon SWF is designed to help users do what?
**Choose the correct answer:**
- [ ] Design graphical user interface interactions
- [ ] Manage user identification and authorization
- [ ] Store Web content
- [x] Coordinate synchronous and asynchronous tasks which are distributed and fault tolerant.

148.
Can I control if and when MySQL based RDS Instance is upgraded to new supported versions?
**Choose the correct answer:**
- [ ] No
- [ ] Only in VPC
- [x] Yes

149.
If I modify a DB Instance or the DB parameter group associated with the instance, should I reboot the instance for the changes to take effect?
**Choose the correct answer:**
- [ ] No
- [x] Yes

150.
When you view the block device mapping for your instance, you can see only the EBS volumes, not the instance store volumes.
**Choose the correct answer:**
- [ ] Depends on the instance type
- [ ] FALSE
- [ ] Depends on whether you use API call
- [x] TRUE

151.
By default, EBS volumes that are created and attached to an instance at launch are deleted when that instance is terminated. You can modify this behavior by changing the value of the flag _____ to false when you launch the instance.
**Choose the correct answer:**
- [x] DeleteOnTermination
- [ ] RemoveOnDeletion
- [ ] RemoveOnTermination
- [ ] TerminateOnDeletion

152.
What are the initial settings of an user created security group?
**Choose the correct answer:**
- [ ] Allow all inbound traffic and Allow no outbound traffic
- [ ] Allow no inbound traffic and Allow no outbound traffic
- [x] Allow no inbound traffic and Allow all outbound traffic
- [ ] Allow all inbound traffic and Allow all outbound traffic

153.
Will my standby RDS instance be in the same Region as my primary?
**Choose the correct answer:**
- [ ] Only for Oracle RDS types
- [x] Yes 
- [ ] Only if configured at launch
- [ ] No

154.
What does Amazon Elastic Beanstalk provide?
**Choose the correct answer:**
- [ ] A scalable storage appliance on top of Amazon Web Services.
- [x] An application container on top of Amazon Web Services.
- [ ] A service by this name doesn't exist.
- [ ] A scalable cluster of EC2 instances.

155.
When using IAM to control access to your RDS resources, the key names that can be used are case sensitive. For example, aws:CurrentTime is NOT equivalent to AWS:currenttime.
**Choose the correct answer:**
- [x] TRUE 
- [ ] FALSE

156.
What will be the status of the snapshot until the snapshot is complete.
**Choose the correct answer:**
- [ ] running
- [ ] working
- [ ] progressing
- [x] pending

157.
Can an EBS volume be attached to more than one EC2 instance at the same time?
**Choose the correct answer:**
- [x] No
- [ ] Yes.
- [ ] Only EC2-optimized EBS volumes.
- [ ] Only in read mode.

158.
Automated backups are enabled by default for a new DB Instance.
**Choose the correct answer:**
- [x] TRUE
- [ ] FALSE

159.
What does the AWS Storage Gateway provide?
**Choose the correct answer:**
- [x] Integration of on-premises IT environments with Cloud Storage.
- [ ] A direct encrypted connection to Amazon S3.
- [ ] A backup solution that provides an on-premises Cloud storage.
- [ ] It provides an encrypted SSL endpoint for backups in the Cloud.

160.
Amazon RDS automated backups and DB Snapshots are currently supported for only the ______ storage engine
**Choose the correct answer:**
- [x] InnoDB 
- [ ] MyISAM

161.
How many relational database engines does RDS currently support?
**Choose the correct answer:**
- [x] Six: Amazon Aurora, Oracle, Microsoft SQL Server, PostgreSQL, MySQL and MariaDB 
- [ ] Just two: MySQL and Oracle.
- [ ] Five: MySQL, PostgreSQL, MongoDB, Cassandra and SQLite.
- [ ] Just one: MySQL.

162.
Fill in the blanks: The base URI for all requests for instance metadata is _____
**Choose the correct answer:**
- [ ] http://254.169.169.254/latest/
- [ ] http://169.169.254.254/latest/
- [ ] http://127.0.0.1/latest/
- [x] http://169.254.169.254/latest/

163.
While creating the snapshots using the the command line tools, which command should I be using?
**Choose the correct answer:**
- [ ] ec2-deploy-snapshot
- [ ] ec2-fresh-snapshot
- [x] ec2-create-snapshot 
- [ ] ec2-new-snapshot

164.
Typically, you want your application to check whether a request generated an error before you spend any time processing results. The easiest way to find out if an error occurred is to look for an ______ node in the response from the Amazon RDS API.
**Choose the correct answer:**
- [ ] Incorrect
- [x] Error
- [ ] FALSE

165.
What are the two permission types used by AWS?
**Choose the correct answer:**
- [ ] Resource-based and Product-based
- [ ] Product-based and Service-based
- [ ] Service-based
- [x] User-based and Resource-based

166.
In Amazon CloudWatch, which metric should I be checking to ensure that your DB Instance has enough free storage space?
**Choose the correct answer:**
- [ ] FreeStorage
- [x] FreeStorageSpace 
- [ ] FreeStorageVolume
- [ ] FreeDBStorageSpace

167.
Amazon RDS DB snapshots and automated backups are stored in
**Choose the correct answer:**
- [x] Amazon S3 
- [ ] Amazon ECS Volume
- [ ] Amazon RDS
- [ ] Amazon EMR

168.
What is the maximum key length of a tag?
**Choose the correct answer:**
- [ ] 512 Unicode characters
- [ ] 64 Unicode characters
- [ ] 256 Unicode characters
- [x] 128 Unicode characters

169.
Security Groups can't _____.
**Choose the correct answer:**
- [ ] be nested more than 3 levels
- [x] be nested at all
- [ ] be nested more than 4 levels
- [ ] be nested more than 2 levels

170.
You must increase storage size in increments of at least _____ %
**Choose the correct answer:**
- [ ] 40
- [ ] 20
- [ ] 50
- [x] 10