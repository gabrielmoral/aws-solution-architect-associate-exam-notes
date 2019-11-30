#### EBS (Elastic Block System)

It provides persistent block storage volumes for use with Amazon EC2 instances.
Each Amazon EBS volume is replicated within its AZ to protect you from component failure, offering HA and durability.

Volumes exist on EBS.

You can change EBS volumes sizes on the fly, including the size and the storage type. EBS volumes support live configuration changes while in production which it means that you can modify the volume type, size and IOPS capacity without service interruptions.

Volumes will always be in the same AZ as the EC2 instance.

Termination protection is **turned off** by default.

When an EC2 instance is terminated **the default action is for the root EBS volume to be deleted**. Any additional volumes will persist.


**Types**
-   General Purpose SSD (gp2) (Max 16,000 IOPS)
General purpose
-   Provisioned IOPS SSD (io1)  (Max 64,000 IOPS)
More IOPS. Small and random IO operations.
-   Throughput Optimised HDD (st1)
Big Data & Datawarehouse. Large and sequential I/O operations
-   Cold HDD (sc1)
File Servers. Lowest cost.
-   EBS Magnetic (Standard)

HDD types cannot be root volumes.

**Snapshots**
Snapshots exist in S3.
Snapshots are point of time copies of Volumes.
Snapshots are incremental. 
The first snapshot, it may take some time to create.
You can create AMI from Volumes and Snapshots.
Volumes restored from encrypted snapshots are encrypted automatically.
You can share snapshots, but only if the are unencrypted.

Amazon Data Lifecycle Manager (Amazon DLM) helps to automate the creation, retention, and deletion of snapshots                        taken to back up your Amazon EBS volumes.

**Migrating EBS**
To move an EC2 volume from an AZ to another, take a snapshot of it, create and AMI from the snapshot and then use the AMI to create and EC2 instance in a new AZ.

To move an EC2 volume from one region to another, take a snapshot of it, create and AMI from the snapshot and then copy the AMI from one region to another. Then use the copied AMI to create and EC2 instance in the new region.

**Encryption**
Root device volumes can now be encrypted.
To encrypt an existing root device volume create a snapshot then create a copy of the Snapshot and select the encrypt option. Finally create an AMI from the encrypted snapshot.

All data moving between the volume and the instance are encrypted.

**Instance store volumes**
Called also Ephemeral storage.
They cannot be stopped, If the underlying hosts fails, you will loose your data.
They give more IOPS because they are attached to the EC2 hosts directly.
You cannot stop instance store volumes. If you reboot the instance the data will remain but if you terminate the instance the data will be gone.