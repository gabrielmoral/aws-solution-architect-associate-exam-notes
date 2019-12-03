#### Load Balancers

There are 3 types:

**Application Load Balancer**
7 layer and they are application aware. They are intelligent, and you can create advanced request routing, sending specified requests to specific web servers.

**Network Load Balancer**
They are best suited for load balancing of TCP traffic where extreme performance is required. Layer 4.

**Classic Load Balancers**
Legacy Elastic load balancer. 7 layer specific features as X-Forwarded and sticky sessions. You can also use strict Layer 4. If you application stop responding the classic load balancer responds with a 504 error.


**ELB provides access logs** that capture detailed information about requests sent to your load balancer. Request time, ip, data, responses. By default is not activated.

Configuring **Connection Draining** you can specify a maximum time for the load balancer to keep connections alive before reporting the instance as de-registered. The maximum timeout value can be set between 1 and 3,600 seconds (the default is 300 seconds). When the maximum time limit is reached, the load balancer forcibly closes connections to the de-registering instance. 

X-Forwarded header contains the public ip address of the request.

Health Checks check the instance health by talking to it.
Instances monitored by ELB are reported as InService, or OutOfService.

Load Balancers have their own DNS name. They do not have pre-defined IPv4 addresses; you resolve them using a DNS name.


**Sticky sessions** enable your users to stick to the same EC2 instance. It can be useful if you are storing information locally to that instance.

**Cross Zone Load Balancing** enables you to load balance across multiple AZ. Your load balancer nodes distribute incoming requests evenly across the Availability Zones enabled for your load balancer. Otherwise, each load balancer node distributes requests only to instances in its Availability Zone.

Path patterns allow yo to direct traffic to different EC2 instances based on the URL contained in the request.

**Target groups**
They are where your load balancers are going to route requests to the targets in that group. It is a way to group EC2 instances.