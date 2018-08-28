## AWS CSA Associate 模拟题4
171.
Changes to the backup window take effect ______.
**Choose the correct answer:**
- [ ] from the next billing cycle
- [ ] after 30 minutes
- [x] immediately 
- [ ] after 24 hoursA

172.
Using Amazon CloudWatch's Free Tier, what is the frequency of metric updates which you receive?
**Choose the correct answer:**
- [x] 5 minutes 
- [ ] 500 milliseconds.
- [ ] 30 seconds
- [ ] 1 minute

173.
Which is the default region in AWS?
**Choose the correct answer:**
- [ ] eu-west-1
- [x] us-east-1 
- [ ] us-east-2
- [ ] ap-southeast-1

174.
What are the Amazon EC2 API tools?
**Choose the correct answer:**
- [ ] They don't exist. The Amazon EC2 AMI tools, instead, are used to manage permissions.
- [x] Command-line tools to the Amazon EC2 web service.
- [ ] They are a set of graphical tools to manage EC2 instances.
- [ ] They don't exist. The Amazon API tools are a client interface to Amazon Web Services.

175.
What are the two types of licensing options available for using Amazon RDS for Oracle?
**Choose the correct answer:**
- [ ] BYOL and Enterprise License
- [x] BYOL and License Included
- [ ] Enterprise License and License Included
- [ ] Role based License and License Included

176.
What does a "Domain" refer to in Amazon SWF?
**Choose the correct answer:**
- [ ] A security group in which only tasks inside can communicate with each other
- [ ] A special type of worker
- [x] A collection of related Workflows
- [ ] The DNS record for the Amazon SWF service

177.
EBS Snapshots occur _____
**Choose the correct answer:**
- [x] Asynchronously 
- [ ] Synchronously
- [ ] Weekly

178.
Disabling automated backups disables the point-in-time recovery feature.
**Choose the correct answer:**
- [x] True
- [ ] False

179.
Out of the striping options available for the EBS volumes, which one has the following disadvantage : 'Doubles the amount of I/O required from the instance to EBS compared to RAID 0, because you're mirroring all writes to a pair of volumes, limiting how much you can stripe.' ?
**Choose the correct answer:**
- [ ] Raid 5
- [ ] Raid 6
- [x] Raid 1
- [ ] Raid 2

180.
Is creating a Read Replica of another Read Replica supported?
**Choose the correct answer:**
- [ ] Only in certain regions
- [ ] Only with MSSQL based RDS
- [ ] Only for Oracle RDS types
- [x] No

181.
Can Amazon S3 uploads resume on failure or do they need to restart?
**Choose the correct answer:**
- [ ] Restart from beginning
- [ ] You can resume them, if you flag the "resume on failure" option before uploading.
- [x] Resume on failure
- [ ] Depends on the file size

182.
Which of the following cannot be used in EC2 to control who has access to specific EC2 instances?
**Choose the correct answer:**
- [ ] Security Groups
- [x] IAM System
- [ ] SSH keys
- [ ] Windows passwords

183.
Fill in the blanks : _____ let you categorize your EC2 resources in different ways, for example, by purpose, owner, or environment.
**Choose the correct answer:**
- [ ] wildcards
- [ ] pointers
- [x] tags 
- [ ] special filters

184.
How can I change the security group membership for interfaces owned by other AWS, such as Elastic Load Balancing?
**Choose the correct answer:**
- [x] By using the service specific console or API\CLI commands
- [ ] None of these
- [ ] Using Amazon EC2 API/CLI
- [ ] Using all these methods

185.
What is the maximum write throughput I can provision per table for a single DynamoDB table?
**Choose the correct answer:**
- [ ] 5,000 us east, 1,000 all other regions
- [ ] 100,000 us east, 10, 000 all other regions 
- [x] Designed to scale without limits, but if you go beyond 40,000 us east/10,000 all other regions you have to contact AWS first.
- [ ] There is no limit

186.
What does the ec2-revoke command do with respect to the Amazon EC2 security groups?
**Choose the correct answer:**
- [ ] Removes one or more security groups from a rule.
- [ ] Removes one or more security groups from an Amazon EC2 instance.
- [x] Removes one or more rules from a security group.
- [ ] Removes a security group from an account.

