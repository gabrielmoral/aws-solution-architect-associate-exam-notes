#### VPC (Virtual Private Cloud)

It consists of IGW (or Virtual Provate Gateways), Route Tables, Network Acess Control Lists (NACL), Subnets and Security groups.

When you create a VPC, by default it creates a Route table, a NACL and a Security Group associated. It won't create any subnets nor IGW.

Only 1 IGW per VPC.

Amazon always reserves 5 IP adresses within your subnets.

1 subnet = 1 AZ

Security Groups are Stateful. Opening Inbound traffic and outboud traffic is automatically; NACL are Stateless, you need to open inbound and outbound traffic.

No transitive Peering.

Minimum of two public subnets to deploy an internet ELB.

**VPC Flow Logs**
Logs traffic for the VPC.
After creation you cannot change its configuration.
Not all IP traffic is monitored (Windows license activation, Traffic from 169.254.169.254, DHCP traffic, reserved Ip addresses traffic)

**NAT instances**
Used to provide internet instance in private subnets.
They must be in a publc subnet.
When creating a NAT instance, disable Source/Destination check on the instance.
The must be a route out of the private subnet to the NAT instance, in order for this to work.
The amount of traffic that NAT instances can support depends on the instance size. If you are bottlenecking, increase the instance size.
NAT instances are always behinds a security group.

**NAT gateways**
Used to provide internet to instances in private subnets.
Redundancy inside the AZ.
Starts at 5Gbps.
No need to patch.
Not associated with security groups.
Automatically assigned a public ip address.
It must have a route out to the internet in the private subnet route table.
To create an AZ indenpendent architecture, create a NAT gateway in each AZ to avoid multiples AZ going to the same NAT gateway in case of NAT Gateway being down.

NAT gatewayes are billed:

- A cost per hour.
- All traffic processed, regardless of it's direction.

**Network ACL's**
They contain a numbered list of rules that are evaluated in order.
Separated outbound and inbound rules.
When created with the VPC it allows all inbound and outbound traffic.
Custom Network ACL denies all inbound and outbound traffic until you add rules.
Each subnet in you VPC must be associated with a NACL. If you do not specify one it will be associated the default one.
It is possible block IP addresses with NACL.
A NACL can be associated with multiple subnets; however a subnet can only be associated with one NACL.

**Bastion (or jump box)**
It is a host to connect with instances in privates subnets.

**Direct connect**
It connects directly your data center to AWS.
Useful for high throughput workloads or if you need a stable and reliable secure connection.

**VPC Endpoints**
A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by PrivateLink without requiring an an internet gateway, NAT device, VPN connection, or AWS Direct Connect. Traffic between yout VPC and the other services does not leave Amazon network.
They are virtual devices, horizontally scaled, redundant and highly available.
Two types of VPC endpoints:

- Interface Endpoints.
- Gateway Endpoints
  - Amazon S3
  - DynamoDB

**Egress-only Internet gateway**

It allows outbound communication over IPv6 from your instances in your VPC to the Internet. It blocks the Internet from initiating an IPv6 connection with your instances.