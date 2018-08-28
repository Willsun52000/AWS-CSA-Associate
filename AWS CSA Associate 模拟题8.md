## AWS CSA Associate 模拟题8

473.
Please select the most correct answer regarding the persistence of the Amazon Instance Store
- [x] The data on an instance store volume persists only during the life of the associated Amazon EC2 instance
- [ ] The data on an instance store volume is lost when the security group rule of the associated instance is changed.
- [ ] The data on an instance store volume persists even after associated Amazon EC2 instance is deleted

474.
A user has launched an EC2 instance from an instance store backed AMI. The user has attached an additional instance store volume to the instance. The user wants to create an AMI from the running instance. Will the AMI have the additional instance store volume data?
- [x] Yes, the block device mapping will have information about the additional instance store volume
- [ ] No, since the instance store backed AMI can have only the root volume bundled
- [ ] It is not possible to attach an additional instance store volume to the existing instance store backed AMI instance
- [ ] No, since this is ephemeral storage it will not be a part of the AMI

475.
When an EC2 instance that is backed by an S3-based AMI Is terminated, what happens to the data on the root volume?
- [ ] Data is automatically saved as an EBS volume.
- [ ] Data is automatically saved as an EBS snapshot.
- [x] Data is automatically deleted
- [ ] Data is unavailable until the instance is restarted.

476.
A user has launched an EC2 instance from an instance store backed AMI. If the user restarts the instance, what will happen to the ephemeral storage data?
- [ ] All the data will be erased but the ephemeral storage will stay connected
- [ ] All data will be erased and the ephemeral storage is released
- [ ] It is not possible to restart an instance launched from an instance store backed AMI
- [x] The data is preserved

477.
When an EC2 EBS-backed instance is stopped, what happens to the data on any ephemeral store volumes?
- [x] Data will be deleted and will no longer be accessible
- [ ] Data is automatically saved in an EBS volume.
- [ ] Data is automatically saved as an EBS snapshot
- [ ] Data is unavailable until the instance is restarted

478.*
A user has launched an EC2 Windows instance from an instance store backed AMI. The user has also set the Instance initiated shutdown behavior to stop. What will happen when the user shuts down the OS?
- [ ] It will not allow the user to shutdown the OS when the shutdown behavior is set to Stop
- [x] It is not possible to set the termination behavior to Stop for an Instance store backed AMI instance
- [ ] The instance will stay running but the OS will be shutdown
- [ ] The instance will be terminated

479.
Which of the following will occur when an EC2 instance in a VPC (Virtual Private Cloud) with an associated Elastic IP is stopped and started? (Choose 2 answers)
- [ ] The Elastic IP will be dissociated from the instance
- [x] All data on instance-store devices will be lost
- [ ] All data on EBS (Elastic Block Store) devices will be lost
- [ ] The ENI (Elastic Network Interface) is detached
- [x] The underlying host for the instance is changed

480.
You are designing an enterprise data storage system. Your data management software system requires mountable disks and a real filesystem, so you cannot use S3 for storage. You need persistence, so you will be using AWS EBS Volumes for your system. The system needs as low-cost storage as possible, and access is not frequent or high throughput, and is mostly sequential reads. Which is the most appropriate EBS Volume Type for this scenario?
- [ ] gp1
- [ ] io1
- [x] standard (Standard or Magnetic volumes are suited for cold workloads where data is infrequently accessed, or scenarios where the lowest storage cost is important)
- [ ] gp2

481.
Which EBS volume type is best for high performance NoSQL cluster deployments?
- [x] io1 (io1 volumes, or Provisioned IOPS (PIOPS) SSDs, are best for: Critical business applications that require sustained IOPS performance, or more than 10,000 IOPS or 160 MiB/s of throughput per volume, like large database workloads, such as MongoDB.)
- [ ] gp1
- [ ] standard
- [ ] gp2

482.
Provisioned IOPS Costs: you are charged for the IOPS and storage whether or not you use them in a given month.
- [ ] FALSE
- [x] TRUE

483.
A user is trying to create a PIOPS EBS volume with 8 GB size and 200 IOPS. Will AWS create the volume?
- [x] Yes, since the ratio between EBS and IOPS is less than 30
- [ ] No, since the PIOPS and EBS size ratio is less than 30
- [ ] No, the EBS size is less than 10 GB
- [ ] Yes, since PIOPS is higher than 100

