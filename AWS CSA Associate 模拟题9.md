## AWS CSA Associate 模拟题9

544.
Which of the following are valid statements about Amazon S3? Choose 2 answers
- [ ] S3 provides read-after-write consistency for any type of PUT or DELETE.
- [ ] Consistency is not guaranteed for any type of PUT or DELETE.
- [x] A successful response to a PUT request only occurs when a complete object is saved
- [ ] Partially saved objects are immediately readable with a GET after an overwrite PUT.
- [x] S3 provides eventual consistency for overwrite PUTS and DELETES

545.
A customer is leveraging Amazon Simple Storage Service in eu-west-1 to store static content for web-based property. The customer is storing objects using the Standard Storage class. Where are the customers’ objects replicated?
- [ ] Single facility in eu-west-1 and a single facility in eu-central-1
- [ ] Single facility in eu-west-1 and a single facility in us-east-1
- [x] Multiple facilities in eu-west-1
- [ ] A single facility in eu-west-1

546.
A user has an S3 object in the US Standard region with the content “color=red”. The user updates the object with the content as “color=”white”. If the user tries to read the value 1 minute after it was uploaded, what will S3 return?
- [ ] It will return “color=white”
- [ ] It will return “color=red”
- [ ] It will return an error saying that the object was not found
- [x] It may return either “color=red” or “color=white” i.e. any of the value (Eventual Consistency)

547.
An organization’s security policy requires multiple copies of all critical data to be replicated across at least a primary and backup data center. The organization has decided to store some critical data on Amazon S3. Which option should you implement to ensure this requirement is met?
- [ ] Use the S3 copy API to replicate data between two S3 buckets in different regions
- [ ] You do not need to implement anything since S3 data is automatically replicated between regions
- [ ] Use the S3 copy API to replicate data between two S3 buckets in different facilities within an AWS Region
- [x] You do not need to implement anything since S3 data is automatically replicated between multiple facilities within an AWS Region

548.
A customer wants to track access to their Amazon Simple Storage Service (S3) buckets and also use this information for their internal security and access audits. Which of the following will meet the Customer requirement?
- [ ] Enable AWS CloudTrail to audit all Amazon S3 bucket access.
- [x] Enable server access logging for all required Amazon S3 buckets
- [ ] Enable the Requester Pays option to track access via AWS Billing
- [ ] Enable Amazon S3 event notifications for Put and Post.

549.
A user is enabling a static website hosting on an S3 bucket. Which of the below mentioned parameters cannot be configured by the user?
- [ ] Error document
- [x] Conditional error on object name
- [ ] Index document
- [ ] Conditional redirection on object name

560.
Company ABCD is running their corporate website on Amazon S3 accessed from http//www.companyabcd.com. Their marketing team has published new web fonts to a separate S3 bucket accessed by the S3 endpoint: https://s3-us-west1.amazonaws.com/abcdfonts. While testing the new web fonts, Company ABCD recognized the web fonts are being blocked by the browser. What should Company ABCD do to prevent the web fonts from being blocked by the browser?
- [ ] Enable versioning on the abcdfonts bucket for each web font
- [ ] Create a policy on the abcdfonts bucket to enable access to everyone
- [ ] Add the Content-MD5 header to the request for webfonts in the abcdfonts bucket from the website
- [x] Configure the abcdfonts bucket to allow cross-origin requests by creating a CORS configuration

551.
Company ABCD is currently hosting their corporate site in an Amazon S3 bucket with Static Website Hosting enabled. Currently, when visitors go to http://www.companyabcd.com the index.html page is returned. Company C now would like a new page welcome.html to be returned when a visitor enters http://www.companyabcd.com in the browser. Which of the following steps will allow Company ABCD to meet this requirement? Choose 2 answers.
- [x] Upload an html page named welcome.html to their S3 bucket
- [ ] Create a welcome subfolder in their S3 bucket
- [x] Set the Index Document property to welcome.html
- [ ] Move the index.html page to a welcome subfolder
- [ ] Set the Error Document property to welcome.html

552.
What does RRS stand for when talking about S3?
- [ ] Redundancy Removal System
- [ ] Relational Rights Storage
- [ ] Regional Rights Standard
- [x] Reduced Redundancy Storage

553.
What is the durability of S3 RRS?
- [x] 99.99%
- [ ] 99.95%
- [ ] 99.995%
- [ ] 99.999999999%

554.
What is the Reduced Redundancy option in Amazon S3?
- [x] Less redundancy for a lower cost
- [ ] It doesn’t exist in Amazon S3, but in Amazon EBS.
- [ ] It allows you to destroy any copy of your files outside a specific jurisdiction.
- [ ] It doesn’t exist at all

555.
An application is generating a log file every 5 minutes. The log file is not critical but may be required only for verification in case of some major issue. The file should be accessible over the internet whenever required. Which of the below mentioned options is a best possible storage solution for it?
- [ ] AWS S3
- [ ] AWS Glacier
- [ ] AWS RDS
- [x] AWS S3 RRS (Reduced Redundancy Storage (RRS) is an Amazon S3 storage option that enables customers to store noncritical, reproducible data at lower levels of redundancy than Amazon S3’s standard storage. RRS is designed to sustain the loss of data in a single facility.)