187.
Can a 'user' be associated with multiple AWS accounts?
**Choose the correct answer:**
- [x] No
- [ ] Yes

188.
True or False: Manually created DB Snapshots are deleted after the DB Instance is deleted.
**Choose the correct answer:**
- [ ] TRUE
- [x] FALSE

189.
What is Amazon Glacier?
**Choose the correct answer:**
- [ ] There is no such thing
- [ ] A security tool that allows "freezing" an EBS volume to perform computer forensics on it.
- [x] A low-cost storage service that provides secure and durable storage for data archiving and backup.
- [ ] A security tool that allows "freezing" an EC2 instance to perform computer forensics on it.

190.
What is the durability of S3 RRS? 
**Choose the correct answer:**
- [x] 99.99%
- [ ] 99.95%
- [ ] 99.995%
- [ ] 99.999999999%

191.
What does specifying the mapping /dev/sdc=none do when launching an EC2 instance?
**Choose the correct answer:**
- [ ] Prevents /dev/sdc from creating the instance.
- [ ] Prevents /dev/sdc from deleting the instance.
- [ ] Set the value of /dev/sdc to 'zero'.
- [x] Prevents /dev/sdc from attaching to the instance.

192.*
Is Federated Storage Engine currently supported by Amazon RDS for MySQL? 
**Choose the correct answer:**
- [ ] Only for Oracle RDS instances
- [x] No
- [ ] Yes
- [ ] Only in VPC

193.
What is the maximum groups an IAM user be a member of?
**Choose the correct answer:**
- [ ] 20
- [ ] 5
- [x] 10
- [ ] 15

194.*
True or False: When you perform a restore operation to a point in time or from a DB Snapshot, a new DB Instance is created with a new endpoint.
**Choose the correct answer:**
- [ ] FALSE
- [ ] TRUE

195.
A/An _____ acts as a firewall that controls the traffic allowed to reach one or more instances. 
**Choose the correct answer:**
- [x] security group
- [ ] ACL
- [ ] IAM
- [ ] Private IP Addresses

196.
Will my standby RDS instance be in the same Availability Zone as my primary?
**Choose the correct answer:**
- [ ] Only for Oracle RDS types
- [ ] Yes
- [ ] Only if configured at launch
- [x] No

197.
While launching an RDS DB instance, on which page I can select the Availability Zone?
**Choose the correct answer:**
- [ ] Review
- [ ] DB Instance Details
- [ ] Management Options
- [x] Additional Configuration

198.
What does the ec2-create-group command do with respect to the Amazon EC2 security groups? 
**Choose the correct answer:**
- [ ] Groups the user created security groups in to a new group for easy access.
- [x] Creates a new security group for use with your account.
- [ ] Creates a new group inside the security group.
- [ ] Creates a new rule inside the security group.

199.
In the Launch Db Instance Wizard, where can I select the backup and maintenance options?
**Choose the correct answer:**
- [ ] DB Instance Details
- [ ] Review
- [x] Management Options
- [ ] Engine Selection

200.
You are charged for the IOPS and storage whether or not you use them in a given month? 
**Choose the correct answer:**
- [ ] FALSE
- [x] TRUE

201.
IAM provides several policy templates you can use to automatically assign permissions to the groups you create. The _____ policy template gives the Admins group permission to access all account resources, except your AWS account information.
**Choose the correct answer:**
- [ ] Read Only Access
- [ ] Power User Access
- [ ] AWS CloudFormation Read Only Access
- [x] Administrator Access

202.
While performing volume status checks using volume status checks, if the status is insufficient-data, if the status is 'insufficient-data', what does it mean?
**Choose the correct answer:**
- [x] checks may still be in progress on the volume
- [ ] check has passed
- [ ] check has failed
- [ ] there is no such status