484.*
A user has provisioned 2000 IOPS to the EBS volume. The application hosted on that EBS is experiencing less IOPS than provisioned. Which of the below mentioned options does not affect the IOPS of the volume?
- [ ] The application does not have enough IO for the volume
- [ ] Instance is EBS optimized
- [ ] The EC2 instance has 10 Gigabit Network connectivity
- [x] Volume size is too large

485.
A user is trying to create a PIOPS EBS volume with 4000 IOPS and 100 GB size. AWS does not allow the user to create this volume. What is the possible root cause for this?
- [x] The ratio between IOPS and the EBS volume is higher than 30
- [ ] The maximum IOPS supported by EBS is 3000
- [ ] The ratio between IOPS and the EBS volume is lower than 50
- [ ] PIOPS is supported for EBS higher than 500 GB size

486.*
An existing application stores sensitive information on a non-boot Amazon EBS data volume attached to an Amazon Elastic Compute Cloud instance. Which of the following approaches would protect the sensitive data on an Amazon EBS volume?
- [ ] Upload your customer keys to AWS CloudHSM. Associate the Amazon EBS volume with AWS CloudHSM. Remount the Amazon EBS volume.
- [x] Create and mount a new, encrypted Amazon EBS volume. Move the data to the new volume. Delete the old Amazon EBS volume.
- [ ] Unmount the EBS volume. Toggle the encryption attribute to True. Re-mount the Amazon EBS volume.
- [ ] Snapshot the current Amazon EBS volume. Restore the snapshot to a new, encrypted Amazon EBS volume. Mount the Amazon EBS volume (Need to create a snapshot, create an encrypted copy of snapshot and then create a EBS volume and mount it)

487.*
Is it possible to access your EBS snapshots?
- [ ] Yes, through the Amazon S3 APIs.
- [x] Yes, through the Amazon EC2 APIs
- [ ] No, EBS snapshots cannot be accessed; they can only be used to create a new EBS volume.
- [ ] EBS doesn’t provide snapshots.

488.
Which of the following approaches provides the lowest cost for Amazon Elastic Block Store snapshots while giving you the ability to fully restore data?
- [ ] Maintain two snapshots: the original snapshot and the latest incremental snapshot
- [ ] Maintain a volume snapshot; subsequent snapshots will overwrite one another
- [x] Maintain a single snapshot the latest snapshot is both Incremental and complete
- [ ] Maintain the most current snapshot, archive the original and incremental to Amazon Glacier.

489.
Which procedure for backing up a relational database on EC2 that is using a set of RAIDed EBS volumes for storage minimizes the time during which the database cannot be written to and results in a consistent backup?
- [ ] Detach EBS volumes, 2. Start EBS snapshot of volumes, 3. Re-attach EBS volumes
- [ ] Stop the EC2 Instance. 2. Snapshot the EBS volumes
- [ ] Suspend disk I/O, 2. Create an image of the EC2 Instance, 3. Resume disk I/O
- [ ] Suspend disk I/O, 2. Start EBS snapshot of volumes, 3. Resume disk I/O
- [x] Suspend disk I/O, 2. Start EBS snapshot of volumes, 3. Wait for snapshots to complete, 4. Resume disk I/O

490.
How can an EBS volume that is currently attached to an EC2 instance be migrated from one Availability Zone to another?
- [ ] Detach the volume and attach it to another EC2 instance in the other AZ.
- [ ] Simply create a new volume in the other AZ and specify the original volume as the source.
- [x] Create a snapshot of the volume, and create a new volume from the snapshot in the other AZ
- [ ] Detach the volume, then use the ec2-migrate-volume command to move it to another AZ.

491.
How are the EBS snapshots saved on Amazon S3?
- [ ] Exponentially
- [x] Incrementally
- [ ] EBS snapshots are not stored in the Amazon S3
- [ ] Decrementally

492.
EBS Snapshots occur _____
- [x] Asynchronously
- [ ] Synchronously
- [ ] Weekly

493.
What will be the status of the snapshot until the snapshot is complete?
- [ ] Running
- [ ] Working
- [ ] Progressing
- [x] Pending

494.
Before I delete an EBS volume, what can I do if I want to recreate the volume later?
- [ ] Create a copy of the EBS volume (not a snapshot)
- [x] Create and Store a snapshot of the volume
- [ ] Download the content to an EC2 instance
- [ ] Back up the data in to a physical disk