556.*
A user has moved an object to Glacier using the life cycle rules. The user requests to restore the archive after 6 months. When the restore request is completed the user accesses that archive. Which of the below mentioned statements is not true in this condition?
- [ ] The archive will be available as an object for the duration specified by the user during the restoration request
- [x] The restored object’s storage class will be RRS (After the object is restored the storage class still remains GLACIER. Read more)
- [ ] The user can modify the restoration period only by issuing a new restore request with the updated period
- [ ] The user needs to pay storage for both RRS (restored) and Glacier (Archive) Rates

567.
Which of the below mentioned options can be a good use case for storing content in AWS RRS?
- [ ] Storing mission critical data Files
- [ ] Storing infrequently used log files
- [ ] Storing a video file which is not reproducible
- [x] Storing image thumbnails

568.
Which set of Amazon S3 features helps to prevent and recover from accidental data loss?
- [ ] Object lifecycle and service access logging
- [x] Object versioning and Multi-factor authentication
- [ ] Access controls and server-side encryption
- [ ] Website hosting and Amazon S3 policies

569.
You use S3 to store critical data for your company Several users within your group currently have full permissions to your S3 buckets. You need to come up with a solution that does not impact your users and also protect against the accidental deletion of objects. Which two options will address this issue? Choose 2 answers
- [x] Enable versioning on your S3 Buckets
- [x] Configure your S3 Buckets with MFA delete
- [ ] Create a Bucket policy and only allow read only permissions to all users at the bucket level
- [ ] Enable object life cycle policies and configure the data older than 3 months to be archived in Glacier

570.
To protect S3 data from both accidental deletion and accidental overwriting, you should
- [x] enable S3 versioning on the bucket
- [ ] access S3 data using only signed URLs
- [ ] disable S3 delete using an IAM bucket policy
- [ ] enable S3 Reduced Redundancy Storage
- [ ] enable Multi-Factor Authentication (MFA) protected access

571.
A user has not enabled versioning on an S3 bucket. What will be the version ID of the object inside that bucket?
- [ ] 0
- [ ] There will be no version attached
- [x] Null
- [ ] Blank

572.
A user is trying to find the state of an S3 bucket with respect to versioning. Which of the below mentioned states AWS will not return when queried?
- [ ] versioning-enabled
- [ ] versioning-suspended
- [ ] unversioned
- [x] versioned

573.
Your firm has uploaded a large amount of aerial image data to S3. In the past, in your on-premises environment, you used a dedicated group of servers to oaten process this data and used Rabbit MQ, an open source messaging system, to get job information to the servers. Once processed the data would go to tape and be shipped offsite. Your manager told you to stay with the current design, and leverage AWS archival storage and messaging services to minimize cost. Which is correct?
- [ ] Use SQS for passing job messages, use Cloud Watch alarms to terminate EC2 worker instances when they become idle. Once data is processed, change the storage class of the S3 objects to Reduced Redundancy Storage (Need to replace On-Premises Tape functionality)
- [ ] Setup Auto-Scaled workers triggered by queue depth that use spot instances to process messages in SQS. Once data is processed, change the storage class of the S3 objects to Reduced Redundancy Storage (Need to replace On-Premises Tape functionality)
- [x] Setup Auto-Scaled workers triggered by queue depth that use spot instances to process messages in SQS. Once data is processed, change the storage class of the S3 objects to Glacier (Glacier suitable for Tape backup)
- [ ] Use SNS to pass job messages use Cloud Watch alarms to terminate spot worker instances when they become idle. Once data is processed, change the storage class of the S3 object to Glacier.

574.
You have a proprietary data store on-premises that must be backed up daily by dumping the data store contents to a single compressed 50GB file and sending the file to AWS. Your SLAs state that any dump file backed up within the past 7 days can be retrieved within 2 hours. Your compliance department has stated that all data must be held indefinitely. The time required to restore the data store from a backup is approximately 1 hour. Your on-premise network connection is capable of sustaining 1gbps to AWS. Which backup methods to AWS would be most cost-effective while still meeting all of your requirements?
- [ ] Send the daily backup files to Glacier immediately after being generated (will not meet the RTO)
- [ ] Transfer the daily backup files to an EBS volume in AWS and take daily snapshots of the volume (Not cost effective)
- [x] Transfer the daily backup files to S3 and use appropriate bucket lifecycle policies to send to Glacier (Store in S3 for seven days and then archive to Glacier)
- [ ] Host the backup files on a Storage Gateway with Gateway-Cached Volumes and take daily snapshots (Not Cost effective as local storage as well as S3 storage)

575.
Which features can be used to restrict access to data in S3? Choose 2 answers
- [x] Set an S3 ACL on the bucket or the object.
- [ ] Create a CloudFront distribution for the bucket.
- [x] Set an S3 bucket policy.
- [ ] Enable IAM Identity Federation
- [ ] Use S3 Virtual Hosting

