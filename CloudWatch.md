#### CloudWatch

It is a monitoring service to monitor your AWS resources, as well as the applications you run in AWS.

CloudWatch monitors performance.

It can monitor:
- Compute
  - EC2 intances
  - Autoscaling groups
  - ELB
  - Route53 Health checks
- Storage / Content delivery
  - EBS
  - Storage Gateways
  - CloudFront
- Host level metrics
  - CPU
  - Network
  - Disk
  - Status check

By default it monitors EC2 every 5 minutes. There is an option to activate detailed monitoring (1 minute).

Enhanced metrics for RDS CloudWatch are able to monitor RDS child processes and OS processes.