495.*
Which of the following are true regarding encrypted Amazon Elastic Block Store (EBS) volumes? Choose 2 answers
- [x] Supported on all Amazon EBS volume types
- [x] Snapshots are automatically encrypted
- [ ] Available to all instance types
- [ ] Existing volumes can be encrypted
- [ ] Shared volumes can be encrypted

496.
Amazon EBS snapshots have which of the following two characteristics? (Choose 2.) Choose 2 answers
- [x] EBS snapshots only save incremental changes from snapshot to snapshot
- [x] EBS snapshots can be created in real-time without stopping an EC2 instance (the snapshot can be taken real time however it will not be consistent and the recommended way is to stop or freeze the IO)
- [ ] EBS snapshots can only be restored to an EBS volume of the same size or smaller (EBS volume restored from snapshots need to be of the same size of larger size)
- [ ] EBS snapshots can only be restored and mounted to an instance in the same Availability Zone as the original EBS volume (Snapshots are specific to Region and can be used to create a volume in any AZ and does not depend on the original EBS volume AZ)

497.
A user is planning to schedule a backup for an EBS volume. The user wants security of the snapshot data. How can the user achieve data encryption with a snapshot?
- [x] Use encrypted EBS volumes so that the snapshot will be encrypted by AWS (Refer link)
- [ ] While creating a snapshot select the snapshot with encryption
- [ ] By default the snapshot is encrypted by AWS
- [ ] Enable server side encryption for the snapshot using S3

498.
A sys admin is trying to understand EBS snapshots. Which of the below mentioned statements will not be useful to the admin to understand the concepts about a snapshot?
- [x] Snapshot is synchronous
- [ ] It is recommended to stop the instance before taking a snapshot for consistent data
- [ ] Snapshot is incremental
- [ ] Snapshot captures the data that has been written to the hard disk when the snapshot command was executed

499.*
When creation of an EBS snapshot is initiated but not completed, the EBS volume
- [ ] Cannot be detached or attached to an EC2 instance until me snapshot completes
- [ ] Can be used in read-only mode while me snapshot is in progress
- [x] Can be used while the snapshot is in progress
- [ ] Cannot be used until the snapshot completes

500.
You have a server with a 5O0GB Amazon EBS data volume. The volume is 80% full. You need to back up the volume at regular intervals and be able to re-create the volume in a new Availability Zone in the shortest time possible. All applications using the volume can be paused for a period of a few minutes with no discernible user impact. Which of the following backup methods will best fulfill your requirements?
- [x] Take periodic snapshots of the EBS volume
- [ ] Use a third-party Incremental backup application to back up to Amazon Glacier
- [ ] Periodically back up all data to a single compressed archive and archive to Amazon S3 using a parallelized multi-part upload
- [ ] Create another EBS volume in the second Availability Zone attach it to the Amazon EC2 instance, and use a disk manager to mirror me two disks

501.
A user is creating a snapshot of an EBS volume. Which of the below statements is incorrect in relation to the creation of an EBS snapshot?
- [ ] Its incremental
- [ ] It can be used to launch a new instance
- [x] It is stored in the same AZ as the volume (stored in the same region)
- [ ] It is a point in time backup of the EBS volume

502.
A user has created a snapshot of an EBS volume. Which of the below mentioned usage cases is not possible with respect to a snapshot?
- [ ] Mirroring the volume from one AZ to another AZ
- [ ] Launch an instance
- [x] Decrease the volume size
- [ ] Increase the size of the volume

503.
What is true of the way that encryption works with EBS?
- [ ] Snapshotting an encrypted volume makes an encrypted snapshot; restoring an encrypted snapshot creates an encrypted volume when specified / requested.
- [ ] Snapshotting an encrypted volume makes an encrypted snapshot when specified / requested; restoring an encrypted snapshot creates an encrypted volume when specified / requested.
- [x] Snapshotting an encrypted volume makes an encrypted snapshot; restoring an encrypted snapshot always creates an encrypted volume.
- [ ] Snapshotting an encrypted volume makes an encrypted snapshot when specified / requested; restoring an encrypted snapshot always creates an encrypted volume.