576.
Which method can be used to prevent an IP address block from accessing public objects in an S3 bucket?
- [x] Create a bucket policy and apply it to the bucket
- [ ] Create a NACL and attach it to the VPC of the bucket
- [ ] Create an ACL and apply it to all objects in the bucket
- [ ] Modify the IAM policies of any users that would access the bucket

577.
A user has granted read/write permission of his S3 bucket using ACL. Which of the below mentioned options is a valid ID to grant permission to other AWS accounts (grantee. using ACL?
- [ ] IAM User ID
- [ ] S3 Secure ID
- [ ] Access ID
- [x] Canonical user ID

578.
A root account owner has given full access of his S3 bucket to one of the IAM users using the bucket ACL. When the IAM user logs in to the S3 console, which actions can he perform?
- [ ] He can just view the content of the bucket
- [ ] He can do all the operations on the bucket
- [x] It is not possible to give access to an IAM user using ACL
- [ ] The IAM user can perform all operations on the bucket using only API/SDK

579.
A root AWS account owner is trying to understand various options to set the permission to AWS S3. Which of the below mentioned options is not the right option to grant permission for S3?
- [x] User Access Policy
- [ ] S3 Object Policy
- [ ] S3 Bucket Policy
- [ ] S3 ACL

580.*
A system admin is managing buckets, objects and folders with AWS S3. Which of the below mentioned statements is true and should be taken in consideration by the sysadmin?
- [ ] Folders support only ACL
- [ ] Both the object and bucket can have an Access Policy but folder cannot have policy
- [ ] Folders can have a policy
- [x] Both the object and bucket can have ACL but folders cannot have ACL

581.*
A user has created an S3 bucket which is not publicly accessible. The bucket is having thirty objects which are also private. If the user wants to make the objects public, how can he configure this with minimal efforts?
- [ ] User should select all objects from the console and apply a single policy to mark them public
- [ ] User can write a program which programmatically makes all objects public using S3 SDK
- [x] Set the AWS bucket policy which marks all objects as public
- [ ] Make the bucket ACL as public so it will also mark all objects as public

582.
You need to configure an Amazon S3 bucket to serve static assets for your public-facing web application. Which methods ensure that all objects uploaded to the bucket are set to public read? Choose 2 answers
- [x] Set permissions on the object to public read during upload.
- [ ] Configure the bucket ACL to set all objects to public read.
- [x] Configure the bucket policy to set all objects to public read.
- [ ] Use AWS Identity and Access Management roles to set the bucket to public read.
- [ ] Amazon S3 objects default to public read, so no action is needed.

583.
Amazon S3 doesn’t automatically give a user who creates _____ permission to perform other actions on that bucket or object.
- [ ] a file
- [x] a bucket or object
- [ ] a bucket or file
- [ ] a object or file

584.
A root account owner is trying to understand the S3 bucket ACL. Which of the below mentioned options cannot be used to grant ACL on the object using the authorized predefined group?
- [ ] Authenticated user group
- [ ] All users group
- [ ] Log Delivery Group
- [x] Canonical user group

585.*
A user is enabling logging on a particular bucket. Which of the below mentioned options may be best suitable to allow access to the log bucket?
- [ ] Create an IAM policy and allow log access
- [ ] It is not possible to enable logging on the S3 bucket
- [ ] Create an IAM Role, which has access to the log bucket
- [x] Provide ACL for the logging group

586.*
A user is trying to configure access with S3. Which of the following options is not possible to provide access to the S3 bucket / object?
- [ ] Define the policy for the IAM user
- [ ] Define the ACL for the object
- [x] Define the policy for the object
- [ ] Define the policy for the bucket

587.
A user is having access to objects of an S3 bucket, which is not owned by him. If he is trying to set the objects of that bucket public, which of the below mentioned options may be a right fit for this action?
- [ ] Make the bucket public with full access
- [ ] Define the policy for the bucket
- [x] Provide ACL on the object
- [ ] Create an IAM user with permission

488.
A bucket owner has allowed another account’s IAM users to upload or access objects in his bucket. The IAM user of Account A is trying to access an object created by the IAM user of account B. What will happen in this scenario?
- [ ] The bucket policy may not be created as S3 will give error due to conflict of Access Rights
- [ ] It is not possible to give permission to multiple IAM users
- [x] AWS S3 will verify proper rights given by the owner of Account A, the bucket owner as well as by the IAM user B to the object
- [ ] It is not possible that the IAM user of one account accesses objects of the other IAM user

589.
A company is storing data on Amazon Simple Storage Service (S3). The company’s security policy mandates that data is encrypted at rest. Which of the following methods can achieve this? Choose 3 answers
- [x] Use Amazon S3 server-side encryption with AWS Key Management Service managed keys
- [x] Use Amazon S3 server-side encryption with customer-provided keys
- [ ] Use Amazon S3 server-side encryption with EC2 key pair.
- [ ] Use Amazon S3 bucket policies to restrict access to the data at rest.
- [x] Encrypt the data on the client-side before ingesting to Amazon S3 using their own master key
- [ ] Use SSL to encrypt the data while in transit to Amazon S3.

490.
A user has enabled versioning on an S3 bucket. The user is using server side encryption for data at Rest. If the user is supplying his own keys for encryption (SSE-C) which of the below mentioned statements is true?
- [ ] The user should use the same encryption key for all versions of the same object
- [x] It is possible to have different encryption keys for different versions of the same object
- [ ] AWS S3 does not allow the user to upload his own keys for server side encryption
- [ ] The SSE-C does not work when versioning is enabled

591.
A storage admin wants to encrypt all the objects stored in S3 using server side encryption. The user does not want to use the AES 256 encryption key provided by S3. How can the user achieve this?
- [ ] The admin should upload his secret key to the AWS console and let S3 decrypt the objects
- [ ] The admin should use CLI or API to upload the encryption key to the S3 bucket. When making a call to the S3 API mention the encryption key URL in each request
- [ ] S3 does not support client supplied encryption keys for server side encryption
- [x] The admin should send the keys and encryption algorithm with each API call

492.
A user has enabled versioning on an S3 bucket. The user is using server side encryption for data at rest. If the user is supplying his own keys for encryption (SSE-C), what is recommended to the user for the purpose of security?
- [ ] User should not use his own security key as it is not secure
- [ ] Configure S3 to rotate the user’s encryption key at regular intervals
- [ ] Configure S3 to store the user’s keys securely with SSL
- [x] Keep rotating the encryption key manually at the client side

593.
A system admin is planning to encrypt all objects being uploaded to S3 from an application. The system admin does not want to implement his own encryption algorithm; instead he is planning to use server side encryption by supplying his own key (SSE-C.. Which parameter is not required while making a call for SSE-C?
- [x] x-amz-server-side-encryption-customer-key-AES-256
- [ ] x-amz-server-side-encryption-customer-key
- [ ] x-amz-server-side-encryption-customer-algorithm
- [ ] x-amz-server-side-encryption-customer-key-MD5

594.
A customer is leveraging Amazon Simple Storage Service in eu-west-1 to store static content for a web-based property. The customer is storing objects using the Standard Storage class. Where are the customers objects replicated?
- [ ] A single facility in eu-west-1 and a single facility in eu-central-1
- [ ] A single facility in eu-west-1 and a single facility in us-east-1
- [x] Multiple facilities in eu-west-1
- [ ] A single facility in eu-west-1

595.
You are designing a personal document-archiving solution for your global enterprise with thousands of employee. Each employee has potentially gigabytes of data to be backed up in this archiving solution. The solution will be exposed to he employees as an application, where they can just drag and drop their files to the archiving system. Employees can retrieve their archives through a web interface. The corporate network has high bandwidth AWS DirectConnect connectivity to AWS. You have regulatory requirements that all data needs to be encrypted before being uploaded to the cloud. How do you implement this in a highly available and cost efficient way?
- [ ] Manage encryption keys on-premise in an encrypted relational database. Set up an on-premises server with sufficient storage to temporarily store files and then upload them to Amazon S3, providing a client-side master key. (Storing temporary increases cost and not a high availability option)
- [ ] Manage encryption keys in a Hardware Security Module(HSM) appliance on-premise server with sufficient storage to temporarily store, encrypt, and upload files directly into amazon Glacier. (Not cost effective)
- [x] Manage encryption keys in amazon Key Management Service (KMS), upload to amazon simple storage service (s3) with client-side encryption using a KMS customer master key ID and configure Amazon S3 lifecycle policies to store each object using the amazon glacier storage tier. (with CSE-KMS the encryption happens at client side before the object is upload to S3 and KMS is cost effective as well)
- [ ] Manage encryption keys in an AWS CloudHSM appliance. Encrypt files prior to uploading on the employee desktop and then upload directly into amazon glacier (Not cost effective)

496.
A user has enabled server side encryption with S3. The user downloads the encrypted object from S3. How can the user decrypt it?
- [ ] S3 does not support server side encryption
- [ ] S3 provides a server side key to decrypt the object
- [ ] The user needs to decrypt the object using their own private key
- [x] S3 manages encryption and decryption automatically

597.
When uploading an object, what request header can be explicitly specified in a request to Amazon S3 to encrypt object data when saved on the server side?
- [ ] x-amz-storage-class
- [ ] Content-MD5
- [ ] x-amz-security-token
- [x] x-amz-server-side-encryption

498.
A media company produces new video files on-premises every day with a total size of around 100GB after compression. All files have a size of 1-2 GB and need to be uploaded to Amazon S3 every night in a fixed time window between 3am and 5am. Current upload takes almost 3 hours, although less than half of the available bandwidth is used. What step(s) would ensure that the file uploads are able to complete in the allotted time window?
- [ ] Increase your network bandwidth to provide faster throughput to S3
- [x] Upload the files in parallel to S3 using multipart upload
- [ ] Pack all files into a single archive, upload it to S3, then extract the files in AWS
- [ ] Use AWS Import/Export to transfer the video files

599.
You are designing a web application that stores static assets in an Amazon Simple Storage Service (S3) bucket. You expect this bucket to immediately receive over 150 PUT requests per second. What should you do to ensure optimal performance?
- [ ] Use multi-part upload.
- [x] Add a random prefix to the key names.
- [ ] Amazon S3 will automatically manage performance at this scale.
- [ ] Use a predictable naming scheme, such as sequential numbers or date time sequences, in the key names

600.
You have an application running on an Amazon Elastic Compute Cloud instance, that uploads 5 GB video objects to Amazon Simple Storage Service (S3). Video uploads are taking longer than expected, resulting in poor application performance. Which method will help improve performance of your application?
- [ ] Enable enhanced networking
- [x] Use Amazon S3 multipart upload
- [ ] Leveraging Amazon CloudFront, use the HTTP POST method to reduce latency.
- [ ] Use Amazon Elastic Block Store Provisioned IOPs and use an Amazon EBS-optimized instance

601.
Which of the following methods gives you protection against accidental loss of data stored in Amazon S3? (Choose 2)
- [x] Set bucket policies to restrict deletes, and also enable versioning
- [ ] By default, versioning is enabled on a new bucket so you don’t have to worry about it (Not enabled by default)
- [ ] Build a secondary index of your keys to protect the data (improves performance only)
- [ ] Back up your bucket to a bucket owned by another AWS account for redundancy

602
A startup company hired you to help them build a mobile application that will ultimately store billions of image and videos in Amazon S3. The company is lean on funding, and wants to minimize operational costs, however, they have an aggressive marketing plan, and expect to double their current installation base every six months. Due to the nature of their business, they are expecting sudden and large increases to traffic to and from S3, and need to ensure that it can handle the performance needs of their application. What other information must you gather from this customer in order to determine whether S3 is the right option?
- [ ] You must know how many customers that company has today, because this is critical in understanding what their customer base will be in two years. (No. of customers do not matter)
- [x] You must find out total number of requests per second at peak usage.
- [ ] You must know the size of the individual objects being written to S3 in order to properly design the key namespace. (Size does not relate to the key namespace design but the count does)
- [ ] In order to build the key namespace correctly, you must understand the total amount of storage needs for each S3 bucket. (S3 provided unlimited storage the key namespace design would depend on the number)

603.
A document storage company is deploying their application to AWS and changing their business model to support both free tier and premium tier users. The premium tier users will be allowed to store up to 200GB of data and free tier customers will be allowed to store only 5GB. The customer expects that billions of files will be stored. All users need to be alerted when approaching 75 percent quota utilization and again at 90 percent quota use. To support the free tier and premium tier users, how should they architect their application?
- [x] The company should utilize an amazon simple workflow service activity worker that updates the users data counter in amazon dynamo DB. The activity worker will use simple email service to send an email if the counter increases above the appropriate thresholds.
- [ ] The company should deploy an amazon relational data base service relational database with a store objects table that has a row for each stored object along with size of each object. The upload server will query the aggregate consumption of the user in questions (by first determining the files store by the user, and then querying the stored objects table for respective file sizes) and send an email via Amazon Simple Email Service if the thresholds are breached. (Good Approach to use RDS but with so many objects might not be a good option)
- [ ] The company should write both the content length and the username of the files owner as S3 metadata for the object. They should then create a file watcher to iterate over each object and aggregate the size for each user and send a notification via Amazon Simple Queue Service to an emailing service if the storage threshold is exceeded. (List operations on S3 not feasible)
- [ ] The company should create two separated amazon simple storage service buckets one for data storage for free tier users and another for data storage for premium tier users. An amazon simple workflow service activity worker will query all objects for a given user based on the bucket the data is stored in and aggregate storage. The activity worker will notify the user via Amazon Simple Notification Service when necessary (List operations on S3 not feasible as well as SNS does not address email requirement)

604.
Your company host a social media website for storing and sharing documents. the web application allow users to upload large files while resuming and pausing the upload as needed. Currently, files are uploaded to your php front end backed by Elastic Load Balancing and an autoscaling fleet of amazon elastic compute cloud (EC2) instances that scale upon average of bytes received (NetworkIn) After a file has been uploaded. it is copied to amazon simple storage service(S3). Amazon Ec2 instances use an AWS Identity and Access Management (AMI) role that allows Amazon s3 uploads. Over the last six months, your user base and scale have increased significantly, forcing you to increase the auto scaling groups Max parameter a few times. Your CFO is concerned about the rising costs and has asked you to adjust the architecture where needed to better optimize costs. Which architecture change could you introduce to reduce cost and still keep your web application secure and scalable?
- [ ] Replace the Autoscaling launch Configuration to include c3.8xlarge instances; those instances can potentially yield a network throughput of 10gbps. (no info of current size and might increase cost)
- [ ] Re-architect your ingest pattern, have the app authenticate against your identity provider as a broker fetching temporary AWS credentials from AWS Secure token service (GetFederation Token). Securely pass the credentials and s3 endpoint/prefix to your app. Implement client-side logic to directly upload the file to amazon s3 using the given credentials and S3 Prefix. (will not provide the ability to handle pause and restarts)
- [ ] Re-architect your ingest pattern, and move your web application instances into a VPC public subnet. Attach a public IP address for each EC2 instance (using the auto scaling launch configuration settings). Use Amazon Route 53 round robin records set and http health check to DNS load balance the app request this approach will significantly reduce the cost by bypassing elastic load balancing. (ELB is not the bottleneck)
- [x] Re-architect your ingest pattern, have the app authenticate against your identity provider as a broker fetching temporary AWS credentials from AWS Secure token service (GetFederation Token). Securely pass the credentials and s3 endpoint/prefix to your app. Implement client-side logic that used the S3 multipart upload API to directly upload the file to Amazon s3 using the given credentials and s3 Prefix. (multipart allows one to start uploading directly to S3 before the actual size is known or complete data is downloaded)

605.
If an application is storing hourly log files from thousands of instances from a high traffic web site, which naming scheme would give optimal performance on S3?
- [ ] Sequential
- [ ] instanceID_log-HH-DD-MM-YYYY
- [ ] instanceID_log-YYYY-MM-DD-HH
- [x] HH-DD-MM-YYYY-log_instanceID (HH will give some randomness to start with instead of instaneId where the first characters would be i-)
- [ ] YYYY-MM-DD-HH-log_instanceID

606.
You are running a successful multi-tier web application on AWS and your marketing department has asked you to add a reporting tier to the application. The reporting tier will aggregate and publish status reports every 30 minutes from user-generated information that is being stored in your web applications database. You are currently running a Multi-AZ RDS MySQL instance for the database tier. You also have implemented ElastiCache as a database caching layer between the application tier and database tier. Please select the answer that will allow you to successfully implement the reporting tier with as little impact as possible to your database.
- [ ] Continually send transaction logs from your master database to an S3 bucket and generate the reports off the S3 bucket using S3 byte range requests.
- [ ] Generate the reports by querying the synchronously replicated standby RDS MySQL instance maintained through Multi-AZ (Standby instance cannot be used as a scaling solution)
- [x] Launch a RDS Read Replica connected to your Multi-AZ master database and generate reports by querying the Read Replica.
- [ ] Generate the reports by querying the ElastiCache database caching tier. (ElasticCache does not maintain full data and is simply a caching solution)

607.
A company is deploying a new two-tier web application in AWS. The company has limited staff and requires high availability, and the application requires complex queries and table joins. Which configuration provides the solution for the company’s requirements?
- [ ] MySQL Installed on two Amazon EC2 Instances in a single Availability Zone (does not provide High Availaility out of the box)
- [x] Amazon RDS for MySQL with Multi-AZ
- [ ] Amazon ElastiCache (Just a caching solution)
- [ ] Amazon DynamoDB (Not suitable for complex queries and joins)

608.
Your company is getting ready to do a major public announcement of a social media site on AWS. The website is running on EC2 instances deployed across multiple Availability Zones with a Multi-AZ RDS MySQL Extra Large DB Instance. The site performs a high number of small reads and writes per second and relies on an eventual consistency model. After comprehensive tests you discover that there is read contention on RDS MySQL. Which are the best approaches to meet these requirements? (Choose 2 answers)
- [x] Deploy ElastiCache in-memory cache running in each availability zone
- [ ] Implement sharding to distribute load to multiple RDS MySQL instances (this is only a read contention, the writes work fine)
- [ ] Increase the RDS MySQL Instance size and Implement provisioned IOPS (not scalable, this is only a read contention, the writes work fine)
- [x] Add an RDS MySQL read replica in each availability zone

609.
Your company has HQ in Tokyo and branch offices all over the world and is using logistics software with a multi-regional deployment on AWS in Japan, Europe and US. The logistic software has a 3-tier architecture and currently uses MySQL 5.6 for data persistence. Each region has deployed its own database. In the HQ region you run an hourly batch process reading data from every region to compute cross-regional reports that are sent by email to all offices this batch process must be completed as fast as possible to quickly optimize logistics. How do you build the database architecture in order to meet the requirements?
- [x] For each regional deployment, use RDS MySQL with a master in the region and a read replica in the HQ region
- [ ] For each regional deployment, use MySQL on EC2 with a master in the region and send hourly EBS snapshots to the HQ region
- [ ] For each regional deployment, use RDS MySQL with a master in the region and send hourly RDS snapshots to the HQ region
- [ ] For each regional deployment, use MySQL on EC2 with a master in the region and use S3 to copy data files hourly to the HQ region
- [ ] Use Direct Connect to connect all regional MySQL deployments to the HQ region and reduce network latency for the batch process

610.
What would happen to an RDS (Relational Database Service) multi-Availability Zone deployment if the primary DB instance fails?
- [ ] IP of the primary DB Instance is switched to the standby DB Instance.
- [ ] A new DB instance is created in the standby availability zone.
- [x] The canonical name record (CNAME) is changed from primary to standby.
- [ ] The RDS (Relational Database Service) DB instance reboots.

611.
Your business is building a new application that will store its entire customer database on a RDS MySQL database, and will have various applications and users that will query that data for different purposes. Large analytics jobs on the database are likely to cause other applications to not be able to get the query results they need to, before time out. Also, as your data grows, these analytics jobs will start to take more time, increasing the negative effect on the other applications. How do you solve the contention issues between these different workloads on the same data?
- [ ] Enable Multi-AZ mode on the RDS instance
- [ ] Use ElastiCache to offload the analytics job data
- [x] Create RDS Read-Replicas for the analytics work
- [ ] Run the RDS instance on the largest size possible

612.
Will my standby RDS instance be in the same Availability Zone as my primary?
- [ ] Only for Oracle RDS types
- [ ] Yes
- [ ] Only if configured at launch
- [x] No

613.
Is creating a Read Replica of another Read Replica supported?
- [ ] Only in certain regions
- [x] Only with MySQL based RDS
- [ ] Only for Oracle RDS types
- [ ] No

614.
A user is planning to set up the Multi-AZ feature of RDS. Which of the below mentioned conditions won’t take advantage of the Multi-AZ feature?
- [ ] Availability zone outage
- [ ] A manual failover of the DB instance using Reboot with failover option
- [x] Region outage
- [ ] When the user changes the DB instance’s server type

615.
When you run a DB Instance as a Multi-AZ deployment, the “_____” serves database writes and reads
- [ ] secondary
- [ ] backup
- [ ] stand by
- [x] primary

616.
When running my DB Instance as a Multi-AZ deployment, can I use the standby for read or write operations?
- [ ] Yes
- [ ] Only with MSSQL based RDS
- [ ] Only for Oracle RDS instances
- [x] No

617.
Read Replicas require a transactional storage engine and are only supported for the _________ storage engine
- [ ] OracleISAM
- [ ] MSSQLDB
- [x] InnoDB
- [ ] MyISAM

618.
A user is configuring the Multi-AZ feature of an RDS DB. The user came to know that this RDS DB does not use the AWS technology, but uses server mirroring to achieve replication. Which DB is the user using right now?
- [ ] MySQL
- [ ] Oracle
- [x] MS SQL
- [ ] PostgreSQL

619.
If I have multiple Read Replicas for my master DB Instance and I promote one of them, what happens to the rest of the Read Replicas?
- [x] The remaining Read Replicas will still replicate from the older master DB Instance
- [ ] The remaining Read Replicas will be deleted
- [ ] The remaining Read Replicas will be combined to one read replica

620.
If you have chosen Multi-AZ deployment, in the event of a planned or unplanned outage of your primary DB Instance, Amazon RDS automatically switches to the standby replica. The automatic failover mechanism simply changes the ______ record of the main DB Instance to point to the standby DB Instance.
- [ ] DNAME
- [x] CNAME
- [ ] TXT
- [ ] MX

621.
When automatic failover occurs, Amazon RDS will emit a DB Instance event to inform you that automatic failover occurred. You can use the _____ to return information about events related to your DB Instance
- [ ] FetchFailure
- [ ] DescriveFailure
- [x] DescribeEvents
- [ ] FetchEvents

622.
The new DB Instance that is created when you promote a Read Replica retains the backup window period.
- [x] TRUE
- [ ] FALSE

623.
Will I be alerted when automatic failover occurs?
- [x] Only if SNS configured
- [ ] No
- [ ] Yes
- [ ] Only if Cloudwatch configured

624.
Can I initiate a “forced failover” for my MySQL Multi-AZ DB Instance deployment?
- [ ] Only in certain regions
- [ ] Only in VPC
- [x] Yes
- [ ] No

625.
A user is accessing RDS from an application. The user has enabled the Multi-AZ feature with the MS SQL RDS DB. During a planned outage how will AWS ensure that a switch from DB to a standby replica will not affect access to the application?
- [ ] RDS will have an internal IP which will redirect all requests to the new DB
- [x] RDS uses DNS to switch over to standby replica for seamless transition
- [ ] The switch over changes Hardware so RDS does not need to worry about access
- [ ] RDS will have both the DBs running independently and the user has to manually switch over

626.
Which of the following is part of the failover process for a Multi-AZ Amazon Relational Database Service (RDS) instance?
- [ ] The failed RDS DB instance reboots.
- [ ] The IP of the primary DB instance is switched to the standby DB instance.
- [x] The DNS record for the RDS endpoint is changed from primary to standby.
- [ ] A new DB instance is created in the standby availability zone.

627.
Which of these is not a reason a Multi-AZ RDS instance will failover?
- [ ] An Availability Zone outage
- [ ] A manual failover of the DB instance was initiated using Reboot with failover
- [x] To autoscale to a higher instance class (Refer link)
- [ ] The primary DB instance fails

628.
You need to scale an RDS deployment. You are operating at 10% writes and 90% reads, based on your logging. How best can you scale this in a simple way?
- [ ] Create a second master RDS instance and peer the RDS groups.
- [ ] Cache all the database responses on the read side with CloudFront.
- [x] Create read replicas for RDS since the load is mostly reads.
- [ ] Create a Multi-AZ RDS installs and route read traffic to standby.

629.
How does Amazon RDS multi Availability Zone model work?
- [x] A second, standby database is deployed and maintained in a different availability zone from master, using synchronous replication. (Refer link)
- [ ] A second, standby database is deployed and maintained in a different availability zone from master using asynchronous replication.
- [ ] A second, standby database is deployed and maintained in a different region from master using asynchronous replication.
- [ ] A second, standby database is deployed and maintained in a different region from master using synchronous replication.

630.
A customer is running an application in US-West (Northern California) region and wants to setup disaster recovery failover to the Asian Pacific (Singapore) region. The customer is interested in achieving a low Recovery Point Objective (RPO) for an Amazon RDS multi-AZ MySQL database instance. Which approach is best suited to this need?
- [ ] Synchronous replication
- [x] Asynchronous replication
- [ ] Route53 health checks
- [ ] Copying of RDS incremental snapshots

631.
A user is using a small MySQL RDS DB. The user is experiencing high latency due to the Multi AZ feature. Which of the below mentioned options may not help the user in this situation?
- [ ] Schedule the automated back up in non-working hours
- [ ] Use a large or higher size instance
- [ ] Use PIOPS
- [x] Take a snapshot from standby Replica

632.
Are Reserved Instances available for Multi-AZ Deployments?
- [ ] Only for Cluster Compute instances
- [x] Yes for all instance types
- [ ] Only for M3 instance types

633.
My Read Replica appears “stuck” after a Multi-AZ failover and is unable to obtain or apply updates from the source DB Instance. What do I do?
- [x] You will need to delete the Read Replica and create a new one to replace it.
- [ ] You will need to disassociate the DB Engine and re associate it.
- [ ] The instance should be deployed to Single AZ and then moved to Multi- AZ once again
- [ ] You will need to delete the DB Instance and create a new one to replace it.

634.
What is the charge for the data transfer incurred in replicating data between your primary and standby?
- [x] No charge. It is free.
- [ ] Double the standard data transfer charge
- [ ] Same as the standard data transfer charge
- [ ] Half of the standard data transfer charge

635.
A user has enabled the Multi AZ feature with the MS SQL RDS database server. Which of the below mentioned statements will help the user understand the Multi AZ feature better?
- [ ] In a Multi AZ, AWS runs two DBs in parallel and copies the data asynchronously to the replica copy
- [ ] In a Multi AZ, AWS runs two DBs in parallel and copies the data synchronously to the replica copy
- [x] In a Multi AZ, AWS runs just one DB but copies the data synchronously to the standby replica
- [ ] AWS MS SQL does not support the Multi AZ feature

636.
A company is running a batch analysis every hour on their main transactional DB running on an RDS MySQL instance to populate their central Data Warehouse running on Redshift. During the execution of the batch their transactional applications are very slow. When the batch completes they need to update the top management dashboard with the new data. The dashboard is produced by another system running on-premises that is currently started when a manually-sent email notifies that an update is required The on-premises system cannot be modified because is managed by another team. How would you optimize this scenario to solve performance issues and automate the process as much as possible?
- [ ] Replace RDS with Redshift for the batch analysis and SNS to notify the on-premises system to update the dashboard
- [ ] Replace RDS with Redshift for the batch analysis and SQS to send a message to the on-premises system to update the dashboard
- [x] Create an RDS Read Replica for the batch analysis and SNS to notify me on-premises system to update the dashboard
- [ ] Create an RDS Read Replica for the batch analysis and SQS to send a message to the on-premises system to update the dashboard.

637.
When should I choose Provisioned IOPS over Standard RDS storage?
- [ ] If you have batch-oriented workloads
- [x] If you use production online transaction processing (OLTP) workloads
- [ ] If you have workloads that are not sensitive to consistent performance

638.
Is decreasing the storage size of a DB Instance permitted?
- [ ] Depends on the RDMS used
- [ ] Yes
- [x] No

639.
Because of the extensibility limitations of striped storage attached to Windows Server, Amazon RDS does not currently support increasing storage on a _____ DB Instance.
- [x] SQL Server
- [ ] MySQL
- [ ] Oracle

640.
If I want to run a database in an Amazon instance, which is the most recommended Amazon storage option?
- [ ] Amazon Instance Storage
- [x] Amazon EBS
- [ ] You can’t run a database inside an Amazon instance.
- [ ] Amazon S3

641.
For each DB Instance class, what is the maximum size of associated storage capacity?
- [ ] 1TB
- [ ] 2TB
- [ ] 500GB
- [x] 6TB (Except SQL Server which is currently 4TB)
