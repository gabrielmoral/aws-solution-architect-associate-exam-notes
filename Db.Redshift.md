#### Redshift

It is used for business intelligence (DWH service) (OLAP).

It can be Single node or multi-node.

Massively Parallel Processing (MPP). Redshift automatically distributes data and query load across all nodes. 
It is only enabled in 1 AZ.

It does not currently support Multi-AZ or Multi-Region deployments.

Backups
- Enabled by default with 1 day period retention.
- Maximum retention period is 35 days.
- It can replicate your snapshots to S3 in another region for disaster recovery. (Enable Cross-Region Snapshots Copy)


Security
- Encripted at transit using SSL.
- Encrypted at rest using AES-256 encryption.
- By default Redshift takes care of key management. (You can manage you own keys and use AWS KMS)