504.
Why are more frequent snapshots of EBS Volumes faster?
- [ ] Blocks in EBS Volumes are allocated lazily, since while logically separated from other EBS Volumes, Volumes often share the same physical hardware. Snapshotting the first time forces full block range allocation, so the second snapshot doesn’t need to perform the allocation phase and is faster.
- [x] The snapshots are incremental so that only the blocks on the device that have changed after your last snapshot are saved in the new snapshot.
- [ ] AWS provisions more disk throughput for burst capacity during snapshots if the drive has been pre-warmed by snapshotting and reading all blocks.
- [ ] The drive is pre-warmed, so block access is more rapid for volumes when every block on the device has already been read at least one time.

505.
Which is not a restriction on AWS EBS Snapshots?
- [x] Snapshots which are shared cannot be used as a basis for other snapshots (Snapshots shared with other users are usable in full by the recipient, including but limited to the ability to base modified volumes and snapshots)
- [ ] You cannot share a snapshot containing an AWS Access Key ID or AWS Secret Access Key
- [ ] You cannot share encrypted snapshots (NOTE: this has be updated partially where you can share a encrypted snapshot with other accounts)
- [ ] Snapshot restorations are restricted to the region in which the snapshots are created

506.
There is a very serious outage at AWS. EC2 is not affected, but your EC2 instance deployment scripts stopped working in the region with the outage. What might be the issue?
- [ ] The AWS Console is down, so your CLI commands do not work.
- [x] S3 is unavailable, so you can’t create EBS volumes from a snapshot you use to deploy new volumes. (EBS volume snapshots are stored in S3. If S3 is unavailable, snapshots are unavailable)
- [ ] AWS turns off the <code>DeployCode</code> API call when there are major outages, to protect from system floods.
- [ ] None of the other answers make sense. If EC2 is not affected, it must be some other issue.

507.
A user is trying to pre-warm a blank EBS volume attached to a Linux instance. Which of the below mentioned steps should be performed by the user?
- [x] There is no need to pre-warm an EBS volume (with latest update no pre-warming is needed)
- [ ] Contact AWS support to pre-warm (This used to be the case before, but pre warming is not necessary now)
- [ ] Unmount the volume before pre-warming
- [ ] Format the device

508.
A user has created an EBS volume of 10 GB and attached it to a running instance. The user is trying to access EBS for first time. Which of the below mentioned options is the correct statement with respect to a first time EBS access?
- [ ] The volume will show a size of 8 GB
- [ ] The volume will show a loss of the IOPS performance the first time (the volume needed to be wiped cleaned before for new volumes, however pre warming is not needed any more)
- [x] The volume will be blank
- [ ] If the EBS is mounted it will ask the user to create a file system

509.
You are running a database on an EC2 instance, with the data stored on Elastic Block Store (EBS) for persistence At times throughout the day, you are seeing large variance in the response times of the database queries Looking into the instance with the isolate command you see a lot of wait time on the disk volume that the database’s data is stored on. What two ways can you improve the performance of the database’s storage while maintaining the current persistence of the data? Choose 2 answers
- [ ] Move to an SSD backed instance
- [x] Move the database to an EBS-Optimized Instance
- [x] Use Provisioned IOPs EBS
- [ ] Use the ephemeral storage on an m2.4xLarge Instance Instead

510.
You have launched an EC2 instance with four (4) 500 GB EBS Provisioned IOPS volumes attached. The EC2 Instance is EBS-Optimized and supports 500 Mbps throughput between EC2 and EBS. The two EBS volumes are configured as a single RAID 0 device, and each Provisioned IOPS volume is provisioned with 4,000 IOPS (4000 16KB reads or writes) for a total of 16,000 random IOPS on the instance. The EC2 Instance initially delivers the expected 16,000 IOPS random read and write performance. Sometime later in order to increase the total random I/O performance of the instance, you add an additional two 500 GB EBS Provisioned IOPS volumes to the RAID. Each volume is provisioned to 4,000 IOPS like the original four for a total of 24,000 IOPS on the EC2 instance Monitoring shows that the EC2 instance CPU utilization increased from 50% to 70%, but the total random IOPS measured at the instance level does not increase at all. What is the problem and a valid solution?
- [ ] Larger storage volumes support higher Provisioned IOPS rates: increase the provisioned volume storage of each of the 6 EBS volumes to 1TB.
- [x] EBS-Optimized throughput limits the total IOPS that can be utilized use an EBS-Optimized instance that provides larger throughput. (EC2 Instance types have limit on max throughput and would require larger instance types to provide 24000 IOPS)
- [ ] Small block sizes cause performance degradation, limiting the I’O throughput, configure the instance device driver and file system to use 64KB blocks to increase throughput.
RAID 0 only scales linearly to about 4 devices, use RAID 0 with 4 EBS Provisioned IOPS volumes but increase each Provisioned IOPS EBS volume to 6.000 IOPS.
- [ ] The standard EBS instance root volume limits the total IOPS rate, change the instant root volume to also be a 500GB 4,000 Provisioned IOPS volume