203.
By default, when an EBS volume is attached to a Windows instance, it may show up as any drive letter on the instance. You can change the settings of the _____ Service to set the drive letters of the EBS volumes per your specifications. 
**Choose the correct answer:**
- [ ] EBSConfig Service
- [ ] AMIConfig Service
- [x] Ec2Config Service
- [ ] Ec2-AMIConfig Service

204.
SQL Server stores logins and passwords in the master database. 
**Choose the correct answer:**
- [x] True
- [ ] False

205.
Does Amazon RDS allow direct host access via Telnet, Secure Shell (SSH), or Windows Remote Desktop Connection?
**Choose the correct answer:**
- [ ] Yes
- [x] No
- [ ] Depends on if it is in VPC or not

206.
To view information about an Amazon EBS volume, open the Amazon EC2 console, go to EC2, click _____ in the Navigation pane. 
**Choose the correct answer:**
- [ ] EBS
- [ ] Describe
- [ ] Details
- [x] Volumes

207.
Using Amazon IAM, I can give permissions based on organizational groups? 
**Choose the correct answer:**
- [x] True
- [ ] False

208.
While creating an EC2 snapshot using the API, which Action should I be using?
**Choose the correct answer:**
- [ ] MakeSnapShot
- [ ] FreshSnapshot
- [ ] DeploySnapshot
- [x] CreateSnapshot

209.
While signing in REST/ Query requests, for additional security, you should transmit your requests using Secure Sockets Layer (SSL) by using _____.
**Choose the correct answer:**
- [ ] HTTP
- [ ] Internet Protocol Security(IPsec)
- [ ] TLS (Transport Layer Security)
- [x] HTTPS

210.
What happens to the I/O operations while you take a database snapshot in a single AZ database?
**Choose the correct answer:**
- [x] I/O operations to the database are suspended for a few minutes while the backup is in progress.
- [ ] I/O operations to the database are sent to a Replica (if available) for a few minutes while the backup is in progress.
- [ ] I/O operations will be functioning normally
- [ ] I/O operations to the database are suspended for an hour while the backup is in progress

211.
Read Replicas require a transactional storage engine and are only supported for the _____ storage engine.
**Choose the correct answer:**
- [ ] OracleISAM
- [ ] MSSQLDB
- [x] InnoDB
- [ ] MyISAM

212.
When running my DB Instance as a Multi-AZ deployment, can I use the standby for read or write operations? 
**Choose the correct answer:**
- [ ] Yes
- [ ] Only with MSSQL based RDS
- [ ] Only for Oracle RDS instances
- [x] No

213.
When should I choose Provisioned IOPS over Standard RDS storage? 
**Choose the correct answer:**
- [ ] If you have batch-oriented workloads
- [x] If you use production online transaction processing (OLTP) workloads.
- [ ] If you have workloads that are not sensitive to consistent performance
- [ ] If you infrequently read or write to the drive.

214.
In the 'Detailed' monitoring data available for your Amazon EBS volumes, Provisioned IOPS volumes automatically send _____ minute metrics to Amazon CloudWatch. 
**Choose the correct answer:**
- [ ] 3
- [x] 1
- [ ] 5
- [ ] 2

215.
What is the minimum charge for the data transferred between Amazon RDS and Amazon EC2 Instances in the same Availability Zone? 
**Choose the correct answer:**
- [ ] USD 0.10 per GB
- [x] No charge. It is free.
- [ ] USD 0.02 per GB
- [ ] USD 0.01 per GB

216.
Reserved Instances are available for Multi-AZ Deployments.
**Choose the correct answer:**
- [x] True
- [ ] False

217.
Which service enables AWS customers to manage users and permissions in AWS?
**Choose the correct answer:**
- [ ] AWS Access Control Service (ACS)
- [x] AWS Identity and Access Management (IAM)
- [ ] AWS Identity Manager (AIM)
- [ ] AWS Security Groups

218.
Which Amazon Storage behaves like raw, unformatted, external block devices that you can attach to your instances?
**Choose the correct answer:**
- [ ] None of these.
- [ ] Amazon Instance Storage
- [x] Amazon EBS
- [ ] All of these

