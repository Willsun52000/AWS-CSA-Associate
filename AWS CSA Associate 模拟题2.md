
## AWS CSA Associate 模拟题2

80.
Your supervisor asks you to create a highly-available website which serves static content from EC2 instances. Which of the following is not a requirement to accomplish this goal?
**Choose the correct answer:**
- [ ] Multiple Availability Zones
- [ ] Multiple subnets
- [x] An SQS queue
- [ ] An Auto Scaling group to recover from EC2 instance failures

81.
For basic monitoring on AWS, which metrics are not included as part of the basic monitoring package?
**Choose the 2 correct answers:**
- [ ] CPU utilization
- [x] Free memory
- [ ] Network utilization
- [x] Free swap

82.
The KPL is an easy-to-use, highly-configurable library that helps you write to an Amazon Kinesis stream. It acts as an intermediary between your producer application code and the stream's API actions. One of its key concepts is aggregation. Which of the following best describes aggregation as it relates to the KPL?
**Choose the correct answer:**
- [ ] It refers to batching multiple streams' records and sending them in a single HTTP request with a call to the API operation PutRecords, instead of sending each stream's record in its own HTTP request
- [ ] It is a blob of data that has particular meaning to the user. Examples include a JSON blob representing a UI event on a web site, or a log entry from a web server
- [x] It refers to the storage of multiple records in a stream's record and allows customers to increase the number of records sent per API call, which effectively increases producer throughput
- [ ] It refers to performing a single action on multiple items instead of repeatedly performing the action on each individual item

83.
Your company is posting a big article on the front page of your website tomorrow. It is expected that the demand could potentially overwhelm your infrastructure. In the event of a load failure, how can you set up DNS failover to a static website?
**Choose the correct answer:**
- [ ] Enable failover to an on-premises data center
- [ ] Duplicate the exact application architecture in another region and configure DNS latency-based routing
- [x] Use Route 53 and the failover option to failover to a static S3 website bucket or CloudFront distribution in the event of an issue
- [ ] Build out additional capacity to ensure there is no scenario in which the application can fail

84.
Which statements are true about Amazon S3?
Choose the 2 correct answers:
- [ ] Provides %99.99 durability to S3 objects
- [ ] Provides %99.999999999 availability to S3 objects
- [x] Provides %99.999999999 durability to S3 objects
- [x] Provides %99.99 availability to S3 objects

85.
Your company requires that all the data on your EBS-backed EC2 volumes be encrypted. How would you go about doing this?
**Choose the correct answer:**
- [ ] You cannot enable EBS encryption on a specific volume
- [x] AWS allows you to encrypt the file system on an EBS volume on EBS volume setup
- [ ] Encryption can be done on the OS layer of the EBS volume
- [ ] None of the above

86.
Your AWS environment contains several reserved EC2 instances dedicated to a project that has just been cancelled. Your supervisor would like to recuperate cost for these reserved instances, but also does not want to lose the data just yet in case the project is revived next fiscal year. What can you do to minimize charges for these instances?
**Choose the 2 correct answers:**
- [x] Take snapshots of the EBS volumes and terminate the instances
- [ ] Contact AWS and explain the situation
- [x] Sell the instances on the AWS Reserved Instance Marketplace
- [ ] Stop the instances as soon as possible

87.
An EC2 instance retrieves a message from an SQS queue, begins processing the message, then crashes. What happens to the message?
**Choose the correct answer:**
- [ ] To prevent data loss, it remains in the queue in a locked state until the EC2 instance comes back online
- [x] When the message visibility timeout expires, the message becomes available for processing by other EC2 instances
- [ ] To prevent data corruption, if the EC2 instance does not respond to a customizable number of pings, the message is deleted
- [ ] To prevent data corruption, when the message hide timeout expires, the message is duplicated, the original message is archived, and the duplicate message becomes available for processing by other EC2 instances

88.
After building an application that makes use of an Elastic Load Balancer over port 80, you notice that your instances, even though they are healthy as per the health check, are not serving traffic when you go to the ELB DNS cname. What might be the cause of this issue?
**Choose the 2 correct answers:**
- [x] The ELB security group does not have port 80 open
- [ ] There is no attached Internet gateway on the private subnet
- [x] The EC2 instances security group does not have port 80 open
- [ ] The EC2 instances are part of a public subnet

