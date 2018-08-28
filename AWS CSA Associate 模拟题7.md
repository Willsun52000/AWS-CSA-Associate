## AWS CSA Associate 模拟题7

401.
IAM’s Policy Evaluation Logic always starts with a default ____________ for every request, except for those that use the AWS account’s root security credentials
- [ ] Permit
- [x] Deny
- [ ] Cancel

402.*
An organization has created 10 IAM users. The organization wants each of the IAM users to have access to a separate DynamoDB table. All the users are added to the same group and the organization wants to setup a group level policy for this. How can the organization achieve this?
- [ ] Define the group policy and add a condition which allows the access based on the IAM name
- [x] Create a DynamoDB table with the same name as the IAM user name and define the policy rule which grants access based on the DynamoDB ARN using a variable
- [ ] Create a separate DynamoDB database for each user and configure a policy in the group based on the DB variable
- [ ] It is not possible to have a group level policy which allows different IAM users to different DynamoDB Tables

403.*
An organization has setup multiple IAM users. The organization wants that each IAM user accesses the IAM console only within the organization and not from outside. How can it achieve this?
- [ ] Create an IAM policy with the security group and use that security group for AWS console login
- [x] Create an IAM policy with a condition which denies access when the IP address range is not from the organization
- [ ] Configure the EC2 instance security group which allows traffic only from the organization’s IP range
- [ ] Create an IAM policy with VPC and allow a secure gateway between the organization and AWS Console

404.
Can I attach more than one policy to a particular entity?
- [x] Yes always
- [ ] Only if within GovCloud
- [ ] No
- [ ] Only if within VPC

407.
A __________ is a document that provides a formal statement of one or more permissions.
- [x] policy
- [ ] permission
- [ ] Role
- [ ] resource

408.
A __________ is the concept of allowing (or disallowing) an entity such as a user, group, or role some type of access to one or more resources.
- [ ] user
- [ ] AWS Account
- [ ] resource
- [x] permission

409.
True or False: When using IAM to control access to your RDS resources, the key names that can be used are case sensitive. For example, aws:CurrentTime is NOT equivalent to AWS:currenttime.
- [ ] TRUE
- [x] FALSE (Refer link)

410.
A user has set an IAM policy where it allows all requests if a request from IP 10.10.10.1/32. Another policy allows all the requests between 5 PM to 7 PM. What will happen when a user is requesting access from IP 10.10.10.1/32 at 6 PM?
- [ ] IAM will throw an error for policy conflict
- [ ] It is not possible to set a policy based on the time or IP
- [ ] It will deny access
- [x] It will allow access

411.
Which of the following are correct statements with policy evaluation logic in AWS Identity and Access Management? Choose 2 answers.
- [x] By default, all requests are denied
- [ ] An explicit allow overrides an explicit deny
- [x] An explicit allow overrides default deny
- [ ] An explicit deny does not override an explicit allow
- [ ] By default, all request are allowed

412.
What are the two permission types used by AWS?
- [ ] Resource-based and Product-based
- [ ] Product-based and Service-based
- [ ] Service-based
- [x] User-based and Resource-based

413.
What’s the policy used for cross account access? (Choose 2)
- [x] Trust policy
- [x] Permissions Policy
- [ ] Key policy

414.
A company has an AWS account that contains three VPCs (Dev, Test, and Prod) in the same region. Test is peered to both Prod and Dev. All VPCs have non-overlapping CIDR blocks. The company wants to push minor code releases from Dev to Prod to speed up time to market. Which of the following options helps the company accomplish this?
- [x] Create a new peering connection Between Prod and Dev along with appropriate routes.
- [ ] Create a new entry to Prod in the Dev route table using the peering connection as the target.
- [ ] Attach a second gateway to Dev. Add a new entry in the Prod route table identifying the gateway as the target.
- [ ] The VPCs have non-overlapping CIDR blocks in the same account. The route tables contain local routes for all VPCs.

415.
You have in total 5 offices, and the entire employee related information is stored under AWS VPC instances. Now all the offices want to connect the instances in VPC using VPN. Which of the below help you to implement this?
- [ ] you can have redundant customer gateways between your data center and your VPC
- [ ] you can have multiple locations connected to the AWS VPN CloudHub
- [ ] You have to define 5 different static IP addresses in route table.
- [x] 1 and 2
- [ ] 1,2 and 3