219.
Which Amazon service can I use to define a virtual network that closely resembles a traditional data center?
**Choose the correct answer:**
- [x] Amazon VPC
- [ ] Amazon ServiceBus
- [ ] Amazon EMR
- [ ] Amazon RDS

220.
What is the command line instruction for running the remote desktop client in Windows?
**Choose the correct answer:**
- [ ] desk.cpl
- [x] mstsc

221.
Amazon RDS automated backups and DB Snapshots are currently supported for only the ______ storage engine.
**Choose the correct answer:**
- [ ] MyISAM
- [x] InnoDB

222.
MySQL installations default to port _____.
**Choose the correct answer:**
- [x] 3306
- [ ] 443
- [ ] 80
- [ ] 1158

223.
If you have chosen Multi-AZ deployment, in the event of an outage of your primary DB Instance, Amazon RDS automatically switches to the standby replica. The automatic failover mechanism simply changes the ______ record of the main DB Instance to point to the standby DB Instance.
**Choose the correct answer:**
- [ ] DNAME
- [x] CNAME
- [ ] TXT
- [ ] MX

224.
If I modify a DB Instance or the DB parameter group associated with the instance, I should reboot the instance for the changes to take effect?
**Choose the correct answer:**
- [x] True
- [ ] False

225.
If I want to run a database in an Amazon instance, which is the most recommended Amazon storage option?
**Choose the correct answer:**
- [ ] Amazon Instance Storage
- [x] Amazon EBS
- [ ] You can't run a database inside an Amazon instance.
- [ ] Amazon S3

226.
In regards to IAM you can edit user properties later, but you cannot use the console to change the _____.
**Choose the correct answer:**
- [x] user name
- [ ] password
- [ ] default group

227.
If you add a tag that has the same key as an existing tag on a DB Instance, the new value overwrites the old value.
**Choose the correct answer:**
- [ ] FALSE
- [x] TRUE

228.
Making your snapshot public shares all snapshot data with everyone. Can the snapshots with AWS Marketplace product codes be made public?
**Choose the correct answer:**
- [x] No
- [ ] Yes

229.
Fill in the blanks: "To ensure failover capabilities, consider using a _____ for incoming traffic on a network interface".
**Choose the correct answer:**
- [ ] primary public IP
- [x] secondary private IP
- [ ] secondary public IP
- [ ] add on secondary IP

230.
If I have multiple Read Replicas for my master DB Instance and I promote one of them, what happens to the rest of the Read Replicas?
**Choose the correct answer:**
- [x] The remaining Read Replicas will still replicate from the older master DB Instance
- [ ] The remaining Read Replicas will be deleted
- [ ] The remaining Read Replicas will be combined to one read replica

231.
What does Amazon CloudFormation provide?
**Choose the correct answer:**
- [ ] The ability to setup Autoscaling for Amazon EC2 instances.
- [ ] None of these.
- [x] A template resource creation for Amazon Web Services.
- [ ] A template to map network resources for Amazon Web Services.

232.
Can I encrypt connections between my application and my DB Instance using SSL?
**Choose the correct answer:**
- [ ] No
- [x] Yes
- [ ] Only in VPC
- [ ] Only in certain regions

233.
What are the four levels of AWS Premium Support?
**Choose the correct answer:**
- [x] Basic, Developer, Business, Enterprise
- [ ] Basic, Startup, Business, Enterprise
- [ ] Free, Bronze, Silver, Gold
- [ ] All support is free

234.
What can I access by visiting the URL: http://status.aws.amazon.com/ ?
**Choose the correct answer:**
- [ ] Amazon Cloud Watch
- [ ] Status of the Amazon RDS DB
- [x] AWS Service Health Dashboard
- [ ] AWS Cloud Monitor

235.
Please select the Amazon EC2 resource which cannot be tagged.
**Choose the correct answer:**
- [ ] Images (AMIs, kernels, RAM disks)
- [ ] Amazon EBS volumes
- [x] Elastic IP addresses
- [ ] VPCs

236.
Because of the extensibility limitations of striped storage attached to Windows Server, Amazon RDS does not currently support increasing storage on a _____ DB Instance.
**Choose the correct answer:**
- [x] SQL Server
- [ ] MySQL
- [ ] Oracle