511.
A user has deployed an application on an EBS backed EC2 instance. For a better performance of application, it requires dedicated EC2 to EBS traffic. How can the user achieve this?
- [ ] Launch the EC2 instance as EBS provisioned with PIOPS EBS
- [ ] Launch the EC2 instance as EBS enhanced with PIOPS EBS
- [ ] Launch the EC2 instance as EBS dedicated with PIOPS EBS
- [x] Launch the EC2 instance as EBS optimized with PIOPS EBS

512.
You are responsible for a legacy web application whose server environment is approaching end of life. You would like to migrate this application to AWS as quickly as possible, since the application environment currently has the following limitations: The VM’s single 10GB VMDK is almost full. The virtual network interface still uses the 10Mbps driver, which leaves your 100Mbps WAN connection completely underutilized. It is currently running on a highly customized Windows VM within a VMware environment: You do not have the installation media. This is a mission critical application with an RTO (Recovery Time Objective) of 8 hours. RPO (Recovery Point Objective) of 1 hour. How could you best migrate this application to AWS while meeting your business continuity requirements?
- [ ] Use the EC2 VM Import Connector for vCenter to import the VM into EC2
- [x] Use Import/Export to import the VM as an EBS snapshot and attach to EC2. (Import/Export is used to transfer large amount of data)
- [ ] Use S3 to create a backup of the VM and restore the data into EC2.
- [ ] Use the ec2-bundle-instance API to Import an Image of the VM into EC2 (only bundles an windows instance store instance)

513.
You are tasked with moving a legacy application from a virtual machine running inside your datacenter to an Amazon VPC. Unfortunately this app requires access to a number of on-premises services and no one who configured the app still works for your company. Even worse there’s no documentation for it. What will allow the application running inside the VPC to reach back and access its internal dependencies without being reconfigured? (Choose 3 answers)
- [x] An AWS Direct Connect link between the VPC and the network housing the internal services (VPN or a DX for communication)
- [ ] An Internet Gateway to allow a VPN connection. (Virtual and Customer gateway is needed)
- [ ] An Elastic IP address on the VPC instance (Don’t need a EIP as private subnets can also interact with on-premises network)
- [x] An IP address space that does not conflict with the one on-premises (IP address cannot conflict)
- [ ] Entries in Amazon Route 53 that allow the Instance to resolve its dependencies’ IP addresses (Route 53 is not required)
- [x] A VM Import of the current virtual machine (VM Import to copy the VM to AWS as there is no documentation it can’t be configured from scratch)

514.
You have multiple Amazon EC2 instances running in a cluster across multiple Availability Zones within the same region. What combination of the following should be used to ensure the highest network performance (packets per second), lowest latency, and lowest jitter? Choose 3 answers
- [ ] Amazon EC2 placement groups (would not work for multiple AZs)
- [x] Enhanced networking (provides network performance, lowest latency)
- [ ] Amazon PV AMI (Requires HVM)
- [x] Amazon HVM AMI (Requires HVM)
- [ ] Amazon Linux (Can be on others as well)
- [x] Amazon VPC (works only in VPC, can’t enable enhanced networking if the instance is in EC2-Classic)

515.
A group of researchers is studying the migration pattern of a beetle that eats and destroys gram. The researchers must process massive amounts of data and run statistics. Which one of the following options provides the high performance computing for this purpose.
- [ ] Configure an Autoscaling Scaling group to launch dozens of spot instances to run the statistical analysis simultaneously
- [ ] Launch AMI instances that support SR-IOV in a single Availability Zone
- [ ] Launch compute optimized (C4) instances in at least two Availability Zones
- [x] Launch enhanced network type instances in a placement group