89.
When reviewing the Auto Scaling events, it is noticed that an application is scaling up and down multiple times within the hour. What design change could you make to optimize cost while preserving elasticity?
**Choose the correct answer:**
- [ ] Add provisioned IOPS to the instances
- [ ] Change the scale down CloudWatch metric to a higher threshold
- [ ] Increase the instance type in the launch configuration
- [ ] Increase the base number of Auto Scaling instances for the Auto Scaling group

90.
You are consulting for a company with a limited budget for on-premises hardware; however, they need to store large amounts of data that is easily accessible through a network share with on-premises employees. Which AWS solution would you implement for this company?
**Choose the correct answer:**
- [ ] Configure Storage Gateway with gateway-stored volumes
- [ ] Configure S3 as a file system on a local on-premises server
- [ ] EC2 instances with large EBS volumes and a VPN from VPC to the on-premises network
- [ ] Configure Storage Gateway with gateway-cached volumes

91.
In the basic monitoring package for EC2, Amazon CloudWatch provides the following metrics:
**Choose the correct answer:**
- [ ] Web service visible metrics, such as number failed transaction requests
- [ ] Operating system visible metrics, such as memory utilization
- [ ] Hypervisor visible metrics, such as CPU utilization
- [ ] Database memory usage

92.
Your organization has been using an HSM (Hardware Security Module) for secure key storage. It is only used for generating keys for your EC2 instances. Unfortunately, the HSM has been zeroized after someone attempted to log in as the administrator three times using an invalid password. This means that the encryption keys on it have been wiped. You did not have a copy of the keys stored anywhere else. How can you obtain a new copy of the keys that you had stored on HSM?
**Choose the correct answer:**
- [ ] You can still connect via CLI; use the command 'get-client-configuration' and you can get a copy of the keys
- [ ] Contact AWS Support; your incident will be routed to the team that supports AWS - [ ] CloudHSM and a copy of the keys will be sent to you after verification
- [ ] Restore a snapshot of the HSM
- [ ] You cannot; the keys are lost if you did not have a copy.

93.
Ten students have just been employed by your company for one week, and it is your task to provide them with access to AWS, through IAM. Your supervisor has come to you and said that he wants to be able to track these students as a group, rather than individually. Because of this, he has requested for them to all have the same login ID but completely different passwords. Which of the following is the best way to achieve this?
**Choose the correct answer:**
- [x] It isn't possible to have the same login ID for multiple IAM users of the same account
- [ ] Create a separate login ID, but give each IAM user the same alias so that each one can login with their alias
- [ ] Create various groups and add each user with the same login ID to different groups. The user can login with their own group ID
- [ ] Use Multi Factor Authentication to verify each user and they will all be able to use the same login

94.
As part of your application architecture requirements, the company you are working for has requested the ability to run analytics against all combined log files from the Elastic Load Balancer. Which services are used together to collect logs and process log file analysis in an AWS environment?
**Choose the correct answer:**
- [ ] Amazon DynamoDB to store the logs and EC2 for running custom log analysis scripts
- [ ] Amazon EC2 for storing and processing the log files
- [x] Amazon S3 for storing ELB log files and Amazon EMR for processing the log files in analysis
- [ ] Amazon S3 for storing the ELB log files and EC2 for processing the log files in analysis

95.
Which of the following is not a legitimate concern?
**Choose the correct answer:**
- [ ] Multi-AZ RDS deployments require a minimum of two subnets in a subnet group
- [ ] Databases typically should not be deployed on a public subnet
- [ ] Multi-AZ RDS deployments require at least two Availability Zones
- [x] US-East-1 is does not support Multi-AZ RDS deployments.