237.
Through which of the following interfaces is AWS Identity and Access Management available? 
**Choose the correct answer:**
- [ ] AWS Management Console
- [ ] Command line interface (CLI)
- [ ] IAM Query API
- [x] All of the above

238.
**Select the incorrect statement.**
- [ ] In Amazon EC2, private IP address is only returned to Amazon EC2 when the instance is stopped or terminated
- [ ] In Amazon VPC, an instance retains its private IP address when the instance is stopped.
- [x] In Amazon VPC, an instance does NOT retain its private IP address when the instance is stopped.
- [ ] In Amazon EC2, the private IP address is associated exclusively with the instance for its lifetime

239.
How are the EBS snapshots saved on Amazon S3?
**Choose the correct answer:**
- [ ] Exponentially
- [x] Incrementally
- [ ] EBS snapshots are not stored in the Amazon S3
- [ ] Decrementally

240.
What is the type of monitoring data (for Amazon EBS volumes) which is available automatically in 5-minute periods at no charge called?
**Choose the correct answer:**
- [x] Basic
- [ ] Primary
- [ ] Detailed
- [ ] Local

241.
The new DB Instance that is created when you promote a Read Replica retains the backup window period.
**Choose the correct answer:**
- [x] TRUE
- [ ] FALSE

232.
What happens when you create a topic on Amazon SNS?
**Choose the correct answer:**
- [ ] The topic is created, and it has the name you specified for it.
- [x] An ARN (Amazon Resource Name) is created.
- [ ] You can create a topic on Amazon SQS, not on Amazon SNS.
- [ ] This question doesn't make sense.

233.
Can I delete a snapshot of the root device of an EBS volume used by a registered AMI?
**Choose the correct answer:**
- [ ] Only via API
- [ ] Only via Console
- [x] Yes
- [ ] No

234.
New database versions will automatically be applied to AWS RDS instances as they become available. 
**Choose the correct answer:**
- [ ] True
- [x] False

235.
What is the maximum response time for a Business level Premium Support case?
**Choose the correct answer:**
- [ ] 120 seconds
- [x] 1 hour
- [ ] 10 minutes
- [ ] 12 hours

236.
The _____ service is targeted at organizations with multiple users or systems that use AWS products such as Amazon EC2, Amazon SimpleDB, and the AWS Management Console.
**Choose the correct answer:**
- [ ] Amazon RDS
- [ ] AWS Integrity Management
- [x] AWS Identity and Access Management
- [ ] Amazon EMR

237.
Without IAM, you cannot control the tasks a particular user or system can do and what AWS resources they might use.
**Choose the correct answer:**
- [ ] FALSE
- [x] TRUE

238.
When you use the AWS Management Console to delete an IAM user, IAM also deletes any signing certificates and any access keys belonging to the user. 
**Choose the correct answer:**
- [ ] FALSE
- [x] TRUE

239.
When automatic failover occurs, Amazon RDS will emit a DB Instance event to inform you that automatic failover occurred. You can use the _____ to return information about events related to your DB Instance.
**Choose the correct answer:**
- [ ] FetchFailure
- [ ] DescribeFailure
- [x] DescribeEvents
- [ ] FetchEvents

240.
What is the default maximum number of MFA devices in use per AWS account (at the root account level)?
**Choose the correct answer:**
- [x] 1
- [ ] 5
- [ ] 15
- [ ] 10

241.
Is there a limit to how many groups a user can be in?
**Choose the correct answer:**
- [x] Yes for all users except root
- [ ] Yes unless special permission granted
- [ ] Yes for all users
- [ ] No

242.
Do the Amazon EBS volumes persist independently from the running life of an Amazon EC2 instance?
**Choose the correct answer:**
- [ ] Only if instructed to when created
- [x] Yes
- [ ] No

243.
Can we attach an EBS volume to more than one EC2 instance at the same time?
**Choose the correct answer:**
- [ ] Yes
- [x] No
- [ ] Only EC2-optimized EBS volumes.
- [ ] Only in read mode.

