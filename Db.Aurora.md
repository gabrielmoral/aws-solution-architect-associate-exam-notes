#### Aurora

Better performance than MySQL and less expensive that comercial databases while delivering similar performance and availavility.

It always maintains 2 copy of your data in each availability zones with a minimum of 3 AZ, 6 copies of your data.

Two types of read replicas:
- Aurora read replicas (Up to 15)
- MySQL read replicas (Up to 5)

Automated backups are always enabled.
There is no impact performance when backups and snapshots.
You can share Aurora snapshots with other accounts.
Automated failover is available with Aurora Replicas.
Aurora provides different endpoints as Reader or Cluster to access the Aurora Cluster.