516.
A user is launching an EC2 instance in the US East region. Which of the below mentioned options is recommended by AWS with respect to the selection of the availability zone?
- [ ] Always select the US-East-1-a zone for HA
- [x] Do not select the AZ; instead let AWS select the AZ
- [ ] The user can never select the availability zone while launching an instance
- [ ] Always select the AZ while launching an instance

517.
You have multiple Amazon EC2 instances running in a cluster across multiple Availability Zones within the same region. What combination of the following should be used to ensure the highest network performance (packets per second), lowest latency, and lowest jitter? Choose 3 answers
- [ ] Amazon EC2 placement groups (would not work for multiple AZs)
- [x] Enhanced networking (provides network performance, lowest latency)
- [ ] Amazon PV AMI (Needs HVM)
- [x] Amazon HVM AMI
- [ ] Amazon Linux (Can work on other flavors of Unix as well)
- [x] Amazon VPC (Enhanced networking works only in VPC)

518.
Regarding the attaching of ENI to an instance, what does ‘warm attach’ refer to?
- [x] Attaching an ENI to an instance when it is stopped
- [ ] Attaching an ENI to an instance when it is running
- [ ] Attaching an ENI to an instance during the launch process

519.
Can I detach the primary (eth0) network interface when the instance is running or stopped?
- [ ] Yes, You can.
- [x] You cannot
- [ ] Depends on the state of the interface at the time

520.
By default what are ENIs that are automatically created and attached to instances using the EC2 console set to do when the attached instance terminates?
- [ ] Remain as is
- [x] Terminate
- [ ] Hibernate
- [ ] Pause

521.
Select the incorrect statement
- [ ] In Amazon EC2, the private IP addresses only returned to Amazon EC2 when the instance is stopped or terminated
- [ ] In Amazon VPC, an instance retains its private IP addresses when the instance is stopped.
- [x] In Amazon VPC, an instance does NOT retain its private IP addresses when the instance is stopped
- [ ] In Amazon EC2, the private IP address is associated exclusively with the instance for its lifetime

522.
To ensure failover capabilities, consider using a _____ for incoming traffic on a network interface”.
- [ ] primary public IP
- [x] secondary private IP
- [ ] secondary public IP
- [ ] add on secondary IP

523.
Which statements are true about Elastic Network Interface (ENI)? (Choose 2 answers)
- [ ] You can attach an ENI in one AZ to an instance in another AZ
- [x] You can change the security group membership of an ENI
- [x] You can attach an instance to tow different subnets within a VPC by using two ENIs
- [ ] You can attach an ENI in one VPC to an instance in another VPC

524.*
A user is planning to host a web server as well as an app server on a single EC2 instance, which is a part of the public subnet of a VPC. How can the user setup to have two separate public IPs and separate security groups for both the application as well as the web server?
- [ ] Launch a VPC instance with two network interfaces. Assign a separate security group to each and AWS will assign a separate public IP to them. (AWS cannot assign public IPs for instance with multiple ENIs)
- [ ] Launch VPC with two separate subnets and make the instance a part of both the subnets.
- [x] Launch a VPC instance with two network interfaces. Assign a separate security group and elastic IP to them.
- [ ] Launch a VPC with ELB such that it redirects requests to separate VPC instances of the public subnet.

525.
An organization has created multiple components of a single application for compartmentalization. Currently all the components are hosted on a single EC2 instance. Due to security reasons the organization wants to implement two separate SSLs for the separate modules although it is already using VPC. How can the organization achieve this with a single instance?
- [ ] Create a VPC instance, which will have both the ACL and the security group attached to it and have separate rules for each IP address.
- [x] Create a VPC instance, which will have multiple network interfaces with multiple elastic IP addresses.
- [ ] You have to launch two instances each in a separate subnet and allow VPC peering for a single IP.
- [ ] Create a VPC instance, which will have multiple subnets attached to it and each will have a separate IP address.

526.
Your system automatically provisions EIPs to EC2 instances in a VPC on boot. The system provisions the whole VPC and stack at once. You have two of them per VPC. On your new AWS account, your attempt to create a Development environment failed, after successfully creating Staging and Production environments in the same region. What happened?
- [ ] You didn’t choose the Development version of the AMI you are using.
- [ ] You didn’t set the Development flag to true when deploying EC2 instances.
- [x] You hit the soft limit of 5 EIPs per region and requested a 6th. (There is a soft limit of 5 EIPs per Region for VPC on new accounts. The third environment could not allocate the 6th EIP)
- [ ] You hit the soft limit of 2 VPCs per region and requested a 3rd.