96.
Your EC2 instances are configured to run behind an Amazon VPC. You have assigned two web servers instances to an Elastic Load Balancer. However, the instances and the ELB are not reachable via URL to the elastic load balancer serving the web app data from the EC2 instances. How might you resolve the issue so that your instances are serving the web app data to the public Internet?
**Choose the correct answer:**
- [x] Attach an internet gateway to the VPC and route it to the subnet
- [ ] Add an elastic IP address to the instance
- [ ]Use Amazon Elastic Load Balancer to serve requests to your instances located in the  internal subnet
- [ ] None of the above

97.
When a snapshot is being taken against an EBS volume, the volume becomes unavailable and the instance no longer has the ability to communicate with the EBS volume until the snapshot is complete.
**Choose the correct answer:**
- [ ] True
- [x] False

98.
Which of the following is not a benefit of a decoupled architecture using EC2, Auto Scaling, and SQS?
**Choose the correct answer:**
- [ ] Auto Scaling can spin up new EC2 instances to handle an increased number of items in an SQS queue
- [ ] An application does not become unavailable due to the failure of a single EC2 instance
- [x] An application does not become unavailable due to the deletion of a single SQS queue
- [ ] Unprocessed SQS messages are not lost due to the failure of a single EC2 instance

99.
You are using IOT sensors to monitor the movement of a group of hikers on a three day trek and send the information into an Kinesis Stream. They each have a sensor in their shoe and you know for certain that there is no problem with mobile coverage so all the data is getting back to the stream. You have used default settings for the stream. At the end of the third day, the data is sent to an S3 bucket. When you go to interpret the data in S3 there is only data for the last day and nothing for the first 2 days. Which of the following is the most probable cause of this?
**Choose the correct answer:**
- [ ] You cannot send Kinesis data to the same bucket on consecutive days if you do not have versioning enabled on the bucket. If you don't have versioning enabled you would need to define 3 different buckets or else the data is overwritten each day
- [ ] Temporary loss of mobile coverage; although mobile coverage was good in the area, even temporary loss of data will stop the streaming
- [ ] A sensor probably stopped working on the second day. If one sensor fails, no data is sent to the stream until that sensor is fixed
- [x] Data records are only accessible for a default of 24 hours from the time they are added to a stream.

100.
What is the difference between an Availability Zone and an edge location?
**Choose the correct answer:**
- [ ] Edge locations are used as control stations for AWS resources
- [ ] An Availability Zone is a grouping of AWS resources in a specific region; an edge location is a specific resource within the AWS region
- [ ] An edge location is used as a link when building load balancing between regions
- [x] An Availability Zone is an Amazon resource within an AWS region; an edge location will deliver cached content to the closest location to reduce latency

101.
You are building a system to distribute confidential training videos to employees. Using CloudFront, what method would be used to serve content that is stored in S3 but not publicly accessible from S3 directly?
**Choose the correct answer:**
- [ ] Add the CloudFront account security group
- [x] Create an Origin Access Identify (OAI) for CloudFront and grant access to the objects in your S3 bucket to that OAI
- [ ] Create a S3 bucket policy that lists the CloudFront distribution ID as the principal and the target bucket as the Amazon Resource Name (ARN)
- [ ] Create an Identity and Access Management (IAM) user for CloudFront and grant access to the objects in your S3 bucket to that IAM user.

102.
Your supervisor asks you to create a decoupled application whose process includes dependencies on EC2 instances and servers located in your company’s on-premises datacenter. Which of these are you least likely to recommend as part of that process?
**Choose the correct answer:**
- [ ] SQS polling from an on-premises server using IAM user credentials
- [ ] SQS polling from an EC2 instance deployed with an IAM role
- [x] SQS polling from an EC2 instance using IAM user credentials
- [ ] An SWF workflow

103.
You recently purchased hardware to run a decoupled application in your on-premises datacenter. The application is working great, but has seen an increased workload in recent weeks that makes you concerned that your hardware cannot handle the load. Your supervisor asks you to analyze the possibility of expanding the application using cloud resources. You cannot completely migrate the application to AWS because of the investment you have already made in on-premises hardware. What items will most likely be included in your analysis?
**Choose the 2 correct answers:**
- [x] You can leverage SWF to utilize both on-premises servers and EC2 instances for your decoupled application
- [ ] SQS is not a valid option to help you use on-premises servers and EC2 instances in the same application, as it cannot be polled by on-premises servers
- [ ] SWF is not a valid option to help you use on-premises servers and EC2 instances in the same application, as on-premises servers cannot be used as activity task workers
- [x] You can leverage SQS to utilize both on-premises servers and EC2 instances for your decoupled application