416.
You have in total 15 offices, and the entire employee related information is stored under AWS VPC instances. Now all the offices want to connect the instances in VPC using VPN. What problem do you see in this scenario?
- [ ] You can not create more than 1 VPN connections with single VPC (Can be created)
- [ ] You can not create more than 10 VPN connections with single VPC (soft limit can be extended)
- [ ] When you create multiple VPN connections, the virtual private gateway can not sends network traffic to the appropriate VPN connection using statically assigned routes. (Can route the traffic to correct connection)
- [ ] Statically assigned routes cannot be configured in case of more than 1 VPN with virtual private gateway. (can be configured)
- [x] None of above

417.
You have been asked to virtually extend two existing data centers into AWS to support a highly available application that depends on existing, on-premises resources located in multiple data centers and static content that is served from an Amazon Simple Storage Service (S3) bucket. Your design currently includes a dual-tunnel VPN connection between your CGW and VGW. Which component of your architecture represents a potential single point of failure that you should consider changing to make the solution more highly available?
- [ ] Add another VGW in a different Availability Zone and create another dual-tunnel VPN connection.
- [x] Add another CGW in a different data center and create another dual-tunnel VPN connection. (Refer link)
- [ ] Add a second VGW in a different Availability Zone, and a CGW in a different data center, and create another dual-tunnel.
- [ ] No changes are necessary: the network architecture is currently highly available.

418.
After launching an instance that you intend to serve as a NAT (Network Address Translation) device in a public subnet you modify your route tables to have the NAT device be the target of internet bound traffic of your private subnet. When you try and make an outbound connection to the Internet from an instance in the private subnet, you are not successful. Which of the following steps could resolve the issue?
- [ ] Attaching a second Elastic Network interface (ENI) to the NAT instance, and placing it in the private subnet
- [ ] Attaching an Elastic IP address to the instance in the private subnet
- [ ] Attaching a second Elastic Network Interface (ENI) to the instance in the private subnet, and placing it in the public subnet
- [x] Disabling the Source/Destination Check attribute on the NAT instance

419.
You manually launch a NAT AMI in a public subnet. The network is properly configured. Security groups and network access control lists are property configured. Instances in a private subnet can access the NAT. The NAT can access the Internet. However, private instances cannot access the Internet. What additional step is required to allow access from the private instances?
- [ ] Enable Source/Destination Check on the private Instances.
- [ ] Enable Source/Destination Check on the NAT instance.
- [ ] Disable Source/Destination Check on the private instances
- [x] Disable Source/Destination Check on the NAT instance