244.
Select the correct set of options. The initial settings for the default security group are:
**Choose the correct answer:**
- [x] Allow no inbound traffic, Allow all outbound traffic and Allow instances associated with this security group to talk to each other
- [ ] Allow all inbound traffic, Allow no outbound traffic and Allow instances associated with this security group to talk to each other
- [ ] Allow no inbound traffic, Allow all outbound traffic and Does NOT allow instances associated with this security group to talk to each other
- [ ] Allow all inbound traffic, Allow all outbound traffic and Does NOT allow instances associated with this security group to talk to each other

245.
What does Amazon Route53 provide?
**Choose the correct answer:**
- [ ] A global Content Delivery Network.
- [ ] None of these.
- [x] A scalable Domain Name System.
- [ ] An SSH endpoint for Amazon EC2.

246.
What does Amazon ElastiCache provide?
**Choose the correct answer:**
- [ ] A service by this name doesn't exist. Perhaps you mean Amazon CloudCache.
- [ ] A virtual server with a huge amount of memory.
- [x] A managed In-memory cache service.
- [ ] An Amazon EC2 instance with the Memcached software already pre-installed.

247.
What is the default per account limit of Elastic IPs? 
**Choose the correct answer:**
- [ ] 1
- [ ] 3
- [x] 5
- [ ] 0

248.
What is a Security Group?
**Choose the correct answer:**
- [ ] None of these.
- [ ] A list of users that can access Amazon EC2 instances.
- [ ] An Access Control List (ACL) for AWS resources.
- [x] It acts as a virtual firewall that controls the traffic for one or more instances.

249.
Please select the Amazon EC2 resource which can be tagged.
**Choose the correct answer:**
- [ ] Key pairs
- [ ] Elastic IP addresses
- [ ] Placement groups
- [x] EBS snapshots

250.
What is Amazon Glacier?
**Choose the correct answer:**
- [ ] It's a security tool that allows to "freeze" an EC2 instance and perform computer forensics on it.
- [ ] A security tool that allows to "freeze" an EBS volume and perform computer forensics on it.
- [x] A low-cost storage service that provides secure and durable storage for data archiving and backup.
- [ ] You mean Amazon "Iceberg": it's a low-cost storage service.

251.
If an Amazon EBS volume is the root device of an instance, can I detach it without stopping the instance?
**Choose the correct answer:**
- [ ] Yes but only if Windows instance
- [x] No
- [ ] Yes
- [ ] Yes but only if a Linux instance

252.
If you are using Amazon RDS Provisioned IOPS storage with MySQL and Oracle database engines, you can scale the throughput of your database Instance by specifying the IOPS rate from _____ .
**Choose the correct answer:**
- [ ] 1,000 to 1,00,000
- [ ] 100 to 1,000
- [ ] 10,000 to 1,00,000
- [x] 1,000 to 10,000

253.
Every user you create in the IAM system starts with ______.
**Choose the correct answer:**
- [ ] full permissions
- [x] no permissions
- [ ] partial permissions

254.
After an EC2-VPC instance is launched, can I change the VPC security groups it belongs to?
**Choose the correct answer:**
- [ ] Only if the tag "VPC_Change_Group" is true
- [x] Yes
- [ ] No
- [ ] Only if the tag "VPC Change Group" is true

255.
A______ is an individual, system, or application that interacts with AWS programmatically.
**Choose the correct answer:**
- [x] User
- [ ] AWS Account
- [ ] Group
- [ ] Role

256.*
Select the correct statement:
**Choose the correct answer:**
- [ ] You don't need not specify the resource identifier while stopping a resource
- [ ] You can terminate, stop, or delete a resource based solely on its tags
- [x] You can't terminate, stop, or delete a resource based solely on its tags
- [ ] You don't need to specify the resource identifier while terminating a resource

257.
Can I initiate a "forced failover" for my MySQL Multi-AZ DB Instance deployment?
**Choose the correct answer:**
- [ ] Only in certain regions
- [ ] Only in VPC
- [x] Yes
- [ ] No

258.
A group can contain many users. Can a user belong to multiple groups?
**Choose the correct answer:**
- [x] Yes
- [ ] No
- [ ] Only if they are using two factor authentication
- [ ] Only in VPC