104.
You are asked to evaluate a company’s AWS environment to find ways to reduce cost. You discover they are running three production web server reserved EC2 instances with EBS-backed root volumes. These instances have a consistent CPU load of 80%. Traffic is being distributed to these instances by an Elastic Load Balancer. They also have production and development Multi-AZ RDS MySQL databases. What recommendation would you make to reduce cost in this environment without affecting availability of mission-critical systems?
**Choose the correct answer:**
- [ ] Consider using on-demand instances instead of reserved EC2 instances
- [ ] Consider not using a Multi-AZ RDS deployment for the development database
- [ ] Consider using spot instances instead of reserved EC2 instances
- [ ] Consider removing the Elastic Load Balancer

105.
A colleague would like a new subnet configured in AWS for a database cluster she is building. She expects that the subnet will never need more than six IP addresses. Which of the following will likely be the most appropriate choice for this subnet?
**Choose the correct answer:**
- [ ] A /29 private subnet
- [ ] A /29 public subnet
- [x] A /28 private subnet
- [ ] A /28 public subnet

106.
You recently purchased and deployed four reserved EC2 instances in the US-East-1 region’s Availability Zone 1 for a new project. Your supervisor just informed you that this project only requires two EC2 instances. Rather than selling the reserved instances, she asked you to terminate the extra instances and convert two of the on-demand instances already running in Availability Zone 1 to reserved instances. Can this be done?
**Choose the correct answer:**
- [ ] No, it cannot be done
- [x] Yes, you can terminate the reserved instances and AWS will automatically begin billing the two on-demand instances as reserved instances
- [ ] Yes, you can request this billing change through an AWS form
- [ ] Yes, you can terminate the on-demand instances and re-deploy them as reserved instances

107.
You are consulting for a healthcare company that has strict compliance and auditing requirements. When architecting the application environment on AWS, which services or service features might you enable to take advantage of monitoring to ensure auditing the environment for compliance is easy and follows the strict healthcare compliance requirements?
**Choose the correct answer:**
- [ ] Multi Factor Authentication
- [ ] S3 logging
- [ ] Encrypted data storage
- [x] CloudTrail for security logs

108.
You manage a web application on EC2 instances. Your website occasionally experiences brief but large spikes in traffic that cause your EC2 instances’ resources to become overwhelmed and the application to freeze up and lose recently-submitted requests from end users. You use Auto Scaling to deploy additional resources to handle the load during spikes, but the new instances do not deploy fast enough to prevent the existing application servers from freezing. Assuming you cannot find a pattern to when these spikes occur, which of the following is likely to provide the most cost-effective solution to avoid losing recently submitted requests?
**Choose the correct answer:**
- [x] Use an SQS queue to decouple the application components
- [ ] Use larger instances for your application
- [ ] Pre-warm your Elastic Load Balancer
- [ ] Keep one extra EC2 instance always powered on in case a spike occurs

109.
Your company is concerned with EBS volume backups on Amazon EC2 and wants to ensure they have proper backups so that the data is durable. What solution would you implement and why?
**Choose the correct answer:**
- [ ] Write a cronjob on the server that compresses the data that needs to be backed up using gzip compression, then use AWS CLI to copy the data into an S3 bucket for durability
- [x] Write a cronjob that uses the AWS CLI to take a snapshot of production EBS volumes. - [ ] The data is durable because EBS snapshots are stored on the Amazon S3 standard storage class
- [ ] Use a lifecycle policy to back up EBS volumes stored on Amazon S3 for durability
Configure Amazon Storage Gateway with EBS volumes as the data source and store the backups on premise through the storage gateway

110.
Amazon Auto Scaling is not meant to handle instant load spikes but is built to grow with a gradual increase in usage over a short time period.
Choose the correct answer:
- [x] True
- [ ] False

