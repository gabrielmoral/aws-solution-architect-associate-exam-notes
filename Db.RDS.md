#### RDS

Online Transaction Processing (OLTP)

- SQL Server
- MySQL
- PostgreSQL
- MariaDB
- Oracle
- Aurora (serverless)

RDS runs on virtual machines. You can't login however.

Patching of the RDS system and DB is Amazon responsibility.

There are two different types of backups for RDS:
- Automated backups
- Database snapshots

Read replicas:
- Can be Multi-AZ.
- Used to increase performance.
- Must have backups turned on.
- Can be in different regions.
- Only supported by MySQL, PostgreSQL, MariaDB, Oracle, Aurora.
- Can be promoted to master, this will break the Read Replica.

Multi AZ.
- Used for disaster recovery (DR).
- You can force a failover from one AZ to another by rebooting the RDS instance.
- The standby replica will not perform any read/write operations while the primary instance is running.

Encryption at rest is supported for MySQL, PostgreSQL, MariaDB, Oracle and Aurora. It is done by AWS KMS service. Once the instance is encrypted, the data in the underling storage, backups, read replicas and snapshots will be too. At the present time, encrypting an existing DB Instance is not supported. To use Amazon RDS encryption for an existing database, create a new DB Instance with encryption enabled and migrate your data into it.