259.
Is the encryption of connections between my application and my DB Instance using SSL for the MySQL server engines available?
**Choose the correct answer:**
- [x] Yes
- [ ] Only in VPC
- [ ] Only in certain regions
- [ ] No

260.*
Which AWS instance address has the following characteristics? :"If you stop an instance, its Elastic IP address is unmapped, and you must remap it when you restart the instance."
**Choose the correct answer:**
- [ ] None of these
- [ ] EC2-VPC Addresses
- [x] EC2-Classic Addresses

261.
Please select the most correct answer regarding the persistence of the Amazon Instance Store:
**Choose the correct answer:**
- [x] The data on an instance store volume persists only during the life of the associated Amazon EC2 instance
- [ ] The data on an instance store volume is lost when the security group rule of the associated instance is changed.
- [ ] The data on an instance store volume persists even after associated Amazon EC2 instance is deleted

262.
Multi-AZ deployment is supported for Microsoft SQL Server DB Instances.
**Choose the correct answer:**
- [x] True
- [ ] False

263.
Security groups act like a firewall at the instance level, whereas _____ are an additional layer of security that act at the subnet level.
**Choose the correct answer:**
- [ ] DB Security Groups
- [ ] VPC Security Groups
- [x] Network ACLs

264.
Does AWS allow for the use of Multi Factor Authentication tokens?
**Choose the correct answer:**
- [x] Yes, with both hardware or virtual MFA devices
- [ ] Yes, but only virtual MFA devices.
- [ ] Yes, but only physical (hardware) MFA devices.
- [ ] No

265.
What does Amazon SWF stand for?
**Choose the correct answer:**
- [ ] Simple Wireless Forms
- [ ] Simple Web Form
- [x] Simple Work Flow
- [ ] Simple Web Flow

266.
What does Amazon Elastic Beanstalk provide?
**Choose the correct answer:**
- [x] An application container on top of Amazon Web Services.
- [ ] A scalable storage appliance on top of Amazon Web Services.
- [ ] A scalable cluster of EC2 instances.
- [ ] A service by this name doesn't exist.

267.
Is the SQL Server Audit feature supported in the Amazon RDS SQL Server engine?
**Choose the correct answer:**
- [x] No
- [ ] Yes

268.
Are you able to integrate a multi-factor token service with the AWS Platform?
**Choose the correct answer:**
- [x] Yes, using the AWS multi-factor token devices to authenticate users on the AWS platform.
- [ ] No, you cannot integrate multi-factor token devices with the AWS platform.
- [ ] Yes, you can integrate private multi-factor token devices to authenticate users to the AWS platform.

269.
My Read Replica appears "stuck" after a Multi-AZ failover and is unable to obtain or apply updates from the source DB Instance. What do I do?
**Choose the correct answer:**
- [x] You will need to delete the Read Replica and create a new one to replace it.
- [ ] You will need to disassociate the DB Engine and re associate it.
- [ ] The instance should be deployed to Single AZ and then moved to Multi- AZ once again
- [ ] You will need to delete the DB Instance and create a new one to replace it.

270.
Which DNS name can only be resolved within Amazon EC2?
**Choose the correct answer:**
- [x] Internal DNS name
- [ ] External DNS name
- [ ] Global DNS name
- [ ] Private DNS name

271.
If your DB instance runs out of storage space or file system resources, its status will change to _____ and your DB Instance will no longer be available.
**Choose the correct answer:**
- [ ] storage-overflow
- [x] storage-full
- [ ] storage-exceed
- [ ] storage-overage

272.
Will my standby RDS instance be in the same Availability Zone as my primary?
**Choose the correct answer:**
- [ ] Only for Oracle RDS types
- [ ] Only if configured at launch
- [ ] Yes
- [x] No

273.
Does Amazon RDS for SQL Server currently support importing data into the msdb database?
**Choose the correct answer:**
- [x] No
- [ ] Yes

