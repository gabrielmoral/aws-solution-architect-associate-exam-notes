#### EC2 (Elastic Compute Cloud)

It is a web service that provides resizable compute capacity in the cloud. It allows you to scale capacity both up and down.

There is a soft limit of 20 instances per region which it can be increased submitting a request increase form to AWS.

Pricing types:

**On demand**
Fixed rate by the hour or second with no commitment.

**Reserved**
Offers capacity reservation and offers a significant discount on the hourly charge. Contract terms are 1 Year or 3 Year Terms. There is a market where you can sell reserved instances that you do not want.

**Spot**
Enables you to bid whatever price you want for instance capacity, providing greater saving if you app have flexible start and end times.

If the spot instance is terminated, you won't be charged for a partial hour of usage. However, if you terminate the instance yourself, you will be charged for any hour in which the instance ran.

**Dedicated hosts**
Physical EC2 server dedicated for your use. It can help you to reduce costs by allowing you to use your existing server-bound software licenses.

**Security groups**
All inbound traffic is always blocked by default.
All Outbound traffic is allowed.
Changes take effect immediately.
Multiple EC2 instances within a security group.
Multiple security groups attached to EC2 instances.
Security groups are STATEFUL. When you open a port is going to be open inbound and outbound.
You cannot block specific IP addresses using security groups, instead use NACL.
You can specify allow rules but not deny rules.

**Bootstrap scripts**
They run when an EC2 instance first boots.
It is a powerful way of automating software installs and updates.

**Instance metadata**
Used to get information about an instance (such as public ip)
http://169.254.169.254/latest/meta-data/
http://169.254.169.254/latest/user-data/ (bootstrap data)

**EC2 Placement Groups**
It is how you place your EC2 instances.

-   Clustered placement group.
    Low network latency / High network throughput. Same instances in the same AZ.
-   Spread placement group.
    Individual critical EC2 instances. Different AZ, different pieces of hardware.
-   Partitioned
    Multiple EC2 instances into a partition and each partition in separate hardware and racks.

The name for the placement group must be unique in your AWS account.

Only certain types of instances can be launched in a placement group.

You can't merge placement groups and you can't move existing instances into a placement group.