527.*
A user has created a VPC with a public subnet. The user has terminated all the instances, which are part of the subnet. Which of the below mentioned statements is true with respect to this scenario?
- [ ] The user cannot delete the VPC since the subnet is not deleted
- [x] All network interface attached with the instances will be deleted
- [ ] When the user launches a new instance it cannot use the same subnet
- [ ] The subnet to which the instances were launched with will be deleted

528.
You launch an Amazon EC2 instance without an assigned AWS identity and Access Management (IAM) role. Later, you decide that the instance should be running with an IAM role. Which action must you take in order to have a running Amazon EC2 instance with an IAM role assigned to it?
- [ ] Create an image of the instance, and register the image with an IAM role assigned and an Amazon EBS volume mapping.
- [x] Create a new IAM role with the same permissions as an existing IAM role, and assign it to the running instance. (As per AWS latest enhancement, this is possible now)
- [ ] Create an image of the instance, add a new IAM role with the same permissions as the desired IAM role, and deregister the image with the new role assigned.
- [ ] Create an image of the instance, and use this image to launch a new instance with the desired IAM role assigned (This was correct before, as it was not possible to add an IAM role to an existing instance)

529.
What does the following command do with respect to the Amazon EC2 security groups? ec2-revoke RevokeSecurityGroupIngress
- [ ] Removes one or more security groups from a rule.
- [ ] Removes one or more security groups from an Amazon EC2 instance.
- [x] Removes one or more rules from a security group
- [ ] Removes a security group from our account.

530.
Which of the following cannot be used in Amazon EC2 to control who has access to specific Amazon EC2 instances?
- [ ] Security Groups
- [x] IAM System
- [ ] SSH keys
- [ ] Windows passwords

531.
You must assign each server to at least _____ security group
- [ ] 3
- [ ] 2
- [ ] 4
- [x] 1

532.
A company is building software on AWS that requires access to various AWS services. Which configuration should be used to ensure that AWS credentials (i.e., Access Key ID/Secret Access Key combination) are not compromised?
- [ ] Enable Multi-Factor Authentication for your AWS root account.
- [x] Assign an IAM role to the Amazon EC2 instance
- [ ] Store the AWS Access Key ID/Secret Access Key combination in software comments.
- [ ] Assign an IAM user to the Amazon EC2 Instance.

533.
Which of the following items are required to allow an application deployed on an EC2 instance to write data to a DynamoDB table? Assume that no security keys are allowed to be stored on the EC2 instance. (Choose 2 answers)
- [x] Create an IAM Role that allows write access to the DynamoDB table
- [x] Add an IAM Role to a running EC2 instance. (As per AWS latest enhancement, this is possible now)
- [ ] Create an IAM User that allows write access to the DynamoDB table.
Add an IAM User to a running EC2 instance.
- [ ] Launch an EC2 Instance with the IAM Role included in the launch configuration (This was correct before, as it was not possible to add an IAM role to an existing instance)

534.
You have an application running on an EC2 Instance, which will allow users to download files from a private S3 bucket using a pre-assigned URL. Before generating the URL the application should verify the existence of the file in S3. How should the application use AWS credentials to access the S3 bucket securely?
- [ ] Use the AWS account access Keys the application retrieves the credentials from the source code of the application.
- [ ] Create a IAM user for the application with permissions that allow list access to the S3 bucket launch the instance as the IAM user and retrieve the IAM user’s credentials from the EC2 instance user data.
- [x] Create an IAM role for EC2 that allows list access to objects in the S3 bucket. Launch the instance with the role, and retrieve the role’s credentials from the EC2 Instance metadata
- [ ] Create an IAM user for the application with permissions that allow list access to the S3 bucket. The application retrieves the IAM user credentials from a temporary directory with permissions that allow read access only to the application user.

535.
A user has created an application, which will be hosted on EC2. The application makes calls to DynamoDB to fetch certain data. The application is using the DynamoDB SDK to connect with from the EC2 instance. Which of the below mentioned statements is true with respect to the best practice for security in this scenario?
- [x] The user should attach an IAM role with DynamoDB access to the EC2 instance
- [ ] The user should create an IAM user with DynamoDB access and use its credentials within the application to connect with DynamoDB
- [ ] The user should create an IAM role, which has EC2 access so that it will allow deploying the application
- [ ] The user should create an IAM user with DynamoDB and EC2 access. Attach the user with the application so that it does not use the root account credentials