274.
Does Route 53 support MX Records?
**Choose the correct answer:**
- [x] Yes
- [ ] It supports CNAME records, but not MX records.
- [ ] No
- [ ] Only Primary MX records. Secondary MX records are not supported.

275.
How can I change the security group membership for interfaces owned by other AWS services, such as Elastic Load Balancing?
**Choose the correct answer:**
- [ ] using all these methods
- [x] By using the service specific console or API\CLI commands
- [ ] None of these

276.
When you perform a restore operation to a point in time or from a DB Snapshot, a new DB Instance is created with a new endpoint.
**Choose the correct answer:**
- [ ] FALSE
- [x] TRUE

277.
Which Amazon storage do you think is the best for my database-style applications that frequently encounter many random reads and writes across the dataset.
**Choose the correct answer:**
- [ ] None of these
- [ ] Amazon Instance Storage
- [ ] Any of these
- [x] Amazon EBS

278.*
In a management network scenario, which interface on the instance handles public-facing traffic?
**Choose the correct answer:**
- [ ] Primary network interface
- [ ] Subnet interface
- [x] Secondary network interface

279.
Select the correct set of steps for exposing the snapshot only to specific AWS accounts:
**Choose the correct answer:**
- [ ] Select public for all the accounts and check mark those accounts with whom you want to expose the snapshots and click save.
- [x] SelectPrivate, enter the IDs of those AWS accounts, and clickSave.
- [ ] SelectPublic, enter the IDs of those AWS accounts, and clickSave.
- [ ] SelectPublic, mark the IDs of those AWS accounts as private, and clickSave.

280.
Is decreasing the storage size of a DB Instance permitted?
**Choose the correct answer:**
- [ ] Depends on the RDMS used
- [x] Yes
- [ ] No

281.
When should I choose Provisioned IOPS over Standard RDS storage?
**Choose the correct answer:**
- [x] If you use production online transaction processing (OLTP) workloads.
- [ ] If you have batch-oriented workloads
- [ ] If you have workloads that are not sensitive to consistent performance

282.
In the 'Detailed' monitoring data available for your Amazon EBS volumes, Provisioned IOPS volumes automatically send _____ minute metrics to Amazon CloudWatch.
**Choose the correct answer:**
- [ ] 5
- [ ] 2
- [x] 1
- [ ] 3

283.
It is advised that you watch the Amazon CloudWatch _____ metric carefully and recreate the Read Replica should it fall behind due to replication errors.
**Choose the correct answer:**
- [ ] WriteLag
- [ ] ReadReplica
- [x] ReplicaLag
- [ ] SingleReplica

284.
Can the string value of 'Key' be prefixed with ":aws:"?
**Choose the correct answer:**
- [x] No
- [ ] Only for EC2 not S3
- [ ] Yes
- [ ] Only for S3 not EC2

285.
By default, what happens to ENIs that are automatically created and attached to EC2 instances when the attached instance terminates?
**Choose the correct answer:**
- [ ] Remain as is
- [x] Terminate
- [ ] Hibernate
- [ ] Pause

286.
You can use _____ and _____ to help secure the instances in your VPC.
**Choose the correct answer:**
- [ ] security groups and multi-factor authentication
- [ ] security groups and 2-Factor authentication
- [ ] security groups and biometric authentication
- [x] security groups and network ACLs

287.
_____ is a durable, block-level storage volume that you can attach to a single, running Amazon EC2 instance.
**Choose the correct answer:**
- [ ] Amazon S3
- [x] Amazon EBS
- [ ] Amazon EFS
- [ ] All of these

288.
Do the Amazon EBS volumes persist independently from the running life of an Amazon EC2 instance?
**Choose the correct answer:**
- [ ] No
- [ ] Only if instructed to when created
- [x] Yes

289.
If I want my instance to run on a single-tenant hardware, which value do I have to set the instance's tenancy attribute to?
**Choose the correct answer:**
- [x] dedicated
- [ ] isolated
- [ ] one
- [ ] reserved

290.
What does Amazon RDS stand for?
**Choose the correct answer:**
- [ ] Regional Data Server.
- [x] Relational Database Service.
- [ ] Nothing.
- [ ] Regional Database Service.
