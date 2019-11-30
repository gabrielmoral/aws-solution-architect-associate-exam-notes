#### Route53

ELB do not have pre-defined IPv4 addresses; you resolve them using a DNS name.

**DNS types**

SOA Records
When you buy a domain every DNS address being with SOA records. It stores information about name of the server that supply the data for the zone, the administrator of the zone, the current version of the data file and the default seconds of TTL file on resource records.

NS Records
They are used by Top Level Domain servers to direct traffic to the Content DNS server which contains the authoritative DNS records.

A Records
It is used to translate the name of the domain to an IP address.

CNAMES (Canonical Name)
It is used to resolve one domain name to another.

MX Records
Used for mail.

PTR Records
The reverse of an A Records. A way to look the a DNS name given an IP address.

The difference between an Alias Record and a CNAME is that CNAME can't be used for naked domains. Given the choice, always choose an Alias Record over a CNAME.

**Routing policies**

Simple routing policy.
One record with multiple IP addresses without health check.
If you specify multiple values in a record, Route 53 returns all values to the user in a random order.

Weighted routing policy.
Traffic goes based on the weight we have indicated for each region, ie. 20%-80%.

Latency routing policy.
It is based on users location, traffic will go to the faster fleet of EC2 instances.

Failover routing policy.
If for some reason the active environment starts failing Route 53 will send traffic to the passive route.

Geolocation routing policy.
It allows, for instance, the European customers to be sent to Europe region by taking into account the geolocalization of the user.

Geoproximity routing.
It lets Amazon 53 route traffic to your resources based on the geographic location of your users and your resources. To use it you must user Route 53 traffic flux.

Multivalue answer policy.
Essentially the same as with Simple based routing, except you get Health Checks.


**Health checks**
You can set health checks on individual record sets.
If a record set fails a health check it will be removed from Route53 until it passes the health check.
You can set SNS notifications to alert you if a health check is failed.