536.
Your application is leveraging IAM Roles for EC2 for accessing object stored in S3. Which two of the following IAM policies control access to you S3 objects.
- [x] An IAM trust policy allows the EC2 instance to assume an EC2 instance role.
- [x] An IAM access policy allows the EC2 role to access S3 objects
- [ ] An IAM bucket policy allows the EC2 role to access S3 objects. (Bucket policy is defined with S3 and not with IAM)
- [ ] An IAM trust policy allows applications running on the EC2 instance to assume as EC2 role (Trust policy allows EC2 instance to assume the role)
- [ ] An IAM trust policy allows applications running on the EC2 instance to access S3 objects. (Applications can access S3 through EC2 assuming the role)

537.
You have an application running on an EC2 Instance, which will allow users to download files from a private S3 bucket using a pre-assigned URL. Before generating the URL the application should verify the existence of the file in S3. How should the application use AWS credentials to access the S3 bucket securely?
- [ ] Use the AWS account access Keys the application retrieves the credentials from the source code of the application.
- [ ] Create a IAM user for the application with permissions that allow list access to the S3 bucket launch the instance as the IAM user and retrieve the IAM user’s credentials from the EC2 instance user data.
- [x] Create an IAM role for EC2 that allows list access to objects in the S3 bucket. Launch the instance with the role, and retrieve the role’s credentials from the EC2 Instance metadata
- [ ] Create an IAM user for the application with permissions that allow list access to the S3 bucket. The application retrieves the IAM user credentials from a temporary directory with permissions that allow read access only to the application user.

538.
In the basic monitoring package for EC2, Amazon CloudWatch provides the following metrics:
- [ ] Web server visible metrics such as number failed transaction requests
- [ ] Operating system visible metrics such as memory utilization
- [ ] Database visible metrics such as number of connections
- [x] Hypervisor visible metrics such as CPU utilization

539.
Which of the following requires a custom CloudWatch metric to monitor?
- [x] Memory Utilization of an EC2 instance
- [ ] CPU Utilization of an EC2 instance
- [ ] Disk usage activity of an EC2 instance
- [ ] Data transfer of an EC2 instance

540.
A user has configured CloudWatch monitoring on an EBS backed EC2 instance. If the user has not attached any additional device, which of the below mentioned metrics will always show a 0 value?
- [x] DiskReadBytes
- [ ] NetworkIn
- [ ] NetworkOut
- [ ] CPUUtilization

541.
A user is running a batch process on EBS backed EC2 instances. The batch process starts a few instances to process Hadoop Map reduce jobs, which can run between 50 – 600 minutes or sometimes for more time. The user wants to configure that the instance gets terminated only when the process is completed. How can the user configure this with CloudWatch?
- [x] Setup the CloudWatch action to terminate the instance when the CPU utilization is less than 5%
- [ ] Setup the CloudWatch with Auto Scaling to terminate all the instances
- [ ] Setup a job which terminates all instances after 600 minutes
- [ ] It is not possible to terminate instances automatically

542.
An AWS account owner has setup multiple IAM users. One IAM user only has CloudWatch access. He has setup the alarm action, which stops the EC2 instances when the CPU utilization is below the threshold limit. What will happen in this case?
- [ ] It is not possible to stop the instance using the CloudWatch alarm
- [ ] CloudWatch will stop the instance when the action is executed
- [ ] The user cannot set an alarm on EC2 since he does not have the permission
- [x] The user can setup the action but it will not be executed if the user does not have EC2 rights

543.
A user has launched 10 instances from the same AMI ID using Auto Scaling. The user is trying to see the average CPU utilization across all instances of the last 2 weeks under the CloudWatch console. How can the user achieve this?
- [x] View the Auto Scaling CPU metrics (Refer AS Instance Monitoring)
- [ ] Aggregate the data over the instance AMI ID (Works but needs detailed monitoring enabled)
- [ ] The user has to use the CloudWatchanalyser to find the average data across instances
- [ ] It is not possible to see the average CPU utilization of the same AMI ID since the instance ID is different