420.
A user has created a VPC with public and private subnets. The VPC has CIDR 20.0.0.0/16. The private subnet uses CIDR 20.0.1.0/24 and the public subnet uses CIDR 20.0.0.0/24. The user is planning to host a web server in the public subnet (port 80. and a DB server in the private subnet (port 3306.. The user is configuring a security group of the NAT instance. Which of the below mentioned entries is not required for the NAT security group?
- [ ] For Inbound allow Source: 20.0.1.0/24 on port 80
- [ ] For Outbound allow Destination: 0.0.0.0/0 on port 80
- [x] For Inbound allow Source: 20.0.0.0/24 on port 80 (Refer NATSG)
- [ ] For Outbound allow Destination: 0.0.0.0/0 on port 443

421.
A web company is looking to implement an external payment service into their highly available application deployed in a VPC. Their application EC2 instances are behind a public facing ELB. Auto scaling is used to add additional instances as traffic increases. Under normal load the application runs 2 instances in the Auto Scaling group but at peak it can scale 3x in size. The application instances need to communicate with the payment service over the Internet, which requires whitelisting of all public IP addresses used to communicate with it. A maximum of 4 whitelisting IP addresses are allowed at a time and can be added through an API. How should they architect their solution?
- [x] Route payment requests through two NAT instances setup for High Availability and whitelist the Elastic IP addresses attached to the NAT instances
- [ ] Whitelist the VPC Internet Gateway Public IP and route payment requests through the Internet Gateway. (Internet gateway is only to route traffic)
- [ ] Whitelist the ELB IP addresses and route payment requests from the Application servers through the ELB. (ELB does not have a fixed IP address)
- [ ] Automatically assign public IP addresses to the application instances in the Auto Scaling group and run a script on boot that adds each instances public IP address to the payment validation whitelist API. (would exceed the allowed 4 IP addresses)

422.
Instance A and instance B are running in two different subnets A and B of a VPC. Instance A is not able to ping instance B. What are two possible reasons for this? (Pick 2 correct answers)
- [ ] The routing table of subnet A has no target route to subnet B
- [x] The security group attached to instance B does not allow inbound ICMP traffic
- [ ] The policy linked to the IAM role on instance A is not configured correctly
- [x] The NACL on subnet B does not allow outbound ICMP traffic

423.
An instance is launched into a VPC subnet with the network ACL configured to allow all inbound traffic and deny all outbound traffic. The instance’s security group is configured to allow SSH from any IP address and deny all outbound traffic. What changes need to be made to allow SSH access to the instance?
- [ ] The outbound security group needs to be modified to allow outbound traffic.
- [x] The outbound network ACL needs to be modified to allow outbound traffic.
- [ ] Nothing, it can be accessed from any IP address using SSH.
- [ ] Both the outbound security group and outbound network ACL need to be modified to allow outbound traffic.

424.
From what services I can block incoming/outgoing IPs?
- [ ] Security Groups
- [ ] DNS
- [ ] ELB
- [ ] VPC subnet
- [ ] IGW
- [x] NACL

425.
What is the difference between a security group in VPC and a network ACL in VPC (chose 3 correct answers)
- [ ] Security group restricts access to a Subnet while ACL restricts traffic to EC2
- [x] Security group restricts access to EC2 while ACL restricts traffic to a subnet
- [ ] Security group can work outside the VPC also while ACL only works within a VPC
- [x] Network ACL performs stateless filtering and Security group provides stateful filtering
- [x] Security group can only set Allow rule, while ACL can set Deny rule also

426.
You are currently hosting multiple applications in a VPC and have logged numerous port scans coming in from a specific IP address block. Your security team has requested that all access from the offending IP address block be denied for the next 24 hours. Which of the following is the best method to quickly and temporarily deny access from the specified IP address block?
- [ ] Create an AD policy to modify Windows Firewall settings on all hosts in the VPC to deny access from the IP address block
- [x] Modify the Network ACLs associated with all public subnets in the VPC to deny access from the IP address block
- [ ] Add a rule to all of the VPC 5 Security Groups to deny access from the IP address block
- [ ] Modify the Windows Firewall settings on all Amazon Machine Images (AMIs) that your organization uses in that VPC to deny access from the IP address block

427.
You have two Elastic Compute Cloud (EC2) instances inside a Virtual Private Cloud (VPC) in the same Availability Zone (AZ) but in different subnets. One instance is running a database and the other instance an application that will interface with the database. You want to confirm that they can talk to each other for your application to work properly. Which two things do we need to confirm in the VPC settings so that these EC2 instances can communicate inside the VPC? Choose 2 answers
- [x] A network ACL that allows communication between the two subnets.
- [ ] Both instances are the same instance class and using the same Key-pair.
- [ ] That the default route is set to a NAT instance or Internet Gateway (IGW) for them to communicate.
- [x] Security groups are set to allow the application host to talk to the database on the right port/protocol

428.
A benefits enrollment company is hosting a 3-tier web application running in a VPC on AWS, which includes a NAT (Network Address Translation) instance in the public Web tier. There is enough provisioned capacity for the expected workload tor the new fiscal year benefit enrollment period plus some extra overhead Enrollment proceeds nicely for two days and then the web tier becomes unresponsive, upon investigation using CloudWatch and other monitoring tools it is discovered that there is an extremely large and unanticipated amount of inbound traffic coming from a set of 15 specific IP addresses over port 80 from a country where the benefits company has no customers. The web tier instances are so overloaded that benefit enrollment administrators cannot even SSH into them. Which activity would be useful in defending against this attack?
- [ ] Create a custom route table associated with the web tier and block the attacking IP addresses from the IGW (internet Gateway)
- [ ] Change the EIP (Elastic IP Address) of the NAT instance in the web tier subnet and update the Main Route Table with the new EIP
- [ ] Create 15 Security Group rules to block the attacking IP addresses over port 80
- [x] Create an inbound NACL (Network Access control list) associated with the web tier subnet with deny rules to block the attacking IP addresses

429.
Which of the following statements describes network ACLs? (Choose 2 answers)
- [x] Responses to allowed inbound traffic are allowed to flow outbound regardless of outbound rules, and vice versa (are stateless)
- [ ] Using network ACLs, you can deny access from a specific IP range
- [ ] Keep network ACL rules simple and use a security group to restrict application level access
- [x] NACLs are associated with a single Availability Zone (associated with Subnet)

430.
You are designing security inside your VPC. You are considering the options for establishing separate security zones and enforcing network traffic rules across different zone to limit Instances can communications.  How would you accomplish these requirements? Choose 2 answers
- [ ] Configure a security group for every zone. Configure a default allow all rule. Configure explicit deny rules for the zones that shouldn’t be able to communicate with one another (Security group does not allow deny rules)
- [x] Configure you instances to use pre-set IP addresses with an IP address range every security zone. Configure NACL to explicitly allow or deny communication between the different IP address ranges, as required for interzone communication
- [x] Configure a security group for every zone. Configure allow rules only between zone that need to be able to communicate with one another. Use implicit deny all rule to block any other traffic
- [ ] Configure multiple subnets in your VPC, one for each zone. Configure routing within your VPC in such a way that each subnet only has routes to other subnets with which it needs to communicate, and doesn’t have routes to subnets with which it shouldn’t be able to communicate. (default routes are unmodifiable)

431.
Your entire AWS infrastructure lives inside of one Amazon VPC. You have an Infrastructure monitoring application running on an Amazon instance in Availability Zone (AZ) A of the region, and another application instance running in AZ B. The monitoring application needs to make use of ICMP ping to confirm network reachability of the instance hosting the application. Can you configure the security groups for these instances to only allow the ICMP ping to pass from the monitoring instance to the application instance and nothing else” If so how?
- [ ] No Two instances in two different AZ’s can’t talk directly to each other via ICMP ping as that protocol is not allowed across subnet (i.e. broadcast) boundaries (Can communicate)
- [ ] Yes Both the monitoring instance and the application instance have to be a part of the same security group, and that security group needs to allow inbound ICMP (Need not have to be part of same security group)
- [x] Yes, The security group for the monitoring instance needs to allow outbound ICMP and the application instance’s security group needs to allow Inbound ICMP (is stateful, so just allow outbound ICMP from monitoring and inbound ICMP on monitored instance)
- [ ] Yes, Both the monitoring instance’s security group and the application instance’s security group need to allow both inbound and outbound ICMP ping packets since ICMP is not a connection-oriented protocol (Security groups are stateful)

432.
A user has configured a VPC with a new subnet. The user has created a security group. The user wants to configure that instances of the same subnet communicate with each other. How can the user configure this with the security group?
- [ ] There is no need for a security group modification as all the instances can communicate with each other inside the same subnet
- [ ] Configure the subnet as the source in the security group and allow traffic on all the protocols and ports
- [x] Configure the security group itself as the source and allow traffic on all the protocols and ports
- [ ] The user has to use VPC peering to configure this

433.
You are designing a data leak prevention solution for your VPC environment. You want your VPC Instances to be able to access software depots and distributions on the Internet for product updates. The depots and distributions are accessible via third party CDNs by their URLs. You want to explicitly deny any other outbound connections from your VPC instances to hosts on the Internet. Which of the following options would you consider?
- [x] Configure a web proxy server in your VPC and enforce URL-based rules for outbound access Remove default routes. (Security group and NACL cannot have URLs in the rules nor does the route)
- [ ] Implement security groups and configure outbound rules to only permit traffic to software depots.
- [ ] Move all your instances into private VPC subnets remove default routes from all routing tables and add specific routes to the software depots and distributions only.
- [ ] Implement network access control lists to all specific destinations, with an Implicit deny as a rule.

434.
You have an EC2 Security Group with several running EC2 instances. You change the Security Group rules to allow inbound traffic on a new port and protocol, and launch several new instances in the same Security Group. The new rules apply:
- [x] Immediately to all instances in the security group.
- [ ] Immediately to the new instances only.
- [ ] Immediately to the new instances, but old instances must be stopped and restarted before the new rules apply.
- [ ] To all instances, but it may take several minutes for old instances to see the changes.

435.
A customer is running a multi-tier web application farm in a virtual private cloud (VPC) that is not connected to their corporate network. They are connecting to the VPC over the Internet to manage all of their Amazon EC2 instances running in both the public and private subnets. They have only authorized the bastion-security-group with Microsoft Remote Desktop Protocol (RDP) access to the application instance security groups, but the company wants to further limit administrative access to all of the instances in the VPC. Which of the following Bastion deployment scenarios will meet this requirement?
- [ ] Deploy a Windows Bastion host on the corporate network that has RDP access to all instances in the VPC.
- [ ] Deploy a Windows Bastion host with an Elastic IP address in the public subnet and allow SSH access to the bastion from anywhere.
- [ ] Deploy a Windows Bastion host with an Elastic IP address in the private subnet, and restrict RDP access to the bastion from only the corporate public IP addresses.
- [x] Deploy a Windows Bastion host with an auto-assigned Public IP address in the public subnet, and allow RDP access to the bastion from only the corporate public IP addresses.

436.
You are designing a system that has a Bastion host. This component needs to be highly available without human intervention. Which of the following approaches would you select?
- [ ] Run the bastion on two instances one in each AZ
- [ ] Run the bastion on an active Instance in one AZ and have an AMI ready to boot up in the event of failure
- [x] Configure the bastion instance in an Auto Scaling group Specify the Auto Scaling group to include multiple AZs but have a min-size of 1 and max-size of 1
- [ ] Configure an ELB in front of the bastion instance

437.
You’ve been brought in as solutions architect to assist an enterprise customer with their migration of an ecommerce platform to Amazon Virtual Private Cloud (VPC) The previous architect has already deployed a 3- tier VPC. The configuration is as follows: VPC vpc-2f8t>C447
IGW ig-2d8bc445
NACL acl-2080c448
Subnets and Route Tables:
Web server’s subnet-258bc44d
Application server’s subnet-248DC44c
Database server’s subnet-9189c6f9
Route Tables:
rtb-2i8bc449
rtb-238bc44b
Associations:
Subnet-258bc44d: rtb-2i8bc449
Subnet-248DC44c: rtb-238bc44b
Subnet-9189c6f9: rtb-238bc44b
You are now ready to begin deploying EC2 instances into the VPC. Web servers must have direct access to the internet Application and database servers cannot have direct access to the internet. Which configuration below will allow you the ability to remotely administer your application and database servers, as well as allow these servers to retrieve updates from the Internet?
- [ ] Create a bastion and NAT Instance in subnet-258bc44d and add a route from rtb-238bc44b to subnet-258bc44d. (Route should point to the NAT)
- [ ] Add a route from rtb-238bc44b to igw-2d8bc445 and add a bastion and NAT instance within Subnet-248DC44c. (Adding IGW to routertb-238bc44b would expose the Application and Database server to internet. Bastion and NAT should be in public subnet)
- [ ] Create a Bastion and NAT Instance in subnet-258bc44d. Add a route from rtb-238bc44b to igw-2d8bc445. And a new NACL that allows access between subnet-258bc44d and subnet-248bc44c. (Route should point to NAT and not Internet Gateway else it would be internet accessible.)
- [x] Create a Bastion and NAT instance in subnet-258bc44d and add a route from rtb-238bc44b to the NAT instance. (Bastion and NAT should be in the public subnet. As Web Server has direct access to Internet, the subnet subnet-258bc44d should be public and  Route rtb-2i8bc449 pointing to IGW. Route rtb-238bc44b for private subnets should point to NAT for outgoing internet access)

438.
You are tasked with setting up a Linux bastion host for access to Amazon EC2 instances running in your VPC. Only clients connecting from the corporate external public IP address 72.34.51.100 should have SSH access to the host. Which option will meet the customer requirement?
- [x] Security Group Inbound Rule: Protocol – TCP. Port Range – 22, Source 72.34.51.100/32
- [ ] Security Group Inbound Rule: Protocol – UDP, Port Range – 22, Source 72.34.51.100/32
- [ ] Network ACL Inbound Rule: Protocol – UDP, Port Range – 22, Source 72.34.51.100/32
- [ ] Network ACL Inbound Rule: Protocol – TCP, Port Range-22, Source 72.34.51.100/0

439.
A user has launched an EC2 instance from an instance store backed AMI. The infrastructure team wants to create an AMI from the running instance. Which of the below mentioned credentials is not required while creating the AMI?
- [ ] AWS account ID
- [ ] 509 certificate and private key
- [x] AWS login ID to login to the console
- [ ] Access key and secret access key

440.
A user has launched an EC2 Windows instance from an instance store backed AMI. The user wants to convert the AMI to an EBS backed AMI. How can the user convert it?
- [ ] Attach an EBS volume to the instance and unbundle all the AMI bundled data inside the EBS
- [x] A Windows based instance store backed AMI cannot be converted to an EBS backed AMI
- [ ] It is not possible to convert an instance store backed AMI to an EBS backed AMI
- [ ] Attach an EBS volume and use the copy command to copy all the ephemeral content to the EBS Volume

441.
A user has launched two EBS backed EC2 instances in the US-East-1a region. The user wants to change the zone of one of the instances. How can the user change it?
- [ ] Stop one of the instances and change the availability zone
- [ ] The zone can only be modified using the AWS CLI
- [ ] From the AWS EC2 console, select the Actions – > Change zones and specify new zone
- [x] Create an AMI of the running instance and launch the instance in a separate AZ

442.
A user has launched a large EBS backed EC2 instance in the US-East-1a region. The user wants to achieve Disaster Recovery (DR) for that instance by creating another small instance in Europe. How can the user achieve DR?
- [ ] Copy the running instance using the “Instance Copy” command to the EU region
- [x] Create an AMI of the instance and copy the AMI to the EU region. Then launch the instance from the EU AMI
- [ ] Copy the instance from the US East region to the EU region
- [ ] Use the “Launch more like this” option to copy the instance from one region to another

443.
A user has launched an EC2 instance store backed instance in the US-East-1a zone. The user created AMI #1 and copied it to the Europe region. After that, the user made a few updates to the application running in the US-East-1a zone. The user makes an AMI#2 after the changes. If the user launches a new instance in Europe from the AMI #1 copy, which of the below mentioned statements is true?
- [ ] The new instance will have the changes made after the AMI copy as AWS just copies the reference of the original AMI during the copying. Thus, the copied AMI will have all the updated data
- [ ] The new instance will have the changes made after the AMI copy since AWS keeps updating the AMI
- [ ] It is not possible to copy the instance store backed AMI from one region to another
- [x] The new instance in the EU region will not have the changes made after the AMI copy

444.
George has shared an EC2 AMI created in the US East region from his AWS account with Stefano. George copies the same AMI to the US West region. Can Stefano access the copied AMI of George’s account from the US West region?
- [x] No, copy AMI does not copy the permission
- [ ] It is not possible to share the AMI with a specific account
- [ ] Yes, since copy AMI copies all private account sharing permissions
- [ ] Yes, since copy AMI copies all the permissions attached with the AMI

445.
EC2 instances are launched from Amazon Machine images (AMIS). A given public AMI can:
- [ ] be used to launch EC2 Instances in any AWS region.
- [ ] only be used to launch EC2 instances in the same country as the AMI is stored.
- [x] only be used to launch EC2 instances in the same AWS region as the AMI is stored. (An AMI is tied to the region where its files are located within Amazon S3)
- [ ] only be used to launch EC2 instances in the same AWS availability zone as the AMI is stored.

446.
Which of the following instance types are available as Amazon EBS-backed only? Choose 2 answers
- [x] General purpose T2
- [ ] General purpose M3
- [x] Compute-optimized C4
- [ ] Compute-optimized C3
- [ ] Storage-optimized 12

447.
A t2.medium EC2 instance type must be launched with what type of Amazon Machine Image (AMI)?
- [ ] An Instance store Hardware Virtual Machine AMI
- [ ] An Instance store Paravirtual AMI
- [x] An Amazon EBS-backed Hardware Virtual Machine AMI
- [ ] An Amazon EBS-backed Paravirtual AMI

448.*
You have identified network throughput as a bottleneck on your m1.small EC2 instance when uploading data Into Amazon S3 In the same region. How do you remedy this situation? Add an additional ENI
- [x] Change to a larger Instance
- [ ] Use DirectConnect between EC2 and S3
- [ ] Use EBS PIOPS on the local volume

449.
You are using an m1.small EC2 Instance with one 300 GB EBS volume to host a relational database. You determined that write throughput to the database needs to be increased. Which of the following approaches can help achieve this? Choose 2 answers
- [x] Use an array of EBS volumes (Striping to increase throughput)
- [ ] Enable Multi-AZ mode.
- [ ] Place the instance in an Auto Scaling Groups
- [ ] Add an EBS volume and place into RAID 5 (RAID 5 is not recommended as it provides parity and EBS volumes are already replicated across multiple servers in an Availability Zone for availability and durability, so AWS recommends striping for performance rather than durability)
- [x] Increase the size of the EC2 Instance.
- [ ] Put the database behind an Elastic Load Balancer.

450.
You are tasked with setting up a cluster of EC2 Instances for a NoSQL database. The database requires random read IO disk performance up to a 100,000 IOPS at 4KB block side per node. Which of the following EC2 instances will perform the best for this workload?
- [ ] A High-Memory Quadruple Extra Large (m2.4xlarge) with EBS-Optimized set to true and a PIOPs EBS volume
- [ ] A Cluster Compute Eight Extra Large (cc2.8xlarge) using instance storage
- [x] High I/O Quadruple Extra Large (hi1.4xlarge) using instance storage
- [ ] A Cluster GPU Quadruple Extra Large (cg1.4xlarge) using four separate 4000 PIOPS EBS volumes in a RAID 0 configuration

451.
If I want my instance to run on a single-tenant hardware, which value do I have to set the instance’s tenancy attribute to?
- [x] dedicated
- [ ] isolated
- [ ] one
- [ ] reserved

452.
You have a video transcoding application running on Amazon EC2. Each instance polls a queue to find out which video should be transcoded, and then runs a transcoding process. If this process is interrupted, the video will be transcoded by another instance based on the queuing system. You have a large backlog of videos, which need to be transcoded, and would like to reduce this backlog by adding more instances. You will need these instances only until the backlog is reduced. Which type of Amazon EC2 instances should you use to reduce the backlog in the most cost efficient way?
- [ ] Reserved instances
- [x] Spot instances
- [ ] Dedicated instances
- [ ] On-demand instances

453.
The one-time payment for Reserved Instances is __________ refundable if the reservation is cancelled.
- [ ] always
- [ ] in some circumstances
- [x] never

454.
You run a web application where web servers on EC2 Instances are In an Auto Scaling group Monitoring over the last 6 months shows that 6 web servers are necessary to handle the minimum load. During the day up to 12 servers are needed Five to six days per year, the number of web servers required might go up to 15. What would you recommend to minimize costs while being able to provide hill availability?
- [x] 6 Reserved instances (heavy utilization). 6 Reserved instances (medium utilization), rest covered by On-Demand instances
- [ ] 6 Reserved instances (heavy utilization). 6 On-Demand instances, rest covered by Spot Instances (don’t go for spot as availability not guaranteed)
- [ ] 6 Reserved instances (heavy utilization) 6 Spot instances, rest covered by On-Demand instances (don’t go for spot as availability not guaranteed)
- [ ] 6 Reserved instances (heavy utilization) 6 Reserved instances (medium utilization) rest covered by Spot instances (don’t go for spot as availability not guaranteed)

455.
A user is running one instance for only 3 hours every day. The user wants to save some cost with the instance. Which of the below mentioned Reserved Instance categories is advised in this case?
- [x] The user should not use RI; instead only go with the on-demand pricing (seems question before the introduction of the Scheduled Reserved instances in Jan 2016, which can be used in this case)
- [ ] The user should use the AWS high utilized RI
- [ ] The user should use the AWS medium utilized RI
- [ ] The user should use the AWS low utilized RI

456.
Which of the following are characteristics of a reserved instance? Choose 3 answers (but 4 answers seem correct)
- [x] It can be migrated across Availability Zones (can be modified)
- [ ] It is specific to an Amazon Machine Image (AMI) (specific to platform)
- [x] It can be applied to instances launched by Auto Scaling (are allowed)
- [ ] It is specific to an instance Type (specific to instance family but instance type can be changed)
- [x] It can be used to lower Total Cost of Ownership (TCO) of a system (helps to reduce cost)

457.
You have a distributed application that periodically processes large volumes of data across multiple Amazon EC2 Instances. The application is designed to recover gracefully from Amazon EC2 instance failures. You are required to accomplish this task in the most cost-effective way. Which of the following will meet your requirements?
- [x] Spot Instances
- [ ] Reserved instances
- [ ] Dedicated instances
- [ ] On-Demand instances

458.
Can I move a Reserved Instance from one Region to another?
- [x] No
- [ ] Only if they are moving into GovCloud
- [ ] Yes
- [ ] Only if they are moving to US East from another region

459.
An application you maintain consists of multiple EC2 instances in a default tenancy VPC. This application has undergone an internal audit and has been determined to require dedicated hardware for one instance. Your compliance team has given you a week to move this instance to single-tenant hardware. Which process will have minimal impact on your application while complying with this requirement?
- [ ] Create a new VPC with tenancy=dedicated and migrate to the new VPC (possible but impact not minimal)
- [ ] Use ec2-reboot-instances command line and set the parameter “dedicated=true”
- [ ] Right click on the instance, select properties and check the box for dedicated tenancy
- [x] Stop the instance, create an AMI, launch a new instance with tenancy=dedicated, and terminate the old instance

460.
What does Amazon EC2 provide?
- [x] Virtual servers in the Cloud
- [ ] A platform to run code (Java, PHP, Python), paying on an hourly basis.
- [ ] Computer Clusters in the Cloud.
- [ ] Physical servers, remotely managed by the customer.

461.
A user has enabled termination protection on an EC2 instance. The user has also set Instance initiated shutdown behavior to terminate. When the user shuts down the instance from the OS, what will happen?
- [ ] The OS will shutdown but the instance will not be terminated due to protection
- [x] It will terminate the instance
- [ ] It will not allow the user to shutdown the instance from the OS
- [ ] It is not possible to set the termination protection when an Instance initiated shutdown is set to Terminate

462.
A user has launched an EC2 instance and deployed a production application in it. The user wants to prohibit any mistakes from the production team to avoid accidental termination. How can the user achieve this?
- [x] The user can the set DisableApiTermination attribute to avoid accidental termination
- [ ] It is not possible to avoid accidental termination
- [ ] The user can set the Deletion termination flag to avoid accidental termination
- [ ] The user can set the InstanceInitiatedShutdownBehavior flag to avoid accidental termination

463.
You have been doing a lot of testing of your VPC Network by deliberately failing EC2 instances to test whether instances are failing over properly. Your customer who will be paying the AWS bill for all this asks you if he being charged for all these instances. You try to explain to him how the billing works on EC2 instances to the best of your knowledge. What would be an appropriate response to give to the customer in regards to this?
- [ ] Billing commences when Amazon EC2 AMI instance is completely up and billing ends as soon as the instance starts to shutdown.
- [x] Billing commences when Amazon EC2 initiates the boot sequence of an AMI instance and billing ends when the instance shuts down.
- [ ] Billing only commences only after 1 hour of uptime and billing ends when the instance terminates.
- [ ] Billing commences when Amazon EC2 initiates the boot sequence of an AMI instance and billing ends as soon as the instance starts to shutdown.

464.
How can software determine the public and private IP addresses of the Amazon EC2 instance that it is running on?
- [x] Query the local instance metadata
- [ ] Query the appropriate Amazon CloudWatch metric.
- [ ] Query the local instance userdata.
- [ ] Use ipconfig or ifconfig command.

465.
The base URI for all requests for instance metadata is ___________
- [ ] http://254.169.169.254/latest/
- [ ] http://169.169.254.254/latest/
- [ ] http://127.0.0.1/latest/
- [x] http://169.254.169.254/latest/

466.
Which Amazon Elastic Compute Cloud feature can you query from within the instance to access instance properties?
- [ ] Instance user data
- [ ] Resource tags
- [x] Instance metadata
- [ ] Amazon Machine Image

467.
You need to pass a custom script to new Amazon Linux instances created in your Auto Scaling group. Which feature allows you to accomplish this?
- [x] User data
- [ ] EC2Config service
- [ ] IAM roles
- [ ] AWS Config

468.
By default, when an EBS volume is attached to a Windows instance, it may show up as any drive letter on the instance. You can change the settings of the _____ Service to set the drive letters of the EBS volumes per your specifications.
- [ ] EBSConfig Service
- [ ] AMIConfig Service
- [x] EC2Config Service
- [ ] Ec2-AMIConfig Service

469.
What is a placement group?
- [ ] A collection of Auto Scaling groups in the same Region
- [x] Feature that enables EC2 instances to interact with each other via high bandwidth, low latency connections
- [ ] A collection of Elastic Load Balancers in the same Region or Availability Zone
- [ ] A collection of authorized Cloud Front edge locations for a distribution

470.
In order to optimize performance for a compute cluster that requires low inter-node latency, which feature in the following list should you use?
- [ ] AWS Direct Connect
ß- [x] Placement Groups
- [ ] VPC private subnets
- [ ] EC2 Dedicated Instances
- [ ] Multiple Availability Zones

471.
What is required to achieve gigabit network throughput on EC2? You already selected cluster-compute, 10GB instances with enhanced networking, and your workload is already network-bound, but you are not seeing 10 gigabit speeds.
- [ ] Enable biplex networking on your servers, so packets are non-blocking in both directions and there’s no switching overhead.
- [ ] Ensure the instances are in different VPCs so you don’t saturate the Internet Gateway on any one VPC.
- [ ] Select PIOPS for your drives and mount several, so you can provision sufficient disk throughput
- [x] Use a placement group for your instances so the instances are physically near each other in the same Availability Zone. (You are not guaranteed 10 gigabit performance, except within a placement group. Using placement groups enables applications to participate in a low-latency, 10 Gbps network)

472.
You need the absolute highest possible network performance for a cluster computing application. You already selected homogeneous instance types supporting 10 gigabit enhanced networking, made sure that your workload was network bound, and put the instances in a placement group. What is the last optimization you can make?
- [x] Use 9001 MTU instead of 1500 for Jumbo Frames, to raise packet body to packet overhead ratios. (For instances that are collocated inside a placement group, jumbo frames help to achieve the maximum network throughput possible, and they are recommended in this case)
- [ ] Segregate the instances into different peered VPCs while keeping them all in a placement group, so each one has its own Internet Gateway.
- [ ] Bake an AMI for the instances and relaunch, so the instances are fresh in the placement group and do not have noisy neighbors
- [ ] Turn off SYN/ACK on your TCP stack or begin using UDP for higher throughput.